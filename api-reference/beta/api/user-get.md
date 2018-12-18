---
title: Obtener un usuario
description: Recupere las propiedades y las relaciones del objeto de usuario.
author: dkershaw10
ms.openlocfilehash: eb2b3efe96e3fd4e4608ae045addaf8a1fe6911a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341576"
---
# <a name="get-a-user"></a><span data-ttu-id="f87c9-103">Obtener un usuario</span><span class="sxs-lookup"><span data-stu-id="f87c9-103">Get a user</span></span>

> <span data-ttu-id="f87c9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f87c9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f87c9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f87c9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f87c9-106">Recupere las propiedades y las relaciones del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="f87c9-106">Retrieve the properties and relationships of user object.</span></span>

<span data-ttu-id="f87c9-107">Puesto que el recurso de **usuario** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="f87c9-107">Since the **user** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **user** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="f87c9-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="f87c9-108">Permissions</span></span>
<span data-ttu-id="f87c9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f87c9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f87c9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f87c9-111">Permission type</span></span>      | <span data-ttu-id="f87c9-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f87c9-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f87c9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f87c9-113">Delegated (work or school account)</span></span> | <span data-ttu-id="f87c9-114">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f87c9-114">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f87c9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f87c9-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f87c9-116">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f87c9-116">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="f87c9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f87c9-117">Application</span></span> | <span data-ttu-id="f87c9-118">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f87c9-118">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f87c9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f87c9-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f87c9-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f87c9-120">Optional query parameters</span></span>
<span data-ttu-id="f87c9-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f87c9-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f87c9-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f87c9-122">Request headers</span></span>
| <span data-ttu-id="f87c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f87c9-123">Header</span></span>       | <span data-ttu-id="f87c9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f87c9-124">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="f87c9-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="f87c9-125">Authorization</span></span>  | <span data-ttu-id="f87c9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f87c9-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="f87c9-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f87c9-128">Content-Type</span></span>   | <span data-ttu-id="f87c9-129">application/json</span><span class="sxs-lookup"><span data-stu-id="f87c9-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f87c9-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f87c9-130">Request body</span></span>
<span data-ttu-id="f87c9-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f87c9-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f87c9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f87c9-132">Response</span></span>

<span data-ttu-id="f87c9-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f87c9-133">If successful, this method returns a `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f87c9-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f87c9-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f87c9-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f87c9-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/beta/me
```
##### <a name="response"></a><span data-ttu-id="f87c9-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f87c9-136">Response</span></span>
<span data-ttu-id="f87c9-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f87c9-137">Here is an example of the response.</span></span> <span data-ttu-id="f87c9-138">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f87c9-138">Note: The response object shown here may be truncated for brevity.</span></span> 

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

## <a name="see-also"></a><span data-ttu-id="f87c9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f87c9-139">See also</span></span>

- [<span data-ttu-id="f87c9-140">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="f87c9-140">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="f87c9-141">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="f87c9-141">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="f87c9-142">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="f87c9-142">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
