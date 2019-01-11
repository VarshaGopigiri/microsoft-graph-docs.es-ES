---
title: 'workbookRange: visibleView'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
localization_priority: Normal
ms.openlocfilehash: f994866c8f55ec2ffbc0b680d4576fbc6a8b7bb8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875169"
---
# <a name="workbookrange-visibleview"></a><span data-ttu-id="d5c2d-104">workbookRange: visibleView</span><span class="sxs-lookup"><span data-stu-id="d5c2d-104">workbookRange: visibleView</span></span>

> <span data-ttu-id="d5c2d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d5c2d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-106">Use of these APIs in production applications is not supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="d5c2d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d5c2d-107">Permissions</span></span>
<span data-ttu-id="d5c2d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d5c2d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d5c2d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d5c2d-110">Permission type</span></span>      | <span data-ttu-id="d5c2d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d5c2d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d5c2d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d5c2d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d5c2d-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5c2d-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d5c2d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d5c2d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d5c2d-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5c2d-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d5c2d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d5c2d-116">Application</span></span> | <span data-ttu-id="d5c2d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d5c2d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5c2d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView
```
## <a name="request-headers"></a><span data-ttu-id="d5c2d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5c2d-119">Request headers</span></span>
| <span data-ttu-id="d5c2d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d5c2d-120">Name</span></span>       | <span data-ttu-id="d5c2d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5c2d-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d5c2d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5c2d-122">Authorization</span></span>  | <span data-ttu-id="d5c2d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d5c2d-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d5c2d-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="d5c2d-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d5c2d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d5c2d-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="d5c2d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5c2d-129">Response</span></span>

<span data-ttu-id="d5c2d-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-130">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d5c2d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5c2d-131">Example</span></span>
<span data-ttu-id="d5c2d-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d5c2d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d5c2d-133">Request</span></span>
<span data-ttu-id="d5c2d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_visibleview"
}-->
```http
GET https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView
```

##### <a name="response"></a><span data-ttu-id="d5c2d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5c2d-135">Response</span></span>
<span data-ttu-id="d5c2d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d5c2d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
