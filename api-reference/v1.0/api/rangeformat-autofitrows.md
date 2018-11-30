---
title: 'RangeFormat: autofitRows'
description: Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).
ms.openlocfilehash: 8aa8f47f1bea169cf8d72d386ced207953f08f2c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032674"
---
# <a name="rangeformat-autofitrows"></a><span data-ttu-id="0ba53-103">RangeFormat: autofitRows</span><span class="sxs-lookup"><span data-stu-id="0ba53-103">RangeFormat: autofitRows</span></span>

<span data-ttu-id="0ba53-104">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="0ba53-104">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>
## <a name="permissions"></a><span data-ttu-id="0ba53-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0ba53-105">Permissions</span></span>
<span data-ttu-id="0ba53-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0ba53-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0ba53-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0ba53-108">Permission type</span></span>      | <span data-ttu-id="0ba53-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0ba53-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0ba53-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0ba53-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0ba53-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0ba53-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0ba53-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0ba53-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0ba53-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ba53-113">Not supported.</span></span>    |
|<span data-ttu-id="0ba53-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0ba53-114">Application</span></span> | <span data-ttu-id="0ba53-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ba53-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0ba53-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0ba53-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/format/autofitRows
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/autofitRows
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/autofitRows

```
## <a name="request-headers"></a><span data-ttu-id="0ba53-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0ba53-117">Request headers</span></span>
| <span data-ttu-id="0ba53-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="0ba53-118">Name</span></span>       | <span data-ttu-id="0ba53-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ba53-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0ba53-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="0ba53-120">Authorization</span></span>  | <span data-ttu-id="0ba53-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0ba53-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0ba53-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0ba53-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="0ba53-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0ba53-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0ba53-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0ba53-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="0ba53-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ba53-127">Response</span></span>

<span data-ttu-id="0ba53-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ba53-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0ba53-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0ba53-130">Example</span></span>
<span data-ttu-id="0ba53-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0ba53-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0ba53-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0ba53-132">Request</span></span>
<span data-ttu-id="0ba53-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ba53-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitrows"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/autofitRows
```

##### <a name="response"></a><span data-ttu-id="0ba53-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ba53-134">Response</span></span>
<span data-ttu-id="0ba53-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ba53-135">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFormat: autofitRows",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->