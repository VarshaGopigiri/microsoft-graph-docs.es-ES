---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Restaurar una versión anterior
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 9f8492b3a6e4b01b61288b235cc0dfa19ffd78d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946080"
---
# <a name="restore-a-previous-version-of-a-driveitem"></a><span data-ttu-id="905ec-102">Restaurar una versión anterior de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="905ec-102">Restore a previous version of a DriveItem</span></span>

> <span data-ttu-id="905ec-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="905ec-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="905ec-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="905ec-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="905ec-105">Restaure una versión anterior de un objeto DriveItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="905ec-105">Restore a previous version of a DriveItem to be the current version.</span></span> <span data-ttu-id="905ec-106">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del archivo.</span><span class="sxs-lookup"><span data-stu-id="905ec-106">This will create a new version with the contents of the previous version, but preserves all existing versions of the file.</span></span>

## <a name="permissions"></a><span data-ttu-id="905ec-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="905ec-107">Permissions</span></span>

<span data-ttu-id="905ec-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="905ec-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="905ec-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="905ec-110">Permission type</span></span>      | <span data-ttu-id="905ec-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="905ec-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="905ec-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="905ec-112">Delegated (work or school account)</span></span> | <span data-ttu-id="905ec-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="905ec-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="905ec-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="905ec-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="905ec-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="905ec-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="905ec-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="905ec-116">Application</span></span> | <span data-ttu-id="905ec-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="905ec-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="905ec-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="905ec-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/versions/{version-id}/restoreVersion
POST /groups/{groupId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /me/drive/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{siteId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /users/{userId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="905ec-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="905ec-119">Request body</span></span>

<span data-ttu-id="905ec-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="905ec-120">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="905ec-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="905ec-121">Example</span></span>

<span data-ttu-id="905ec-122">En este ejemplo, se restaura una versión de un archivo identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="905ec-122">This example restores a version of a file identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="905ec-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="905ec-123">Response</span></span>

<span data-ttu-id="905ec-124">Si se realiza correctamente, la llamada API devuelve `204 No content`.</span><span class="sxs-lookup"><span data-stu-id="905ec-124">If successful, the API call returns a `204 No content`.</span></span>

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
