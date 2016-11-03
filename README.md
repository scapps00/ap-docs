# Get Started

Before you can send your first SMS message, you will need to

1. [Sign up](https://catapult.inetwork.com/beta/signup) for a free Bandwidth API account.
2. Get a number under the “My Numbers” tab (more specific instructions [here](https://bandwidth.github.io/howto/buytn.html))

## Base URL
`https://api.catapult.inetwork.com/v1`

## Send your First SMS Message
To send your first SMS message we have included instructions for using Postman, a helpful program for testing APIs (download), and also code that can be found further down this page.

### Run in Stoplight!
<div style='display: inline-block;'>
  <a href='https://app.stoplight.io/scenarios/share/pHgmMR4Wthk2Pdpo3'>
    <img width='150' src='https://cdn.stoplight.io/run-buttons/solid-blue.png' alt='Run in Stoplight' style='display: block;' />
  </a>
</div>

## Using Postman

<input type="text" id="apiToken-input" placeholder="Your API Token">
<input type="text" id="apiSecret-input" placeholder="Your API Secret">
<input type="text" id="userId-input" placeholder="Your User Id">
<input type="text" id="tn-input" placeholder="Your Phone Number">
<button onclick="myFunction()">Update</button>

<div class="postman-run-button"
data-postman-action="collection/import"
data-postman-var-1="4235678e85fc6b87e742"
data-postman-param="env%5BBandwidth%20Creds%5D=W3sia2V5Ijoic2VjcmV0IiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoidG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0IiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJ1c2VySWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0IiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJmcm9tTnVtYmVyIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoidG9OdW1iZXIiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0IiwiZW5hYmxlZCI6dHJ1ZX1d"></div>
<script type="text/javascript">
  (function (p,o,s,t,m,a,n) {
    !p[s] && (p[s] = function () { (p[t] || (p[t] = [])).push(arguments); });
    !o.getElementById(s+t) && o.getElementsByTagName("head")[0].appendChild((
      (n = o.createElement("script")),
      (n.id = s+t), (n.async = 1), (n.src = m), n
    ));
  }(window, document, "_pm", "PostmanRunObject", "https://run.pstmn.io/button.js"));
 </script>

 <script>
	function myFunction() {
		var apiToken = document.getElementById('apiToken-input').value;
		var apiSecret = document.getElementById('apiSecret-input').value;
		var userId = document.getElementById('userId-input').value;
		var tn = document.getElementById('tn-input').value;

    if (typeof(Storage) !== "undefined") {

        localStorage.setItem("apiToken", apiToken);
        localStorage.setItem("apiSecret", apiSecret);
        localStorage.setItem("userId", userId);
        localStorage.setItem("tn", tn);
    } else {
        Console.log("No localStorage Support");
    }

		envData = { token: apiToken, secret: apiSecret, userId: userId, toNumber: tn };
		//console.log(envData);
		var res = _pm('env.assign', 'Bandwidth Creds', envData);
		//console.log("PM: " + res);
  };
</script>




* Import the example to Postman by clicking the button and access it in “Collections”.
* Make sure to replace the `{userId}` in the url and the `{token}` and `{secret}` in Authorization.  Your credentials can be found in the “Account” tab of the API console.
* Also set the phone numbers and message in Body.

## REST API Reference Index

| Resource                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`/account`](methods/account/account.md)                                      | Account API allows you to retrieve your current balance, transaction list, account type and all elements related to your platform account.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [`/applications`](methods/applications/applications.md)                       | The Applications resource lets you define call and message handling applications. You write an application on your own servers and have Bandwidth API send events to it by configuring a callback URL.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [`/availableNumbers`](methods/availableNumbers/availableNumbers.md)           | The Available Numbers resource lets you search for numbers that are available for use with your application.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [`/bridges`](methods/bridges/bridges.md)                                      | The Bridges resource allows you to bridge two calls together allowing for two way audio between them. A common example is bridging an incoming phone call together with a outgoing phone call.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [`/calls`](methods/calls/calls.md)                                            | The Calls resource lets you make phone calls and view information about previous inbound and outbound calls.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [`/conferences`](methods/conferences/conferences.md)                          | The Conference resource allows you create conferences, add members to it, play audio, speak text, mute/unmute members, hold/unhold members and other things related to conferencing. Once a conference is created there is no timeout associated with it, i.e., the conference will stay in created state until it is explicitly terminated. After the last member of a conference is removed from it, the conference will be set automatically as completed.                                                                                                                                                                                                                                                                                                                                                                                      |
| [`/domains`](methods/domains/domains.md)                                      | A domain is a way to logically group endpoints. There is a 100 domain max. per account limit. Most use cases require using a single domain for all endpoints. The name of the domain will be part of a public DNS record. For that reason, we let the customer choose their domain names. Once a domain has been created, endpoints can be created and managed within the context of the domain. Because endpoints can only exist within the context of a domain, creating a domain is the first step in creating endpoints.                                                                                                                                                                                                                                                                                                                       |
| [`/endpoints`](methods/endpoints/endpoints.md)                                | An endpoint represents is an entity that can register with the Application Platform SIP Registrar and place and receive calls. This can be a device like a phone or a pad, or it can be a softphone on a computer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [`/errors`](methods/errors/errors.md)                                         | The Errors resource lets you see information about errors that happened in your API calls and during applications callbacks. This error information can be very helpful when you're debugging an application. Because error information can be large, and errors in the distant past are less useful than new ones, Bandwidth API limits the number of user errors it keeps.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [`/media`](methods/media/media.md)                                            | The Media resource lets you upload your media files to Bandwidth API servers so they can be used in applications without requiring a separate hosting provider. You can upload files up to 65MB and file storage is free for an unlimited number of files. Files you upload can only be accessed by you when you supply your API access token and secret. They are not available to anonymous users. Bandwidth API supports the Cache-Control header when you upload files.                                                                                                                                                                                                                                                                                                                                                                        |
| [`/messages`](methods/messages/messages.md)                                   | The Messages resource lets you send SMS/MMS messages and view messages that were previously sent or received.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [`/numberInfo`](methods/numberInfo/numberInfo.md)                             | This resource provides a CNAM number info. CNAM is an acronym which stands for Caller ID Name. CNAM can be used to display the calling party's name alongside the phone number, to help users easily identify a caller. CNAM API allows the user to get the CNAM information of a particular number.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [`/phoneNumbers`](methods/phoneNumbers/phoneNumbers.md)                       | The Phone Numbers resource lets you get phone numbers for use with your programs and manage numbers you already have.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [`/recordings`](methods/recordings/recordings.md)                             | Retrieve information about call recordings. The recording information retrieved by GET method contains only textual data related to call recording as described on Properties section. To properly work with recorded media content such as download and removal of media file, please access /media documentation. To learn about how to transcribe recordings, read the /recordings/{id}/transcriptions documentation.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [`/recordings/{id}/transcriptions`](methods/transcriptions/transcriptions.md) | The Transcription resource lets you transcribe a voicemail recording. This resource can be either created automatically when the call property transcriptionEnabled is set to true, when call is created, or during the call by posting an event. The transcription is based on a call audio recording. By enabling/disabling call property recordingEnabled, a call can have more than one recording, so it's possible to have one or more transcriptions for each one of those recordings. When transcriptionEnabled is set to true all the recordings generated within that call are going to be transcribed, i.e, if you start to record a call, at any given time when the call is active, and then terminate the recording, the transcription resource will be automatically started for this recording; this process can happen many times. |

## REST API Callback Reference Index

## Messaging Events

| Event                            | Description                                                                       |
|:---------------------------------|:----------------------------------------------------------------------------------|
| [SMS Event](apiCallbacks/sms.md) | Bandwidth API sends this event to the application when an SMS is sent or received |
| [MMS Event](apiCallbacks/mms.md) | Events sent to your server for inbound and outbound MMS messages.                 |

## Voice Events

| Event                                                             | Description                                                                                                                                                                                               |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Answer Event](apiCallbacks/answer.md)                            | Bandwidth API sends this message to the application when the call is answered.                                                                                                                            |
| [Audio File Playback Events](apiCallbacks/audio.md)               | Bandwidth API sends this message to the application when audio file playback is started or done playing.                                                                                                  |
| [CallTimeout Event](apiCallbacks/timeout.md)                      | Bandwidth API sends this message to the application when the call is not answered until the specified timeout.                                                                                            |
| [Conference Event](apiCallbacks/conf.md)                          | Bandwidth API sends this event to the application when a conference is created or completed.                                                                                                              |
| [Conference Audio File Playback Event](apiCallbacks/confAudio.md) | Bandwidth API sends this message to the application when audio playback has started or is done (stopped) in a conference. Note: For playback event in conference member, use the call playback event.     |
| [Conference Member Event](apiCallbacks/confMember.md)             | Bandwidth API sends this message to the application when a conference member has joined / left the conference or when it as muted or put on hold.                                                         |
| [Conference Speak Event](apiCallbacks/confSpeak.md)               | Bandwidth API sends this message to the application when text-to-speech speaking has started or is done (stopped) in a conference. Note:— For speak event in conference member, use the call speak event. |
| [DTMF Event](apiCallbacks/dtmf.md)                                | Bandwidth API sends this message to the application when it receives number pad tone signals during a call.                                                                                               |
| [Gather Event](apiCallbacks/gather.md)                            | The Bandwidth API generates a gather event when the gather command completes in a call.                                                                                                                   |
| [Incoming Call Event](apiCallbacks/incomingCall.md)               | Bandwidth API sends this message to the application when an incoming call arrives. For incoming call the callback set is the one related to the Application associated with the called number.            |
| [Hangup Event](apiCallbacks/hangup.md)                            | Bandwidth API sends this message to the application when the call ends.                                                                                                                                   |
| [Recording Event](apiCallbacks/recording.md)                      | Bandwidth API sends this event to the application when an the recording media file is saved or an error occurs while saving it.                                                                           |
| [Reject Event](apiCallbacks/reject.md)                            | Bandwidth API sends this message to the application when the call is rejected.                                                                                                                            |
| [Speak Event](apiCallbacks/speak.md)                              | Bandwidth API sends this message to the application when text-to-speech starts or stops.                                                                                                                  |
| [Transcription Event – BETA](apiCallbacks/transcription.md)       | Bandwidth API sends this event to the application when a transcription is terminated or an error occurs while processing it.                                                                              |

## BXML verbs

| Verb                                             | Description                                                                                                                                                                              |
|:-------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`<Call>`](bxml/verbs/call.md)                   | The Call verb is used to create call to another number.                                                                                                                                  |
| [`<Conference>`](bxml/verbs/Conference.md)       | The Conference verb is used to create conferences.                                                                                                                                       |
| [`<Gather>`](bxml/verbs/gather.md)               | The Gather verb is used to collect digits for some period of time.                                                                                                                       |
| [`<Hangup>`](bxml/verbs/hangup.md)               | The Hangup verb is used to hangup current call.                                                                                                                                          |
| [`<Media>`](bxml/verbs/media.md)                 | <Media> is a noun that is used exclusively within [`<SendMessage>`](bxml/verbs/sendMessage.md) to provide attached media (MMS) capability messages. <br> **This feature is coming soon** |
| [`<Pause>`](bxml/verbs/pause.md)                 | Pause is a verb to specify the length of seconds to wait before executing the next verb. <br> ** This feature is coming soon**                                                           |
| [`<PlayAudio>`](bxml/verbs/playAudio.md)         | The PlayAudio verb is used to play an audio file in the call.                                                                                                                            |
| [`<Record>`](bxml/verbs/record.md)               | The Record verb allows call recording. At the end of the call, a call recording event containing the media with recorded audio URL is generated                                          |
| [`<Redirect>`](bxml/verbs/redirect.md)           | The Redirect verb is used to redirect the current XML execution to another URL.                                                                                                          |
| [`<Reject>`](bxml/verbs/reject.md)               | The Reject verb is used to reject incoming calls.<br>  **This feature is coming soon. **                                                                                                 |
| [`<SendMessage>`](bxml/verbs/sendMessage.md)     | The SendMessage verb is used to send a text message.                                                                                                                                     |
| [`<SpeakSentence>`](bxml/verbs/speakSentence.md) | The SpeakSentence verb is used to convert any text into speak for the caller.                                                                                                            |
| [`<Transfer>`](bxml/verbs/transfer.md)           | The Transfer verb is used to transfer the call to another number.                                                                                                                        |

## BXML Callbacks

| Event                                                 | Description                                                                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Answer Event](bxml/callBacks/answer.md)              | Bandwidth API sends this message to the application when the call is answered.                                                                                                                 |
| [Gather event](bxml/callBacks/gather.md)              | Bandwidth API generates a gather event when the gather command completes in a call.                                                                                                            |
| [Hangup Event](bxml/callBacks/hangup.md)              | Bandwidth API sends this message to the application when the call ends.                                                                                                                        |
| [Incoming Call Event](bxml/callBacks/incomingCall.md) | Bandwidth API sends this message to the application when an incoming call arrives. For incoming call the callback set is the one related to the Application associated with the called number. |
| [Recording event](bxml/callBacks/recording.md)        | Bandwidth API sends this event to the application when an the recording media file is saved or an error occurs while saving it.                                                                |
| [Redirect event](bxml/callBacks/redirect.md)          | Bandwidth API sends this event to the application when a `<Redirect>` is requested                                                                                                             |
| [SMS event](bxml/callBacks/sms.md)                    | Bandwidth API sends this event to the application when an SMS is sent or received                                                                                                              |
| [Transfer Complete Event](bxml/callBacks/transfer.md) | Bandwidth API sends this event to the application when the `<Transfer>`is complete                                                                                                             |

---