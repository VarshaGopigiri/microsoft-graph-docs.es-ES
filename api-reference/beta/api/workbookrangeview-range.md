---
title: 'workbookRangeView: range'
description: Devolver el rango asociado al recurso rangeView.
ms.openlocfilehash: 7210501eaad8b99eb57f002292fcbef6a2f4c73c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090889"
---
# <a name="workbookrangeview-range"></a><span data-ttu-id="676cf-103">workbookRangeView: range</span><span class="sxs-lookup"><span data-stu-id="676cf-103">workbookRangeView: range</span></span>

> <span data-ttu-id="676cf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="676cf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="676cf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="676cf-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="676cf-106">Devolver el rango asociado al recurso rangeView.</span><span class="sxs-lookup"><span data-stu-id="676cf-106">Return the range associated with the rangeView resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="676cf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="676cf-107">Permissions</span></span>
<span data-ttu-id="676cf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="676cf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="676cf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="676cf-110">Permission type</span></span>      | <span data-ttu-id="676cf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="676cf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="676cf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="676cf-112">Delegated (work or school account)</span></span> | <span data-ttu-id="676cf-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="676cf-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="676cf-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="676cf-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="676cf-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="676cf-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="676cf-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="676cf-116">Application</span></span> | <span data-ttu-id="676cf-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="676cf-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="676cf-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="676cf-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(addres={address})/visibleView/range

```
## <a name="request-headers"></a><span data-ttu-id="676cf-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="676cf-119">Request headers</span></span>
| <span data-ttu-id="676cf-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="676cf-120">Name</span></span>       | <span data-ttu-id="676cf-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="676cf-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="676cf-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="676cf-122">Authorization</span></span>  | <span data-ttu-id="676cf-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="676cf-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="676cf-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="676cf-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="676cf-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="676cf-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="676cf-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="676cf-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="676cf-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="676cf-129">Response</span></span>

<span data-ttu-id="676cf-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="676cf-130">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="676cf-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="676cf-131">Example</span></span>
<span data-ttu-id="676cf-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="676cf-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="676cf-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="676cf-133">Request</span></span>
<span data-ttu-id="676cf-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="676cf-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrangeview_range"
}-->
```http
GET https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView/range
```

##### <a name="response"></a><span data-ttu-id="676cf-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="676cf-135">Response</span></span>
<span data-ttu-id="676cf-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="676cf-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
