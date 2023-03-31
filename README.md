# Celestia Monitoring Script

This is a Bash script to monitor the Celestia process and relaunch it automatically if it crashes.

## Features
- Continuously monitors the Celestia process and relaunches it if it crashes.
- Sends a webhook notification when the node is down and a relaunch occurs.
- Waits for a specified time before checking the Celestia light node status again.
- Waits for a longer time before checking again if a relaunch fails.


## Requirements

- `celestia` command-line tool installed on the machine https://docs.celestia.org/nodes/itn-deploy-light/
- curl

## Usage

1. Edit the script to set your webhook (Telegram, Discord...) URL and Celestia command.
2. Make the script executable: `chmod +x celestia_monitor.sh`
3. Run the script: `./celestia_monitor.sh`

### Configuration

The script has the following configuration options:

- `WEBHOOK_URL`: the URL of the webhook to use for notifications.
- `CELESTIA_CMD`: the command to use to start the Celestia light node process.
- `WAIT_TIME`: the time to wait before checking the status of the Celestia process again (in seconds).
- `RELAUNCH_WAIT_TIME`: the time to wait before attempting to relaunch the Celestia process after a failure (in seconds).
