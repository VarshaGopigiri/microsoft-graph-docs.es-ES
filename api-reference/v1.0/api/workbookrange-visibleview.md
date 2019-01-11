---
title: 'workbookRange: visibleView'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
localization_priority: Normal
ms.openlocfilehash: 1832c30c8a223b1a5067cede03796bcab16d5a94
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826911"
---
# <a name="workbookrange-visibleview"></a><span data-ttu-id="54b4b-104">workbookRange: visibleView</span><span class="sxs-lookup"><span data-stu-id="54b4b-104">workbookRange: visibleView</span></span>


## <a name="permissions"></a><span data-ttu-id="54b4b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="54b4b-105">Permissions</span></span>
<span data-ttu-id="54b4b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54b4b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54b4b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54b4b-108">Permission type</span></span>      | <span data-ttu-id="54b4b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54b4b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="54b4b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54b4b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="54b4b-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="54b4b-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="54b4b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54b4b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="54b4b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54b4b-113">Not supported.</span></span>    |
|<span data-ttu-id="54b4b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54b4b-114">Application</span></span> | <span data-ttu-id="54b4b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54b4b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="54b4b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54b4b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView
```
## <a name="request-headers"></a><span data-ttu-id="54b4b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54b4b-117">Request headers</span></span>
| <span data-ttu-id="54b4b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="54b4b-118">Name</span></span>       | <span data-ttu-id="54b4b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="54b4b-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="54b4b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="54b4b-120">Authorization</span></span>  | <span data-ttu-id="54b4b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54b4b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="54b4b-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="54b4b-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="54b4b-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="54b4b-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="54b4b-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54b4b-126">Request body</span></span>

### <a name="response"></a><span data-ttu-id="54b4b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54b4b-127">Response</span></span>
<span data-ttu-id="54b4b-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54b4b-128">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54b4b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54b4b-129">Example</span></span>
<span data-ttu-id="54b4b-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="54b4b-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="54b4b-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54b4b-131">Request</span></span>
<span data-ttu-id="54b4b-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54b4b-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_visibleview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView
```

##### <a name="response"></a><span data-ttu-id="54b4b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54b4b-133">Response</span></span>
<span data-ttu-id="54b4b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54b4b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
