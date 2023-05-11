# IO.Swagger - the C# library for the Swagger Petstore

This is a sample Petstore server.  You can find out more about Swagger at [http://swagger.io](http://swagger.io) or on [irc.freenode.net, #swagger](http://swagger.io/irc/). 

This C# SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- SDK version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.dotnet.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET 4.0 or later
- Windows Phone 7.1 (Mango)

<a name="dependencies"></a>
## Dependencies
- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later
- [JsonSubTypes](https://www.nuget.org/packages/JsonSubTypes/) - 1.2.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
Install-Package JsonSubTypes
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

<a name="installation"></a>
## Installation
Run the following command to generate the DLL
- [Mac/Linux] `/bin/sh build.sh`
- [Windows] `build.bat`

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;
```
<a name="packaging"></a>
## Packaging

A `.nuspec` is included with the project. You can follow the Nuget quickstart to [create](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#create-the-package) and [publish](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#publish-the-package) packages.

This `.nuspec` uses placeholders from the `.csproj`, so build the `.csproj` directly:

```
nuget pack -Build -OutputDirectory out IO.Swagger.csproj
```

Then, publish to a [local feed](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds) or [other host](https://docs.microsoft.com/en-us/nuget/hosting-packages/overview) and consume the new package via Nuget as usual.

<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            var apiInstance = new DefaultApi();

            try
            {
                List<string> result = apiInstance.TestMethod();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.TestMethod: " + e.Message );
            }
        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**TestMethod**](docs/DefaultApi.md#testmethod) | **GET** /test | 
*PetApi* | [**AddParrot**](docs/PetApi.md#addparrot) | **POST** /parrot | Add a new parrow to the store
*PetApi* | [**AddPet**](docs/PetApi.md#addpet) | **POST** /pet | Add a new pet to the store
*PetApi* | [**DeletePet**](docs/PetApi.md#deletepet) | **DELETE** /pet/{petId} | Deletes a pet
*PetApi* | [**DoCategoryStuff**](docs/PetApi.md#docategorystuff) | **POST** /pet/category | 
*PetApi* | [**FeedPet**](docs/PetApi.md#feedpet) | **POST** /pet/feed/{petId} | Find pet by ID
*PetApi* | [**FindPetsByStatus**](docs/PetApi.md#findpetsbystatus) | **GET** /pet/findByStatus | Finds Pets by status
*PetApi* | [**FindPetsByTags**](docs/PetApi.md#findpetsbytags) | **GET** /pet/findByTags | Finds Pets by tags
*PetApi* | [**GetParrots**](docs/PetApi.md#getparrots) | **GET** /parrot | get Parrots
*PetApi* | [**GetPetById**](docs/PetApi.md#getpetbyid) | **GET** /pet/{petId} | Find pet by ID
*PetApi* | [**UpdateParrots**](docs/PetApi.md#updateparrots) | **PUT** /parrot | update parrots
*PetApi* | [**UpdatePet**](docs/PetApi.md#updatepet) | **PUT** /pet | Update an existing pet
*PetApi* | [**UpdatePetWithForm**](docs/PetApi.md#updatepetwithform) | **POST** /pet/{petId} | Updates a pet in the store with form data
*PetApi* | [**UploadFile**](docs/PetApi.md#uploadfile) | **POST** /pet/{petId}/uploadImage | uploads an image
*StoreApi* | [**DeleteOrder**](docs/StoreApi.md#deleteorder) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
*StoreApi* | [**GetInventory**](docs/StoreApi.md#getinventory) | **GET** /store/inventory | Returns pet inventories by status
*StoreApi* | [**GetOrderById**](docs/StoreApi.md#getorderbyid) | **GET** /store/order/{orderId} | Find purchase order by ID
*StoreApi* | [**PlaceOrder**](docs/StoreApi.md#placeorder) | **POST** /store/order | Place an order for a pet
*UserApi* | [**CreateUser**](docs/UserApi.md#createuser) | **POST** /user | Create user
*UserApi* | [**CreateUsersWithArrayInput**](docs/UserApi.md#createuserswitharrayinput) | **POST** /user/createWithArray | Creates list of users with given input array
*UserApi* | [**CreateUsersWithListInput**](docs/UserApi.md#createuserswithlistinput) | **POST** /user/createWithList | Creates list of users with given input array
*UserApi* | [**DeleteUser**](docs/UserApi.md#deleteuser) | **DELETE** /user/{username} | Delete user
*UserApi* | [**GetUserByName**](docs/UserApi.md#getuserbyname) | **GET** /user/{username} | Get user by user name
*UserApi* | [**LoginUser**](docs/UserApi.md#loginuser) | **GET** /user/login | Logs user into the system
*UserApi* | [**LogoutUser**](docs/UserApi.md#logoutuser) | **GET** /user/logout | Logs out current logged in user session
*UserApi* | [**UserUsernamePut**](docs/UserApi.md#userusernameput) | **PUT** /user/{username} | Updated user

<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AllOfSubCategoryCategory](docs/AllOfSubCategoryCategory.md)
 - [Model.AllOfSubCategoryPetsItems](docs/AllOfSubCategoryPetsItems.md)
 - [Model.AllPetsResponse](docs/AllPetsResponse.md)
 - [Model.AnyOfparrotBodyParrotsItems](docs/AnyOfparrotBodyParrotsItems.md)
 - [Model.Cat](docs/Cat.md)
 - [Model.Category](docs/Category.md)
 - [Model.Dog](docs/Dog.md)
 - [Model.InlineResponse200](docs/InlineResponse200.md)
 - [Model.InlineResponse2001](docs/InlineResponse2001.md)
 - [Model.Macaw](docs/Macaw.md)
 - [Model.ModelApiResponse](docs/ModelApiResponse.md)
 - [Model.NullableEnumModel](docs/NullableEnumModel.md)
 - [Model.OneOfAllPetsResponseItems](docs/OneOfAllPetsResponseItems.md)
 - [Model.OneOfPartMasterDestination](docs/OneOfPartMasterDestination.md)
 - [Model.OneOfPartMasterOrigin](docs/OneOfPartMasterOrigin.md)
 - [Model.OneOfPetPartItems](docs/OneOfPetPartItems.md)
 - [Model.OneOfPup](docs/OneOfPup.md)
 - [Model.OneOfinlineResponse200ParrotsItems](docs/OneOfinlineResponse200ParrotsItems.md)
 - [Model.OneOfvalMembersValMemberItems](docs/OneOfvalMembersValMemberItems.md)
 - [Model.Order](docs/Order.md)
 - [Model.Parakeet](docs/Parakeet.md)
 - [Model.ParrotBody](docs/ParrotBody.md)
 - [Model.ParrotBody1](docs/ParrotBody1.md)
 - [Model.PartFour](docs/PartFour.md)
 - [Model.PartMaster](docs/PartMaster.md)
 - [Model.PartOne](docs/PartOne.md)
 - [Model.PartThree](docs/PartThree.md)
 - [Model.PartTwo](docs/PartTwo.md)
 - [Model.Pet](docs/Pet.md)
 - [Model.PetPetIdBody](docs/PetPetIdBody.md)
 - [Model.Pup](docs/Pup.md)
 - [Model.SubCategory](docs/SubCategory.md)
 - [Model.Tag](docs/Tag.md)
 - [Model.User](docs/User.md)
 - [Model.ValMemberChoice1](docs/ValMemberChoice1.md)
 - [Model.ValMemberChoice2](docs/ValMemberChoice2.md)
 - [Model.ValMembers](docs/ValMembers.md)

<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="api_key"></a>
### api_key

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

<a name="bearer"></a>
### bearer


<a name="petstore_auth"></a>
### petstore_auth

- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: http://petstore.swagger.io/oauth/dialog
- **Scopes**: 
  - write:pets: modify pets in your account
  - read:pets: read your pets
