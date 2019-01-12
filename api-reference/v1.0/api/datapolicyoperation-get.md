---
title: Obtener dataPolicyOperation
description: Recuperar las propiedades del objeto dataPolicyOperation.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 2f9c4608aaa8d951b5a5fed6b499643e5a4d63d0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956342"
---
# <a name="get-datapolicyoperation"></a><span data-ttu-id="7b7e3-103">Obtener dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="7b7e3-103">Get dataPolicyOperation</span></span>

<span data-ttu-id="7b7e3-104">Recuperar las propiedades de un objeto **dataPolicyOperation** .</span><span class="sxs-lookup"><span data-stu-id="7b7e3-104">Retrieve the properties of a **dataPolicyOperation** object.</span></span>

## <a name="permissions"></a><span data-ttu-id="7b7e3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b7e3-105">Permissions</span></span>
<span data-ttu-id="7b7e3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b7e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7b7e3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b7e3-108">Permission type</span></span>      | <span data-ttu-id="7b7e3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b7e3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7b7e3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b7e3-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="7b7e3-111">User.Export.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b7e3-111">User.Export.All, User.Read.All</span></span>  |
|<span data-ttu-id="7b7e3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b7e3-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="7b7e3-113">No aplicable</span><span class="sxs-lookup"><span data-stu-id="7b7e3-113">Not applicable</span></span>  |
|<span data-ttu-id="7b7e3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b7e3-114">Application</span></span> | <span data-ttu-id="7b7e3-115">User.Export.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b7e3-115">User.Export.All, User.Read.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="7b7e3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b7e3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /dataPolicyOperations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="7b7e3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b7e3-117">Request headers</span></span>
| <span data-ttu-id="7b7e3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b7e3-118">Name</span></span>      |<span data-ttu-id="7b7e3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b7e3-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="7b7e3-120">Autorización</span><span class="sxs-lookup"><span data-stu-id="7b7e3-120">Authorization</span></span>  | <span data-ttu-id="7b7e3-121">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="7b7e3-121">Bearer {token}</span></span>|

## <a name="request-body"></a><span data-ttu-id="7b7e3-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b7e3-122">Request body</span></span>
<span data-ttu-id="7b7e3-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7b7e3-123">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="7b7e3-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b7e3-124">Response</span></span>
<span data-ttu-id="7b7e3-125">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [dataPolicyOperation](../resources/datapolicyoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b7e3-125">If successful, this method returns a `200 OK` response code and a [dataPolicyOperation](../resources/datapolicyoperation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7b7e3-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b7e3-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7b7e3-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b7e3-127">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_datapolicyoperation"
}-->
```http
GET https://graph.microsoft.com/v1.0/dataPolicyOperations/{id}
```
##### <a name="response"></a><span data-ttu-id="7b7e3-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b7e3-128">Response</span></span>
><span data-ttu-id="7b7e3-p102">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b7e3-p102">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.dataPolicyOperation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 212

{
  "completedDateTime": "datetime-value",
  "id": "id-value",
  "status": "status-value",
  "storageLocation": "storageLocation-value",
  "userId": "userId-value",
  "submittedDateTime": "datetime-value", 
  "progress": "double-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get dataPolicyOperation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
