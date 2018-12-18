---
title: 'workbookPivotTable: refreshAll'
description: Actualiza la tabla dinámica en una hoja de cálculo determinada.
author: lumine2008
ms.openlocfilehash: dc94e5841440ba5110d7382abb04920e2d91015d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337915"
---
# <a name="workbookpivottable-refreshall"></a><span data-ttu-id="a5d99-103">workbookPivotTable: refreshAll</span><span class="sxs-lookup"><span data-stu-id="a5d99-103">workbookPivotTable: refreshAll</span></span>

<span data-ttu-id="a5d99-104">Actualiza la tabla dinámica en una hoja de cálculo determinada.</span><span class="sxs-lookup"><span data-stu-id="a5d99-104">Refreshes the PivotTable within a given worksheet.</span></span>

## <a name="permissions"></a><span data-ttu-id="a5d99-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5d99-105">Permissions</span></span>
<span data-ttu-id="a5d99-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5d99-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5d99-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5d99-108">Permission type</span></span>      | <span data-ttu-id="a5d99-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5d99-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5d99-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5d99-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a5d99-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5d99-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a5d99-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5d99-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5d99-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5d99-113">Not supported.</span></span>    |
|<span data-ttu-id="a5d99-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5d99-114">Application</span></span> | <span data-ttu-id="a5d99-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5d99-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a5d99-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5d99-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/refreshAll

```
## <a name="request-headers"></a><span data-ttu-id="a5d99-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5d99-117">Request headers</span></span>
| <span data-ttu-id="a5d99-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a5d99-118">Name</span></span>       | <span data-ttu-id="a5d99-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5d99-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a5d99-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5d99-120">Authorization</span></span>  | <span data-ttu-id="a5d99-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5d99-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a5d99-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a5d99-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="a5d99-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5d99-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5d99-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5d99-126">Request body</span></span>

### <a name="response"></a><span data-ttu-id="a5d99-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5d99-127">Response</span></span>
<span data-ttu-id="a5d99-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5d99-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5d99-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5d99-130">Example</span></span>
<span data-ttu-id="a5d99-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a5d99-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a5d99-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5d99-132">Request</span></span>
<span data-ttu-id="a5d99-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5d99-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refreshall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/pivotTables/refreshAll
```

##### <a name="response"></a><span data-ttu-id="a5d99-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5d99-134">Response</span></span>
<span data-ttu-id="a5d99-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5d99-135">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```
