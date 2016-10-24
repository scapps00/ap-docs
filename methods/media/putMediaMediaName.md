{% method %}
## PUT media/{mediaName}
Uploads a file the normal HTTP way. You may add headers to the request in order to provide some control to your media-file.

<aside class="alert general small">
You can upload files up to `65MB` and file storage is free for an unlimited number of files.
</aside>

### Properties
| Header         | Description                                                                                                                        | Mandatory |
|:---------------|:-----------------------------------------------------------------------------------------------------------------------------------|:----------|
| Content-Length | Indicates the size of the entity-body.                                                                                             | Yes       |
| Cache-Control  | General-header field is used to specify directives that MUST be obeyed by all caching mechanisms along the request/response chain. | No        |
| Content-Type   | The media type of the entity-body.                                                                                                 | No        |

{% common %}
### Example: Upload an MP3 File

{% sample lang="bash" %}
```bash
#coming soon
```

{% sample lang="js" %}
```js
//Coming soon
```

{% sample lang="csharp" %}
```csharp
await client.Media.UploadAsync(new UploadMediaData{
		MediaName = "file.mp3",
		Path = "/path/to/file.mp3",
		ContentType = "audio/mp3"
	}
);
```

{% sample lang="ruby" %}
```ruby
Media.upload(client, "file.mp3", File.open("/path/to/file.mp3"), "audio/mp3")
```
{% endmethod %}