# Render pilot heartbeat

This repository contains only a scheduled GET request to the public Sistema Marcos pilot URL. It contains no application source, database connection, credentials, or customer data.

The schedule runs every 10 minutes because Render Free spins down after 15 minutes without inbound traffic. The request goes to `/`, which serves the app shell without querying Neon. GitHub Actions in this public repository uses standard runners without billable private-repository minutes.

Scheduled GitHub workflows can be delayed or dropped, so this improves availability but cannot guarantee continuous uptime. Render can also restart a Free service at any time. The service's monthly Free instance hours are consumed while it stays awake.

To stop the heartbeat, disable the workflow in the repository's **Actions** tab or remove the cron schedule.
