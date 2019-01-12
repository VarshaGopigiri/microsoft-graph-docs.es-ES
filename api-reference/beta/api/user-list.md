---
title: List users
description: Recupera una lista de objetos de usuario.
author: dkershaw10
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 874ae4d3f54cfa67e6ac542cacab4b6eb39be716
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939514"
---
# <a name="list-users"></a><span data-ttu-id="c9083-103">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="c9083-103">List users</span></span>

> <span data-ttu-id="c9083-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c9083-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c9083-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c9083-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c9083-106">Recupera una lista de objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="c9083-106">Retrieve a list of user objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="c9083-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c9083-107">Permissions</span></span>

<span data-ttu-id="c9083-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c9083-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c9083-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c9083-110">Permission type</span></span>      | <span data-ttu-id="c9083-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c9083-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c9083-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c9083-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c9083-113">User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c9083-113">User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c9083-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c9083-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9083-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c9083-115">Not supported.</span></span>    |
|<span data-ttu-id="c9083-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c9083-116">Application</span></span> | <span data-ttu-id="c9083-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c9083-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c9083-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c9083-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c9083-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c9083-119">Optional query parameters</span></span>

<span data-ttu-id="c9083-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9083-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c9083-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c9083-121">Request headers</span></span>
| <span data-ttu-id="c9083-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9083-122">Header</span></span>        | <span data-ttu-id="c9083-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c9083-123">Value</span></span>                      |
|:--------------|:---------------------------|
| <span data-ttu-id="c9083-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="c9083-124">Authorization</span></span> | <span data-ttu-id="c9083-125">{token} de portador (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="c9083-125">Bearer {token} (required)</span></span>  |
| <span data-ttu-id="c9083-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c9083-126">Content-Type</span></span>  | <span data-ttu-id="c9083-127">application/json</span><span class="sxs-lookup"><span data-stu-id="c9083-127">application/json</span></span>           |

## <a name="request-body"></a><span data-ttu-id="c9083-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c9083-128">Request body</span></span>

<span data-ttu-id="c9083-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c9083-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c9083-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9083-130">Response</span></span>

<span data-ttu-id="c9083-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9083-131">If successful, this method returns a `200 OK` response code and collection of [user](../resources/user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c9083-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c9083-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c9083-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c9083-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/beta/users
```

##### <a name="response"></a><span data-ttu-id="c9083-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9083-134">Response</span></span>

<span data-ttu-id="c9083-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9083-135">Here is an example of the response.</span></span> <span data-ttu-id="c9083-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="c9083-136">Note: The response object shown here may be truncated for brevity.</span></span> 

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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List users",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
