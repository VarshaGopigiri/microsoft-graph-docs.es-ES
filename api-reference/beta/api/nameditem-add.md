---
title: Agregar un elemento con nombre
description: Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.
localization_priority: Normal
ms.openlocfilehash: 57ae84505327f2afbe2936b2671b655e76a85bd4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836704"
---
# <a name="add-named-item"></a><span data-ttu-id="6f275-103">Agregar un elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="6f275-103">Add Named Item</span></span>

> <span data-ttu-id="6f275-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6f275-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6f275-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6f275-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6f275-106">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="6f275-106">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="permissions"></a><span data-ttu-id="6f275-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f275-107">Permissions</span></span>
<span data-ttu-id="6f275-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6f275-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6f275-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f275-110">Permission type</span></span>      | <span data-ttu-id="6f275-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f275-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f275-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f275-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6f275-113">Files.ReadWrite, Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="6f275-113">Files.ReadWrite, Sites.Read.All</span></span>    |
|<span data-ttu-id="6f275-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f275-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f275-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6f275-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6f275-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f275-116">Application</span></span> | <span data-ttu-id="6f275-117">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="6f275-117">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f275-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f275-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="6f275-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f275-119">Request headers</span></span>
| <span data-ttu-id="6f275-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f275-120">Name</span></span>       | <span data-ttu-id="6f275-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f275-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6f275-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f275-122">Authorization</span></span>  | <span data-ttu-id="6f275-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f275-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6f275-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6f275-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="6f275-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6f275-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6f275-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f275-128">Request body</span></span>
<span data-ttu-id="6f275-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f275-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6f275-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6f275-130">Parameter</span></span>    | <span data-ttu-id="6f275-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f275-131">Type</span></span>   |<span data-ttu-id="6f275-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f275-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6f275-133">name</span><span class="sxs-lookup"><span data-stu-id="6f275-133">name</span></span>|<span data-ttu-id="6f275-134">string</span><span class="sxs-lookup"><span data-stu-id="6f275-134">string</span></span>|<span data-ttu-id="6f275-135">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="6f275-135">The name of the named item.</span></span>|
|<span data-ttu-id="6f275-136">reference</span><span class="sxs-lookup"><span data-stu-id="6f275-136">reference</span></span>|<span data-ttu-id="6f275-137">string</span><span class="sxs-lookup"><span data-stu-id="6f275-137">string</span></span>|<span data-ttu-id="6f275-138">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="6f275-138">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="6f275-139">comment</span><span class="sxs-lookup"><span data-stu-id="6f275-139">comment</span></span>|<span data-ttu-id="6f275-140">string</span><span class="sxs-lookup"><span data-stu-id="6f275-140">string</span></span>|<span data-ttu-id="6f275-141">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="6f275-141">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="6f275-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f275-142">Response</span></span>

<span data-ttu-id="6f275-143">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [NamedItem](../resources/nameditem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f275-143">If successful, this method returns `200 OK` response code and [NamedItem](../resources/nameditem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f275-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f275-144">Example</span></span>
<span data-ttu-id="6f275-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6f275-145">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="6f275-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f275-146">Request</span></span>
<span data-ttu-id="6f275-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f275-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "NamedItemcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names/add
Content-type: application/json
Content-length: 54

{
  "name": "test5",
  "reference": "=Sheet1!$F$15:$N$27",
  "comment": "Comment for the named item"
}


```

##### <a name="response"></a><span data-ttu-id="6f275-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f275-148">Response</span></span>
<span data-ttu-id="6f275-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f275-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "tocPath": ""
}-->
