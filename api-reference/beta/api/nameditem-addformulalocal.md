---
title: 'Agregar FormulaLocal del elemento con nombre '
description: Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.
localization_priority: Normal
ms.openlocfilehash: 064bc4a6e8183b58242522dfe663d2585eed09b5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859573"
---
# <a name="add-named-item-formulalocal"></a><span data-ttu-id="d4722-103">Agregar FormulaLocal del elemento con nombre </span><span class="sxs-lookup"><span data-stu-id="d4722-103">Add Named Item FormulaLocal</span></span>
<span data-ttu-id="d4722-104">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="d4722-104">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="permissions"></a><span data-ttu-id="d4722-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d4722-105">Permissions</span></span>
<span data-ttu-id="d4722-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4722-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4722-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4722-108">Permission type</span></span>      | <span data-ttu-id="d4722-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4722-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d4722-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4722-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d4722-111">Files.ReadWrite, Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="d4722-111">Files.ReadWrite, Sites.Read.All</span></span>    |
|<span data-ttu-id="d4722-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4722-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d4722-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4722-113">Not supported.</span></span>    |
|<span data-ttu-id="d4722-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4722-114">Application</span></span> | <span data-ttu-id="d4722-115">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="d4722-115">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d4722-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4722-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="d4722-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4722-117">Request headers</span></span>
| <span data-ttu-id="d4722-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d4722-118">Name</span></span>       | <span data-ttu-id="d4722-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4722-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d4722-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d4722-120">Authorization</span></span>  | <span data-ttu-id="d4722-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d4722-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d4722-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d4722-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="d4722-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d4722-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d4722-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4722-126">Request body</span></span>
<span data-ttu-id="d4722-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d4722-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d4722-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d4722-128">Parameter</span></span>    | <span data-ttu-id="d4722-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4722-129">Type</span></span>   |<span data-ttu-id="d4722-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4722-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4722-131">name</span><span class="sxs-lookup"><span data-stu-id="d4722-131">name</span></span>|<span data-ttu-id="d4722-132">string</span><span class="sxs-lookup"><span data-stu-id="d4722-132">string</span></span>|<span data-ttu-id="d4722-133">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="d4722-133">The name of the named item.</span></span>|
|<span data-ttu-id="d4722-134">formula</span><span class="sxs-lookup"><span data-stu-id="d4722-134">formula</span></span>|<span data-ttu-id="d4722-135">string</span><span class="sxs-lookup"><span data-stu-id="d4722-135">string</span></span>|<span data-ttu-id="d4722-136">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="d4722-136">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="d4722-137">comment</span><span class="sxs-lookup"><span data-stu-id="d4722-137">comment</span></span>|<span data-ttu-id="d4722-138">string</span><span class="sxs-lookup"><span data-stu-id="d4722-138">string</span></span>|<span data-ttu-id="d4722-139">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="d4722-139">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="d4722-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4722-140">Response</span></span>

<span data-ttu-id="d4722-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [NamedItem](../resources/nameditem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4722-141">If successful, this method returns `200 OK` response code and [NamedItem](../resources/nameditem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4722-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4722-142">Example</span></span>
<span data-ttu-id="d4722-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d4722-143">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="d4722-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4722-144">Request</span></span>
<span data-ttu-id="d4722-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4722-145">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "NamedItemcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names/addFormulaLocal
Content-type: application/json
Content-length: 54

{
  "name": "test7",
  "formula": "=SUM(Sheet2!$A$1+Sheet2!$A$2)",
  "comment": "Comment for the named item"
}
```

##### <a name="response"></a><span data-ttu-id="d4722-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4722-146">Response</span></span>
<span data-ttu-id="d4722-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4722-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.namedItem"
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
