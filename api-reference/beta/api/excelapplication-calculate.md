---
title: 'Aplicación: calcular'
description: Recalcula todos los libros abiertos actualmente en Excel.
localization_priority: Normal
ms.openlocfilehash: 3d80fc89c002d7c89fcc5d68920895b9b1fe1c4e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818336"
---
# <a name="application-calculate"></a><span data-ttu-id="e1f17-103">Aplicación: calcular</span><span class="sxs-lookup"><span data-stu-id="e1f17-103">Application: calculate</span></span>

> <span data-ttu-id="e1f17-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e1f17-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e1f17-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e1f17-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e1f17-106">Recalcula todos los libros abiertos actualmente en Excel.</span><span class="sxs-lookup"><span data-stu-id="e1f17-106">Recalculate all currently opened workbooks in Excel.</span></span>
## <a name="permissions"></a><span data-ttu-id="e1f17-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1f17-107">Permissions</span></span>
<span data-ttu-id="e1f17-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1f17-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1f17-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1f17-110">Permission type</span></span>      | <span data-ttu-id="e1f17-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1f17-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1f17-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1f17-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e1f17-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1f17-113">Not supported.</span></span>    |
|<span data-ttu-id="e1f17-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1f17-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1f17-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1f17-115">Not supported.</span></span>    |
|<span data-ttu-id="e1f17-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1f17-116">Application</span></span> | <span data-ttu-id="e1f17-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1f17-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1f17-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1f17-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/application/calculate

```
## <a name="request-headers"></a><span data-ttu-id="e1f17-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1f17-119">Request headers</span></span>
| <span data-ttu-id="e1f17-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1f17-120">Name</span></span>       | <span data-ttu-id="e1f17-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1f17-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e1f17-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1f17-122">Authorization</span></span>  | <span data-ttu-id="e1f17-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1f17-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1f17-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1f17-125">Request body</span></span>
<span data-ttu-id="e1f17-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e1f17-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e1f17-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e1f17-127">Parameter</span></span>    | <span data-ttu-id="e1f17-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1f17-128">Type</span></span>   |<span data-ttu-id="e1f17-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1f17-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e1f17-130">calculationType</span><span class="sxs-lookup"><span data-stu-id="e1f17-130">calculationType</span></span>|<span data-ttu-id="e1f17-131">string</span><span class="sxs-lookup"><span data-stu-id="e1f17-131">string</span></span>|<span data-ttu-id="e1f17-132">Especifica el tipo de cálculo que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="e1f17-132">Specifies the calculation type to use.</span></span>  <span data-ttu-id="e1f17-133">Los valores posibles son: `Recalculate`, `Full` y `FullRebuild`.</span><span class="sxs-lookup"><span data-stu-id="e1f17-133">Possible values are: `Recalculate`, `Full`, `FullRebuild`.</span></span>|

## <a name="response"></a><span data-ttu-id="e1f17-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1f17-134">Response</span></span>

<span data-ttu-id="e1f17-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1f17-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1f17-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1f17-137">Example</span></span>
<span data-ttu-id="e1f17-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e1f17-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e1f17-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1f17-139">Request</span></span>
<span data-ttu-id="e1f17-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1f17-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="e1f17-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1f17-141">Response</span></span>
<span data-ttu-id="e1f17-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1f17-142">Here is an example of the response.</span></span> 
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
