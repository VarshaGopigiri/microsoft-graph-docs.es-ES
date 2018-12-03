---
title: 'Range: merge'
description: Combinar las celdas del rango en una región de la hoja de cálculo.
ms.openlocfilehash: 8680afec198cebb820fc695cf7714494a2539cdc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087073"
---
# <a name="range-merge"></a><span data-ttu-id="6ecb6-103">Range: merge</span><span class="sxs-lookup"><span data-stu-id="6ecb6-103">Range: merge</span></span>

> <span data-ttu-id="6ecb6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6ecb6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6ecb6-106">Combinar las celdas del rango en una región de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-106">Merge the range cells into one region in the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="6ecb6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ecb6-107">Permissions</span></span>
<span data-ttu-id="6ecb6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ecb6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ecb6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ecb6-110">Permission type</span></span>      | <span data-ttu-id="6ecb6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ecb6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6ecb6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ecb6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6ecb6-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ecb6-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6ecb6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ecb6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ecb6-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ecb6-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6ecb6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ecb6-116">Application</span></span> | <span data-ttu-id="6ecb6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6ecb6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ecb6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/merge
POST /workbook/worksheets/{id|name}/range(address='<address>')/merge
POST /workbook/tables/{id|name}/columns/{id|name}/range/merge

```
## <a name="request-headers"></a><span data-ttu-id="6ecb6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ecb6-119">Request headers</span></span>
| <span data-ttu-id="6ecb6-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ecb6-120">Name</span></span>       | <span data-ttu-id="6ecb6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ecb6-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6ecb6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ecb6-122">Authorization</span></span>  | <span data-ttu-id="6ecb6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6ecb6-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6ecb6-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="6ecb6-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ecb6-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ecb6-128">Request body</span></span>
<span data-ttu-id="6ecb6-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6ecb6-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6ecb6-130">Parameter</span></span>    | <span data-ttu-id="6ecb6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ecb6-131">Type</span></span>   |<span data-ttu-id="6ecb6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ecb6-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6ecb6-133">across</span><span class="sxs-lookup"><span data-stu-id="6ecb6-133">across</span></span>|<span data-ttu-id="6ecb6-134">boolean</span><span class="sxs-lookup"><span data-stu-id="6ecb6-134">boolean</span></span>|<span data-ttu-id="6ecb6-p105">Opcional. Verdadero para que se combinen las celdas de cada fila del rango especificado como celdas combinadas distintas. El valor predeterminado es falso.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-p105">Optional. Set true to merge cells in each row of the specified range as separate merged cells. The default value is false.</span></span>|

## <a name="response"></a><span data-ttu-id="6ecb6-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ecb6-138">Response</span></span>

<span data-ttu-id="6ecb6-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ecb6-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ecb6-141">Example</span></span>
<span data-ttu-id="6ecb6-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6ecb6-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ecb6-143">Request</span></span>
<span data-ttu-id="6ecb6-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_merge"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/merge
Content-type: application/json
Content-length: 20

{
  "across": true
}
```

##### <a name="response"></a><span data-ttu-id="6ecb6-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ecb6-145">Response</span></span>
<span data-ttu-id="6ecb6-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ecb6-146">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: merge",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->