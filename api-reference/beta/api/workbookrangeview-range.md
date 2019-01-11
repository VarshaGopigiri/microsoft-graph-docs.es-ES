---
title: 'workbookRangeView: range'
description: Devolver el rango asociado al recurso rangeView.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 8c116a80e01c0b649ff1846de3e324874e7dd837
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863423"
---
# <a name="workbookrangeview-range"></a><span data-ttu-id="2f22f-103">workbookRangeView: range</span><span class="sxs-lookup"><span data-stu-id="2f22f-103">workbookRangeView: range</span></span>

> <span data-ttu-id="2f22f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f22f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f22f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f22f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2f22f-106">Devolver el rango asociado al recurso rangeView.</span><span class="sxs-lookup"><span data-stu-id="2f22f-106">Return the range associated with the rangeView resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="2f22f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2f22f-107">Permissions</span></span>
<span data-ttu-id="2f22f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2f22f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2f22f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2f22f-110">Permission type</span></span>      | <span data-ttu-id="2f22f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2f22f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2f22f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2f22f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2f22f-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2f22f-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2f22f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2f22f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2f22f-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2f22f-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2f22f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2f22f-116">Application</span></span> | <span data-ttu-id="2f22f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f22f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2f22f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f22f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(addres={address})/visibleView/range

```
## <a name="request-headers"></a><span data-ttu-id="2f22f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f22f-119">Request headers</span></span>
| <span data-ttu-id="2f22f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f22f-120">Name</span></span>       | <span data-ttu-id="2f22f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f22f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2f22f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2f22f-122">Authorization</span></span>  | <span data-ttu-id="2f22f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f22f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2f22f-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2f22f-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="2f22f-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2f22f-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2f22f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2f22f-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="2f22f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f22f-129">Response</span></span>

<span data-ttu-id="2f22f-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f22f-130">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2f22f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f22f-131">Example</span></span>
<span data-ttu-id="2f22f-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2f22f-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2f22f-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f22f-133">Request</span></span>
<span data-ttu-id="2f22f-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f22f-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrangeview_range"
}-->
```http
GET https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView/range
```

##### <a name="response"></a><span data-ttu-id="2f22f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f22f-135">Response</span></span>
<span data-ttu-id="2f22f-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2f22f-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```
