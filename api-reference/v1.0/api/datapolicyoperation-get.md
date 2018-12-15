---
title: Obtener dataPolicyOperation
description: Recuperar las propiedades del objeto dataPolicyOperation.
ms.openlocfilehash: 8e5e4b6c10e086769fadcdd575cfd71339a5dcde
ms.sourcegitcommit: f3d479edf03935d0edbbc7668a65f7cde2a56c92
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2018
ms.locfileid: "27284115"
---
# <a name="get-datapolicyoperation"></a><span data-ttu-id="91878-103">Obtener dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="91878-103">Get dataPolicyOperation</span></span>

<span data-ttu-id="91878-104">Recuperar las propiedades de un objeto **dataPolicyOperation** .</span><span class="sxs-lookup"><span data-stu-id="91878-104">Retrieve the properties of a **dataPolicyOperation** object.</span></span>

## <a name="permissions"></a><span data-ttu-id="91878-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="91878-105">Permissions</span></span>
<span data-ttu-id="91878-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91878-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="91878-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="91878-108">Permission type</span></span>      | <span data-ttu-id="91878-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="91878-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="91878-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="91878-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="91878-111">User.Export.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="91878-111">User.Export.All, User.Read.All</span></span>  |
|<span data-ttu-id="91878-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="91878-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="91878-113">No aplicable</span><span class="sxs-lookup"><span data-stu-id="91878-113">Not applicable</span></span>  |
|<span data-ttu-id="91878-114">Application</span><span class="sxs-lookup"><span data-stu-id="91878-114">Application</span></span> | <span data-ttu-id="91878-115">User.Export.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="91878-115">User.Export.All, User.Read.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="91878-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91878-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /dataPolicyOperations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="91878-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91878-117">Request headers</span></span>
| <span data-ttu-id="91878-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="91878-118">Name</span></span>      |<span data-ttu-id="91878-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="91878-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="91878-120">Autorización</span><span class="sxs-lookup"><span data-stu-id="91878-120">Authorization</span></span>  | <span data-ttu-id="91878-121">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="91878-121">Bearer {token}</span></span>|

## <a name="request-body"></a><span data-ttu-id="91878-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="91878-122">Request body</span></span>
<span data-ttu-id="91878-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="91878-123">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="91878-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91878-124">Response</span></span>
<span data-ttu-id="91878-125">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [dataPolicyOperation](../resources/datapolicyoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91878-125">If successful, this method returns a `200 OK` response code and a [dataPolicyOperation](../resources/datapolicyoperation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="91878-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91878-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="91878-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91878-127">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_datapolicyoperation"
}-->
```http
GET https://graph.microsoft.com/v1.0/dataPolicyOperations/{id}
```
##### <a name="response"></a><span data-ttu-id="91878-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91878-128">Response</span></span>
><span data-ttu-id="91878-p102">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="91878-p102">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
