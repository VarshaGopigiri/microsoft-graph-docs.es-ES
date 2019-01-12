---
title: 'workbookRangeView: itemAt'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 423c20f6cbdcbfe65a2f8db965a4765c93079f18
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960584"
---
# <a name="workbookrangeview-itemat"></a><span data-ttu-id="62163-104">workbookRangeView: itemAt</span><span class="sxs-lookup"><span data-stu-id="62163-104">workbookRangeView: itemAt</span></span>

> <span data-ttu-id="62163-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="62163-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="62163-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="62163-106">Use of these APIs in production applications is not supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="62163-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="62163-107">Permissions</span></span>
<span data-ttu-id="62163-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62163-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62163-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62163-110">Permission type</span></span>      | <span data-ttu-id="62163-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62163-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="62163-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62163-112">Delegated (work or school account)</span></span> | <span data-ttu-id="62163-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62163-113">Not supported.</span></span>    |
|<span data-ttu-id="62163-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62163-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="62163-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62163-115">Not supported.</span></span>    |
|<span data-ttu-id="62163-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62163-116">Application</span></span> | <span data-ttu-id="62163-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62163-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="62163-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62163-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(addres={address})/visibleView/itemAt(index={n})

```
## <a name="request-headers"></a><span data-ttu-id="62163-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62163-119">Request headers</span></span>
| <span data-ttu-id="62163-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="62163-120">Name</span></span>       | <span data-ttu-id="62163-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="62163-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="62163-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="62163-122">Authorization</span></span>  | <span data-ttu-id="62163-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="62163-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="62163-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="62163-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="62163-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="62163-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="62163-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62163-128">Request body</span></span>
<span data-ttu-id="62163-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="62163-129">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="62163-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="62163-130">Parameter</span></span>    | <span data-ttu-id="62163-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="62163-131">Type</span></span>   |<span data-ttu-id="62163-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="62163-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="62163-133">index</span><span class="sxs-lookup"><span data-stu-id="62163-133">index</span></span>|<span data-ttu-id="62163-134">Int32</span><span class="sxs-lookup"><span data-stu-id="62163-134">Int32</span></span>|<span data-ttu-id="62163-135">Índice del elemento que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="62163-135">Index of the item to be returned.</span></span>|

## <a name="response"></a><span data-ttu-id="62163-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62163-136">Response</span></span>

<span data-ttu-id="62163-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62163-137">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="62163-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62163-138">Example</span></span>
<span data-ttu-id="62163-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="62163-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="62163-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="62163-140">Request</span></span>
<span data-ttu-id="62163-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62163-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrangeview_itemat"
}-->
```http
GET https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView/itemAt(index=0)

```

##### <a name="response"></a><span data-ttu-id="62163-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62163-142">Response</span></span>
<span data-ttu-id="62163-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62163-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeView"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 194

{
  "cellAddresses": "cellAddresses-value",
  "columnCount": 99,
  "formulas": "formulas-value",
  "formulasLocal": "formulasLocal-value",
  "formulasR1C1": "formulasR1C1-value",
  "index": 99
}
```
