---
title: 'Table: DataBodyRange'
description: Obtiene el objeto de rango asociado al cuerpo de datos de la tabla.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: b8bcc6a23478f8199c1d19aa575e9700c7bff84f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940557"
---
# <a name="table-databodyrange"></a><span data-ttu-id="bca2e-103">Table: DataBodyRange</span><span class="sxs-lookup"><span data-stu-id="bca2e-103">Table: DataBodyRange</span></span>

> <span data-ttu-id="bca2e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bca2e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bca2e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bca2e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bca2e-106">Obtiene el objeto de rango asociado al cuerpo de datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bca2e-106">Gets the range object associated with the data body of the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="bca2e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bca2e-107">Permissions</span></span>
<span data-ttu-id="bca2e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bca2e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bca2e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bca2e-110">Permission type</span></span>      | <span data-ttu-id="bca2e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bca2e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bca2e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bca2e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bca2e-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bca2e-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bca2e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bca2e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bca2e-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bca2e-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bca2e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bca2e-116">Application</span></span> | <span data-ttu-id="bca2e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bca2e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bca2e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bca2e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/DataBodyRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/DataBodyRange

```
## <a name="request-headers"></a><span data-ttu-id="bca2e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bca2e-119">Request headers</span></span>
| <span data-ttu-id="bca2e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="bca2e-120">Name</span></span>       | <span data-ttu-id="bca2e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bca2e-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bca2e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="bca2e-122">Authorization</span></span>  | <span data-ttu-id="bca2e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bca2e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bca2e-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bca2e-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="bca2e-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bca2e-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bca2e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bca2e-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="bca2e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bca2e-129">Response</span></span>

<span data-ttu-id="bca2e-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bca2e-130">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bca2e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bca2e-131">Example</span></span>
<span data-ttu-id="bca2e-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bca2e-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bca2e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bca2e-133">Request</span></span>
<span data-ttu-id="bca2e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bca2e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_databodyrange"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/DataBodyRange
```

##### <a name="response"></a><span data-ttu-id="bca2e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bca2e-135">Response</span></span>
<span data-ttu-id="bca2e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bca2e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Table: DataBodyRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
