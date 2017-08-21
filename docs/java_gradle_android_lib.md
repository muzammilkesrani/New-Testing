# Getting started

## How to Build

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

* Browse to locate the folder containing the source code. Select the location of the WinSMSREST gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

## How to Use

The following section explains how to use the WinSMSREST library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Following this, select the ``` Phone and Tablet ```` option as shown in the illustration below and click ``` Next ```. 

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':WinSMSREST')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=WinSMS%20REST&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > WinSMSRESTLib > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### 

API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java

za.co.winsms.www.Configuration.initialize(appContext);
WinSMSRESTClient client = new WinSMSRESTClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SmsController](#sms_controller)
* [CreditsController](#credits_controller)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png "za.co.winsms.www.controllers.SmsController") SmsController

### Get singleton instance

The singleton instance of the ``` SmsController ``` class can be accessed from the API Client.

```java
SmsController sms = client.getSms();
```

### <a name="get_sms_incoming_async"></a>![Method: ](https://apidocs.io/img/method.png "za.co.winsms.www.controllers.SmsController.getSmsIncomingAsync") getSmsIncomingAsync

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming


```java
void getSmsIncomingAsync(
        final String authorization,
        final APICallBack<HttpJsonschemaNet> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```java
String authorization = "Authorization";
// Invoking the API call with sample inputs
sms.getSmsIncomingAsync(authorization, new APICallBack<HttpJsonschemaNet>() {
    public void onSuccess(HttpContext context, HttpJsonschemaNet response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="get_sms_scheduled_async"></a>![Method: ](https://apidocs.io/img/method.png "za.co.winsms.www.controllers.SmsController.getSmsScheduledAsync") getSmsScheduledAsync

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled


```java
void getSmsScheduledAsync(
        final String authorization,
        final APICallBack<HttpJsonschemaNet> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```java
String authorization = "Authorization";
// Invoking the API call with sample inputs
sms.getSmsScheduledAsync(authorization, new APICallBack<HttpJsonschemaNet>() {
    public void onSuccess(HttpContext context, HttpJsonschemaNet response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_send_async"></a>![Method: ](https://apidocs.io/img/method.png "za.co.winsms.www.controllers.SmsController.createSmsOutgoingSendAsync") createSmsOutgoingSendAsync

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend


```java
void createSmsOutgoingSendAsync(
        final String authorization,
        final SmsOutgoingSendRequest body,
        final APICallBack<SmsOutgoingSendResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String authorization = "Authorization";
    SmsOutgoingSendRequest body = new SmsOutgoingSendRequest();
    // Invoking the API call with sample inputs
    sms.createSmsOutgoingSendAsync(authorization, body, new APICallBack<SmsOutgoingSendResponse>() {
        public void onSuccess(HttpContext context, SmsOutgoingSendResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_status_async"></a>![Method: ](https://apidocs.io/img/method.png "za.co.winsms.www.controllers.SmsController.createSmsOutgoingStatusAsync") createSmsOutgoingStatusAsync

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus


```java
void createSmsOutgoingStatusAsync(
        final String authorization,
        final List<Integer> body,
        final APICallBack<HttpJsonschemaNet> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String authorization = "Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
";
    String bodyValue = "[1892,1893,1894]";
    List<Integer> body = mapper.readValue(bodyValue,new TypeReference<List<Integer>> (){});
    // Invoking the API call with sample inputs
    sms.createSmsOutgoingStatusAsync(authorization, body, new APICallBack<HttpJsonschemaNet>() {
        public void onSuccess(HttpContext context, HttpJsonschemaNet response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_scheduled_delete_async"></a>![Method: ](https://apidocs.io/img/method.png "za.co.winsms.www.controllers.SmsController.createSmsScheduledDeleteAsync") createSmsScheduledDeleteAsync

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete


```java
void createSmsScheduledDeleteAsync(
        final String authorization,
        final HttpJsonschemaNet body,
        final APICallBack<HttpJsonschemaNet> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String authorization = "Authorization";
    HttpJsonschemaNet body = new HttpJsonschemaNet();
    // Invoking the API call with sample inputs
    sms.createSmsScheduledDeleteAsync(authorization, body, new APICallBack<HttpJsonschemaNet>() {
        public void onSuccess(HttpContext context, HttpJsonschemaNet response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)

## <a name="credits_controller"></a>![Class: ](https://apidocs.io/img/class.png "za.co.winsms.www.controllers.CreditsController") CreditsController

### Get singleton instance

The singleton instance of the ``` CreditsController ``` class can be accessed from the API Client.

```java
CreditsController credits = client.getCredits();
```

### <a name="get_credits_balance_async"></a>![Method: ](https://apidocs.io/img/method.png "za.co.winsms.www.controllers.CreditsController.getCreditsBalanceAsync") getCreditsBalanceAsync

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance


```java
void getCreditsBalanceAsync(
        final String authorization,
        final APICallBack<CreditsBalanceResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```java
String authorization = "Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
";
// Invoking the API call with sample inputs
credits.getCreditsBalanceAsync(authorization, new APICallBack<CreditsBalanceResponse>() {
    public void onSuccess(HttpContext context, CreditsBalanceResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)



