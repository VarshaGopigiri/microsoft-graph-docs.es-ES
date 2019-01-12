---
title: 'TableCollection: add'
description: Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 4b2523725c65f0b09e6f91296eacfcb9c75e2927
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919732"
---
# <a name="tablecollection-add"></a><span data-ttu-id="0e134-105">TableCollection: add</span><span class="sxs-lookup"><span data-stu-id="0e134-105">TableCollection: add</span></span>

<span data-ttu-id="0e134-p102">Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="0e134-p102">Create a new table. The range source address determines the worksheet under which the table will be added. If the table cannot be added (e.g., because the address is invalid, or the table would overlap with another table), an error will be thrown.</span></span>

## <a name="error-handling"></a><span data-ttu-id="0e134-109">Control de errores</span><span class="sxs-lookup"><span data-stu-id="0e134-109">Error Handling</span></span>

<span data-ttu-id="0e134-110">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="0e134-110">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="0e134-111">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e134-111">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e134-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e134-112">Permissions</span></span>
<span data-ttu-id="0e134-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e134-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e134-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e134-115">Permission type</span></span>      | <span data-ttu-id="0e134-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e134-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e134-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e134-117">Delegated (work or school account)</span></span> | <span data-ttu-id="0e134-118">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0e134-118">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0e134-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e134-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0e134-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e134-120">Not supported.</span></span>    |
|<span data-ttu-id="0e134-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e134-121">Application</span></span> | <span data-ttu-id="0e134-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e134-122">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0e134-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e134-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/add
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="0e134-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e134-124">Request headers</span></span>
| <span data-ttu-id="0e134-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e134-125">Name</span></span>       | <span data-ttu-id="0e134-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e134-126">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0e134-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e134-127">Authorization</span></span>  | <span data-ttu-id="0e134-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e134-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0e134-130">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0e134-130">Workbook-Session-Id</span></span>  | <span data-ttu-id="0e134-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0e134-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e134-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e134-133">Request body</span></span>
<span data-ttu-id="0e134-134">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0e134-134">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0e134-135">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0e134-135">Parameter</span></span>    | <span data-ttu-id="0e134-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e134-136">Type</span></span>   |<span data-ttu-id="0e134-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e134-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0e134-138">address</span><span class="sxs-lookup"><span data-stu-id="0e134-138">address</span></span>|<span data-ttu-id="0e134-139">string</span><span class="sxs-lookup"><span data-stu-id="0e134-139">string</span></span>|<span data-ttu-id="0e134-p107">Dirección o nombre del objeto de intervalo que representa el origen de datos. Si la dirección no contiene un nombre de hoja, se usa la hoja activa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="0e134-p107">Address or name of the range object representing the data source. If the address does not contain a sheet name, the currently-active sheet is used.</span></span>|
|<span data-ttu-id="0e134-142">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="0e134-142">hasHeaders</span></span>|<span data-ttu-id="0e134-143">boolean</span><span class="sxs-lookup"><span data-stu-id="0e134-143">boolean</span></span>|<span data-ttu-id="0e134-p108">Valor booleano que indica si los datos que se están importando tienen etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará automáticamente el encabezado desplazando los datos una fila hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="0e134-p108">Boolean value that indicates whether the data being imported has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="0e134-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e134-147">Response</span></span>

<span data-ttu-id="0e134-148">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookTable](../resources/table.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e134-148">If successful, this method returns `200 OK` response code and [WorkbookTable](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e134-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e134-149">Example</span></span>
<span data-ttu-id="0e134-150">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0e134-150">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0e134-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e134-151">Request</span></span>
<span data-ttu-id="0e134-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e134-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/add
Content-type: application/json
Content-length: 54

{
  "address": "Sheet1!A1:D5",
  "hasHeaders": true
}
```

##### <a name="response"></a><span data-ttu-id="0e134-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e134-153">Response</span></span>
<span data-ttu-id="0e134-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e134-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTable"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
