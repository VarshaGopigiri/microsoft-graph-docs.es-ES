---
title: Obtener un usuario
description: Recupere las propiedades y las relaciones del objeto de usuario.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: 8b21e45c5b6e86a539a2056859a0afa007614fcf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886216"
---
# <a name="get-a-user"></a><span data-ttu-id="eb433-103">Obtener un usuario</span><span class="sxs-lookup"><span data-stu-id="eb433-103">Get a user</span></span>

<span data-ttu-id="eb433-104">Recupere las propiedades y las relaciones del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="eb433-104">Retrieve the properties and relationships of user object.</span></span>

> <span data-ttu-id="eb433-p101">Nota: La obtención de un usuario solo devuelve un conjunto predeterminado de propiedades (*businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName*). Use `$select` para obtener otras propiedades y relaciones del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="eb433-p101">Note: Getting a user returns a default set of properties only (*businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName*). Use `$select` to get the other properties and relationships for the [user](../resources/user.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="eb433-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eb433-107">Permissions</span></span>
<span data-ttu-id="eb433-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb433-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb433-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb433-110">Permission type</span></span>      | <span data-ttu-id="eb433-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb433-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb433-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb433-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eb433-113">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eb433-113">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eb433-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb433-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb433-115">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eb433-115">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="eb433-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb433-116">Application</span></span> | <span data-ttu-id="eb433-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb433-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb433-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb433-118">HTTP request</span></span>
<span data-ttu-id="eb433-119">Para un usuario específico:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="eb433-119">For a specific user: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /users/{id | userPrincipalName}
```

<span data-ttu-id="eb433-120">Para el usuario ha iniciado sesión:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="eb433-120">For the signed-in user: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me
```

## <a name="optional-query-parameters"></a><span data-ttu-id="eb433-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="eb433-121">Optional query parameters</span></span>
<span data-ttu-id="eb433-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb433-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="eb433-123">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="eb433-123">By default, only a limited set of properties are returned ( _businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_ ).</span></span> 

<span data-ttu-id="eb433-124">Para devolver un conjunto de propiedades alternativo, tiene que especificar el conjunto de propiedades de [usuario](../resources/user.md) que prefiera con el parámetro de consulta `$select` de OData.</span><span class="sxs-lookup"><span data-stu-id="eb433-124">To return an alternative property set, you must specify the desired set of [user](../resources/user.md) properties using the OData `$select` query parameter.</span></span> <span data-ttu-id="eb433-125">Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="eb433-125">For example, to return _displayName_, _givenName_, and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

## <a name="request-headers"></a><span data-ttu-id="eb433-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb433-126">Request headers</span></span>
| <span data-ttu-id="eb433-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb433-127">Header</span></span>       | <span data-ttu-id="eb433-128">Valor</span><span class="sxs-lookup"><span data-stu-id="eb433-128">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="eb433-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb433-129">Authorization</span></span>  | <span data-ttu-id="eb433-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb433-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eb433-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="eb433-132">Content-Type</span></span>   | <span data-ttu-id="eb433-133">application/json</span><span class="sxs-lookup"><span data-stu-id="eb433-133">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="eb433-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb433-134">Request body</span></span>
<span data-ttu-id="eb433-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eb433-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eb433-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb433-136">Response</span></span>

<span data-ttu-id="eb433-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb433-137">If successful, this method returns a `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="eb433-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eb433-138">Examples</span></span>

### <a name="example-1-standard-users-request"></a><span data-ttu-id="eb433-139">Ejemplo 1: Solicitud de usuarios estándar</span><span class="sxs-lookup"><span data-stu-id="eb433-139">Example 1: Standard users request</span></span>

<span data-ttu-id="eb433-140">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="eb433-140">By default, only a limited set of properties are returned ( _businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_ ).</span></span> <span data-ttu-id="eb433-141">Este ejemplo ilustra las solicitudes y respuestas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="eb433-141">This example illustrates the default request and response.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/users/{id | userPrincipalName}
```

##### <a name="response"></a><span data-ttu-id="eb433-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb433-142">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "businessPhones": [
       "businessPhones-value"
   ],
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "jobTitle": "jobTitle-value",
   "mail": "mail-value",
   "mobilePhone": "mobilePhone-value",
   "officeLocation": "officeLocation-value",
   "preferredLanguage": "preferredLanguage-value",
   "surname": "surname-value",
   "userPrincipalName": "userPrincipalName-value",
   "id": "id-value"
}
```


### <a name="example-2-signed-in-user-request"></a><span data-ttu-id="eb433-143">Ejemplo 2: Solicitud de usuario de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="eb433-143">Example 2: Signed-in user request</span></span>

<span data-ttu-id="eb433-144">Puede obtener la información de usuario para el usuario que hayan iniciado sesión reemplazando `/users/{id | userPrincipalName}` con `/me`.</span><span class="sxs-lookup"><span data-stu-id="eb433-144">You can get the user information for the signed-in user by replacing `/users/{id | userPrincipalName}` with `/me`.</span></span>

##### <a name="request"></a><span data-ttu-id="eb433-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb433-145">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/me
```
##### <a name="response"></a><span data-ttu-id="eb433-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb433-146">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "businessPhones": [
       "businessPhones-value"
   ],
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "jobTitle": "jobTitle-value",
   "mail": "mail-value",
   "mobilePhone": "mobilePhone-value",
   "officeLocation": "officeLocation-value",
   "preferredLanguage": "preferredLanguage-value",
   "surname": "surname-value",
   "userPrincipalName": "userPrincipalName-value",
   "id": "id-value"
}
```

### <a name="example-3-users-request-using-select"></a><span data-ttu-id="eb433-147">Ejemplo 3: Solicitud de los usuarios mediante $select</span><span class="sxs-lookup"><span data-stu-id="eb433-147">Example 3: Users request using $select</span></span>

<span data-ttu-id="eb433-148">Si necesita otro conjunto de propiedades, puede usar el parámetro de consulta `$select` de OData.</span><span class="sxs-lookup"><span data-stu-id="eb433-148">If you need a different property set, you can use the OData `$select` query parameter.</span></span> <span data-ttu-id="eb433-149">Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="eb433-149">For example, to return _displayName_, _givenName_, and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

##### <a name="request"></a><span data-ttu-id="eb433-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb433-150">Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/users/{id | userPrincipalName}?$select=displayName,givenName,postalCode
```
##### <a name="response"></a><span data-ttu-id="eb433-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb433-151">Response</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "postalCode": "postalCode-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
