---
title: Get directoryRole
description: Recupera las propiedades de un objeto directoryRole.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 621e56cca0703e87278120596fd47a9d4001effb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935811"
---
# <a name="get-directoryrole"></a><span data-ttu-id="7c4e3-103">Get directoryRole</span><span class="sxs-lookup"><span data-stu-id="7c4e3-103">Get directoryRole</span></span>

> <span data-ttu-id="7c4e3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c4e3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c4e3-106">Recupera las propiedades de un objeto directoryRole.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-106">Retrieve the properties of a directoryRole object.</span></span>
## <a name="permissions"></a><span data-ttu-id="7c4e3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7c4e3-107">Permissions</span></span>
<span data-ttu-id="7c4e3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7c4e3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7c4e3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7c4e3-110">Permission type</span></span>      | <span data-ttu-id="7c4e3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7c4e3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7c4e3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7c4e3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7c4e3-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7c4e3-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7c4e3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7c4e3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7c4e3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-115">Not supported.</span></span>    |
|<span data-ttu-id="7c4e3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7c4e3-116">Application</span></span> | <span data-ttu-id="7c4e3-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c4e3-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7c4e3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c4e3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7c4e3-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7c4e3-119">Optional query parameters</span></span>
<span data-ttu-id="7c4e3-120">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="7c4e3-120">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="7c4e3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c4e3-121">Request headers</span></span>
| <span data-ttu-id="7c4e3-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c4e3-122">Name</span></span>       | <span data-ttu-id="7c4e3-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c4e3-123">Type</span></span> | <span data-ttu-id="7c4e3-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c4e3-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7c4e3-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="7c4e3-125">Authorization</span></span>  | <span data-ttu-id="7c4e3-126">string</span><span class="sxs-lookup"><span data-stu-id="7c4e3-126">string</span></span>  | <span data-ttu-id="7c4e3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7c4e3-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7c4e3-129">Request body</span></span>
<span data-ttu-id="7c4e3-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7c4e3-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c4e3-131">Response</span></span>

<span data-ttu-id="7c4e3-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-132">If successful, this method returns a `200 OK` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7c4e3-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c4e3-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7c4e3-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c4e3-134">Request</span></span>
<span data-ttu-id="7c4e3-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryrole"
}-->
```http
GET https://graph.microsoft.com/beta/directoryRoles/{id}
```
##### <a name="response"></a><span data-ttu-id="7c4e3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c4e3-136">Response</span></span>
<span data-ttu-id="7c4e3-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c4e3-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 142

{
  "description": "description-value",
  "displayName": "displayName-value",
  "roleTemplateId": "roleTemplateId-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directoryRole",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
