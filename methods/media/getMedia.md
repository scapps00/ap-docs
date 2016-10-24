{% method %}
## GET media
Gets a list of your media files. No query parameters are supported.

## Properties
| Property      | Description                                   |
|:--------------|:----------------------------------------------|
| mediaName     | The mediaName is the unique name of the media |
| contentLength | Size of the media in Bytes `B`                |
| content       | URL to use to GET the specific media file.    |

{% common %}
### Example: List Your Media Files


{% sample lang="bash" %}
```bash
curl -v -X GET https://api.catapult.inetwork.com/v1/users/{userId}/media \
	-u {token}:{secret} \
	-H "Content-type: application/json"
```

{% sample lang="js" %}
```js
client.Media.list()
then(function (media) {
  console.log(media);
});
```

{% sample lang="csharp" %}
```csharp
var list = client.Media.List();
```

{% sample lang="ruby" %}
```ruby
list = Media.list(client)
```

{% common %}

> The above command returns JSON structured like this:

```json
[
  {
    "contentLength": 561276,
    "mediaName": "{mediaName1}",
    "content": "api.catapult.inetwork.com/.../media/{mediaName1}"
  },
  {
    "contentLength": 2703360,
    "mediaName": "{mediaName2}",
    "content": "https://api.catapult.inetwork.com/.../media/{mediaName2}"
  },
  {
    "contentLength": 2257901,
    "mediaName": "{mediaName3}",
        "content": "https://api.catapult.inetwork.com/.../media/{mediaName3}"
  }
]
```
{% endmethod %}