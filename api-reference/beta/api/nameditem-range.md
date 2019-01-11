---
title: 'NamedItem: Range'
description: Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.
localization_priority: Normal
ms.openlocfilehash: 0eb6081baca5c8def5d2e135151abee65a7825c5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851880"
---
# <a name="nameditem-range"></a><span data-ttu-id="b267b-104">NamedItem: Range</span><span class="sxs-lookup"><span data-stu-id="b267b-104">NamedItem: Range</span></span>

> <span data-ttu-id="b267b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b267b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b267b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b267b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b267b-p103">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="b267b-p103">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>
## <a name="permissions"></a><span data-ttu-id="b267b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b267b-109">Permissions</span></span>
<span data-ttu-id="b267b-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b267b-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b267b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b267b-112">Permission type</span></span>      | <span data-ttu-id="b267b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b267b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b267b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b267b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="b267b-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b267b-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b267b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b267b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b267b-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b267b-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b267b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b267b-118">Application</span></span> | <span data-ttu-id="b267b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b267b-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b267b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b267b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/Range

```
## <a name="request-headers"></a><span data-ttu-id="b267b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b267b-121">Request headers</span></span>
| <span data-ttu-id="b267b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b267b-122">Name</span></span>       | <span data-ttu-id="b267b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b267b-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b267b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b267b-124">Authorization</span></span>  | <span data-ttu-id="b267b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b267b-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b267b-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b267b-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="b267b-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b267b-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b267b-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b267b-130">Request body</span></span>

## <a name="response"></a><span data-ttu-id="b267b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b267b-131">Response</span></span>

<span data-ttu-id="b267b-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b267b-132">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b267b-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b267b-133">Example</span></span>
<span data-ttu-id="b267b-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b267b-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b267b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b267b-135">Request</span></span>
<span data-ttu-id="b267b-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b267b-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "nameditem_range"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/Range
```

##### <a name="response"></a><span data-ttu-id="b267b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b267b-137">Response</span></span>
<span data-ttu-id="b267b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b267b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
