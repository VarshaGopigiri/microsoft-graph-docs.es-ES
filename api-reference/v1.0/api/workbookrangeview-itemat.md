---
title: 'workbookRangeView: itemAt'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
localization_priority: Normal
ms.openlocfilehash: f9e5e6617439ad2f8c372a85dbbf07e82ea4c935
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817839"
---
# <a name="workbookrangeview-itemat"></a><span data-ttu-id="ac802-104">workbookRangeView: itemAt</span><span class="sxs-lookup"><span data-stu-id="ac802-104">workbookRangeView: itemAt</span></span>


## <a name="permissions"></a><span data-ttu-id="ac802-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ac802-105">Permissions</span></span>
<span data-ttu-id="ac802-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ac802-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ac802-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac802-108">Permission type</span></span>      | <span data-ttu-id="ac802-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac802-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ac802-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac802-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ac802-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac802-111">Files.ReadWrite</span></span> |
|<span data-ttu-id="ac802-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac802-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ac802-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac802-113">Not supported.</span></span>    |
|<span data-ttu-id="ac802-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac802-114">Application</span></span> | <span data-ttu-id="ac802-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac802-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ac802-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac802-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView/itemAt(index={n})

```
## <a name="request-headers"></a><span data-ttu-id="ac802-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac802-117">Request headers</span></span>
| <span data-ttu-id="ac802-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac802-118">Name</span></span>       | <span data-ttu-id="ac802-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac802-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ac802-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ac802-120">Authorization</span></span>  | <span data-ttu-id="ac802-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac802-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ac802-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ac802-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="ac802-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac802-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="function-parameters"></a><span data-ttu-id="ac802-126">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ac802-126">Function parameters</span></span>
<span data-ttu-id="ac802-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="ac802-127">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="ac802-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac802-128">Parameter</span></span>    | <span data-ttu-id="ac802-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac802-129">Type</span></span>   |<span data-ttu-id="ac802-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac802-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac802-131">index</span><span class="sxs-lookup"><span data-stu-id="ac802-131">index</span></span>|<span data-ttu-id="ac802-132">Int32</span><span class="sxs-lookup"><span data-stu-id="ac802-132">Int32</span></span>|<span data-ttu-id="ac802-133">Índice del elemento que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="ac802-133">Index of the item to be returned.</span></span>|

## <a name="response"></a><span data-ttu-id="ac802-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac802-134">Response</span></span>

<span data-ttu-id="ac802-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac802-135">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ac802-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac802-136">Example</span></span>
<span data-ttu-id="ac802-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ac802-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ac802-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac802-138">Request</span></span>
<span data-ttu-id="ac802-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac802-139">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrangeview_itemat"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/itemAt(index=0)

```

##### <a name="response"></a><span data-ttu-id="ac802-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac802-140">Response</span></span>
<span data-ttu-id="ac802-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac802-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
