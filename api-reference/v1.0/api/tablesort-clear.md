---
title: 'TableSort: clear'
description: Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.
localization_priority: Normal
ms.openlocfilehash: 00d81e05ccaea45be0ce67cd29b828e2d7ce1634
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842752"
---
# <a name="tablesort-clear"></a><span data-ttu-id="8f576-104">TableSort: clear</span><span class="sxs-lookup"><span data-stu-id="8f576-104">TableSort: clear</span></span>

<span data-ttu-id="8f576-p102">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8f576-p102">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>
## <a name="permissions"></a><span data-ttu-id="8f576-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f576-107">Permissions</span></span>
<span data-ttu-id="8f576-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f576-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f576-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f576-110">Permission type</span></span>      | <span data-ttu-id="8f576-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f576-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f576-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f576-112">Delegated (work or school account)</span></span> | <span data-ttu-id="8f576-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f576-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8f576-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f576-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f576-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f576-115">Not supported.</span></span>    |
|<span data-ttu-id="8f576-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f576-116">Application</span></span> | <span data-ttu-id="8f576-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f576-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f576-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f576-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/clear

```
## <a name="request-headers"></a><span data-ttu-id="8f576-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f576-119">Request headers</span></span>
| <span data-ttu-id="8f576-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f576-120">Name</span></span>       | <span data-ttu-id="8f576-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f576-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8f576-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f576-122">Authorization</span></span>  | <span data-ttu-id="8f576-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f576-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8f576-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="8f576-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="8f576-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="8f576-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f576-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f576-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="8f576-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f576-129">Response</span></span>

<span data-ttu-id="8f576-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f576-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f576-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f576-132">Example</span></span>
<span data-ttu-id="8f576-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8f576-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8f576-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f576-134">Request</span></span>
<span data-ttu-id="8f576-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f576-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/clear
```

##### <a name="response"></a><span data-ttu-id="8f576-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f576-136">Response</span></span>
<span data-ttu-id="8f576-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f576-137">Here is an example of the response.</span></span> 
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
  "description": "TableSort: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
