# nas-watchdog
Free (public-repo) watchdog for self-hosted NAS jobs. Every ~10 minutes it checks each target's
self-hosted runners and status heartbeat, opens one `NAS ALERT <name>` issue in the target's own
(private) repo when something is down or stale, and closes it on recovery.
Targets and the read token are repo secrets (`WATCH_CONFIG`, `WATCH_TOKEN`), so nothing private is published.
