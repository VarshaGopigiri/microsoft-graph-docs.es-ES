---
title: 'Aplicación: calcular'
description: Recalcula todos los libros abiertos actualmente en Excel.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: b5db5efda5da15d006188ae55f45b85e1325c38e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921944"
---
# <a name="application-calculate"></a><span data-ttu-id="d9544-103">Aplicación: calcular</span><span class="sxs-lookup"><span data-stu-id="d9544-103">Application: calculate</span></span>

> <span data-ttu-id="d9544-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9544-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9544-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9544-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d9544-106">Recalcula todos los libros abiertos actualmente en Excel.</span><span class="sxs-lookup"><span data-stu-id="d9544-106">Recalculate all currently opened workbooks in Excel.</span></span>
## <a name="permissions"></a><span data-ttu-id="d9544-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9544-107">Permissions</span></span>
<span data-ttu-id="d9544-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9544-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d9544-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d9544-110">Permission type</span></span>      | <span data-ttu-id="d9544-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d9544-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d9544-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9544-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d9544-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9544-113">Not supported.</span></span>    |
|<span data-ttu-id="d9544-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9544-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9544-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9544-115">Not supported.</span></span>    |
|<span data-ttu-id="d9544-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9544-116">Application</span></span> | <span data-ttu-id="d9544-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9544-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9544-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9544-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/application/calculate

```
## <a name="request-headers"></a><span data-ttu-id="d9544-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9544-119">Request headers</span></span>
| <span data-ttu-id="d9544-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9544-120">Name</span></span>       | <span data-ttu-id="d9544-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9544-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d9544-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9544-122">Authorization</span></span>  | <span data-ttu-id="d9544-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9544-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d9544-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9544-125">Request body</span></span>
<span data-ttu-id="d9544-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9544-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d9544-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d9544-127">Parameter</span></span>    | <span data-ttu-id="d9544-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9544-128">Type</span></span>   |<span data-ttu-id="d9544-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9544-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9544-130">calculationType</span><span class="sxs-lookup"><span data-stu-id="d9544-130">calculationType</span></span>|<span data-ttu-id="d9544-131">string</span><span class="sxs-lookup"><span data-stu-id="d9544-131">string</span></span>|<span data-ttu-id="d9544-132">Especifica el tipo de cálculo que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="d9544-132">Specifies the calculation type to use.</span></span>  <span data-ttu-id="d9544-133">Los valores posibles son: `Recalculate`, `Full` y `FullRebuild`.</span><span class="sxs-lookup"><span data-stu-id="d9544-133">Possible values are: `Recalculate`, `Full`, `FullRebuild`.</span></span>|

## <a name="response"></a><span data-ttu-id="d9544-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9544-134">Response</span></span>

<span data-ttu-id="d9544-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9544-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9544-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9544-137">Example</span></span>
<span data-ttu-id="d9544-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d9544-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d9544-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9544-139">Request</span></span>
<span data-ttu-id="d9544-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9544-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "application_calculate"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/application/calculate
Content-type: application/json
Content-length: 48

{
  "calculationType": "calculationType-value"
}
```

##### <a name="response"></a><span data-ttu-id="d9544-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9544-141">Response</span></span>
<span data-ttu-id="d9544-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9544-142">Here is an example of the response.</span></span> 
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
  "description": "Application: calculate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
