### Note
This is a fork of mccreath/isitup-for-slack. I modified this to be deployed easily on Heroku. I removed the hardcoded token to grab from Heroku environment variable (SLACK_SLASH_TOKEN). That way you can test against your own team's configured slash command token. You will need to need to set the variable like so:

```bash
heroku config:set SLACK_SLASH_TOKEN=[your_team_config_token]
```

# isitup-for-slack

Custom slash command to use isitup.org to check if a site is up from within Slack

## REQUIREMENTS

* A custom slash command on a Slack team
* A web server running PHP5 with cURL enabled
* A valid SSL certificate for your web server (not self-signed)

## USAGE

* Place the `isitup.php` script on a server running PHP5 with cURL and a valid SSL certificate.
* Set up a new custom slash command on your Slack team: https://slack.com/apps/A0F82E8CA-slash-commands
* Under "Choose a command", enter whatever you want for the command. /isitup is easy to remember.
* Under "URL", enter the URL for the script on your server.
* Leave "Method" set to "Post".
* Decide whether you want this command to show in the autocomplete list for slash commands.
* If you do, enter a short description and usage hint.
* Update the `isitup.php` script with your slash command's token.

## DOWNLOAD 

You can download the completed script and a tutorial for writing your own at https://github.com/mccreath/isitup-for-slack/
