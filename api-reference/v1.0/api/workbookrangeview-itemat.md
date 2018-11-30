---
title: 'workbookRangeView: itemAt'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
ms.openlocfilehash: b6af086e9867ca4c4d61a4102de1d2800163c453
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028652"
---
# <a name="workbookrangeview-itemat"></a><span data-ttu-id="878f0-104">workbookRangeView: itemAt</span><span class="sxs-lookup"><span data-stu-id="878f0-104">workbookRangeView: itemAt</span></span>


## <a name="permissions"></a><span data-ttu-id="878f0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="878f0-105">Permissions</span></span>
<span data-ttu-id="878f0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="878f0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="878f0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="878f0-108">Permission type</span></span>      | <span data-ttu-id="878f0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="878f0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="878f0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="878f0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="878f0-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="878f0-111">Files.ReadWrite</span></span> |
|<span data-ttu-id="878f0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="878f0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="878f0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="878f0-113">Not supported.</span></span>    |
|<span data-ttu-id="878f0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="878f0-114">Application</span></span> | <span data-ttu-id="878f0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="878f0-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="878f0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="878f0-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView/itemAt(index={n})

```
## <a name="request-headers"></a><span data-ttu-id="878f0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="878f0-117">Request headers</span></span>
| <span data-ttu-id="878f0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="878f0-118">Name</span></span>       | <span data-ttu-id="878f0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="878f0-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="878f0-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="878f0-120">Authorization</span></span>  | <span data-ttu-id="878f0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="878f0-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="878f0-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="878f0-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="878f0-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="878f0-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="function-parameters"></a><span data-ttu-id="878f0-126">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="878f0-126">Function parameters</span></span>
<span data-ttu-id="878f0-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="878f0-127">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="878f0-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="878f0-128">Parameter</span></span>    | <span data-ttu-id="878f0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="878f0-129">Type</span></span>   |<span data-ttu-id="878f0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="878f0-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="878f0-131">index</span><span class="sxs-lookup"><span data-stu-id="878f0-131">index</span></span>|<span data-ttu-id="878f0-132">Int32</span><span class="sxs-lookup"><span data-stu-id="878f0-132">Int32</span></span>|<span data-ttu-id="878f0-133">Índice del elemento que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="878f0-133">Index of the item to be returned.</span></span>|

## <a name="response"></a><span data-ttu-id="878f0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="878f0-134">Response</span></span>

<span data-ttu-id="878f0-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="878f0-135">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="878f0-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="878f0-136">Example</span></span>
<span data-ttu-id="878f0-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="878f0-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="878f0-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="878f0-138">Request</span></span>
<span data-ttu-id="878f0-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="878f0-139">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrangeview_itemat"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/itemAt(index=0)

```

##### <a name="response"></a><span data-ttu-id="878f0-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="878f0-140">Response</span></span>
<span data-ttu-id="878f0-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="878f0-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
