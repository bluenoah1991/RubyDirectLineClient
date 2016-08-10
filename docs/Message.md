# SwaggerClient::Message

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | ID for this message | [optional] 
**conversation_id** | **String** | Conversation ID for this message | [optional] 
**created** | **DateTime** | UTC timestamp when this message was created | [optional] 
**from** | **String** | Identity of the sender of this message | [optional] 
**text** | **String** | Text in this message | [optional] 
**channel_data** | **Object** | Opaque block of data passed to/from bot via the ChannelData field | [optional] 
**images** | **Array&lt;String&gt;** | Array of URLs for images included in this message | [optional] 
**attachments** | [**Array&lt;Attachment&gt;**](Attachment.md) | Array of non-image attachments included in this message | [optional] 
**e_tag** | **String** |  | [optional] 


