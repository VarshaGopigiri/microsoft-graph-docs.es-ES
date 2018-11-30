---
title: 'Agregar FormulaLocal del elemento con nombre '
description: Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.
ms.openlocfilehash: 5e4279447143e1b004d468bdcaa9f7b4c2bf8c8d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031408"
---
# <a name="add-named-item-formulalocal"></a><span data-ttu-id="41231-103">Agregar FormulaLocal del elemento con nombre </span><span class="sxs-lookup"><span data-stu-id="41231-103">Add Named Item FormulaLocal</span></span>
<span data-ttu-id="41231-104">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="41231-104">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="permissions"></a><span data-ttu-id="41231-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="41231-105">Permissions</span></span>
<span data-ttu-id="41231-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41231-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41231-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41231-108">Permission type</span></span>      | <span data-ttu-id="41231-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41231-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="41231-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41231-110">Delegated (work or school account)</span></span> | <span data-ttu-id="41231-111">Files.ReadWrite, Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="41231-111">Files.ReadWrite, Sites.Read.All</span></span>    |
|<span data-ttu-id="41231-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41231-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41231-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41231-113">Not supported.</span></span>    |
|<span data-ttu-id="41231-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41231-114">Application</span></span> | <span data-ttu-id="41231-115">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="41231-115">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="41231-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41231-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="41231-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41231-117">Request headers</span></span>
| <span data-ttu-id="41231-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="41231-118">Name</span></span>       | <span data-ttu-id="41231-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="41231-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="41231-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="41231-120">Authorization</span></span>  | <span data-ttu-id="41231-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="41231-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="41231-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="41231-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="41231-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="41231-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="41231-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41231-126">Request body</span></span>
<span data-ttu-id="41231-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="41231-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="41231-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="41231-128">Parameter</span></span>    | <span data-ttu-id="41231-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="41231-129">Type</span></span>   |<span data-ttu-id="41231-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="41231-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="41231-131">name</span><span class="sxs-lookup"><span data-stu-id="41231-131">name</span></span>|<span data-ttu-id="41231-132">string</span><span class="sxs-lookup"><span data-stu-id="41231-132">string</span></span>|<span data-ttu-id="41231-133">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="41231-133">The name of the named item.</span></span>|
|<span data-ttu-id="41231-134">formula</span><span class="sxs-lookup"><span data-stu-id="41231-134">formula</span></span>|<span data-ttu-id="41231-135">string</span><span class="sxs-lookup"><span data-stu-id="41231-135">string</span></span>|<span data-ttu-id="41231-136">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="41231-136">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="41231-137">comment</span><span class="sxs-lookup"><span data-stu-id="41231-137">comment</span></span>|<span data-ttu-id="41231-138">string</span><span class="sxs-lookup"><span data-stu-id="41231-138">string</span></span>|<span data-ttu-id="41231-139">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="41231-139">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="41231-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41231-140">Response</span></span>

<span data-ttu-id="41231-141">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookNamedItem](../resources/nameditem.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41231-141">If successful, this method returns `200 OK` response code and [WorkbookNamedItem](../resources/nameditem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41231-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41231-142">Example</span></span>
<span data-ttu-id="41231-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="41231-143">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="41231-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41231-144">Request</span></span>
<span data-ttu-id="41231-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41231-145">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "NamedItemcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/addFormulaLocal
Content-type: application/json
Content-length: 54

{
  "name": "test7",
  "formula": "=SUM(Sheet2!$A$1+Sheet2!$A$2)",
  "comment": "Comment for the named item"
}
```

##### <a name="response"></a><span data-ttu-id="41231-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41231-146">Response</span></span>
<span data-ttu-id="41231-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41231-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookNamedItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 109

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#workbookNamedItem",
    "@odata.type": "#microsoft.graph.workbookNamedItem",
    "@odata.id": "/users('ca41eb6e-5828-486b-ab52-c3bd1f7a4047')/drive/root/workbook/names(%27test7%27)",
    "comment": "Comment for the named item",
    "name": "test7",
    "scope": "Workbook",
    "type": "String",
    "value": "0",
    "visible": true
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItemCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
