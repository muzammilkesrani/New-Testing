# Getting started

## How to Build

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=WinSMS%20REST-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the WinSMSREST library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=WinSMS%20REST-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=WinSMS%20REST-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=WinSMS%20REST-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=WinSMS%20REST-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=WinSMS%20REST-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=WinSMS%20REST-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=WinSMS%20REST-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=WinSMS%20REST-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=WinSMS%20REST-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=WinSMS%20REST-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=WinSMS%20REST-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=WinSMS%20REST-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### 

API client can be initialized as following.

```php

$client = new WinSMSRESTLib\WinSMSRESTClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SmsController](#sms_controller)
* [CreditsController](#credits_controller)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SmsController") SmsController

### Get singleton instance

The singleton instance of the ``` SmsController ``` class can be accessed from the API Client.

```php
$sms = $client->getSms();
```

### <a name="get_sms_incoming"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.getSmsIncoming") getSmsIncoming

> *Tags:*  ``` Skips Authentication ``` 

> SmsIncoming


```php
function getSmsIncoming($authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```php
$authorization = 'Authorization';

$result = $sms->getSmsIncoming($authorization);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="get_sms_scheduled"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.getSmsScheduled") getSmsScheduled

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduled


```php
function getSmsScheduled($authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```php
$authorization = 'Authorization';

$result = $sms->getSmsScheduled($authorization);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_send"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsOutgoingSend") createSmsOutgoingSend

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingSend


```php
function createSmsOutgoingSend(
        $authorization,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$body = new SmsOutgoingSendRequest();

$result = $sms->createSmsOutgoingSend($authorization, $body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_outgoing_status"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsOutgoingStatus") createSmsOutgoingStatus

> *Tags:*  ``` Skips Authentication ``` 

> SmsOutgoingStatus


```php
function createSmsOutgoingStatus(
        $authorization,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Set the \'Authorization\' http header of the request to the value of the API Key supplied by WinSMS.
';
$bodyValue = "[1892,1893,1894]";
$body = APIHelper::deserialize($bodyValue);

$result = $sms->createSmsOutgoingStatus($authorization, $body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



### <a name="create_sms_scheduled_delete"></a>![Method: ](https://apidocs.io/img/method.png ".SmsController.createSmsScheduledDelete") createSmsScheduledDelete

> *Tags:*  ``` Skips Authentication ``` 

> SmsScheduledDelete


```php
function createSmsScheduledDelete(
        $authorization,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$body = new HttpJsonschemaNet();

$result = $sms->createSmsScheduledDelete($authorization, $body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)

## <a name="credits_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CreditsController") CreditsController

### Get singleton instance

The singleton instance of the ``` CreditsController ``` class can be accessed from the API Client.

```php
$credits = $client->getCredits();
```

### <a name="get_credits_balance"></a>![Method: ](https://apidocs.io/img/method.png ".CreditsController.getCreditsBalance") getCreditsBalance

> *Tags:*  ``` Skips Authentication ``` 

> CreditsBalance


```php
function getCreditsBalance($authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | Valid API Key supplied by WinSMS |



#### Example Usage

```php
$authorization = 'Set the \'Authorization\' http header of the request to the value of the API Key supplied by WinSMS.
';

$result = $credits->getCreditsBalance($authorization);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 400 | TODO: Add error message |
| 401 | TODO: Add error message |
| 0 | TODO: Add error message |



[Back to List of Controllers](#list_of_controllers)



