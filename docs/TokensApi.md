# SwaggerClient::TokensApi

All URIs are relative to *https://directline.botframework.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tokens_generate_token_for_new_conversation**](TokensApi.md#tokens_generate_token_for_new_conversation) | **POST** /api/tokens/conversation | Generate a token for a new conversation
[**tokens_renew_token**](TokensApi.md#tokens_renew_token) | **GET** /api/tokens/{conversationId}/renew | Renew a token for a conversation


# **tokens_generate_token_for_new_conversation**
> String tokens_generate_token_for_new_conversation

Generate a token for a new conversation

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::TokensApi.new

begin
  #Generate a token for a new conversation
  result = api_instance.tokens_generate_token_for_new_conversation
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling TokensApi->tokens_generate_token_for_new_conversation: #{e}"
end
```

### Parameters
This endpoint does not need any parameter.

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/json, text/html, application/xml, text/xml



# **tokens_renew_token**
> String tokens_renew_token(conversation_id)

Renew a token for a conversation

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::TokensApi.new

conversation_id = "conversation_id_example" # String | 


begin
  #Renew a token for a conversation
  result = api_instance.tokens_renew_token(conversation_id)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling TokensApi->tokens_renew_token: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversation_id** | **String**|  | 

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/json, text/html, application/xml, text/xml



