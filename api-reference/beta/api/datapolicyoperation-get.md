---
title: Obtener dataPolicyOperation
description: Recuperar las propiedades del objeto dataPolicyOperation.
ms.openlocfilehash: f2894b7cc23d6a5d35a03c7626ca9cb4640a9fcc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084566"
---
# <a name="get-datapolicyoperation"></a><span data-ttu-id="ba8b6-103">Obtener dataPolicyOperation</span><span class="sxs-lookup"><span data-stu-id="ba8b6-103">Get dataPolicyOperation</span></span>

<span data-ttu-id="ba8b6-104">Recuperar las propiedades del objeto dataPolicyOperation.</span><span class="sxs-lookup"><span data-stu-id="ba8b6-104">Retrieve the properties of the dataPolicyOperation object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ba8b6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ba8b6-105">Permissions</span></span>
<span data-ttu-id="ba8b6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba8b6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba8b6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba8b6-108">Permission type</span></span>      | <span data-ttu-id="ba8b6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba8b6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba8b6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba8b6-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="ba8b6-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ba8b6-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>  |
|<span data-ttu-id="ba8b6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba8b6-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ba8b6-113">No disponible</span><span class="sxs-lookup"><span data-stu-id="ba8b6-113">Not applicable</span></span>  |
|<span data-ttu-id="ba8b6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba8b6-114">Application</span></span> | <span data-ttu-id="ba8b6-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba8b6-115">Directory.Read.All, Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ba8b6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba8b6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /dataPolicyOperations/<id>
```

## <a name="request-headers"></a><span data-ttu-id="ba8b6-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8b6-117">Request headers</span></span>
| <span data-ttu-id="ba8b6-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ba8b6-118">Name</span></span>      |<span data-ttu-id="ba8b6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8b6-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ba8b6-120">Autorización</span><span class="sxs-lookup"><span data-stu-id="ba8b6-120">Authorization</span></span>  | <span data-ttu-id="ba8b6-121">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="ba8b6-121">Bearer {token}</span></span>|

## <a name="request-body"></a><span data-ttu-id="ba8b6-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8b6-122">Request body</span></span>
<span data-ttu-id="ba8b6-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ba8b6-123">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ba8b6-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba8b6-124">Response</span></span>
<span data-ttu-id="ba8b6-125">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [dataPolicyOperation](../resources/datapolicyoperation.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba8b6-125">If successful, this method returns a `200 OK` response code and [dataPolicyOperation](../resources/datapolicyoperation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ba8b6-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba8b6-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ba8b6-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8b6-127">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_datapolicyoperation"
}-->
```http
GET https://graph.microsoft.com/beta/dataPolicyOperations/<id>
```
##### <a name="response"></a><span data-ttu-id="ba8b6-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba8b6-128">Response</span></span>
<span data-ttu-id="ba8b6-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba8b6-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "submittedDateTime": "datetime-value"
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
