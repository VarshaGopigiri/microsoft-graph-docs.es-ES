---
title: 'Aplicación: calcular'
description: Recalcula todos los libros abiertos actualmente en Excel.
ms.openlocfilehash: 5d2d0d5603f70691d2c73548bd7a20acc03c340e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087720"
---
# <a name="application-calculate"></a><span data-ttu-id="9434f-103">Aplicación: calcular</span><span class="sxs-lookup"><span data-stu-id="9434f-103">Application: calculate</span></span>

> <span data-ttu-id="9434f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9434f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9434f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9434f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9434f-106">Recalcula todos los libros abiertos actualmente en Excel.</span><span class="sxs-lookup"><span data-stu-id="9434f-106">Recalculate all currently opened workbooks in Excel.</span></span>
## <a name="permissions"></a><span data-ttu-id="9434f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9434f-107">Permissions</span></span>
<span data-ttu-id="9434f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9434f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9434f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9434f-110">Permission type</span></span>      | <span data-ttu-id="9434f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9434f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9434f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9434f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9434f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9434f-113">Not supported.</span></span>    |
|<span data-ttu-id="9434f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9434f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9434f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9434f-115">Not supported.</span></span>    |
|<span data-ttu-id="9434f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9434f-116">Application</span></span> | <span data-ttu-id="9434f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9434f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9434f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9434f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/application/calculate

```
## <a name="request-headers"></a><span data-ttu-id="9434f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9434f-119">Request headers</span></span>
| <span data-ttu-id="9434f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9434f-120">Name</span></span>       | <span data-ttu-id="9434f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9434f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9434f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9434f-122">Authorization</span></span>  | <span data-ttu-id="9434f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9434f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9434f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9434f-125">Request body</span></span>
<span data-ttu-id="9434f-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9434f-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9434f-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9434f-127">Parameter</span></span>    | <span data-ttu-id="9434f-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="9434f-128">Type</span></span>   |<span data-ttu-id="9434f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="9434f-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9434f-130">calculationType</span><span class="sxs-lookup"><span data-stu-id="9434f-130">calculationType</span></span>|<span data-ttu-id="9434f-131">string</span><span class="sxs-lookup"><span data-stu-id="9434f-131">string</span></span>|<span data-ttu-id="9434f-132">Especifica el tipo de cálculo que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="9434f-132">Specifies the calculation type to use.</span></span>  <span data-ttu-id="9434f-133">Los valores posibles son: `Recalculate`, `Full` y `FullRebuild`.</span><span class="sxs-lookup"><span data-stu-id="9434f-133">Possible values are: `Recalculate`, `Full`, `FullRebuild`.</span></span>|

## <a name="response"></a><span data-ttu-id="9434f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9434f-134">Response</span></span>

<span data-ttu-id="9434f-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9434f-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9434f-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9434f-137">Example</span></span>
<span data-ttu-id="9434f-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9434f-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9434f-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9434f-139">Request</span></span>
<span data-ttu-id="9434f-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9434f-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="9434f-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9434f-141">Response</span></span>
<span data-ttu-id="9434f-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9434f-142">Here is an example of the response.</span></span> 
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