---
title: 'workbookRangeView: range'
description: Devolver el rango asociado al recurso rangeView.
author: lumine2008
ms.openlocfilehash: 6e9c0c0f36231a29689c24d721d8c8978e8f1bf0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362737"
---
# <a name="workbookrangeview-range"></a><span data-ttu-id="b5292-103">workbookRangeView: range</span><span class="sxs-lookup"><span data-stu-id="b5292-103">workbookRangeView: range</span></span>
<span data-ttu-id="b5292-104">Devolver el rango asociado al recurso rangeView.</span><span class="sxs-lookup"><span data-stu-id="b5292-104">Return the range associated with the rangeView resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="b5292-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b5292-105">Permissions</span></span>
<span data-ttu-id="b5292-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b5292-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="b5292-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5292-108">Permission type</span></span>      | <span data-ttu-id="b5292-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5292-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b5292-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5292-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b5292-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5292-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b5292-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5292-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b5292-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5292-113">Not supported.</span></span>    |
|<span data-ttu-id="b5292-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5292-114">Application</span></span> | <span data-ttu-id="b5292-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5292-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b5292-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5292-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView/range

```
## <a name="request-headers"></a><span data-ttu-id="b5292-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5292-117">Request headers</span></span>
| <span data-ttu-id="b5292-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b5292-118">Name</span></span>       | <span data-ttu-id="b5292-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5292-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b5292-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5292-120">Authorization</span></span>  | <span data-ttu-id="b5292-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5292-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b5292-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b5292-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="b5292-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5292-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b5292-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5292-126">Request body</span></span>

### <a name="response"></a><span data-ttu-id="b5292-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5292-127">Response</span></span>
<span data-ttu-id="b5292-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5292-128">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b5292-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5292-129">Example</span></span>
<span data-ttu-id="b5292-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b5292-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b5292-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5292-131">Request</span></span>
<span data-ttu-id="b5292-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5292-132">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrangeview_range"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/range
```

##### <a name="response"></a><span data-ttu-id="b5292-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5292-133">Response</span></span>
<span data-ttu-id="b5292-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5292-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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
