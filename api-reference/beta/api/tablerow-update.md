---
title: Update tablerow
description: Actualizar las propiedades del objeto tablerow.
ms.openlocfilehash: ebace32ef7eaa841326e94aaf1b991a88212bd9a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086320"
---
# <a name="update-tablerow"></a><span data-ttu-id="4f822-103">Update tablerow</span><span class="sxs-lookup"><span data-stu-id="4f822-103">Update tablerow</span></span>

> <span data-ttu-id="4f822-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4f822-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4f822-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4f822-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4f822-106">Actualizar las propiedades del objeto tablerow.</span><span class="sxs-lookup"><span data-stu-id="4f822-106">Update the properties of tablerow object.</span></span>
## <a name="permissions"></a><span data-ttu-id="4f822-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4f822-107">Permissions</span></span>
<span data-ttu-id="4f822-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4f822-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4f822-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f822-110">Permission type</span></span>      | <span data-ttu-id="4f822-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f822-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f822-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f822-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4f822-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4f822-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4f822-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f822-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f822-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4f822-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4f822-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f822-116">Application</span></span> | <span data-ttu-id="4f822-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f822-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f822-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f822-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/rows(<index>)
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/rows(<index>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="4f822-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="4f822-119">Optional request headers</span></span>
| <span data-ttu-id="4f822-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f822-120">Name</span></span>       | <span data-ttu-id="4f822-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f822-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="4f822-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f822-122">Authorization</span></span>  | <span data-ttu-id="4f822-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f822-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4f822-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4f822-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="4f822-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4f822-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4f822-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f822-128">Request body</span></span>
<span data-ttu-id="4f822-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="4f822-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="4f822-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4f822-132">Property</span></span>     | <span data-ttu-id="4f822-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f822-133">Type</span></span>   |<span data-ttu-id="4f822-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f822-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4f822-135">values</span><span class="sxs-lookup"><span data-stu-id="4f822-135">values</span></span>|<span data-ttu-id="4f822-136">json</span><span class="sxs-lookup"><span data-stu-id="4f822-136">json</span></span>|<span data-ttu-id="4f822-p106">Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="4f822-p106">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="4f822-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f822-140">Response</span></span>

<span data-ttu-id="4f822-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableRow](../resources/tablerow.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f822-141">If successful, this method returns a `200 OK` response code and updated [TableRow](../resources/tablerow.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4f822-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f822-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4f822-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f822-143">Request</span></span>
<span data-ttu-id="4f822-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f822-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_tablerow"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/rows(<index>)
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```
##### <a name="response"></a><span data-ttu-id="4f822-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f822-145">Response</span></span>
<span data-ttu-id="4f822-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f822-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tablerow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->