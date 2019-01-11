---
title: 'TableCollection: add'
description: Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.
localization_priority: Normal
ms.openlocfilehash: 8053ce8e8d0ac62e096fa70255064e82a03630f6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868449"
---
# <a name="tablecollection-add"></a><span data-ttu-id="fc265-105">TableCollection: add</span><span class="sxs-lookup"><span data-stu-id="fc265-105">TableCollection: add</span></span>

> <span data-ttu-id="fc265-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc265-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc265-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc265-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc265-p103">Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="fc265-p103">Create a new table. The range source address determines the worksheet under which the table will be added. If the table cannot be added (e.g., because the address is invalid, or the table would overlap with another table), an error will be thrown.</span></span>

## <a name="error-handling"></a><span data-ttu-id="fc265-111">Control de errores</span><span class="sxs-lookup"><span data-stu-id="fc265-111">Error Handling</span></span>

<span data-ttu-id="fc265-112">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="fc265-112">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="fc265-113">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc265-113">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="fc265-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc265-114">Permissions</span></span>
<span data-ttu-id="fc265-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc265-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc265-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc265-117">Permission type</span></span>      | <span data-ttu-id="fc265-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc265-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fc265-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc265-119">Delegated (work or school account)</span></span> | <span data-ttu-id="fc265-120">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc265-120">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fc265-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc265-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc265-122">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc265-122">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fc265-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc265-123">Application</span></span> | <span data-ttu-id="fc265-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc265-124">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fc265-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc265-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/add
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="fc265-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc265-126">Request headers</span></span>
| <span data-ttu-id="fc265-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc265-127">Name</span></span>       | <span data-ttu-id="fc265-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc265-128">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fc265-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc265-129">Authorization</span></span>  | <span data-ttu-id="fc265-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc265-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fc265-132">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fc265-132">Workbook-Session-Id</span></span>  | <span data-ttu-id="fc265-p107">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc265-p107">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fc265-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc265-135">Request body</span></span>
<span data-ttu-id="fc265-136">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="fc265-136">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="fc265-137">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fc265-137">Parameter</span></span>    | <span data-ttu-id="fc265-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc265-138">Type</span></span>   |<span data-ttu-id="fc265-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc265-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fc265-140">address</span><span class="sxs-lookup"><span data-stu-id="fc265-140">address</span></span>|<span data-ttu-id="fc265-141">string</span><span class="sxs-lookup"><span data-stu-id="fc265-141">string</span></span>|<span data-ttu-id="fc265-p108">Dirección o nombre del objeto de intervalo que representa el origen de datos. Si la dirección no contiene un nombre de hoja, se usa la hoja activa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="fc265-p108">Address or name of the range object representing the data source. If the address does not contain a sheet name, the currently-active sheet is used.</span></span>|
|<span data-ttu-id="fc265-144">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="fc265-144">hasHeaders</span></span>|<span data-ttu-id="fc265-145">boolean</span><span class="sxs-lookup"><span data-stu-id="fc265-145">boolean</span></span>|<span data-ttu-id="fc265-p109">Valor booleano que indica si los datos que se están importando tienen etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará automáticamente el encabezado desplazando los datos una fila hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="fc265-p109">Boolean value that indicates whether the data being imported has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="fc265-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc265-149">Response</span></span>

<span data-ttu-id="fc265-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc265-150">If successful, this method returns `200 OK` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc265-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc265-151">Example</span></span>
<span data-ttu-id="fc265-152">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fc265-152">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fc265-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc265-153">Request</span></span>
<span data-ttu-id="fc265-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc265-154">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/add
Content-type: application/json
Content-length: 54

{
  "address": "Sheet1!A1:D5",
  "hasHeaders": true
}
```

##### <a name="response"></a><span data-ttu-id="fc265-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc265-155">Response</span></span>
<span data-ttu-id="fc265-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc265-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
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
