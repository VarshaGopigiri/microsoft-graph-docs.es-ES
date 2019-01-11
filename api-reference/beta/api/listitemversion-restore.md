---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Restaurar una versión anterior de un elemento de lista de SharePoint
localization_priority: Normal
ms.openlocfilehash: 0df91bfb33ba395de4724c1ac1a72dc69f8d15e1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811392"
---
# <a name="restore-a-previous-version-of-a-listitem"></a><span data-ttu-id="9a102-102">Restaurar una versión anterior de un objeto ListItem</span><span class="sxs-lookup"><span data-stu-id="9a102-102">Restore a previous version of a ListItem</span></span>

> <span data-ttu-id="9a102-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9a102-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9a102-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9a102-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9a102-105">Restaure una versión anterior de un objeto ListItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="9a102-105">Restore a previous version of a ListItem to be the current version.</span></span> <span data-ttu-id="9a102-106">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.</span><span class="sxs-lookup"><span data-stu-id="9a102-106">This will create a new version with the contents of the previous version, but preserves all existing versions of the item.</span></span>

## <a name="permissions"></a><span data-ttu-id="9a102-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a102-107">Permissions</span></span>

<span data-ttu-id="9a102-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9a102-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="9a102-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a102-110">Permission type</span></span>             |         <span data-ttu-id="9a102-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a102-111">Permissions (from least to most privileged)</span></span>          |
| :------------------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="9a102-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a102-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="9a102-113">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="9a102-113">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |
| <span data-ttu-id="9a102-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a102-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a102-115">N/D</span><span class="sxs-lookup"><span data-stu-id="9a102-115">n/a</span></span>                                                          |
| <span data-ttu-id="9a102-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a102-116">Application</span></span>                            | <span data-ttu-id="9a102-117">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="9a102-117">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a102-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a102-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="9a102-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a102-119">Request body</span></span>

<span data-ttu-id="9a102-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a102-120">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="9a102-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a102-121">Example</span></span>

<span data-ttu-id="9a102-122">En este ejemplo, se restaura una versión de un recurso listItem identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="9a102-122">This example restores a version of a listItem identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version-listItem", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="9a102-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a102-123">Response</span></span>

<span data-ttu-id="9a102-124">Si se realiza correctamente, la llamada API devuelve `204 No content`.</span><span class="sxs-lookup"><span data-stu-id="9a102-124">If successful, the API call returns a `204 No content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
