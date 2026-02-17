Hi Jay,

After confirming with Rupali, it looks like the infrastructure maintenance release has been moved to February 27 instead of this Friday.

I’ve prepared the DDP proposal based on the January DDP.

As usual, we plan to shut down Nexus at 8:00 PM, and the Linux Admin team will begin the RHEL OS upgrade and patching at 8:53 PM. I will coordinate with the Linux Admins working that night to see if they can start the upgrade and patches on lxpd194 and lxpd195 first and notify me once the servers are ready to be brought back up. At that point, I will proceed with the Nexus upgrade.

For the February DDP, I suggest adding the following updates in Section 9 and 10:

9.4.7 – Upgrade Nexus (lxpd195) to 3.89

Predecessor: Upgrade and Apply RHEL OS Patches

10.1.2 – Start Nexus & Validate Nexus

Start Time: 11:25 PM

Finish Time: 11:30 PM

Predecessor: 9.4.7 – Upgrade Nexus (lxpd195) to 3.89

If you agree with this proposal, could you please approve it and forward it to Rupali? She may have concerns about whether this upgrade will impact the overall release end time.

Please let me know your thoughts.

Thank you.
