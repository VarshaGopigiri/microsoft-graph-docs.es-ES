---
title: Get directoryRoleTemplate
description: Recupera las propiedades y relaciones de un objeto directoryroletemplate.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d66cf5f4d8784eeee5d4f84dd4eaa3616bafa5a4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922609"
---
# <a name="get-directoryroletemplate"></a><span data-ttu-id="57ad7-103">Get directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="57ad7-103">Get directoryRoleTemplate</span></span>

<span data-ttu-id="57ad7-104">Recupera las propiedades y relaciones de un objeto directoryroletemplate.</span><span class="sxs-lookup"><span data-stu-id="57ad7-104">Retrieve the properties and relationships of a directoryroletemplate object.</span></span>
## <a name="permissions"></a><span data-ttu-id="57ad7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="57ad7-105">Permissions</span></span>
<span data-ttu-id="57ad7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="57ad7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="57ad7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="57ad7-108">Permission type</span></span>      | <span data-ttu-id="57ad7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="57ad7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="57ad7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="57ad7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="57ad7-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="57ad7-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="57ad7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="57ad7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="57ad7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="57ad7-113">Not supported.</span></span>    |
|<span data-ttu-id="57ad7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="57ad7-114">Application</span></span> | <span data-ttu-id="57ad7-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="57ad7-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="57ad7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="57ad7-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="57ad7-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="57ad7-117">Optional query parameters</span></span>
<span data-ttu-id="57ad7-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="57ad7-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="57ad7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="57ad7-119">Request headers</span></span>
| <span data-ttu-id="57ad7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="57ad7-120">Name</span></span>       | <span data-ttu-id="57ad7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="57ad7-121">Type</span></span> | <span data-ttu-id="57ad7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="57ad7-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="57ad7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="57ad7-123">Authorization</span></span>  | <span data-ttu-id="57ad7-124">string</span><span class="sxs-lookup"><span data-stu-id="57ad7-124">string</span></span>  | <span data-ttu-id="57ad7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="57ad7-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="57ad7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="57ad7-127">Request body</span></span>
<span data-ttu-id="57ad7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="57ad7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="57ad7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="57ad7-129">Response</span></span>

<span data-ttu-id="57ad7-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="57ad7-130">If successful, this method returns a `200 OK` response code and [directoryRoleTemplate](../resources/directoryroletemplate.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="57ad7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="57ad7-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="57ad7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="57ad7-132">Request</span></span>
<span data-ttu-id="57ad7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="57ad7-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplate"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoleTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="57ad7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="57ad7-134">Response</span></span>
<span data-ttu-id="57ad7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="57ad7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
