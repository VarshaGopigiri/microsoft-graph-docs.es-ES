---
title: Get directoryRole
description: Recupera las propiedades de un objeto directoryRole.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 0ddad0f7bd6c62544dcc2aa65ede6c6db93dbd5e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967171"
---
# <a name="get-directoryrole"></a><span data-ttu-id="bcda9-103">Get directoryRole</span><span class="sxs-lookup"><span data-stu-id="bcda9-103">Get directoryRole</span></span>

<span data-ttu-id="bcda9-104">Recupera las propiedades de un objeto directoryRole.</span><span class="sxs-lookup"><span data-stu-id="bcda9-104">Retrieve the properties of a directoryRole object.</span></span>

## <a name="permissions"></a><span data-ttu-id="bcda9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bcda9-105">Permissions</span></span>
<span data-ttu-id="bcda9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bcda9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bcda9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcda9-108">Permission type</span></span>      | <span data-ttu-id="bcda9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcda9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bcda9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcda9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bcda9-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bcda9-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="bcda9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcda9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bcda9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcda9-113">Not supported.</span></span>    |
|<span data-ttu-id="bcda9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcda9-114">Application</span></span> | <span data-ttu-id="bcda9-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bcda9-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bcda9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcda9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bcda9-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bcda9-117">Optional query parameters</span></span>
<span data-ttu-id="bcda9-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="bcda9-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="bcda9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bcda9-119">Request headers</span></span>
| <span data-ttu-id="bcda9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="bcda9-120">Name</span></span>       | <span data-ttu-id="bcda9-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="bcda9-121">Type</span></span> | <span data-ttu-id="bcda9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcda9-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bcda9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bcda9-123">Authorization</span></span>  | <span data-ttu-id="bcda9-124">string</span><span class="sxs-lookup"><span data-stu-id="bcda9-124">string</span></span>  | <span data-ttu-id="bcda9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bcda9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bcda9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcda9-127">Request body</span></span>
<span data-ttu-id="bcda9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bcda9-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bcda9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcda9-129">Response</span></span>

<span data-ttu-id="bcda9-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcda9-130">If successful, this method returns a `200 OK` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bcda9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcda9-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bcda9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcda9-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryrole"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles/{id}
```
##### <a name="response"></a><span data-ttu-id="bcda9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcda9-133">Response</span></span>
<span data-ttu-id="bcda9-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bcda9-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

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
