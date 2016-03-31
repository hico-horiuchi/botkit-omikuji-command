# :crystal_ball: botkit-omikuji-command

![screen.png](https://raw.githubusercontent.com/hico-horiuchi/botkit-omikuji-command/master/screen.png)

Randomly selection from choices like "omikuji."  
This command is implemented by Botkit.

<a href="https://slack.com/oauth/authorize?scope=commands&client_id=12263613568.17678729859"><img alt="Add to Slack" height="32" width="111" src="https://platform.slack-edge.com/img/add_to_slack.png" srcset="https://platform.slack-edge.com/img/add_to_slack.png 1x, https://platform.slack-edge.com/img/add_to_slack@2x.png 2x"></a> [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Install

First, you must create a Slack app at [Slack API: New Application | Slack](https://api.slack.com/applications/new).  
And make sure to configure at least one Slash command.

You can test your oauth authentication locally.  
But, the app must be hosted at a publicly reachable IP or host to use Slash commands in Slack.  
So, I recommend to use Heroku as follows.

    $ heroku create --stack cedar omikuji-command
    $ heroku config:set BOTKIT_SLACK_CLIENT_ID=""
    $ heroku config:set BOTKIT_SLACK_CLIENT_SECRET=""
    $ heroku config:set TZ=Asia/Tokyo
    $ git push heroku master
