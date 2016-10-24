{% method %}
## GET bridges/{bridgeId}/calls

Get the list of calls that are on the bridge.

{% sample lang="bash" %}
```bash
curl -v -X GET https://api.catapult.inetwork.com/v1/users/{userId}/bridges/{bridgeId}/calls \
	-u {token}:{secret} \
	-H "Content-type: application/json" \
```

{% sample lang="js" %}
```js
//Promise
client.Bridge.getCalls('brg-65dhjbiei')
.then(function (response) {
	console.log(response);
});

//Callback
client.Bridge.getCalls('brg-65dhjrmbasiei',
	function (err, response) {
		if(err) {
			console.log(err);
		}
		else {
			console.log(response);
		}
	});
  ```

{% sample lang="csharp" %}
```csharp
var calls = client.Bridge.GetCalls("brg-65dhmbasiei");
```

{% sample lang="ruby" %}
```ruby
calls = bridge.get_calls()
```


  > The above command returns JSON structured like this:

{% sample lang="js" %}
```json
[
    {
        "activeTime": "2013-05-22T19:49:39Z",
        "direction": "out",
        "from": "{fromNumber}",
        "id": "{callId1}",
        "bridgeId": "{bridgeId}",
        "startTime": "2013-05-22T19:49:35Z",
        "state": "active",
        "to": "{toNumber1}",
        "recordingEnabled": false,
        "events": "https://api.catapult.inetwork.com/v1/users/{userId}/calls/{callId1}/events",
        "bridge": "https://api.catapult.inetwork.com/v1/users/{userId}/bridges/{bridgeId}"
    },
    {
        "activeTime": "2013-05-22T19:50:16Z",
        "direction": "out",
        "from": "{fromNumber}",
        "id": "{callId2}",
        "bridgeId": "{bridgeId}",
        "startTime": "2013-05-22T19:50:16Z",
        "state": "active",
        "to": "{toNumber2}",
        "recordingEnabled": false,
        "events": "https://api.catapult.inetwork.com/v1/users/{userId}/calls/{callId2}/events",
        "bridge": "https://api.catapult.inetwork.com/v1/users/{userId}/bridges/{bridgeId}"
    }
]
```

{% endmethod %}