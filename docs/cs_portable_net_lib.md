# Getting started

## How to Build

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

1. Open the solution (WinSMSREST.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the WinSMSREST library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

### 3. Add reference of the library project

In order to use the WinSMSREST library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` WinSMSREST.Tests ``` and click ``` OK ```. By doing this, we have added a reference of the ```WinSMSREST.Tests``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=WinSMS%20REST-CSharp&workspaceName=WinSMSREST&projectName=WinSMSREST.Tests)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### 

API client can be initialized as following.

```csharp

WinSMSRESTClient client = new WinSMSRESTClient();
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SmsController](#sms_controller)
* [CreditsController](#credits_controller)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png "WinSMSREST.Tests.Controllers.SmsController") SmsController

### Get singleton instance

The singleton instance of the ``` SmsController ``` class can be accessed from the API Client.

```csharp
SmsController sms = client.Sms;
```

### <a name="get_sms_incoming"></a>![Method: ](https://apidocs.io/img/method.png "WinSMSREST.Tests.Controllers.SmsController.GetSmsIncoming") GetSmsIncoming

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming


```csharp
Task<PCL.Models.HttpJsonschemaNet> GetSmsIncoming(string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```csharp
string authorization = "Authorization";

PCL.Models.HttpJsonschemaNet result = await sms.GetSmsIncoming(authorization);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |


### <a name="get_sms_scheduled"></a>![Method: ](https://apidocs.io/img/method.png "WinSMSREST.Tests.Controllers.SmsController.GetSmsScheduled") GetSmsScheduled

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled


```csharp
Task<PCL.Models.HttpJsonschemaNet> GetSmsScheduled(string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```csharp
string authorization = "Authorization";

PCL.Models.HttpJsonschemaNet result = await sms.GetSmsScheduled(authorization);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |


### <a name="create_sms_outgoing_send"></a>![Method: ](https://apidocs.io/img/method.png "WinSMSREST.Tests.Controllers.SmsController.CreateSmsOutgoingSend") CreateSmsOutgoingSend

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend


```csharp
Task<PCL.Models.SmsOutgoingSendResponse> CreateSmsOutgoingSend(string authorization, PCL.Models.SmsOutgoingSendRequest body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
var body = new PCL.Models.SmsOutgoingSendRequest();

PCL.Models.SmsOutgoingSendResponse result = await sms.CreateSmsOutgoingSend(authorization, body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |


### <a name="create_sms_outgoing_status"></a>![Method: ](https://apidocs.io/img/method.png "WinSMSREST.Tests.Controllers.SmsController.CreateSmsOutgoingStatus") CreateSmsOutgoingStatus

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus


```csharp
Task<PCL.Models.HttpJsonschemaNet> CreateSmsOutgoingStatus(string authorization, List<int> body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
";
string bodyValue = "[1892,1893,1894]";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<List<int>>(bodyValue);

PCL.Models.HttpJsonschemaNet result = await sms.CreateSmsOutgoingStatus(authorization, body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |


### <a name="create_sms_scheduled_delete"></a>![Method: ](https://apidocs.io/img/method.png "WinSMSREST.Tests.Controllers.SmsController.CreateSmsScheduledDelete") CreateSmsScheduledDelete

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete


```csharp
Task<PCL.Models.HttpJsonschemaNet> CreateSmsScheduledDelete(string authorization, PCL.Models.HttpJsonschemaNet body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
var body = new PCL.Models.HttpJsonschemaNet();

PCL.Models.HttpJsonschemaNet result = await sms.CreateSmsScheduledDelete(authorization, body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |


[Back to List of Controllers](#list_of_controllers)

## <a name="credits_controller"></a>![Class: ](https://apidocs.io/img/class.png "WinSMSREST.Tests.Controllers.CreditsController") CreditsController

### Get singleton instance

The singleton instance of the ``` CreditsController ``` class can be accessed from the API Client.

```csharp
CreditsController credits = client.Credits;
```

### <a name="get_credits_balance"></a>![Method: ](https://apidocs.io/img/method.png "WinSMSREST.Tests.Controllers.CreditsController.GetCreditsBalance") GetCreditsBalance

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance


```csharp
Task<PCL.Models.CreditsBalanceResponse> GetCreditsBalance(string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```csharp
string authorization = "Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
";

PCL.Models.CreditsBalanceResponse result = await credits.GetCreditsBalance(authorization);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |


[Back to List of Controllers](#list_of_controllers)



