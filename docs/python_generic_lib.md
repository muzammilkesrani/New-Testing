# Getting started

## How to Build


You must have Python 2 >=2.7.9 or Python 3 >=3.4 installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=WinSMS%20REST-Python)


## How to Use

The following section explains how to use the Winsmsrest SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=WinSMS%20REST-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=WinSMS%20REST-Python&projectName=winsmsrest)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=WinSMS%20REST-Python&projectName=winsmsrest)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=WinSMS%20REST-Python&projectName=winsmsrest)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from winsmsrest.winsmsrest_client import WinsmsrestClient
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=WinSMS%20REST-Python&libraryName=winsmsrest.winsmsrest_client&projectName=winsmsrest)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=WinSMS%20REST-Python&libraryName=winsmsrest.winsmsrest_client&projectName=winsmsrest)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke 'pip install -r test-requirements.txt'
  3. Invoke 'nosetests'

## Initialization

### 

API client can be initialized as following.

```python

client = WinsmsrestClient()
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SmsController](#sms_controller)
* [CreditsController](#credits_controller)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SmsController") SmsController

### Get controller instance

An instance of the ``` SmsController ``` class can be accessed from the API Client.

```python
 sms_client = client.sms
```

### <a name="get_sms_incoming"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.get_sms_incoming") get_sms_incoming

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming

```python
def get_sms_incoming(self,
                         authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```python
authorization = 'Authorization'

result = sms_client.get_sms_incoming(authorization)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="get_sms_scheduled"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.get_sms_scheduled") get_sms_scheduled

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled

```python
def get_sms_scheduled(self,
                          authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```python
authorization = 'Authorization'

result = sms_client.get_sms_scheduled(authorization)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="create_sms_outgoing_send"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.create_sms_outgoing_send") create_sms_outgoing_send

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend

```python
def create_sms_outgoing_send(self,
                                 authorization,
                                 body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
body = SmsOutgoingSendRequest()

result = sms_client.create_sms_outgoing_send(authorization, body)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="create_sms_outgoing_status"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.create_sms_outgoing_status") create_sms_outgoing_status

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus

```python
def create_sms_outgoing_status(self,
                                   authorization,
                                   body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Set the \'Authorization\' http header of the request to the value of the API Key supplied by WinSMS.
'
body_value = "[1892,1893,1894]"
body = json.loads(body_value)

result = sms_client.create_sms_outgoing_status(authorization, body)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="create_sms_scheduled_delete"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.create_sms_scheduled_delete") create_sms_scheduled_delete

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete

```python
def create_sms_scheduled_delete(self,
                                    authorization,
                                    body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
body = HttpJsonschemaNet()

result = sms_client.create_sms_scheduled_delete(authorization, body)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




[Back to List of Controllers](#list_of_controllers)

## <a name="credits_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CreditsController") CreditsController

### Get controller instance

An instance of the ``` CreditsController ``` class can be accessed from the API Client.

```python
 credits_client = client.credits
```

### <a name="get_credits_balance"></a>![Method: ](https://apidocs.io/img/method.png ".CreditsController.get_credits_balance") get_credits_balance

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance

```python
def get_credits_balance(self,
                            authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```python
authorization = 'Set the \'Authorization\' http header of the request to the value of the API Key supplied by WinSMS.
'

result = credits_client.get_credits_balance(authorization)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |




[Back to List of Controllers](#list_of_controllers)



