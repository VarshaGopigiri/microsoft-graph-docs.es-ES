---
title: Get directoryRoleTemplate
description: Recupera las propiedades y relaciones de un objeto directoryroletemplate.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: d67b539fa01d03e8a22c7153e20282d3f56907bd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811329"
---
# <a name="get-directoryroletemplate"></a><span data-ttu-id="91264-103">Get directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="91264-103">Get directoryRoleTemplate</span></span>

<span data-ttu-id="91264-104">Recupera las propiedades y relaciones de un objeto directoryroletemplate.</span><span class="sxs-lookup"><span data-stu-id="91264-104">Retrieve the properties and relationships of a directoryroletemplate object.</span></span>
## <a name="permissions"></a><span data-ttu-id="91264-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="91264-105">Permissions</span></span>
<span data-ttu-id="91264-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91264-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="91264-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="91264-108">Permission type</span></span>      | <span data-ttu-id="91264-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="91264-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="91264-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="91264-110">Delegated (work or school account)</span></span> | <span data-ttu-id="91264-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="91264-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="91264-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="91264-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="91264-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="91264-113">Not supported.</span></span>    |
|<span data-ttu-id="91264-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="91264-114">Application</span></span> | <span data-ttu-id="91264-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="91264-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="91264-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91264-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="91264-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="91264-117">Optional query parameters</span></span>
<span data-ttu-id="91264-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="91264-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="91264-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91264-119">Request headers</span></span>
| <span data-ttu-id="91264-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="91264-120">Name</span></span>       | <span data-ttu-id="91264-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="91264-121">Type</span></span> | <span data-ttu-id="91264-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="91264-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="91264-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="91264-123">Authorization</span></span>  | <span data-ttu-id="91264-124">string</span><span class="sxs-lookup"><span data-stu-id="91264-124">string</span></span>  | <span data-ttu-id="91264-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="91264-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="91264-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="91264-127">Request body</span></span>
<span data-ttu-id="91264-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="91264-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="91264-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91264-129">Response</span></span>

<span data-ttu-id="91264-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91264-130">If successful, this method returns a `200 OK` response code and [directoryRoleTemplate](../resources/directoryroletemplate.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="91264-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91264-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="91264-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91264-132">Request</span></span>
<span data-ttu-id="91264-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="91264-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplate"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoleTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="91264-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91264-134">Response</span></span>
<span data-ttu-id="91264-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="91264-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRoleTemplate"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 98

{
  "description": "description-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directoryRoleTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
