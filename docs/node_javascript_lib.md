# Getting started

## How to Build

The generated SDK relies on [Node Package Manager](https://www.npmjs.com/) (NPM) being available to resolve dependencies. If you don't already have NPM installed, please go ahead and follow instructions to install NPM from [here](https://nodejs.org/en/download/).
The SDK also requires Node to be installed. If Node isn't already installed, please install it from [here](https://nodejs.org/en/download/)
> NPM is installed by default when Node is installed

To check if node and npm have been successfully installed, write the following commands in command prompt:

* `node --version`
* `npm -version`

![Version Check](https://apidocs.io/illustration/nodejs?step=versionCheck&workspaceFolder=WinSMS%20REST-Node)

Now use npm to resolve all dependencies by running the following command in the root directory (of the SDK folder):

```bash
npm install
```

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency1&workspaceFolder=WinSMS%20REST-Node)

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency2)

This will install all dependencies in the `node_modules` folder.

Once dependencies are resolved, you will need to move the folder `WinSMSRESTLib ` in to your `node_modules` folder.

## How to Use

The following section explains how to use the library in a new project.

### 1. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

Click on `File` and select `Open Folder`.

![Open Folder](https://apidocs.io/illustration/nodejs?step=openFolder)

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![Open Project](https://apidocs.io/illustration/nodejs?step=openProject&workspaceFolder=WinSMS%20REST-Node)

### 2. Creating a Test File

Now right click on the folder name and select the `New File` option to create a new test file. Save it as `index.js` Now import the generated NodeJS library using the following lines of code:

```js
var lib = require('lib');
```

Save changes.

![Create new file](https://apidocs.io/illustration/nodejs?step=createNewFile&workspaceFolder=WinSMS%20REST-Node)

![Save new file](https://apidocs.io/illustration/nodejs?step=saveNewFile&workspaceFolder=WinSMS%20REST-Node)

### 3. Running The Test File

To run the `index.js` file, open up the command prompt and navigate to the Path where the SDK folder resides. Type the following command to run the file:

```
node index.js
```

![Run file](https://apidocs.io/illustration/nodejs?step=runProject&workspaceFolder=WinSMS%20REST-Node)


## How to Test

These tests use Mocha framework for testing, coupled with Chai for assertions. These dependencies need to be installed for tests to run.
Tests can be run in a number of ways:

### Method 1 (Run all tests)

1. Navigate to the root directory of the SDK folder from command prompt.
2. Type `mocha --recursive` to run all the tests.

### Method 2 (Run all tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha *` to run all the tests.

### Method 3 (Run specific controller's tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha  WinSMS RESTController`  to run all the tests in that controller file.

> To increase mocha's default timeout, you can change the `TEST_TIMEOUT` parameter's value in `TestBootstrap.js`.

![Run Tests](https://apidocs.io/illustration/nodejs?step=runTests&controllerName=WinSMS%20RESTController)

## Initialization

### 

API client can be initialized as following:

```JavaScript
const lib = require('lib');


```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SmsController](#sms_controller)
* [CreditsController](#credits_controller)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SmsController") SmsController

### Get singleton instance

The singleton instance of the ``` SmsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.SmsController;
```

### <a name="get_sms_incoming"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.getSmsIncoming") getSmsIncoming

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming


```javascript
function getSmsIncoming(authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```javascript

    var authorization = 'Authorization';

    controller.getSmsIncoming(authorization, function(error, response, context) {

    
    });
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="get_sms_scheduled"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.getSmsScheduled") getSmsScheduled

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled


```javascript
function getSmsScheduled(authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```javascript

    var authorization = 'Authorization';

    controller.getSmsScheduled(authorization, function(error, response, context) {

    
    });
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="create_sms_outgoing_send"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsOutgoingSend") createSmsOutgoingSend

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend


```javascript
function createSmsOutgoingSend(authorization, body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var body = new SmsOutgoingSendRequest({"key":"value"});

    controller.createSmsOutgoingSend(authorization, body, function(error, response, context) {

    
    });
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="create_sms_outgoing_status"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsOutgoingStatus") createSmsOutgoingStatus

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus


```javascript
function createSmsOutgoingStatus(authorization, body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Set the \'Authorization\' http header of the request to the value of the API Key supplied by WinSMS.\n';
    var body = [1892,1893,1894];

    controller.createSmsOutgoingStatus(authorization, body, function(error, response, context) {

    
    });
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




### <a name="create_sms_scheduled_delete"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsScheduledDelete") createSmsScheduledDelete

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete


```javascript
function createSmsScheduledDelete(authorization, body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var body = new HttpJsonschemaNet({"key":"value"});

    controller.createSmsScheduledDelete(authorization, body, function(error, response, context) {

    
    });
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |




[Back to List of Controllers](#list_of_controllers)

## <a name="credits_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CreditsController") CreditsController

### Get singleton instance

The singleton instance of the ``` CreditsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CreditsController;
```

### <a name="get_credits_balance"></a>![Method: ](https://apidocs.io/img/method.png ".CreditsController.getCreditsBalance") getCreditsBalance

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance


```javascript
function getCreditsBalance(authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```javascript

    var authorization = 'Set the \'Authorization\' http header of the request to the value of the API Key supplied by WinSMS.\n';

    controller.getCreditsBalance(authorization, function(error, response, context) {

    
    });
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |




[Back to List of Controllers](#list_of_controllers)



