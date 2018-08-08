{% method %}
## Incoming Call Event

When your account is configured to use BXML, by setting the [application](../../methods/applications/applications.md) with `{ "autoAnswer": true }` and `{ "callbackHttpMethod": "GET" }`. For each incoming call to your Bandwidth Phone Number, Bandwidth will send your server configured as the `incomingCallUrl` both an `incomingCall` event immediately followed by an [`answer`](answer.md) event.

⚠️ **Your server should reply with HTTP 200 to the incomingCall event.  BXML will only be processed in response to the [answer](answer.md) event**

### Properties
| Property  | Description                                                                                                                                                  |
|:----------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventType | The event type, value is `incomingcall`.                                                                                                                     |
| to        | The phone number or SIP address that received the call. Phone numbers are in E.164 format (e.g. +15555555555) -or- SIP addresses (e.g. identify@domain.com). |
| from      | The phone number or SIP address that made the call. Phone numbers are in E.164 format (e.g. +15555555555) -or- SIP addresses (e.g. identify@domain.com).     |
| callState | The call state. Value will be `active`                                                                                                                       |
| callId    | The call id associated with the event.                                                                                                                       |
| callUri   | The full URL of the call resource for this event.                                                                                                            |
| time      | Date when the event occurred. Timestamp follows the ISO8601 format (UTC).                                                                                    |

{% common %}
#### HTTP request sent to the callback url

```html
/{callbackUrl}?
  callState=active&
  to={to-number}&
  withholdCallerNumber=false&
  time=2016-02-20T16%3A22%3A30Z&
  from={from-number}&
  eventType=incomingcall&
  withholdCallerName=false&
  displayName={number}&
  callId={call-id}&
  callUri=https%3A%2F%2Fapi.catapult.inetwork.com%2Fv1%2Fusers%2F{user-id}%2Fcalls%2F{call-id}
```

{% endmethod %}