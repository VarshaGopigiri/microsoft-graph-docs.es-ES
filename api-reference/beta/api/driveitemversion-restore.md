---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Restaurar una versión anterior
ms.openlocfilehash: 507f58e79f209e1e65bfb8dcc2ac666f64a8d45d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084575"
---
# <a name="restore-a-previous-version-of-a-driveitem"></a><span data-ttu-id="eb88f-102">Restaurar una versión anterior de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="eb88f-102">Restore a previous version of a DriveItem</span></span>

> <span data-ttu-id="eb88f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb88f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb88f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb88f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eb88f-105">Restaure una versión anterior de un objeto DriveItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="eb88f-105">Restore a previous version of a DriveItem to be the current version.</span></span> <span data-ttu-id="eb88f-106">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del archivo.</span><span class="sxs-lookup"><span data-stu-id="eb88f-106">This will create a new version with the contents of the previous version, but preserves all existing versions of the file.</span></span>

## <a name="permissions"></a><span data-ttu-id="eb88f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eb88f-107">Permissions</span></span>

<span data-ttu-id="eb88f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb88f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb88f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb88f-110">Permission type</span></span>      | <span data-ttu-id="eb88f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb88f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb88f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb88f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eb88f-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb88f-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="eb88f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb88f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb88f-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb88f-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="eb88f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb88f-116">Application</span></span> | <span data-ttu-id="eb88f-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb88f-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb88f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb88f-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/versions/{version-id}/restoreVersion
POST /groups/{groupId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /me/drive/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{siteId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /users/{userId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="eb88f-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb88f-119">Request body</span></span>

<span data-ttu-id="eb88f-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb88f-120">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="eb88f-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb88f-121">Example</span></span>

<span data-ttu-id="eb88f-122">En este ejemplo, se restaura una versión de un archivo identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="eb88f-122">This example restores a version of a file identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="eb88f-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb88f-123">Response</span></span>

<span data-ttu-id="eb88f-124">Si se realiza correctamente, la llamada API devuelve `204 No content`.</span><span class="sxs-lookup"><span data-stu-id="eb88f-124">If successful, the API call returns a `204 No content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
