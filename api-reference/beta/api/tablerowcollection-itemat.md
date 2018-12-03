---
title: 'TableRowCollection: ItemAt'
description: Obtiene una fila en función de su posición en la colección.
ms.openlocfilehash: 57eccf8f1e21f615759ab5c6b482c73196eab268
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084140"
---
# <a name="tablerowcollection-itemat"></a><span data-ttu-id="d705b-103">TableRowCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="d705b-103">TableRowCollection: ItemAt</span></span>

> <span data-ttu-id="d705b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d705b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d705b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d705b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d705b-106">Obtiene una fila en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="d705b-106">Gets a row based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="d705b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d705b-107">Permissions</span></span>
<span data-ttu-id="d705b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d705b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d705b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d705b-110">Permission type</span></span>      | <span data-ttu-id="d705b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d705b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d705b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d705b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d705b-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d705b-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d705b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d705b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d705b-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d705b-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d705b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d705b-116">Application</span></span> | <span data-ttu-id="d705b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d705b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d705b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d705b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/ItemAt
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="d705b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d705b-119">Request headers</span></span>
| <span data-ttu-id="d705b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d705b-120">Name</span></span>       | <span data-ttu-id="d705b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d705b-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d705b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d705b-122">Authorization</span></span>  | <span data-ttu-id="d705b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d705b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d705b-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d705b-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="d705b-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d705b-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d705b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d705b-128">Request body</span></span>
<span data-ttu-id="d705b-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d705b-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d705b-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d705b-130">Parameter</span></span>    | <span data-ttu-id="d705b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d705b-131">Type</span></span>   |<span data-ttu-id="d705b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d705b-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d705b-133">index</span><span class="sxs-lookup"><span data-stu-id="d705b-133">index</span></span>|<span data-ttu-id="d705b-134">number</span><span class="sxs-lookup"><span data-stu-id="d705b-134">number</span></span>|<span data-ttu-id="d705b-p105">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="d705b-p105">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="d705b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d705b-137">Response</span></span>

<span data-ttu-id="d705b-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d705b-138">If successful, this method returns `200 OK` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d705b-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d705b-139">Example</span></span>
<span data-ttu-id="d705b-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d705b-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d705b-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d705b-141">Request</span></span>
<span data-ttu-id="d705b-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d705b-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/rows/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="d705b-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d705b-143">Response</span></span>
<span data-ttu-id="d705b-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d705b-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableRowCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->