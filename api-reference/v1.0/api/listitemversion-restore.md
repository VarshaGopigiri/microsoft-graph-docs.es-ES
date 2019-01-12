---
title: Restaurar una versión anterior de un objeto ListItem
description: Restaure una versión anterior de un objeto ListItem para que sea la versión actual. Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 3ba63f56838d07a0031baf613dec8e0847aaf2e6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963398"
---
# <a name="restore-a-previous-version-of-a-listitem"></a><span data-ttu-id="22a3b-104">Restaurar una versión anterior de un objeto ListItem</span><span class="sxs-lookup"><span data-stu-id="22a3b-104">Restore a previous version of a ListItem</span></span>

<span data-ttu-id="22a3b-105">Restaure una versión anterior de un objeto ListItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="22a3b-105">Restore a previous version of a ListItem to be the current version.</span></span> <span data-ttu-id="22a3b-106">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.</span><span class="sxs-lookup"><span data-stu-id="22a3b-106">This will create a new version with the contents of the previous version, but preserves all existing versions of the item.</span></span>

## <a name="permissions"></a><span data-ttu-id="22a3b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="22a3b-107">Permissions</span></span>

<span data-ttu-id="22a3b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22a3b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="22a3b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22a3b-110">Permission type</span></span>             |         <span data-ttu-id="22a3b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22a3b-111">Permissions (from least to most privileged)</span></span>          |
| :------------------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="22a3b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22a3b-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="22a3b-113">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="22a3b-113">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |
| <span data-ttu-id="22a3b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22a3b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22a3b-115">N/D</span><span class="sxs-lookup"><span data-stu-id="22a3b-115">n/a</span></span>                                                          |
| <span data-ttu-id="22a3b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22a3b-116">Application</span></span>                            | <span data-ttu-id="22a3b-117">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="22a3b-117">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="22a3b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22a3b-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="22a3b-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="22a3b-119">Request body</span></span>

<span data-ttu-id="22a3b-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="22a3b-120">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="22a3b-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22a3b-121">Example</span></span>

<span data-ttu-id="22a3b-122">En este ejemplo, se restaura una versión de un recurso listItem identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="22a3b-122">This example restores a version of a listItem identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version-listItem", "scopes": "files.readwrite sites.readwrite.all", "target": "action", "tags": "service.graph service.sharepoint" } -->

```http
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="22a3b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22a3b-123">Response</span></span>

<span data-ttu-id="22a3b-124">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="22a3b-124">If successful, the API call returns a `204 No Content`.</span></span>

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
