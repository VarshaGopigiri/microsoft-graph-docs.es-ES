---
title: Create RangeBorder
description: Use esta API para crear un objeto RangeBorder.
ms.openlocfilehash: 0c0d17efd41b3414275639152bc91d8785814524
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085367"
---
# <a name="create-rangeborder"></a><span data-ttu-id="035ad-103">Create RangeBorder</span><span class="sxs-lookup"><span data-stu-id="035ad-103">Create RangeBorder</span></span>

> <span data-ttu-id="035ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="035ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="035ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="035ad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="035ad-106">Use esta API para crear un objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="035ad-106">Use this API to create a new RangeBorder.</span></span>
## <a name="permissions"></a><span data-ttu-id="035ad-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="035ad-107">Permissions</span></span>
<span data-ttu-id="035ad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="035ad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="035ad-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="035ad-110">Permission type</span></span>      | <span data-ttu-id="035ad-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="035ad-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="035ad-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="035ad-112">Delegated (work or school account)</span></span> | <span data-ttu-id="035ad-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="035ad-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="035ad-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="035ad-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="035ad-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="035ad-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="035ad-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="035ad-116">Application</span></span> | <span data-ttu-id="035ad-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="035ad-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="035ad-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="035ad-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/format/borders
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/borders
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/borders

```
## <a name="request-headers"></a><span data-ttu-id="035ad-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="035ad-119">Request headers</span></span>
| <span data-ttu-id="035ad-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="035ad-120">Name</span></span>       | <span data-ttu-id="035ad-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="035ad-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="035ad-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="035ad-122">Authorization</span></span>  | <span data-ttu-id="035ad-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="035ad-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="035ad-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="035ad-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="035ad-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="035ad-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="035ad-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="035ad-128">Request body</span></span>
<span data-ttu-id="035ad-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [RangeBorder](../resources/rangeborder.md).</span><span class="sxs-lookup"><span data-stu-id="035ad-129">In the request body, supply a JSON representation of [RangeBorder](../resources/rangeborder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="035ad-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="035ad-130">Response</span></span>

<span data-ttu-id="035ad-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [RangeBorder](../resources/rangeborder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="035ad-131">If successful, this method returns `201 Created` response code and [RangeBorder](../resources/rangeborder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="035ad-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="035ad-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="035ad-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="035ad-133">Request</span></span>
<span data-ttu-id="035ad-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="035ad-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_rangeborder_from_rangeformat"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/format/borders
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```
<span data-ttu-id="035ad-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [RangeBorder](../resources/rangeborder.md).</span><span class="sxs-lookup"><span data-stu-id="035ad-135">In the request body, supply a JSON representation of [RangeBorder](../resources/rangeborder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="035ad-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="035ad-136">Response</span></span>
<span data-ttu-id="035ad-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="035ad-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeBorder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create RangeBorder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->