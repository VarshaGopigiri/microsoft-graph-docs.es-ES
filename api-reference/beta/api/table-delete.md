---
title: 'Table: delete'
description: Elimina la tabla.
ms.openlocfilehash: 849840a2c89007a0ab19e21fedcadb418c6cee40
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089153"
---
# <a name="table-delete"></a><span data-ttu-id="fb8ea-103">Table: delete</span><span class="sxs-lookup"><span data-stu-id="fb8ea-103">Table: delete</span></span>

> <span data-ttu-id="fb8ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb8ea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fb8ea-106">Elimina la tabla.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-106">Deletes the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="fb8ea-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb8ea-107">Permissions</span></span>
<span data-ttu-id="fb8ea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb8ea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb8ea-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb8ea-110">Permission type</span></span>      | <span data-ttu-id="fb8ea-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb8ea-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb8ea-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb8ea-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fb8ea-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb8ea-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fb8ea-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb8ea-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb8ea-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb8ea-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fb8ea-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb8ea-116">Application</span></span> | <span data-ttu-id="fb8ea-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb8ea-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb8ea-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/delete
POST /workbook/worksheets/{id|name}/tables/{id|name}/delete

```
## <a name="request-headers"></a><span data-ttu-id="fb8ea-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb8ea-119">Request headers</span></span>
| <span data-ttu-id="fb8ea-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb8ea-120">Name</span></span>       | <span data-ttu-id="fb8ea-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8ea-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fb8ea-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fb8ea-122">Authorization</span></span>  | <span data-ttu-id="fb8ea-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fb8ea-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fb8ea-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="fb8ea-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fb8ea-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb8ea-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="fb8ea-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb8ea-129">Response</span></span>

<span data-ttu-id="fb8ea-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb8ea-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb8ea-132">Example</span></span>
<span data-ttu-id="fb8ea-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fb8ea-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb8ea-134">Request</span></span>
<span data-ttu-id="fb8ea-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_delete"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/delete
```

##### <a name="response"></a><span data-ttu-id="fb8ea-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb8ea-136">Response</span></span>
<span data-ttu-id="fb8ea-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb8ea-137">Here is an example of the response.</span></span> 
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
  "description": "Table: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->