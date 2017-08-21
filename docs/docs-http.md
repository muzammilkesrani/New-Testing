# 



## Base URL

The Base URL for this API is `https://www.winsms.co.za/api/rest/v1`









# <a name="api_reference"></a>API Reference

* [sms](#sms)
* [credits](#credits)

## <a name="sms"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "sms") sms


### <a name="sms_incoming"></a>![Endpoint: ](https://apidocs.io/img/method.png "SmsIncoming") SmsIncoming


**`GET`** `/sms/incoming`

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming




#### Request Headers
>Authorization="Authorization";

#### Responses
**200** 


Body ([http://jsonschema.net/](#http://jsonschema.net/)) 
```
{
  "authResult": true,
  "authError": "",
  "validationResult": true,
  "validationError": "",
  "messages": [
    {
      "serverMessageId": 1892,
      "mobileNumber": "27444444444",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241546,
      "creditCost": 1.4
    },
    {
      "serverMessageId": 1893,
      "mobileNumber": "27555555555",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241556,
      "creditCost": 1.0
    },
    {
      "serverMessageId": 1894,
      "mobileNumber": "27666666666",
      "statusDelivered": false,
      "statusErrorCode": 201,
      "statusTime": 201503241545,
      "creditCost": 0.0
    }
  ]
}
```


**Default** 

> TODO: Add error message

Body ([ResponseError_Error](#response_error_error)) 
```
{
  "errorMessage": "errorMessage"
}
```


### <a name="sms_scheduled"></a>![Endpoint: ](https://apidocs.io/img/method.png "SmsScheduled") SmsScheduled


**`GET`** `/sms/scheduled`

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled




#### Request Headers
>Authorization="Authorization";

#### Responses
**200** 


Body ([http://jsonschema.net/](#http://jsonschema.net/)) 
```
{
  "authResult": true,
  "authError": "",
  "validationResult": true,
  "validationError": "",
  "messages": [
    {
      "serverMessageId": 1892,
      "mobileNumber": "27444444444",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241546,
      "creditCost": 1.4
    },
    {
      "serverMessageId": 1893,
      "mobileNumber": "27555555555",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241556,
      "creditCost": 1.0
    },
    {
      "serverMessageId": 1894,
      "mobileNumber": "27666666666",
      "statusDelivered": false,
      "statusErrorCode": 201,
      "statusTime": 201503241545,
      "creditCost": 0.0
    }
  ]
}
```


**Default** 

> TODO: Add error message

Body ([ResponseError_Error](#response_error_error)) 
```
{
  "errorMessage": "errorMessage"
}
```


### <a name="sms_outgoing_send"></a>![Endpoint: ](https://apidocs.io/img/method.png "SmsOutgoingSend") SmsOutgoingSend


**`POST`** `/sms/outgoing/send`

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Authorization="Authorization";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [Sms Outgoing Send request](#sms_outgoing_send_request) |  ``` Required ```  | TODO: Add description | 

 Example 
``` 
{
  "message": "message",
  "mobileNumbers": [
    {
      "mobileNumber": "mobileNumber",
      "clientMessageId": "clientMessageId"
    }
  ],
  "scheduledTime": 119
}
``` 

#### Responses
**200** 


Body ([Sms Outgoing Send response](#sms_outgoing_send_response)) 
```
{
  "timeStamp": "timeStamp",
  "version": "version",
  "statusCode": "statusCode",
  "authResult": false,
  "authError": "authError",
  "validationResult": false,
  "validationError": "validationError",
  "messages": [
    {
      "clientMessageId": "clientMessageId",
      "mobileNumber": "mobileNumber",
      "accepted": false,
      "acceptError": "acceptError",
      "serverMessageId": 119,
      "scheduledTime": 119,
      "creditCost": 119.602792260518
    }
  ]
}
```


**Default** 

> TODO: Add error message

Body ([ResponseError_Error](#response_error_error)) 
```
{
  "errorMessage": "errorMessage"
}
```


### <a name="sms_outgoing_status"></a>![Endpoint: ](https://apidocs.io/img/method.png "SmsOutgoingStatus") SmsOutgoingStatus


**`POST`** `/sms/outgoing/status`

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Authorization=Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [Number](#api_types) |  ``` Required ```  ``` Collection ```  | TODO: Add description | 

 Example 
``` 
[
  1892,
  1893,
  1894
]
``` 

#### Responses
**200** 


Body ([http://jsonschema.net/](#http://jsonschema.net/)) 
```
{
  "authResult": true,
  "authError": "",
  "validationResult": true,
  "validationError": "",
  "messages": [
    {
      "serverMessageId": 1892,
      "mobileNumber": "27444444444",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241546,
      "creditCost": 1.4
    },
    {
      "serverMessageId": 1893,
      "mobileNumber": "27555555555",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241556,
      "creditCost": 1.0
    },
    {
      "serverMessageId": 1894,
      "mobileNumber": "27666666666",
      "statusDelivered": false,
      "statusErrorCode": 201,
      "statusTime": 201503241545,
      "creditCost": 0.0
    }
  ]
}
```


**Default** 

> TODO: Add error message

Body ([ResponseError_Error](#response_error_error)) 
```
{
  "errorMessage": "errorMessage"
}
```


### <a name="sms_scheduled_delete"></a>![Endpoint: ](https://apidocs.io/img/method.png "SmsScheduledDelete") SmsScheduledDelete


**`POST`** `/sms/scheduled/delete`

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Authorization="Authorization";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [http://jsonschema.net/](#http://jsonschema.net/) |  ``` Required ```  | TODO: Add description | 

 Example 
``` 
{
  "authResult": true,
  "authError": "",
  "validationResult": true,
  "validationError": "",
  "messages": [
    {
      "serverMessageId": 1892,
      "mobileNumber": "27444444444",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241546,
      "creditCost": 1.4
    },
    {
      "serverMessageId": 1893,
      "mobileNumber": "27555555555",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241556,
      "creditCost": 1.0
    },
    {
      "serverMessageId": 1894,
      "mobileNumber": "27666666666",
      "statusDelivered": false,
      "statusErrorCode": 201,
      "statusTime": 201503241545,
      "creditCost": 0.0
    }
  ]
}
``` 

#### Responses
**200** 


Body ([http://jsonschema.net/](#http://jsonschema.net/)) 
```
{
  "authResult": true,
  "authError": "",
  "validationResult": true,
  "validationError": "",
  "messages": [
    {
      "serverMessageId": 1892,
      "mobileNumber": "27444444444",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241546,
      "creditCost": 1.4
    },
    {
      "serverMessageId": 1893,
      "mobileNumber": "27555555555",
      "statusDelivered": true,
      "statusErrorCode": 0,
      "statusTime": 201503241556,
      "creditCost": 1.0
    },
    {
      "serverMessageId": 1894,
      "mobileNumber": "27666666666",
      "statusDelivered": false,
      "statusErrorCode": 201,
      "statusTime": 201503241545,
      "creditCost": 0.0
    }
  ]
}
```


**Default** 

> TODO: Add error message

Body ([ResponseError_Error](#response_error_error)) 
```
{
  "errorMessage": "errorMessage"
}
```


[Back to API Reference](#api_reference)

## <a name="credits"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "credits") credits


### <a name="credits_balance"></a>![Endpoint: ](https://apidocs.io/img/method.png "CreditsBalance") CreditsBalance


**`GET`** `/credits/balance`

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance




#### Request Headers
>Authorization=Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
;

#### Responses
**200** 


Body ([Credits Balance response](#credits_balance_response)) 
```
{
  "timeStamp": "20170117054658978",
  "version": "1.0",
  "statusCode": 200,
  "authResult": true,
  "authError": "",
  "validationResult": true,
  "validationError": "",
  "creditBalance": 96.4
}
```


**400** 

> TODO: Add error message

Body ([ResponseError2_Error](#response_error2_error)) 
```
{
  "timeStamp": "timeStamp",
  "version": "version",
  "statusCode": 119,
  "errorMessage": "errorMessage"
}
```
**401** 

> TODO: Add error message

Body ([ResponseError3_Error](#response_error3_error)) 
```
{
  "timeStamp": "timeStamp",
  "version": "version",
  "statusCode": 77,
  "authResult": false,
  "authError": "authError"
}
```
**Default** 

> TODO: Add error message

Body ([ResponseError_Error](#response_error_error)) 
```
{
  "errorMessage": "errorMessage"
}
```


[Back to API Reference](#api_reference)

## <a name="api_types"></a>![Models: ](https://apidocs.io/img/class.png "API Types") API Types

This section provides details on the available types. The primitive types available are:

| Type | Example |
| ---- | -------- |
| **string** | `hello world` |
| **boolean** |	`true` |
| **number** | `1` |
| **precision** | `1.5` |
| **datetime** | `2016-03-13T12:52:32.123Z` |
| **date** | `2016-03-13` |
|**void** | |
| **dynamic** | |
| **binary** | |
| **long** | `12345678910` |
| **file** | |
| **uuid** | `0f8fad5b-d9cb-469f-a165-70867728950e` |


In addition to the above types, the following complex types are also available:
### <a name="credits_balance_response"></a>![Model: ](https://apidocs.io/img/method.png "Credits Balance response") Credits Balance response



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| timeStamp | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| version | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| statusCode | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| validationResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| validationError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| creditBalance | [precision](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="sms_outgoing_send_request"></a>![Model: ](https://apidocs.io/img/method.png "Sms Outgoing Send request") Sms Outgoing Send request



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| message | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| mobileNumbers | [MobileNumber](#mobile_number) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| scheduledTime | [number](#api_types) |  ``` Optional ```  | TODO: Add a property description | 




### <a name="mobile_number"></a>![Model: ](https://apidocs.io/img/method.png "MobileNumber") MobileNumber



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| mobileNumber | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| clientMessageId | [string](#api_types) |  ``` Optional ```  | TODO: Add a property description | 




### <a name="sms_outgoing_send_response"></a>![Model: ](https://apidocs.io/img/method.png "Sms Outgoing Send response") Sms Outgoing Send response



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| timeStamp | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| version | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| statusCode | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| validationResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| validationError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| messages | [Message](#message) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 




### <a name="message"></a>![Model: ](https://apidocs.io/img/method.png "Message") Message



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| clientMessageId | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| mobileNumber | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| accepted | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| acceptError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| serverMessageId | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| scheduledTime | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| creditCost | [precision](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="http://jsonschema.net/"></a>![Model: ](https://apidocs.io/img/method.png "http://jsonschema.net/") http://jsonschema.net/



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| authResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| validationResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| validationError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| messages | [http://jsonschema.net/messages/0](#http://jsonschema.net/messages/0) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 




### <a name="http://jsonschema.net/messages/0"></a>![Model: ](https://apidocs.io/img/method.png "http://jsonschema.net/messages/0") http://jsonschema.net/messages/0



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| serverMessageId | [number](#api_types) |  ``` Optional ```  | TODO: Add a property description | 
| mobileNumber | [string](#api_types) |  ``` Optional ```  | TODO: Add a property description | 
| statusDelivered | [boolean](#api_types) |  ``` Optional ```  | TODO: Add a property description | 
| statusErrorCode | [number](#api_types) |  ``` Optional ```  | TODO: Add a property description | 
| statusTime | [number](#api_types) |  ``` Optional ```  | TODO: Add a property description | 
| creditCost | [precision](#api_types) |  ``` Optional ```  | TODO: Add a property description | 




### <a name="response_error2_error"></a>![Model: ](https://apidocs.io/img/method.png "ResponseError2_Error") ResponseError2_Error



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| timeStamp | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| version | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| statusCode | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| errorMessage | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="response_error3_error"></a>![Model: ](https://apidocs.io/img/method.png "ResponseError3_Error") ResponseError3_Error



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| timeStamp | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| version | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| statusCode | [number](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authResult | [boolean](#api_types) |  ``` Required ```  | TODO: Add a property description | 
| authError | [string](#api_types) |  ``` Required ```  | TODO: Add a property description | 




### <a name="response_error_error"></a>![Model: ](https://apidocs.io/img/method.png "ResponseError_Error") ResponseError_Error



> TODO: Add a method description




| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| errorMessage | [string](#api_types) |  ``` Required ```  | TODO: Add a property description |

