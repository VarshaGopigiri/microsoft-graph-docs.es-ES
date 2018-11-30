---
title: Update nameditem
description: Actualizar las propiedades del objeto nameditem.
ms.openlocfilehash: 2b298cfe567903e7f470b78021efc34bb379ba35
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084153"
---
# <a name="update-nameditem"></a><span data-ttu-id="801fa-103">Update nameditem</span><span class="sxs-lookup"><span data-stu-id="801fa-103">Update nameditem</span></span>

> <span data-ttu-id="801fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="801fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="801fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="801fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="801fa-106">Actualizar las propiedades del objeto nameditem.</span><span class="sxs-lookup"><span data-stu-id="801fa-106">Update the properties of nameditem object.</span></span>
## <a name="permissions"></a><span data-ttu-id="801fa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="801fa-107">Permissions</span></span>
<span data-ttu-id="801fa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="801fa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="801fa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="801fa-110">Permission type</span></span>      | <span data-ttu-id="801fa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="801fa-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="801fa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="801fa-112">Delegated (work or school account)</span></span> | <span data-ttu-id="801fa-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="801fa-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="801fa-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="801fa-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="801fa-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="801fa-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="801fa-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="801fa-116">Application</span></span> | <span data-ttu-id="801fa-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="801fa-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="801fa-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="801fa-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="801fa-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="801fa-119">Optional request headers</span></span>
| <span data-ttu-id="801fa-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="801fa-120">Name</span></span>       | <span data-ttu-id="801fa-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="801fa-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="801fa-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="801fa-122">Authorization</span></span>  | <span data-ttu-id="801fa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="801fa-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="801fa-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="801fa-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="801fa-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="801fa-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="801fa-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="801fa-128">Request body</span></span>
<span data-ttu-id="801fa-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="801fa-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="801fa-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="801fa-132">Property</span></span>     | <span data-ttu-id="801fa-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="801fa-133">Type</span></span>   |<span data-ttu-id="801fa-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="801fa-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="801fa-135">visible</span><span class="sxs-lookup"><span data-stu-id="801fa-135">visible</span></span>|<span data-ttu-id="801fa-136">boolean</span><span class="sxs-lookup"><span data-stu-id="801fa-136">boolean</span></span>|<span data-ttu-id="801fa-137">Especifica si el objeto está visible o no.</span><span class="sxs-lookup"><span data-stu-id="801fa-137">Specifies whether the object is visible or not.</span></span>|
|<span data-ttu-id="801fa-138">comment</span><span class="sxs-lookup"><span data-stu-id="801fa-138">comment</span></span>|   <span data-ttu-id="801fa-139">string</span><span class="sxs-lookup"><span data-stu-id="801fa-139">string</span></span>  |<span data-ttu-id="801fa-140">Representa el comentario asociado a este nombre.</span><span class="sxs-lookup"><span data-stu-id="801fa-140">Represents the comment associated with this name.</span></span>|

## <a name="response"></a><span data-ttu-id="801fa-141">Response</span><span class="sxs-lookup"><span data-stu-id="801fa-141">Response</span></span>

<span data-ttu-id="801fa-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [NamedItem](../resources/nameditem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="801fa-142">If successful, this method returns a `200 OK` response code and updated [NamedItem](../resources/nameditem.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="801fa-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="801fa-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="801fa-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="801fa-144">Request</span></span>
<span data-ttu-id="801fa-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="801fa-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_nameditem"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)
Content-type: application/json
Content-length: 87

{
  "type": "type-value",
  "scope": "scope-value",
  "comment": "comment-value",
  "value": {
  },
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="801fa-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="801fa-146">Response</span></span>
<span data-ttu-id="801fa-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="801fa-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.namedItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 87

{
  "name": "name-value",
  "type": "type-value",
  "value": {
  },
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update nameditem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->