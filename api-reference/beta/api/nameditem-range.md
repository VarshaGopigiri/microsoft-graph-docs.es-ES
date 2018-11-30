---
title: 'NamedItem: Range'
description: Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.
ms.openlocfilehash: fe466d83c9b24c119d9e80f1ec7320f0aa001e5a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090293"
---
# <a name="nameditem-range"></a><span data-ttu-id="19525-104">NamedItem: Range</span><span class="sxs-lookup"><span data-stu-id="19525-104">NamedItem: Range</span></span>

> <span data-ttu-id="19525-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19525-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19525-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19525-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="19525-p103">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="19525-p103">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>
## <a name="permissions"></a><span data-ttu-id="19525-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="19525-109">Permissions</span></span>
<span data-ttu-id="19525-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="19525-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="19525-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19525-112">Permission type</span></span>      | <span data-ttu-id="19525-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19525-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="19525-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19525-114">Delegated (work or school account)</span></span> | <span data-ttu-id="19525-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19525-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="19525-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19525-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="19525-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19525-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="19525-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19525-118">Application</span></span> | <span data-ttu-id="19525-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19525-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="19525-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19525-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/Range

```
## <a name="request-headers"></a><span data-ttu-id="19525-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19525-121">Request headers</span></span>
| <span data-ttu-id="19525-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="19525-122">Name</span></span>       | <span data-ttu-id="19525-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="19525-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="19525-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="19525-124">Authorization</span></span>  | <span data-ttu-id="19525-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19525-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="19525-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="19525-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="19525-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="19525-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="19525-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19525-130">Request body</span></span>

## <a name="response"></a><span data-ttu-id="19525-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19525-131">Response</span></span>

<span data-ttu-id="19525-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19525-132">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="19525-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19525-133">Example</span></span>
<span data-ttu-id="19525-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="19525-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="19525-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19525-135">Request</span></span>
<span data-ttu-id="19525-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19525-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "nameditem_range"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/Range
```

##### <a name="response"></a><span data-ttu-id="19525-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19525-137">Response</span></span>
<span data-ttu-id="19525-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19525-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->