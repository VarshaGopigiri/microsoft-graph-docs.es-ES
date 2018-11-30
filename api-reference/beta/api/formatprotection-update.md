---
title: Update formatprotection
description: Actualiza las propiedades del objeto formatprotection.
ms.openlocfilehash: 7a75af3b340b194df16a53dd7800d5d6981730ae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086631"
---
# <a name="update-formatprotection"></a><span data-ttu-id="04e7b-103">Update formatprotection</span><span class="sxs-lookup"><span data-stu-id="04e7b-103">Update formatprotection</span></span>

> <span data-ttu-id="04e7b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04e7b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04e7b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04e7b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="04e7b-106">Actualiza las propiedades del objeto formatprotection.</span><span class="sxs-lookup"><span data-stu-id="04e7b-106">Update the properties of formatprotection object.</span></span>
## <a name="permissions"></a><span data-ttu-id="04e7b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="04e7b-107">Permissions</span></span>
<span data-ttu-id="04e7b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="04e7b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04e7b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04e7b-110">Permission type</span></span>      | <span data-ttu-id="04e7b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04e7b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="04e7b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04e7b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="04e7b-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="04e7b-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="04e7b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04e7b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="04e7b-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="04e7b-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="04e7b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04e7b-116">Application</span></span> | <span data-ttu-id="04e7b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04e7b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="04e7b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04e7b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/protection
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/protection
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/protection
```
## <a name="optional-request-headers"></a><span data-ttu-id="04e7b-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="04e7b-119">Optional request headers</span></span>
| <span data-ttu-id="04e7b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="04e7b-120">Name</span></span>       | <span data-ttu-id="04e7b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="04e7b-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="04e7b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="04e7b-122">Authorization</span></span>  | <span data-ttu-id="04e7b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04e7b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="04e7b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04e7b-125">Request body</span></span>
<span data-ttu-id="04e7b-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="04e7b-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="04e7b-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04e7b-129">Property</span></span>     | <span data-ttu-id="04e7b-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="04e7b-130">Type</span></span>   |<span data-ttu-id="04e7b-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="04e7b-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="04e7b-132">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="04e7b-132">formulaHidden</span></span>|<span data-ttu-id="04e7b-133">boolean</span><span class="sxs-lookup"><span data-stu-id="04e7b-133">boolean</span></span>|<span data-ttu-id="04e7b-p105">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="04e7b-p105">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="04e7b-136">locked</span><span class="sxs-lookup"><span data-stu-id="04e7b-136">locked</span></span>|<span data-ttu-id="04e7b-137">boolean</span><span class="sxs-lookup"><span data-stu-id="04e7b-137">boolean</span></span>|<span data-ttu-id="04e7b-p106">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="04e7b-p106">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="response"></a><span data-ttu-id="04e7b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04e7b-140">Response</span></span>

<span data-ttu-id="04e7b-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [FormatProtection](../resources/formatprotection.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04e7b-141">If successful, this method returns a `200 OK` response code and updated [FormatProtection](../resources/formatprotection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="04e7b-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04e7b-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="04e7b-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04e7b-143">Request</span></span>
<span data-ttu-id="04e7b-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04e7b-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_formatprotection"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/format/protection
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```
##### <a name="response"></a><span data-ttu-id="04e7b-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04e7b-145">Response</span></span>
<span data-ttu-id="04e7b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04e7b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.formatProtection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update formatprotection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->