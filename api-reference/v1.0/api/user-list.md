---
title: List users
description: Recupera una lista de objetos de usuario.
ms.openlocfilehash: 3ab6d2a663233bcb26b31abee33b430039ac8d25
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029754"
---
# <a name="list-users"></a><span data-ttu-id="f6c1d-103">List users</span><span class="sxs-lookup"><span data-stu-id="f6c1d-103">List users</span></span>

<span data-ttu-id="f6c1d-104">Recupera una lista de objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-104">Retrieve a list of user objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="f6c1d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f6c1d-105">Permissions</span></span>

<span data-ttu-id="f6c1d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6c1d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f6c1d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6c1d-108">Permission type</span></span>      | <span data-ttu-id="f6c1d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6c1d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f6c1d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6c1d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f6c1d-111">User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f6c1d-111">User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f6c1d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6c1d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f6c1d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-113">Not supported.</span></span>    |
|<span data-ttu-id="f6c1d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6c1d-114">Application</span></span> | <span data-ttu-id="f6c1d-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f6c1d-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f6c1d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6c1d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f6c1d-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f6c1d-117">Optional query parameters</span></span>

<span data-ttu-id="f6c1d-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="f6c1d-119">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="f6c1d-119">By default, only a limited set of properties are returned ( _businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_ ).</span></span> 

<span data-ttu-id="f6c1d-120">Para devolver un conjunto de propiedades alternativo, tiene que especificar el conjunto de propiedades de [usuario](../resources/user.md) que prefiera con el parámetro de consulta `$select` de OData.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-120">To return an alternative property set, you must specify the desired set of [user](../resources/user.md) properties using the OData `$select` query parameter.</span></span> <span data-ttu-id="f6c1d-121">Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="f6c1d-121">For example, to return _displayName_, _givenName_, and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

> <span data-ttu-id="f6c1d-p103">Nota: Algunas propiedades no se pueden devolver dentro de una colección de usuario. Las propiedades siguientes solo se admiten al [recuperar un único usuario](./user-get.md): _aboutMe, birthday, hireDate, interests, mySite, pastProjects, preferredName, responsibilities, schools, skills, mailboxSettings_</span><span class="sxs-lookup"><span data-stu-id="f6c1d-p103">Note: Certain properties cannot be returned within a user collection. The following properties are only supported when [retrieving an single user](./user-get.md): _aboutMe, birthday, hireDate, interests, mySite, pastProjects, preferredName, responsibilities, schools, skills, mailboxSettings_</span></span>

## <a name="request-headers"></a><span data-ttu-id="f6c1d-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6c1d-124">Request headers</span></span>

| <span data-ttu-id="f6c1d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6c1d-125">Header</span></span>        | <span data-ttu-id="f6c1d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f6c1d-126">Value</span></span>                      |
|:--------------|:---------------------------|
| <span data-ttu-id="f6c1d-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6c1d-127">Authorization</span></span> | <span data-ttu-id="f6c1d-128">{token} de portador (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="f6c1d-128">Bearer {token} (required)</span></span>  |
| <span data-ttu-id="f6c1d-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f6c1d-129">Content-Type</span></span>  | <span data-ttu-id="f6c1d-130">application/json</span><span class="sxs-lookup"><span data-stu-id="f6c1d-130">application/json</span></span>           |

## <a name="request-body"></a><span data-ttu-id="f6c1d-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6c1d-131">Request body</span></span>

<span data-ttu-id="f6c1d-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f6c1d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6c1d-133">Response</span></span>

<span data-ttu-id="f6c1d-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-134">If successful, this method returns a `200 OK` response code and collection of [user](../resources/user.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="f6c1d-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6c1d-135">Examples</span></span>

### <a name="example-1-standard-users-request"></a><span data-ttu-id="f6c1d-136">Ejemplo 1: Solicitud de usuarios estándar</span><span class="sxs-lookup"><span data-stu-id="f6c1d-136">Example 1: Standard users request</span></span>

<span data-ttu-id="f6c1d-137">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="f6c1d-137">By default, only a limited set of properties are returned (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span></span> <span data-ttu-id="f6c1d-138">Este ejemplo ilustra las solicitudes y respuestas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-138">This example illustrates the default request and response.</span></span> 

##### <a name="request"></a><span data-ttu-id="f6c1d-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6c1d-139">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/users
```

##### <a name="response"></a><span data-ttu-id="f6c1d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6c1d-140">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 608

{
  "value": [
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
  ]
}
```

### <a name="example-2-users-request-using-select"></a><span data-ttu-id="f6c1d-141">Ejemplo 2: Solicitud de los usuarios mediante $select</span><span class="sxs-lookup"><span data-stu-id="f6c1d-141">Example 2: Users request using $select</span></span>

<span data-ttu-id="f6c1d-142">Si necesita otro conjunto de propiedades, puede usar el parámetro de consulta `$select` de OData.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-142">If you need a different property set, you can use the OData `$select` query parameter.</span></span> <span data-ttu-id="f6c1d-143">Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="f6c1d-143">For example, to return _displayName_, _givenName_, and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

##### <a name="request"></a><span data-ttu-id="f6c1d-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6c1d-144">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/users?$select=displayName,givenName,postalCode
```

##### <a name="response"></a><span data-ttu-id="f6c1d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6c1d-145">Response</span></span>

<span data-ttu-id="f6c1d-146">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f6c1d-146">Note: The response object shown here may be truncated for brevity.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 159

{
  "value": [
    {
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "postalCode": "postalCode-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List users",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
