---
title: 'workbookPivotTable: refreshAll'
description: Actualiza la tabla dinámica en una hoja de cálculo determinada.
author: lumine2008
ms.openlocfilehash: 08a4015d58e68a3099448be91537b7970d5c1ddd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308228"
---
# <a name="workbookpivottable-refreshall"></a><span data-ttu-id="fb566-103">workbookPivotTable: refreshAll</span><span class="sxs-lookup"><span data-stu-id="fb566-103">workbookPivotTable: refreshAll</span></span>

> <span data-ttu-id="fb566-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb566-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb566-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb566-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fb566-106">Actualiza la tabla dinámica en una hoja de cálculo determinada.</span><span class="sxs-lookup"><span data-stu-id="fb566-106">Refreshes the PivotTable within a given worksheet.</span></span>

## <a name="permissions"></a><span data-ttu-id="fb566-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb566-107">Permissions</span></span>
<span data-ttu-id="fb566-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb566-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb566-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb566-110">Permission type</span></span>      | <span data-ttu-id="fb566-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb566-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb566-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb566-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fb566-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb566-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fb566-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb566-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb566-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb566-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fb566-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb566-116">Application</span></span> | <span data-ttu-id="fb566-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb566-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb566-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb566-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/refreshAll

```
## <a name="request-headers"></a><span data-ttu-id="fb566-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb566-119">Request headers</span></span>
| <span data-ttu-id="fb566-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb566-120">Name</span></span>       | <span data-ttu-id="fb566-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb566-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fb566-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fb566-122">Authorization</span></span>  | <span data-ttu-id="fb566-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb566-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fb566-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fb566-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="fb566-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb566-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fb566-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb566-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="fb566-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb566-129">Response</span></span>

<span data-ttu-id="fb566-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb566-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb566-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb566-132">Example</span></span>
<span data-ttu-id="fb566-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fb566-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fb566-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb566-134">Request</span></span>
<span data-ttu-id="fb566-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb566-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refreshall"
}-->
```http
POST https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/pivotTables/refreshAll
```

##### <a name="response"></a><span data-ttu-id="fb566-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb566-136">Response</span></span>
<span data-ttu-id="fb566-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb566-137">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```
