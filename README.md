Hi Sean,

I saw in the Feb DDP that you’ll be on call to apply the RHEL patches for lxpd194 and lxpd195. I also noticed you’ll be working on quite a few servers that night.

Quick question — would it be possible to prioritize lxpd194 and lxpd195 when patching starts at 8:53 PM?

We can’t start the Nexus upgrade until those two servers are fully patched and ready. Since it’s been over a year since our last Nexus upgrade, there’s a chance something unexpected could come up, so I’m hoping to leave a bit more buffer time for troubleshooting just in case.

Also, if the upgrade doesn’t go as planned, we may need your help rolling back to the snapshots. If we stick with the original plan and only start the upgrade at 10:53 PM, that might keep you online longer waiting. But if we can patch 194 and 195 first, we could start earlier and, worst case, begin a rollback around 11:15–11:30 PM.

Let me know what you think — totally understand if the patching order is already locked in.

Thanks!
