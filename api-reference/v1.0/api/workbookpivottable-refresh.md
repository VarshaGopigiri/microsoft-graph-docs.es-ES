---
title: 'workbookPivotTable: refresh'
description: Actualiza la tabla dinámica.
ms.openlocfilehash: 3acbe6efb29d6846b48bfae250731640ad533dad
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029749"
---
# <a name="workbookpivottable-refresh"></a><span data-ttu-id="2453d-103">workbookPivotTable: refresh</span><span class="sxs-lookup"><span data-stu-id="2453d-103">workbookPivotTable: refresh</span></span>

<span data-ttu-id="2453d-104">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="2453d-104">Refreshes the PivotTable.</span></span>


## <a name="permissions"></a><span data-ttu-id="2453d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2453d-105">Permissions</span></span>
<span data-ttu-id="2453d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2453d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2453d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2453d-108">Permission type</span></span>      | <span data-ttu-id="2453d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2453d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2453d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2453d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2453d-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2453d-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2453d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2453d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2453d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2453d-113">Not supported.</span></span>    |
|<span data-ttu-id="2453d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2453d-114">Application</span></span> | <span data-ttu-id="2453d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2453d-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2453d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2453d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```
## <a name="request-headers"></a><span data-ttu-id="2453d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2453d-117">Request headers</span></span>
| <span data-ttu-id="2453d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2453d-118">Name</span></span>       | <span data-ttu-id="2453d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2453d-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2453d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2453d-120">Authorization</span></span>  | <span data-ttu-id="2453d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2453d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2453d-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2453d-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="2453d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2453d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2453d-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2453d-126">Request body</span></span>

### <a name="response"></a><span data-ttu-id="2453d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2453d-127">Response</span></span>
<span data-ttu-id="2453d-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2453d-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2453d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2453d-130">Example</span></span>
<span data-ttu-id="2453d-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2453d-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2453d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2453d-132">Request</span></span>
<span data-ttu-id="2453d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2453d-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refresh"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```

##### <a name="response"></a><span data-ttu-id="2453d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2453d-134">Response</span></span>
<span data-ttu-id="2453d-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2453d-135">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```