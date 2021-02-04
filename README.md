
[![NuGet version (NLog.Targets.MicrosoftTeams)](https://img.shields.io/nuget/v/NLog.Targets.MicrosoftTeams.svg?style=flat)](https://www.nuget.org/packages/NLog.Targets.MicrosoftTeams)
# NLog.Targets.MicrosoftTeams
A NLog target that write log to Microsoft Teams channel via O365 Webhook Connector.

# Output
![Example NLog.Targets.MicrosoftTeams output](image/output.png)

# Usage
```xml
<!-- write logs to Microsoft Teams -->
 <target xsi:type="MicrosoftTeams" 
         name="msTeams" 
         WebhookUrl="Your Microsoft Teams Channel Webhook URL"          
         ApplicationName="Your Application Name"
         CardTitle="Title - ${level:uppercase=true}: ${date} - [${logger}]"
         layout="[${level:uppercase=true}] ${logger} - ${message} ${all-event-properties}"
    />
```
