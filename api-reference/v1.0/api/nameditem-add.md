---
title: Agregar un elemento con nombre
description: Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.
localization_priority: Normal
ms.openlocfilehash: eab6116768523d021577bef345151c3e62681fe5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852615"
---
# <a name="add-named-item"></a><span data-ttu-id="4b2cf-103">Agregar un elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="4b2cf-103">Add Named Item</span></span>

<span data-ttu-id="4b2cf-104">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-104">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="permissions"></a><span data-ttu-id="4b2cf-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4b2cf-105">Permissions</span></span>
<span data-ttu-id="4b2cf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4b2cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4b2cf-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4b2cf-108">Permission type</span></span>      | <span data-ttu-id="4b2cf-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4b2cf-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4b2cf-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4b2cf-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4b2cf-111">Files.ReadWrite, Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="4b2cf-111">Files.ReadWrite, Sites.Read.All</span></span>    |
|<span data-ttu-id="4b2cf-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4b2cf-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4b2cf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-113">Not supported.</span></span>    |
|<span data-ttu-id="4b2cf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4b2cf-114">Application</span></span> | <span data-ttu-id="4b2cf-115">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="4b2cf-115">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4b2cf-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4b2cf-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="4b2cf-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4b2cf-117">Request headers</span></span>
| <span data-ttu-id="4b2cf-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b2cf-118">Name</span></span>       | <span data-ttu-id="4b2cf-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b2cf-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4b2cf-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4b2cf-120">Authorization</span></span>  | <span data-ttu-id="4b2cf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4b2cf-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4b2cf-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="4b2cf-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4b2cf-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4b2cf-126">Request body</span></span>
<span data-ttu-id="4b2cf-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4b2cf-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4b2cf-128">Parameter</span></span>    | <span data-ttu-id="4b2cf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b2cf-129">Type</span></span>   |<span data-ttu-id="4b2cf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b2cf-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4b2cf-131">name</span><span class="sxs-lookup"><span data-stu-id="4b2cf-131">name</span></span>|<span data-ttu-id="4b2cf-132">string</span><span class="sxs-lookup"><span data-stu-id="4b2cf-132">string</span></span>|<span data-ttu-id="4b2cf-133">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-133">The name of the named item.</span></span>|
|<span data-ttu-id="4b2cf-134">reference</span><span class="sxs-lookup"><span data-stu-id="4b2cf-134">reference</span></span>|<span data-ttu-id="4b2cf-135">Json</span><span class="sxs-lookup"><span data-stu-id="4b2cf-135">Json</span></span>|<span data-ttu-id="4b2cf-136">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-136">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="4b2cf-137">comment</span><span class="sxs-lookup"><span data-stu-id="4b2cf-137">comment</span></span>|<span data-ttu-id="4b2cf-138">string</span><span class="sxs-lookup"><span data-stu-id="4b2cf-138">string</span></span>|<span data-ttu-id="4b2cf-139">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="4b2cf-139">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="4b2cf-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b2cf-140">Response</span></span>

<span data-ttu-id="4b2cf-141">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookNamedItem](../resources/nameditem.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-141">If successful, this method returns `200 OK` response code and [WorkbookNamedItem](../resources/nameditem.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="4b2cf-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b2cf-142">Example</span></span>
<span data-ttu-id="4b2cf-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-143">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="4b2cf-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4b2cf-144">Request</span></span>
<span data-ttu-id="4b2cf-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "NamedItemcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/add
Content-type: application/json
Content-length: 54

{
  "name": "test5",
  "reference": "=Sheet1!$F$15:$N$27",
  "comment": "Comment for the named item"
}


```

##### <a name="response"></a><span data-ttu-id="4b2cf-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b2cf-146">Response</span></span>
<span data-ttu-id="4b2cf-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4b2cf-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.id": "/users('ca41eb6e-5828-486b-ab52-c3bd1f7a4047')/drive/root/workbook/names(%27test5%27)",
    "comment": "Comment for the named item",
    "name": "test5",
    "scope": "Workbook",
    "type": "Range",
    "value": "Sheet1!$F$15:$N$27",
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
  "suppressions": [
    "Warning: NamedItemcollection_add/value:
      Schemas type was 'Custom' which is not supported. Add a resource type to the definition of property: value"
  ],
  "tocPath": ""
}-->
