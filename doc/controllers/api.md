# API

```csharp
APIController aPIController = client.APIController;
```

## Class Name

`APIController`

## Methods

* [Get User by Id](../../doc/controllers/api.md#get-user-by-id)
* [Create User](../../doc/controllers/api.md#create-user)


# Get User by Id

```csharp
GetUserByIdAsync(
    string id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | - |

## Response Type

[`Task<Models.User>`](../../doc/models/user.md)

## Example Usage

```csharp
string id = "id0";
try
{
    User result = await aPIController.GetUserByIdAsync(id);
}
catch (ApiException e)
{
    // TODO: Handle exception here
    Console.WriteLine(e.Message);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | User not found | [`ErrorException`](../../doc/models/error-exception.md) |


# Create User

```csharp
CreateUserAsync(
    Models.NewUser body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`NewUser`](../../doc/models/new-user.md) | Body, Required | - |

## Response Type

[`Task<Models.User>`](../../doc/models/user.md)

## Example Usage

```csharp
NewUser body = new NewUser
{
    Name = "name6",
    Email = "email0",
};

try
{
    User result = await aPIController.CreateUserAsync(body);
}
catch (ApiException e)
{
    // TODO: Handle exception here
    Console.WriteLine(e.Message);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request | [`ErrorException`](../../doc/models/error-exception.md) |

