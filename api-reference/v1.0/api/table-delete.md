---
title: 'Table: delete'
description: Elimina la tabla.
author: lumine2008
ms.openlocfilehash: e7b9b54ad5e47893c73ff6820eab3919eb67582b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351180"
---
# <a name="table-delete"></a><span data-ttu-id="0dcb9-103">Table: delete</span><span class="sxs-lookup"><span data-stu-id="0dcb9-103">Table: delete</span></span>

<span data-ttu-id="0dcb9-104">Elimina la tabla.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-104">Deletes the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="0dcb9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0dcb9-105">Permissions</span></span>
<span data-ttu-id="0dcb9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0dcb9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0dcb9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0dcb9-108">Permission type</span></span>      | <span data-ttu-id="0dcb9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0dcb9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0dcb9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0dcb9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0dcb9-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0dcb9-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0dcb9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0dcb9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0dcb9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-113">Not supported.</span></span>    |
|<span data-ttu-id="0dcb9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0dcb9-114">Application</span></span> | <span data-ttu-id="0dcb9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0dcb9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0dcb9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/delete
POST /workbook/worksheets/{id|name}/tables/{id|name}/delete

```
## <a name="request-headers"></a><span data-ttu-id="0dcb9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0dcb9-117">Request headers</span></span>
| <span data-ttu-id="0dcb9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="0dcb9-118">Name</span></span>       | <span data-ttu-id="0dcb9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dcb9-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0dcb9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="0dcb9-120">Authorization</span></span>  | <span data-ttu-id="0dcb9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0dcb9-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0dcb9-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="0dcb9-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0dcb9-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0dcb9-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="0dcb9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0dcb9-127">Response</span></span>

<span data-ttu-id="0dcb9-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0dcb9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0dcb9-130">Example</span></span>
<span data-ttu-id="0dcb9-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0dcb9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0dcb9-132">Request</span></span>
<span data-ttu-id="0dcb9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/delete
```

##### <a name="response"></a><span data-ttu-id="0dcb9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0dcb9-134">Response</span></span>
<span data-ttu-id="0dcb9-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dcb9-135">Here is an example of the response.</span></span> 
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
  "description": "Table: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->