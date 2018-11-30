---
title: 'Range: unmerge'
description: Separar las celdas del rango en celdas independientes.
ms.openlocfilehash: d537592f11be2175c369dcef4035bd67da36b1a3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032669"
---
# <a name="range-unmerge"></a><span data-ttu-id="87bff-103">Range: unmerge</span><span class="sxs-lookup"><span data-stu-id="87bff-103">Range: unmerge</span></span>

<span data-ttu-id="87bff-104">Separar las celdas del rango en celdas independientes.</span><span class="sxs-lookup"><span data-stu-id="87bff-104">Unmerge the range cells into separate cells.</span></span>
## <a name="permissions"></a><span data-ttu-id="87bff-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="87bff-105">Permissions</span></span>
<span data-ttu-id="87bff-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="87bff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="87bff-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="87bff-108">Permission type</span></span>      | <span data-ttu-id="87bff-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="87bff-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="87bff-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="87bff-110">Delegated (work or school account)</span></span> | <span data-ttu-id="87bff-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87bff-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="87bff-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="87bff-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="87bff-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="87bff-113">Not supported.</span></span>    |
|<span data-ttu-id="87bff-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="87bff-114">Application</span></span> | <span data-ttu-id="87bff-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="87bff-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="87bff-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="87bff-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/unmerge
POST /workbook/worksheets/{id|name}/range(address='<address>')/unmerge
POST /workbook/tables/{id|name}/columns/{id|name}/range/unmerge

```
## <a name="request-headers"></a><span data-ttu-id="87bff-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="87bff-117">Request headers</span></span>
| <span data-ttu-id="87bff-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="87bff-118">Name</span></span>       | <span data-ttu-id="87bff-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="87bff-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="87bff-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="87bff-120">Authorization</span></span>  | <span data-ttu-id="87bff-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="87bff-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="87bff-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="87bff-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="87bff-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="87bff-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="87bff-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="87bff-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="87bff-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87bff-127">Response</span></span>

<span data-ttu-id="87bff-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87bff-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="87bff-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="87bff-130">Example</span></span>
<span data-ttu-id="87bff-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="87bff-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="87bff-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="87bff-132">Request</span></span>
<span data-ttu-id="87bff-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87bff-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_unmerge"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/unmerge
```

##### <a name="response"></a><span data-ttu-id="87bff-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87bff-134">Response</span></span>
<span data-ttu-id="87bff-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87bff-135">Here is an example of the response.</span></span> 
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
  "description": "Range: unmerge",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->