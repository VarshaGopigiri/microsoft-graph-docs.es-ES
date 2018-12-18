---
title: 'ChartPointsCollection: ItemAt'
description: Recuperar un punto en función de su posición dentro de la serie.
author: lumine2008
ms.openlocfilehash: f48a51e8da2c3dca76952460da61b492ea1235ee
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311588"
---
# <a name="chartpointscollection-itemat"></a><span data-ttu-id="81f51-103">ChartPointsCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="81f51-103">ChartPointsCollection: ItemAt</span></span>

> <span data-ttu-id="81f51-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="81f51-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="81f51-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="81f51-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="81f51-106">Recuperar un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="81f51-106">Retrieve a point based on its position within the series.</span></span>
## <a name="permissions"></a><span data-ttu-id="81f51-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="81f51-107">Permissions</span></span>
<span data-ttu-id="81f51-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="81f51-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="81f51-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="81f51-110">Permission type</span></span>      | <span data-ttu-id="81f51-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="81f51-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="81f51-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="81f51-112">Delegated (work or school account)</span></span> | <span data-ttu-id="81f51-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="81f51-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="81f51-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="81f51-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="81f51-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="81f51-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="81f51-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="81f51-116">Application</span></span> | <span data-ttu-id="81f51-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="81f51-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="81f51-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="81f51-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="81f51-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="81f51-119">Request headers</span></span>
| <span data-ttu-id="81f51-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="81f51-120">Name</span></span>       | <span data-ttu-id="81f51-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="81f51-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="81f51-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="81f51-122">Authorization</span></span>  | <span data-ttu-id="81f51-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="81f51-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="81f51-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="81f51-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="81f51-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="81f51-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="81f51-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="81f51-128">Request body</span></span>
<span data-ttu-id="81f51-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="81f51-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="81f51-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="81f51-130">Parameter</span></span>    | <span data-ttu-id="81f51-131">Type</span><span class="sxs-lookup"><span data-stu-id="81f51-131">Type</span></span>   |<span data-ttu-id="81f51-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="81f51-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="81f51-133">index</span><span class="sxs-lookup"><span data-stu-id="81f51-133">index</span></span>|<span data-ttu-id="81f51-134">number</span><span class="sxs-lookup"><span data-stu-id="81f51-134">number</span></span>|<span data-ttu-id="81f51-p105">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="81f51-p105">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="81f51-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81f51-137">Response</span></span>

<span data-ttu-id="81f51-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [ChartPoint](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81f51-138">If successful, this method returns `200 OK` response code and [ChartPoint](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="81f51-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="81f51-139">Example</span></span>
<span data-ttu-id="81f51-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="81f51-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="81f51-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="81f51-141">Request</span></span>
<span data-ttu-id="81f51-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="81f51-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartpointscollection_itemat"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="81f51-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81f51-143">Response</span></span>
<span data-ttu-id="81f51-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="81f51-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartPoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 20

{
  "value": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPointsCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->