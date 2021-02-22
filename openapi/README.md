# Go API client for openapi

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)

## Overview
This API client was generated by the [OpenAPI Generator](https://openapi-generator.tech) project.  By using the [OpenAPI-spec](https://www.openapis.org/) from a remote server, you can easily generate an API client.

- API version: 536
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.GoClientCodegen

## Installation

Install the following dependencies:

```shell
go get github.com/stretchr/testify/assert
go get golang.org/x/oauth2
go get golang.org/x/net/context
```

Put the package under your project folder and add the following in import:

```golang
import sw "./openapi"
```

To use a proxy, set the environment variable `HTTP_PROXY`:

```golang
os.Setenv("HTTP_PROXY", "http://proxy_name:proxy_port")
```

## Configuration of Server URL

Default configuration comes with `Servers` field that contains server objects as defined in the OpenAPI specification.

### Select Server Configuration

For using other server than the one defined on index 0 set context value `sw.ContextServerIndex` of type `int`.

```golang
ctx := context.WithValue(context.Background(), sw.ContextServerIndex, 1)
```

### Templated Server URL

Templated server URL is formatted using default variables from configuration or from context value `sw.ContextServerVariables` of type `map[string]string`.

```golang
ctx := context.WithValue(context.Background(), sw.ContextServerVariables, map[string]string{
	"basePath": "v2",
})
```

Note, enum values are always validated and all unused variables are silently ignored.

### URLs Configuration per Operation

Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identifield by `"{classname}Service.{nickname}"` string.
Similar rules for overriding default operation server index and variables applies by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```
ctx := context.WithValue(context.Background(), sw.ContextOperationServerIndices, map[string]int{
	"{classname}Service.{nickname}": 2,
})
ctx = context.WithValue(context.Background(), sw.ContextOperationServerVariables, map[string]map[string]string{
	"{classname}Service.{nickname}": {
		"port": "8443",
	},
})
```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**GetAccount**](docs/DefaultApi.md#getaccount) | **Get** /{apiVersion}/reg/{sourceDeviceId}/account | GetAccount
*DefaultApi* | [**GetBoundDevices**](docs/DefaultApi.md#getbounddevices) | **Get** /{apiVersion}/reg/{sourceDeviceId}/account/devices | GetBoundDevices
*DefaultApi* | [**GetClientConfig**](docs/DefaultApi.md#getclientconfig) | **Get** /{apiVersion}/client_config | GetClientConfig
*DefaultApi* | [**GetSourceDevice**](docs/DefaultApi.md#getsourcedevice) | **Get** /{apiVersion}/reg/{sourceDeviceId} | GetSourceDevice
*DefaultApi* | [**Register**](docs/DefaultApi.md#register) | **Post** /{apiVersion}/reg | Register
*DefaultApi* | [**ResetAccountLicense**](docs/DefaultApi.md#resetaccountlicense) | **Post** /{apiVersion}/reg/{sourceDeviceId}/account/license | ResetAccountLicense
*DefaultApi* | [**UpdateAccount**](docs/DefaultApi.md#updateaccount) | **Put** /{apiVersion}/reg/{sourceDeviceId}/account | UpdateAccount
*DefaultApi* | [**UpdateBoundDevice**](docs/DefaultApi.md#updatebounddevice) | **Patch** /{apiVersion}/reg/{sourceDeviceId}/account/reg/{boundDeviceId} | UpdateBoundDevice
*DefaultApi* | [**UpdateSourceDevice**](docs/DefaultApi.md#updatesourcedevice) | **Patch** /{apiVersion}/reg/{sourceDeviceId} | UpdateSourceDevice


## Documentation For Models

 - [GetAccount200Response](docs/GetAccount200Response.md)
 - [GetBoundDevices200Response](docs/GetBoundDevices200Response.md)
 - [GetClientConfig200Response](docs/GetClientConfig200Response.md)
 - [GetClientConfig200ResponseCaptivePortal](docs/GetClientConfig200ResponseCaptivePortal.md)
 - [GetClientConfig200ResponseDenylist](docs/GetClientConfig200ResponseDenylist.md)
 - [GetClientConfig200ResponseNetworks](docs/GetClientConfig200ResponseNetworks.md)
 - [GetClientConfig200ResponseNetworks1](docs/GetClientConfig200ResponseNetworks1.md)
 - [GetClientConfig200ResponseNetworks1V4](docs/GetClientConfig200ResponseNetworks1V4.md)
 - [GetClientConfig200ResponseNetworks1V6](docs/GetClientConfig200ResponseNetworks1V6.md)
 - [GetSourceDevice200Response](docs/GetSourceDevice200Response.md)
 - [GetSourceDevice200ResponseAccount](docs/GetSourceDevice200ResponseAccount.md)
 - [GetSourceDevice200ResponseConfig](docs/GetSourceDevice200ResponseConfig.md)
 - [GetSourceDevice200ResponseConfigEndpoint](docs/GetSourceDevice200ResponseConfigEndpoint.md)
 - [GetSourceDevice200ResponseConfigInterface](docs/GetSourceDevice200ResponseConfigInterface.md)
 - [GetSourceDevice200ResponseConfigInterfaceAddresses](docs/GetSourceDevice200ResponseConfigInterfaceAddresses.md)
 - [GetSourceDevice200ResponseConfigPeers](docs/GetSourceDevice200ResponseConfigPeers.md)
 - [GetSourceDevice200ResponseConfigServices](docs/GetSourceDevice200ResponseConfigServices.md)
 - [Register200Response](docs/Register200Response.md)
 - [RegisterRequest](docs/RegisterRequest.md)
 - [ResetAccountLicense200Response](docs/ResetAccountLicense200Response.md)
 - [UpdateAccount200Response](docs/UpdateAccount200Response.md)
 - [UpdateAccountRequest](docs/UpdateAccountRequest.md)
 - [UpdateBoundDevice200Response](docs/UpdateBoundDevice200Response.md)
 - [UpdateBoundDeviceRequest](docs/UpdateBoundDeviceRequest.md)
 - [UpdateSourceDevice200Response](docs/UpdateSourceDevice200Response.md)
 - [UpdateSourceDevice200ResponseAccount](docs/UpdateSourceDevice200ResponseAccount.md)
 - [UpdateSourceDeviceRequest](docs/UpdateSourceDeviceRequest.md)


## Documentation For Authorization

 Endpoints do not require authorization.


## Documentation for Utility Methods

Due to the fact that model structure members are all pointers, this package contains
a number of utility functions to easily obtain pointers to values of basic types.
Each of these functions takes a value of the given basic type and returns a pointer to it:

* `PtrBool`
* `PtrInt`
* `PtrInt32`
* `PtrInt64`
* `PtrFloat`
* `PtrFloat32`
* `PtrFloat64`
* `PtrString`
* `PtrTime`

## Author


