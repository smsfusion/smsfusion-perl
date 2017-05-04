# WWW::SwaggerClient::DefaultApi

## Load the API package
```perl
use WWW::SwaggerClient::Object::DefaultApi;
```

All URIs are relative to *http://api.smsfusion.com.au/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_hlr**](DefaultApi.md#get_hlr) | **GET** /hlr/ | HLR number lookup
[**get_hlr_callback**](DefaultApi.md#get_hlr_callback) | **GET** /hlr-callback/ | HLR number lookup with results going to a callback URL


# **get_hlr**
> HLRCallback get_hlr(key => $key, num => $num, cc => $cc)

HLR number lookup

Perform HLR on number

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::Configuration;
use WWW::SwaggerClient::DefaultApi;

# Configure API key authorization: api_key
$WWW::SwaggerClient::Configuration::api_key->{'key'} = 'YOUR_API_KEY';
# uncomment below to setup prefix (e.g. Bearer) for API key, if needed
#$WWW::SwaggerClient::Configuration::api_key_prefix->{'key'} = "Bearer";

my $api_instance = WWW::SwaggerClient::DefaultApi->new();
my $key = 'key_example'; # string | API Key as generated from the <a href='https://www.smsfusion.com.au/admin/api/'>admin panel</a>
my $num = 'num_example'; # string | A single phone number or <a href='https://www.smsfusion.com.au/help/msisdn/'>MSDISDN</a>
my $cc = 'cc_example'; # string | 2 character country code <a href='https://en.wikipedia.org/wiki/ISO_3166-2'>ISO 3166-2</a> for formatting local numbers internationally

eval { 
    my $result = $api_instance->get_hlr(key => $key, num => $num, cc => $cc);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DefaultApi->get_hlr: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**| API Key as generated from the &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/admin/api/&#39;&gt;admin panel&lt;/a&gt; | 
 **num** | **string**| A single phone number or &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/help/msisdn/&#39;&gt;MSDISDN&lt;/a&gt; | 
 **cc** | **string**| 2 character country code &lt;a href&#x3D;&#39;https://en.wikipedia.org/wiki/ISO_3166-2&#39;&gt;ISO 3166-2&lt;/a&gt; for formatting local numbers internationally | [optional] 

### Return type

[**HLRCallback**](HLRCallback.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_hlr_callback**
> HLRResult get_hlr_callback(key => $key, num => $num, cb => $cb, cc => $cc)

HLR number lookup with results going to a callback URL

Perform HLR on number with the result being sent to the callback URL provided

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::Configuration;
use WWW::SwaggerClient::DefaultApi;

# Configure API key authorization: api_key
$WWW::SwaggerClient::Configuration::api_key->{'key'} = 'YOUR_API_KEY';
# uncomment below to setup prefix (e.g. Bearer) for API key, if needed
#$WWW::SwaggerClient::Configuration::api_key_prefix->{'key'} = "Bearer";

my $api_instance = WWW::SwaggerClient::DefaultApi->new();
my $key = 'key_example'; # string | API Key as generated from the <a href='https://www.smsfusion.com.au/admin/api/'>admin panel</a>
my $num = []; # ARRAY[string] | Comma separated list of phone numbers or <a href='https://www.smsfusion.com.au/help/msisdn/'>MSDISDN</a>'s
my $cb = 'cb_example'; # string | HTTP or HTTPS callback URL for each result. The result will be sent as POST with a json object included in <b>result</b>. Timeout for callbacks is set to 30 seconds
my $cc = 'cc_example'; # string | 2 character country code <a href='https://en.wikipedia.org/wiki/ISO_3166-2'>ISO 3166-2</a> for formatting local numbers internationally

eval { 
    my $result = $api_instance->get_hlr_callback(key => $key, num => $num, cb => $cb, cc => $cc);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DefaultApi->get_hlr_callback: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**| API Key as generated from the &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/admin/api/&#39;&gt;admin panel&lt;/a&gt; | 
 **num** | [**ARRAY[string]**](string.md)| Comma separated list of phone numbers or &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/help/msisdn/&#39;&gt;MSDISDN&lt;/a&gt;&#39;s | 
 **cb** | **string**| HTTP or HTTPS callback URL for each result. The result will be sent as POST with a json object included in &lt;b&gt;result&lt;/b&gt;. Timeout for callbacks is set to 30 seconds | 
 **cc** | **string**| 2 character country code &lt;a href&#x3D;&#39;https://en.wikipedia.org/wiki/ISO_3166-2&#39;&gt;ISO 3166-2&lt;/a&gt; for formatting local numbers internationally | [optional] 

### Return type

[**HLRResult**](HLRResult.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

