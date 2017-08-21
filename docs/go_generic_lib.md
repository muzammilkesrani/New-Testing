# Getting started

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=WinSMS%20REST-GoLang&projectName=winsmsrest_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=winsmsrest_lib)

## How to Use

The following section explains how to use the WinsmsrestLib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=winsmsrest_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=winsmsrest_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=winsmsrest_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=winsmsrest_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=winsmsrest_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=WinSMS%20REST-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=winsmsrest_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=winsmsrest_lib)

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [sms_pkg](#sms_pkg)
* [credits_pkg](#credits_pkg)

## <a name="sms_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".sms_pkg") sms_pkg

### Get instance

Factory for the ``` SMS ``` interface can be accessed from the package sms_pkg.

```go
sms := sms_pkg.NewSMS()
```

### <a name="get_sms_incoming"></a>![Method: ](https://apidocs.io/img/method.png ".sms_pkg.GetSmsIncoming") GetSmsIncoming

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming


```go
func (me *SMS_IMPL) GetSmsIncoming(authorization string)(*models_pkg.HttpJsonschemaNet,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```go
authorization := "Authorization"

var result *models_pkg.HttpJsonschemaNet
result,_ = sms.GetSmsIncoming(authorization)

```

#### Errors
 
| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="get_sms_scheduled"></a>![Method: ](https://apidocs.io/img/method.png ".sms_pkg.GetSmsScheduled") GetSmsScheduled

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled


```go
func (me *SMS_IMPL) GetSmsScheduled(authorization string)(*models_pkg.HttpJsonschemaNet,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```go
authorization := "Authorization"

var result *models_pkg.HttpJsonschemaNet
result,_ = sms.GetSmsScheduled(authorization)

```

#### Errors
 
| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_send"></a>![Method: ](https://apidocs.io/img/method.png ".sms_pkg.CreateSmsOutgoingSend") CreateSmsOutgoingSend

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend


```go
func (me *SMS_IMPL) CreateSmsOutgoingSend(
            authorization string,
            body *models_pkg.SmsOutgoingSendRequest)(*models_pkg.SmsOutgoingSendResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
var body *models_pkg.SmsOutgoingSendRequest

var result *models_pkg.SmsOutgoingSendResponse
result,_ = sms.CreateSmsOutgoingSend(authorization, body)

```

#### Errors
 
| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_status"></a>![Method: ](https://apidocs.io/img/method.png ".sms_pkg.CreateSmsOutgoingStatus") CreateSmsOutgoingStatus

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus


```go
func (me *SMS_IMPL) CreateSmsOutgoingStatus(
            authorization string,
            body []int64)(*models_pkg.HttpJsonschemaNet,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
"
bodyValue := []byte("[1892,1893,1894]")
var body []int64
json.Unmarshal(bodyValue,&body)

var result *models_pkg.HttpJsonschemaNet
result,_ = sms.CreateSmsOutgoingStatus(authorization, body)

```

#### Errors
 
| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_scheduled_delete"></a>![Method: ](https://apidocs.io/img/method.png ".sms_pkg.CreateSmsScheduledDelete") CreateSmsScheduledDelete

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete


```go
func (me *SMS_IMPL) CreateSmsScheduledDelete(
            authorization string,
            body *models_pkg.HttpJsonschemaNet)(*models_pkg.HttpJsonschemaNet,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
var body *models_pkg.HttpJsonschemaNet

var result *models_pkg.HttpJsonschemaNet
result,_ = sms.CreateSmsScheduledDelete(authorization, body)

```

#### Errors
 
| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)

## <a name="credits_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".credits_pkg") credits_pkg

### Get instance

Factory for the ``` CREDITS ``` interface can be accessed from the package credits_pkg.

```go
credits := credits_pkg.NewCREDITS()
```

### <a name="get_credits_balance"></a>![Method: ](https://apidocs.io/img/method.png ".credits_pkg.GetCreditsBalance") GetCreditsBalance

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance


```go
func (me *CREDITS_IMPL) GetCreditsBalance(authorization string)(*models_pkg.CreditsBalanceResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |


#### Example Usage

```go
authorization := "Set the 'Authorization' http header of the request to the value of the API Key supplied by WinSMS.
"

var result *models_pkg.CreditsBalanceResponse
result,_ = credits.GetCreditsBalance(authorization)

```

#### Errors
 
| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)



