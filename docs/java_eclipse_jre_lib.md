# Getting started

## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?step=import0&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?step=import1&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?step=import2&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?step=import3&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

## How to Use

The following section explains how to use the WinSMSREST library in a new console project.

### 1. Starting a new project

For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location ```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *WinSMSRESTLib* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?step=testProject0&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

Clicking the ``` Add ``` button will open a dialog where you need to specify WinSMSREST in ``` Group Id ``` and WinSMSRESTLib in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject1&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

### 3. Write sample code

Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject2&workspaceFolder=WinSMS%20REST-Java&workspaceName=WinSMSREST&projectName=WinSMSRESTLib&rootNamespace=za.co.winsms.www)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *WinSMSRESTLib* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

### 

API client can be initialized as following.

```java

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



