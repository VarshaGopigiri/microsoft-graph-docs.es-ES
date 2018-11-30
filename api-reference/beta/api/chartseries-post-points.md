---
title: Create ChartPoints
description: Use esta API para crear un objeto ChartPoints.
ms.openlocfilehash: be10973510b053b30178a3c5b35a866f828bf927
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083360"
---
# <a name="create-chartpoints"></a><span data-ttu-id="2d875-103">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="2d875-103">Create ChartPoints</span></span>

> <span data-ttu-id="2d875-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2d875-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2d875-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2d875-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2d875-106">Use esta API para crear un objeto ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="2d875-106">Use this API to create a new ChartPoints.</span></span>
## <a name="permissions"></a><span data-ttu-id="2d875-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2d875-107">Permissions</span></span>
<span data-ttu-id="2d875-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2d875-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2d875-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d875-110">Permission type</span></span>      | <span data-ttu-id="2d875-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d875-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2d875-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d875-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2d875-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2d875-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2d875-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d875-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d875-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2d875-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2d875-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d875-116">Application</span></span> | <span data-ttu-id="2d875-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d875-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2d875-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d875-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points

```
## <a name="request-headers"></a><span data-ttu-id="2d875-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d875-119">Request headers</span></span>
| <span data-ttu-id="2d875-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2d875-120">Name</span></span>       | <span data-ttu-id="2d875-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d875-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2d875-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d875-122">Authorization</span></span>  | <span data-ttu-id="2d875-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d875-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2d875-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2d875-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="2d875-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2d875-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2d875-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d875-128">Request body</span></span>
<span data-ttu-id="2d875-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartPoints](../resources/chartpoint.md).</span><span class="sxs-lookup"><span data-stu-id="2d875-129">In the request body, supply a JSON representation of [ChartPoints](../resources/chartpoint.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="2d875-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d875-130">Response</span></span>

<span data-ttu-id="2d875-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ChartPoints](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d875-131">If successful, this method returns `201 Created` response code and [ChartPoints](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2d875-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d875-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2d875-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d875-133">Request</span></span>
<span data-ttu-id="2d875-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d875-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chartpoints_from_chartseries"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points
Content-type: application/json
Content-length: 3

{
}
```
<span data-ttu-id="2d875-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartPoints](../resources/chartpoint.md).</span><span class="sxs-lookup"><span data-stu-id="2d875-135">In the request body, supply a JSON representation of [ChartPoints](../resources/chartpoint.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="2d875-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d875-136">Response</span></span>
<span data-ttu-id="2d875-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d875-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartPoint"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 3

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ChartPoints",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->