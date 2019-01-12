---
title: List directReports
description: Obtiene los subordinados directos del usuario. Devuelve los usuarios y los contactos para los que se asigna este usuario como administrador.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: da881d46b69153a85de225b895f6b1c2d622ff09
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984440"
---
# <a name="list-directreports"></a><span data-ttu-id="0abf5-104">List directReports</span><span class="sxs-lookup"><span data-stu-id="0abf5-104">List directReports</span></span>

> <span data-ttu-id="0abf5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0abf5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0abf5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0abf5-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0abf5-p103">Obtiene los subordinados directos del usuario. Devuelve los usuarios y los contactos para los que se asigna este usuario como administrador.</span><span class="sxs-lookup"><span data-stu-id="0abf5-p103">Get user's direct reports. Returns the users and contacts for whom this user is assigned as manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="0abf5-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="0abf5-109">Permissions</span></span>
<span data-ttu-id="0abf5-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0abf5-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0abf5-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0abf5-112">Permission type</span></span>      | <span data-ttu-id="0abf5-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0abf5-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0abf5-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0abf5-114">Delegated (work or school account)</span></span> | <span data-ttu-id="0abf5-115">User.Read, User.ReadWrite, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0abf5-115">User.Read, User.ReadWrite, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="0abf5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0abf5-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0abf5-117">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0abf5-117">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="0abf5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0abf5-118">Application</span></span> | <span data-ttu-id="0abf5-119">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0abf5-119">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0abf5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0abf5-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/directReports
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0abf5-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0abf5-121">Optional query parameters</span></span>
<span data-ttu-id="0abf5-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0abf5-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0abf5-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0abf5-123">Request headers</span></span>
| <span data-ttu-id="0abf5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0abf5-124">Header</span></span>       | <span data-ttu-id="0abf5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0abf5-125">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="0abf5-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="0abf5-126">Authorization</span></span>  | <span data-ttu-id="0abf5-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0abf5-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="0abf5-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0abf5-129">Content-Type</span></span>   | <span data-ttu-id="0abf5-130">application/json</span><span class="sxs-lookup"><span data-stu-id="0abf5-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0abf5-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0abf5-131">Request body</span></span>
<span data-ttu-id="0abf5-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0abf5-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0abf5-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0abf5-133">Response</span></span>

<span data-ttu-id="0abf5-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0abf5-134">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0abf5-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0abf5-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0abf5-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0abf5-136">Request</span></span>
<span data-ttu-id="0abf5-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0abf5-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directreports"
}-->
```http
GET https://graph.microsoft.com/beta/me/directReports
```
##### <a name="response"></a><span data-ttu-id="0abf5-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0abf5-138">Response</span></span>
<span data-ttu-id="0abf5-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0abf5-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
