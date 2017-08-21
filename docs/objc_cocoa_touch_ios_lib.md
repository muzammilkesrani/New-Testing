# Getting started

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

Open the project workspace using the (WinSMSREST.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the WinSMSREST library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'WinSMSREST', :path => 'Vendor/WinSMSREST'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the WinSMSREST.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=WinSMS%20REST-ObjC&workspaceName=WinSMSREST&projectName=WinSMSREST&rootNamespace=WinSMSREST)


## Initialization

### 

Configuration variables can be set as following.
```Objc

```

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SmsController](#sms_controller)
* [CreditsController](#credits_controller)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SmsController") SmsController

### Get singleton instance
```objc
Sms* sms = [[Sms alloc]init] ;
```

### <a name="get_sms_incoming_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.getSmsIncomingAsyncWithAuthorization") getSmsIncomingAsyncWithAuthorization

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming


```objc
function getSmsIncomingAsyncWithAuthorization:(NSString*) authorization
                completionBlock:(CompletedGetSmsIncoming) onCompleted(authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";

    [self.sms getSmsIncomingAsyncWithAuthorization: authorization  completionBlock:^(BOOL success, HttpContext* context, HttpJsonschemaNet* response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="get_sms_scheduled_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.getSmsScheduledAsyncWithAuthorization") getSmsScheduledAsyncWithAuthorization

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled


```objc
function getSmsScheduledAsyncWithAuthorization:(NSString*) authorization
                completionBlock:(CompletedGetSmsScheduled) onCompleted(authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";

    [self.sms getSmsScheduledAsyncWithAuthorization: authorization  completionBlock:^(BOOL success, HttpContext* context, HttpJsonschemaNet* response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_send_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsOutgoingSendAsyncWithAuthorization") createSmsOutgoingSendAsyncWithAuthorization

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend


```objc
function createSmsOutgoingSendAsyncWithAuthorization:(NSString*) authorization
                body:(SmsOutgoingSendRequest*) body
                completionBlock:(CompletedPostSmsOutgoingSend) onCompleted(authorization body : body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    SmsOutgoingSendRequest* body = [[SmsOutgoingSendRequest alloc]init];

    [self.sms createSmsOutgoingSendAsyncWithAuthorization: authorization body : body  completionBlock:^(BOOL success, HttpContext* context, SmsOutgoingSendResponse* response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_status_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsOutgoingStatusAsyncWithAuthorization") createSmsOutgoingStatusAsyncWithAuthorization

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus


```objc
function createSmsOutgoingStatusAsyncWithAuthorization:(NSString*) authorization
                body:(NSArray*) body
                completionBlock:(CompletedPostSmsOutgoingStatus) onCompleted(authorization body : body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
";
    NSArray* body = (NSArray*) [APIHelper jsonDeserializeArray: @"[1892,1893,1894]"];

    [self.sms createSmsOutgoingStatusAsyncWithAuthorization: authorization body : body  completionBlock:^(BOOL success, HttpContext* context, HttpJsonschemaNet* response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_scheduled_delete_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsScheduledDeleteAsyncWithAuthorization") createSmsScheduledDeleteAsyncWithAuthorization

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete


```objc
function createSmsScheduledDeleteAsyncWithAuthorization:(NSString*) authorization
                body:(HttpJsonschemaNet*) body
                completionBlock:(CompletedPostSmsScheduledDelete) onCompleted(authorization body : body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    HttpJsonschemaNet* body = [[HttpJsonschemaNet alloc]init];

    [self.sms createSmsScheduledDeleteAsyncWithAuthorization: authorization body : body  completionBlock:^(BOOL success, HttpContext* context, HttpJsonschemaNet* response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)

## <a name="credits_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CreditsController") CreditsController

### Get singleton instance
```objc
Credits* credits = [[Credits alloc]init] ;
```

### <a name="get_credits_balance_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".CreditsController.getCreditsBalanceAsyncWithAuthorization") getCreditsBalanceAsyncWithAuthorization

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance


```objc
function getCreditsBalanceAsyncWithAuthorization:(NSString*) authorization
                completionBlock:(CompletedGetCreditsBalance) onCompleted(authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
";

    [self.credits getCreditsBalanceAsyncWithAuthorization: authorization  completionBlock:^(BOOL success, HttpContext* context, CreditsBalanceResponse* response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)



