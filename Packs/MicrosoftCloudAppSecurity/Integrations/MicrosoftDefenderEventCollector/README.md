Microsoft Defender for Cloud Apps Event Collector integration.

## Configure Microsoft Defender for Cloud Apps Event Collector on Cortex XSOAR

1. Navigate to **Settings** > **Integrations** > **Servers & Services**.
2. Search for Microsoft Defender for Cloud Apps Event Collector.
3. Click **Add instance** to create and configure a new integration instance.

    | **Parameter** | **Description** | **Required** |
    | --- | --- | --- |
    | Endpoint URI | The United States: api-us.security.microsoft.com<br/>Europe: api-eu.security.microsoft.com<br/>The United Kingdom: api-uk.security.microsoft.com | True |
    | Client (Application) ID | The Client \(Application\) ID to use to connect. | True |
    | Client Secret |  | True |
    | Tenant ID |  | True |
    | Scope |  | True |
    | First fetch timestamp (&lt;number&gt; &lt;time unit&gt;, e.g., 12 hours, 7 days) |  | False |
    | Vendor | The vendor name to be used in the dataset name, in this format &amp;lt;vendor&amp;gt;_&amp;lt;product&amp;gt;_raw. | False |
    | Product |  | False |
    | Number of alerts for each fetch. | Due to API limitations, the maximum is 10,000. | False |
    | Fetch events |  | False |
    | Verify SSL Certificate |  | False |
    | Use system proxy settings |  | False |

4. Click **Test** to validate the URLs, token, and connection.
## Commands
You can execute these commands from the Cortex XSOAR CLI, as part of an automation, or in a playbook.
After you successfully execute a command, a DBot message appears in the War Room with the command details.
### microsoft-defender-cloud-apps-get-events
***
Returns a list of alerts.


#### Base Command

`microsoft-defender-cloud-apps-get-events`
#### Input

| **Argument Name** | **Description** | **Required** |
| --- | --- | --- |
| limit | The maximum number of alerts per fetch. Default is 10000. | Optional | 
| after | The first fetch time (&lt;number&gt; &lt;time unit&gt;, for example 12 hours, 1 day, 3 months). Default is 3 days. | Optional | 
| push_to_xsiam | Whether to push the fetched event to XSIAM or not. Possible values are: false, true. Default is false. | Optional | 


#### Context Output

There is no context output for this command.