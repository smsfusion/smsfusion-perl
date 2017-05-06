# WWW::SwaggerClient::SMSApi

## Load the API package
```perl
use WWW::SwaggerClient::Object::SMSApi;
```

All URIs are relative to *https://api.smsfusion.com.au/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**send_sms**](SMSApi.md#send_sms) | **GET** /sms/ | Send an SMS


# **send_sms**
> SMSResult send_sms(key => $key, num => $num, msg => $msg, from => $from, deliverby => $deliverby, dlrcb => $dlrcb, replycb => $replycb, replyemail => $replyemail, validity => $validity, cc => $cc)

Send an SMS

Send one or more SMS

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::Configuration;
use WWW::SwaggerClient::SMSApi;

# Configure API key authorization: api_key
$WWW::SwaggerClient::Configuration::api_key->{'key'} = 'YOUR_API_KEY';
# uncomment below to setup prefix (e.g. Bearer) for API key, if needed
#$WWW::SwaggerClient::Configuration::api_key_prefix->{'key'} = "Bearer";

my $api_instance = WWW::SwaggerClient::SMSApi->new();
my $key = 'key_example'; # string | API Key as generated from the <a href='https://www.smsfusion.com.au/admin/api/'>admin panel</a>
my $num = []; # ARRAY[string] | Comma separated list of phone numbers or <a href='https://www.smsfusion.com.au/help/msisdn/'>MSDISDN</a>'s
my $msg = 'msg_example'; # string | Message content to send
my $from = 'from_example'; # string | MSISDN or vanity alphanumeric source number
my $deliverby = 'deliverby_example'; # string | UTC encoded time to send the SMS
my $dlrcb = 'dlrcb_example'; # string | HTTP or HTTPS callback URL for delivery reports. Timeout for callbacks is set to 30 seconds
my $replycb = 'replycb_example'; # string | HTTP or HTTPS callback URL for replies. Timeout for callbacks is set to 30 seconds
my $replyemail = 'replyemail_example'; # string | Email address to send replies to
my $validity = 56; # int | Time in minutes to keep the SMS valid for
my $cc = 'cc_example'; # string | 2 character country code <a href='https://en.wikipedia.org/wiki/ISO_3166-2'>ISO 3166-2</a> for formatting local numbers internationally

eval { 
    my $result = $api_instance->send_sms(key => $key, num => $num, msg => $msg, from => $from, deliverby => $deliverby, dlrcb => $dlrcb, replycb => $replycb, replyemail => $replyemail, validity => $validity, cc => $cc);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SMSApi->send_sms: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**| API Key as generated from the &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/admin/api/&#39;&gt;admin panel&lt;/a&gt; | 
 **num** | [**ARRAY[string]**](string.md)| Comma separated list of phone numbers or &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/help/msisdn/&#39;&gt;MSDISDN&lt;/a&gt;&#39;s | 
 **msg** | **string**| Message content to send | 
 **from** | **string**| MSISDN or vanity alphanumeric source number | [optional] 
 **deliverby** | **string**| UTC encoded time to send the SMS | [optional] 
 **dlrcb** | **string**| HTTP or HTTPS callback URL for delivery reports. Timeout for callbacks is set to 30 seconds | [optional] 
 **replycb** | **string**| HTTP or HTTPS callback URL for replies. Timeout for callbacks is set to 30 seconds | [optional] 
 **replyemail** | **string**| Email address to send replies to | [optional] 
 **validity** | **int**| Time in minutes to keep the SMS valid for | [optional] 
 **cc** | **string**| 2 character country code &lt;a href&#x3D;&#39;https://en.wikipedia.org/wiki/ISO_3166-2&#39;&gt;ISO 3166-2&lt;/a&gt; for formatting local numbers internationally | [optional] 

### Return type

[**SMSResult**](SMSResult.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

