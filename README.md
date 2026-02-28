Hi team,
I want to provide a quick update on the Nexus upgrade. Nexus is now successfully up and running. However, I’ve identified a display issue where the “Browse” UI appears empty. I believe this is a known side effect related to how the new version handles indexing with the pg_trgm extension. I want to emphasize that this is strictly a display issue within the web interface. I’ve already verified with Nemai and Anatoliy from the OCP team, and they confirmed that pulling images is working perfectly. Therefore, this should not cause any production outages.
To address the UI issue, I have initiated the following tasks in Nexus: Repair – Rebuild repository browse and Repair – Rebuild repository search
The search feature now seems to be working, but the Browse function is still unavailable.
I have generated a Sonatype Support ZIP and opened a ticket with their engineering team for further investigation. However, I’m not sure when they will respond. I will continue to monitor my email over the weekend.
Since we have snapshots retained for 7 days, we can discuss a restore on Monday if necessary.
