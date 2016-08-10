# SwaggerClient::ConversationsApi

All URIs are relative to *https://directline.botframework.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**conversations_get_messages**](ConversationsApi.md#conversations_get_messages) | **GET** /api/conversations/{conversationId}/messages | Get messages in this conversation. This method is paged with the &#39;watermark&#39; parameter.
[**conversations_new_conversation**](ConversationsApi.md#conversations_new_conversation) | **POST** /api/conversations | Start a new conversation
[**conversations_post_message**](ConversationsApi.md#conversations_post_message) | **POST** /api/conversations/{conversationId}/messages | Send a message
[**conversations_upload**](ConversationsApi.md#conversations_upload) | **POST** /api/conversations/{conversationId}/upload | Upload file(s) and send as attachment(s)


# **conversations_get_messages**
> MessageSet conversations_get_messages(conversation_id, opts)

Get messages in this conversation. This method is paged with the 'watermark' parameter.

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::ConversationsApi.new

conversation_id = "conversation_id_example" # String | Conversation ID

opts = { 
  watermark: "watermark_example" # String | (Optional) only returns messages newer than this watermark
}

begin
  #Get messages in this conversation. This method is paged with the 'watermark' parameter.
  result = api_instance.conversations_get_messages(conversation_id, opts)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling ConversationsApi->conversations_get_messages: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversation_id** | **String**| Conversation ID | 
 **watermark** | **String**| (Optional) only returns messages newer than this watermark | [optional] 

### Return type

[**MessageSet**](MessageSet.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/json, text/html, application/xml, text/xml



# **conversations_new_conversation**
> Conversation conversations_new_conversation

Start a new conversation

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::ConversationsApi.new

begin
  #Start a new conversation
  result = api_instance.conversations_new_conversation
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling ConversationsApi->conversations_new_conversation: #{e}"
end
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Conversation**](Conversation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/json, text/html, application/xml, text/xml



# **conversations_post_message**
> ErrorMessage conversations_post_message(conversation_id, message)

Send a message

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::ConversationsApi.new

conversation_id = "conversation_id_example" # String | Conversation ID

message = SwaggerClient::Message.new # Message | Message to send


begin
  #Send a message
  result = api_instance.conversations_post_message(conversation_id, message)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling ConversationsApi->conversations_post_message: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversation_id** | **String**| Conversation ID | 
 **message** | [**Message**](Message.md)| Message to send | 

### Return type

[**ErrorMessage**](ErrorMessage.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/json, text/html, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: Not defined



# **conversations_upload**
> conversations_upload(conversation_id)

Upload file(s) and send as attachment(s)

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::ConversationsApi.new

conversation_id = "conversation_id_example" # String | 


begin
  #Upload file(s) and send as attachment(s)
  api_instance.conversations_upload(conversation_id)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling ConversationsApi->conversations_upload: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversation_id** | **String**|  | 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



