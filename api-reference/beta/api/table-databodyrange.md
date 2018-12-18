---
title: 'Table: DataBodyRange'
description: Obtiene el objeto de rango asociado al cuerpo de datos de la tabla.
author: lumine2008
ms.openlocfilehash: a61690aef261725ca87053a01428b153c5a05c7a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311175"
---
# <a name="table-databodyrange"></a><span data-ttu-id="eda5a-103">Table: DataBodyRange</span><span class="sxs-lookup"><span data-stu-id="eda5a-103">Table: DataBodyRange</span></span>

> <span data-ttu-id="eda5a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eda5a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eda5a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eda5a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eda5a-106">Obtiene el objeto de rango asociado al cuerpo de datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="eda5a-106">Gets the range object associated with the data body of the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="eda5a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eda5a-107">Permissions</span></span>
<span data-ttu-id="eda5a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eda5a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eda5a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eda5a-110">Permission type</span></span>      | <span data-ttu-id="eda5a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eda5a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eda5a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eda5a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eda5a-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eda5a-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eda5a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eda5a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eda5a-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eda5a-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eda5a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eda5a-116">Application</span></span> | <span data-ttu-id="eda5a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eda5a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eda5a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eda5a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/DataBodyRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/DataBodyRange

```
## <a name="request-headers"></a><span data-ttu-id="eda5a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eda5a-119">Request headers</span></span>
| <span data-ttu-id="eda5a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="eda5a-120">Name</span></span>       | <span data-ttu-id="eda5a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="eda5a-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eda5a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="eda5a-122">Authorization</span></span>  | <span data-ttu-id="eda5a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eda5a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eda5a-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="eda5a-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="eda5a-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="eda5a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="eda5a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eda5a-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="eda5a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eda5a-129">Response</span></span>

<span data-ttu-id="eda5a-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eda5a-130">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eda5a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eda5a-131">Example</span></span>
<span data-ttu-id="eda5a-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eda5a-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eda5a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eda5a-133">Request</span></span>
<span data-ttu-id="eda5a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eda5a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_databodyrange"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/DataBodyRange
```

##### <a name="response"></a><span data-ttu-id="eda5a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eda5a-135">Response</span></span>
<span data-ttu-id="eda5a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eda5a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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