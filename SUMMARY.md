# Summary

## Overview

* [Bandwidth](README.md)

## Rest API
* [Rest API](methods/restApi.md)
* [/account](methods/account/account.md)
 * [GET /account](methods/account/getAccount.md)
 * [GET /account/transactions](methods/account/getAccountTransactions.md)
* [/applications](methods/applications/applications.md)
 * [GET /applications](methods/applications/getApplications.md)
 * [POST /applications](methods/applications/postApplications.md)
 * [GET /applications/{applicationId}](methods/applications/getApplicationsApplicationId.md)
 * [POST /applications/{applicationId}](methods/applications/postApplicationsApplicationId.md)
 * [DELETE /applications/{applicationId}](methods/applications/deleteApplicationsApplicationId.md)
* [/availableNumbers](methods/availableNumbers/availableNumbers.md)
 * [GET /availableNumbers/local](methods/availableNumbers/getAvailableNumbersLocal.md)
 * [POST /availableNumbers/local](methods/availableNumbers/postAvailableNumbersLocal.md)
 * [GET /availableNumbers/tollFree](methods/availableNumbers/getAvailableNumbersTollFree.md)
 * [POST /availableNumbers/tollFree](methods/availableNumbers/postAvailableNumbersTollFree.md)
* [/bridges](methods/bridges/bridges.md)
 * [GET /bridges](methods/bridges/getBridges.md)
 * [POST /bridges](methods/bridges/postBridges.md)
 * [GET /bridges/{bridgeId}](methods/bridges/getBridgesBridgeId.md)
 * [POST /bridges/{bridgeId}](methods/bridges/postBridgesBridgeId.md)
 * [POST /bridges/{bridgeId}/audio](methods/bridges/postBridgesBridgeIdAudio.md)
 * [GET /bridges/{bridgeId}/calls](methods/bridges/getBridgesBridgeIdCalls.md)
* [/calls](methods/calls/calls.md)
 * [GET /calls](methods/calls/getCalls.md)
 * [POST /calls](methods/calls/postCalls.md)
 * [GET /calls/{callId}](methods/calls/getCallsCallId.md)
 * [POST /calls/{callId}](methods/calls/postCallsCallId.md)
 * [POST /calls/{callId}/audio](methods/calls/postCallsCallIdAudio.md)
 * [POST /calls/{callId}/DTMF](methods/calls/postCallsCallIdDTMF.md)
 * [GET /calls/{callId}/events](methods/calls/getCallsCallIdEvents.md)
 * [GET /calls/{callId}/events/{eventId}](methods/calls/getCallsCallIdEventsEventId.md)
 * [GET /calls/{callId}/recordings](methods/calls/getCallsCallIdRecordings.md)
 * [GET /calls/{callId}/transcriptions](methods/calls/getCallsCallIdTranscriptions.md)
 * [POST /calls/{callId}/gather](methods/calls/postCallsCallIdGather.md)
 * [GET /calls/{callId}/gather/{gatherId}](methods/calls/getCallsCallIdGatherGatherId.md)
 * [POST /calls/{callId}/gather/{gatherId}](methods/calls/postCallsCallIdGatherGatherId.md)
* [/conferences](methods/conferences/conferences.md)
 * [POST /conferences](methods/conferences/postConferences.md)
 * [GET /conferences/{conferenceId}](methods/conferences/getConferencesConferenceId.md)
 * [POST /conferences/{conferenceId}](methods/conferences/postConferencesConferenceId.md)
 * [POST /conferences/{conferenceId}/audio](methods/conferences/postConferencesConferenceIdAudio.md)
 * [POST /conferences/{conferenceId}/members](methods/conferences/postConferencesConferenceIdMembers.md)
 * [GET /conferences/{conferenceId}/members](methods/conferences/getConferencesConferenceIdMembers.md)
 * [POST /conferences/{conferenceId}/members/{memberId}](methods/conferences/postConferencesConferenceIdMembersMemberId.md)
 * [GET /conferences/{conferenceId}/members/{memberId}](methods/conferences/getConferencesConferenceIdMembersMemberId.md)
 * [POST /conferences/{conferenceId}/members/{memberId}/audio](methods/conferences/postConferencesConferenceIdMembersMemberIdAudio.md)
* [/domains](methods/domains/domains.md)
 * [GET /domains](methods/domains/getDomains.md)
 * [POST /domains](methods/domains/postDomains.md)
 * [DELETE /domains/{domainId}](methods/domains/deleteDomainsDomainId.md)
* [/endpoints](methods/endpoints/endpoints.md)
 * [GET /endpoints](methods/endpoints/getEndpoints.md)
 * [POST /endpoints](methods/endpoints/postEndpoints.md)
 * [GET /endpoints/{endpointId}](methods/endpoints/getEndpointsEndpointId.md)
 * [DELETE /endpoints/{endpointId}](methods/endpoints/deleteEndpointsEndpointId.md)
 * [POST /endpoints/{endpointId}](methods/endpoints/postEndpointsEndpointId.md)
* [/errors](methods/errors/errors.md)
 * [GET /errors](methods/errors/getErrors.md)
 * [GET /errors/{errorId}](methods/errors/getErrorsErrorId.md)
* [/media](methods/media/media.md)
 * [GET /media](methods/media/getMedia.md)
 * [PUT /media/{mediaName}](methods/media/putMediaMediaName.md)
 * [GET /media/{mediaName}](methods/media/getMediaMediaName.md)
 * [DELETE /media/{mediaName}](methods/media/deleteMediaMediaName.md)
* [/messages](methods/messages/messages.md)
 * [GET /messages](methods/messages/getMessages.md)
 * [POST /messages](methods/messages/postMessages.md)
 * [GET /messages/{messageId}](methods/messages/getMessagesMessageId.md)
* [/numberInfo](methods/numberInfo/numberInfo.md)
 * [GET /numberInfo/{number}](methods/numberInfo/getNumberInfo.md)
* [/phoneNumbers](methods/phoneNumbers/phoneNumbers.md)
 * [GET /phoneNumbers](methods/phoneNumbers/getPhoneNumbers.md)
 * [POST /phoneNumbers](methods/phoneNumbers/postPhoneNumbers.md)
 * [GET /phoneNumbers/{numberId}](methods/phoneNumbers/getPhoneNumbersNumberId.md)
 * [POST /phoneNumbers/{numberId}](methods/phoneNumbers/postPhoneNumbersNumberId.md)
 * [DELETE /phoneNumbers/{numberId}](methods/phoneNumbers/deletePhoneNumbersNumberId.md)
* [/recordings](methods/recordings/recordings.md)
 * [GET /recordings](methods/recordings/getRecordings.md)
 * [GET /recordings/{recordingId}](methods/recordings/getRecordingsRecordingId.md)
* [/recordings/{id}/transcriptions](methods/transcriptions/transcriptions.md)
 * [POST /transcriptions](methods/transcriptions/postTranscriptions.md)
 * [GET /transcriptions](methods/transcriptions/getTranscriptions.md)
 * [GET /transcriptions/{transcriptionId}](methods/transcriptions/getTranscriptionsTranscriptionId.md)

## Rest API Callbacks
* [Callbacks](apiCallbacks/callbacks.md)
* [Messaging Events](apiCallbacks/messagingEvents.md)
 * [SMS Event](apiCallbacks/sms.md)
 * [MMS Event](apiCallbacks/mms.md)
* [Voice Events](apiCallbacks/voiceEvents.md)
 * [Answer Event](apiCallbacks/answer.md)
 * [Audio File Playback Events](apiCallbacks/audio.md)
 * [CallTimeout Event](apiCallbacks/timeout.md)
 * [Conference Event](apiCallbacks/conf.md)
 * [Conference Audio File Playback Event](apiCallbacks/confAudio.md)
 * [Conference Member Event](apiCallbacks/confMember.md)
 * [Conference Speak Event](apiCallbacks/confSpeak.md)
 * [DTMF Event](apiCallbacks/dtmf.md)
 * [Gather Event](apiCallbacks/gather.md)
 * [Incoming Call Event](apiCallbacks/incomingCall.md)
 * [Hangup Event](apiCallbacks/hangup.md)
 * [Recording Event](apiCallbacks/recording.md)
 * [Reject Event](apiCallbacks/reject.md)
 * [Speak Event](apiCallbacks/speak.md)
 * [Transcription Event – BETA](apiCallbacks/transcription.md)

## BXML
* [BXML](bxml/bxml.md)
* [Call](bxml/verbs/call.md)
* [Conference](bxml/verbs/conference.md)
* [Gather](bxml/verbs/gather.md)
* [Hangup](bxml/verbs/hangup.md)
* [Media](bxml/verbs/media.md)
* [Pause](bxml/verbs/pause.md)
* [PlayAudio](bxml/verbs/playAudio.md)
* [Record](bxml/verbs/record.md)
* [Reject](bxml/verbs/reject.md)
* [SendMessage](bxml/verbs/sendMessage.md)
* [SpeakSentence](bxml/verbs/speakSentence.md)
* [Transfer](bxml/verbs/transfer.md)

## BXML Callbacks
* [BXML Callbacks](bxml/bxmlCallbacks.md)
* [Answer Event](bxml/callBacks/answer.md)
* [Gather event](bxml/callBacks/gather.md)
* [Hangup Event](bxml/callBacks/hangup.md)
* [Incoming Call Event](bxml/callBacks/incomingCall.md)
* [Recording event](bxml/callBacks/recording.md)
* [Redirect event](bxml/callBacks/redirect.md)
* [SMS event](bxml/callBacks/sms.md)
* [Transfer Complete Event](bxml/callBacks/transfer.md)