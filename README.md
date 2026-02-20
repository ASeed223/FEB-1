import csv
import os

CSV_FILE = "cleanup_list.csv"


def analyze_csv():
    if not os.path.exists(CSV_FILE):
        print(f"File not found: {CSV_FILE}")
        print("Make sure the CSV file is in the same folder as this script")
        return

    total_bytes = 0
    item_count = 0

    print(f"Reading: {CSV_FILE}")

    try:
        with open(CSV_FILE, mode="r", encoding="utf-8-sig", newline="") as file:
            reader = csv.DictReader(file)

            for row in reader:
                name = (row.get("Name") or "").strip()
                version = (row.get("Version") or "").strip()
                size_str = (row.get("Asset Size") or "0").strip()

                if not name:
                    continue

                try:
                    size = int(size_str)
                except ValueError:
                    size = 0

                total_bytes += size
                item_count += 1

                if item_count <= 10:
                    print(f"Item: {name}  Version: {version}  SizeBytes: {size}")
                elif item_count == 11:
                    print("...")

        total_mb = total_bytes / (1024 * 1024)
        total_gb = total_bytes / (1024 * 1024 * 1024)

        print("Report")
        print(f"Items: {item_count}")
        print(f"TotalBytes: {total_bytes}")
        print(f"TotalMB: {total_mb:.4f}")
        print(f"TotalGB: {total_gb:.6f}")

    except Exception as e:
        print(f"Read error: {e}")


if __name__ == "__main__":
    analyze_csv()
