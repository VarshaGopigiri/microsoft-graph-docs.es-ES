---
title: Restaurar una versión anterior de un objeto ListItem
description: Restaure una versión anterior de un objeto ListItem para que sea la versión actual. Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.
ms.openlocfilehash: f8dc4196c40c51287e93aaa667c325e8d4f6dcfb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030378"
---
# <a name="restore-a-previous-version-of-a-listitem"></a><span data-ttu-id="89c14-104">Restaurar una versión anterior de un objeto ListItem</span><span class="sxs-lookup"><span data-stu-id="89c14-104">Restore a previous version of a ListItem</span></span>

<span data-ttu-id="89c14-105">Restaure una versión anterior de un objeto ListItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="89c14-105">Restore a previous version of a ListItem to be the current version.</span></span> <span data-ttu-id="89c14-106">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.</span><span class="sxs-lookup"><span data-stu-id="89c14-106">This will create a new version with the contents of the previous version, but preserves all existing versions of the item.</span></span>

## <a name="permissions"></a><span data-ttu-id="89c14-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="89c14-107">Permissions</span></span>

<span data-ttu-id="89c14-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89c14-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="89c14-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89c14-110">Permission type</span></span>             |         <span data-ttu-id="89c14-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89c14-111">Permissions (from least to most privileged)</span></span>          |
| :------------------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="89c14-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89c14-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="89c14-113">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="89c14-113">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |
| <span data-ttu-id="89c14-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89c14-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89c14-115">N/D</span><span class="sxs-lookup"><span data-stu-id="89c14-115">n/a</span></span>                                                          |
| <span data-ttu-id="89c14-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89c14-116">Application</span></span>                            | <span data-ttu-id="89c14-117">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="89c14-117">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="89c14-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89c14-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="89c14-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="89c14-119">Request body</span></span>

<span data-ttu-id="89c14-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="89c14-120">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="89c14-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89c14-121">Example</span></span>

<span data-ttu-id="89c14-122">En este ejemplo, se restaura una versión de un recurso listItem identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="89c14-122">This example restores a version of a listItem identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version-listItem", "scopes": "files.readwrite sites.readwrite.all", "target": "action", "tags": "service.graph service.sharepoint" } -->

```http
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="89c14-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89c14-123">Response</span></span>

<span data-ttu-id="89c14-124">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="89c14-124">If successful, the API call returns a `204 No Content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
