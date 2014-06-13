Live-WorldCup-Notification-for-Slack
====================================

It's a NodeJS worker that request every 1 minute data from the FIFA World Cup API and notifies via Slack API (It's possible to apply other ways of notification) the changes of the match.

====================================

+ It notifies when a match starts
+ It notifies when the score changes (this means Goal or the match finished)

It is posible to run it as a worker on Heroku :)

## Configurations

### Slack Web Hook

You need to add an Incoming WebHooks integration in Slack settings. Slack will provide a URL, it must be configured on heroku.

Example:
```
SLACKHOOK=https://yourslackdomain.slack.com/services/hooks/incoming-webhook?token=SomeSecretToken
```

### Language

The default language is English (en) but you can configure others, like Portuguese(pt) or Spanish(es). To configure simply set an environment variable in heroku named LANGUAGE.

Example:
```
LANGUAGE=pt
```

### Channel

The default channel is #random but you can change that setting a CHANNEL environnment variable.

Example:
```
CHANNEL=general
```

