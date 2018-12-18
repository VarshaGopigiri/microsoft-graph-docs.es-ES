---
title: Get directoryRoleTemplate
description: Recupera las propiedades y relaciones de un objeto directoryroletemplate.
author: lleonard-msft
ms.openlocfilehash: 1b001f0f648b1ac23c7f7b9445ee5f0f3b6a2354
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333820"
---
# <a name="get-directoryroletemplate"></a><span data-ttu-id="69433-103">Get directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="69433-103">Get directoryRoleTemplate</span></span>

<span data-ttu-id="69433-104">Recupera las propiedades y relaciones de un objeto directoryroletemplate.</span><span class="sxs-lookup"><span data-stu-id="69433-104">Retrieve the properties and relationships of a directoryroletemplate object.</span></span>
## <a name="permissions"></a><span data-ttu-id="69433-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="69433-105">Permissions</span></span>
<span data-ttu-id="69433-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69433-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69433-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69433-108">Permission type</span></span>      | <span data-ttu-id="69433-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69433-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="69433-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69433-110">Delegated (work or school account)</span></span> | <span data-ttu-id="69433-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="69433-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="69433-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69433-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="69433-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69433-113">Not supported.</span></span>    |
|<span data-ttu-id="69433-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69433-114">Application</span></span> | <span data-ttu-id="69433-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69433-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="69433-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69433-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="69433-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="69433-117">Optional query parameters</span></span>
<span data-ttu-id="69433-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="69433-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="69433-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69433-119">Request headers</span></span>
| <span data-ttu-id="69433-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="69433-120">Name</span></span>       | <span data-ttu-id="69433-121">Type</span><span class="sxs-lookup"><span data-stu-id="69433-121">Type</span></span> | <span data-ttu-id="69433-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="69433-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="69433-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="69433-123">Authorization</span></span>  | <span data-ttu-id="69433-124">string</span><span class="sxs-lookup"><span data-stu-id="69433-124">string</span></span>  | <span data-ttu-id="69433-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69433-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="69433-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69433-127">Request body</span></span>
<span data-ttu-id="69433-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="69433-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="69433-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69433-129">Response</span></span>

<span data-ttu-id="69433-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69433-130">If successful, this method returns a `200 OK` response code and [directoryRoleTemplate](../resources/directoryroletemplate.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="69433-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69433-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="69433-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69433-132">Request</span></span>
<span data-ttu-id="69433-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69433-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplate"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoleTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="69433-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69433-134">Response</span></span>
<span data-ttu-id="69433-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69433-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
