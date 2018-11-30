---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Create a new folder
ms.openlocfilehash: 413d3dc5ceb2eaac38d1d088916fc8c9de2401b2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031029"
---
# <a name="create-a-new-folder-in-a-drive"></a><span data-ttu-id="305db-102">Crear una carpeta en una unidad</span><span class="sxs-lookup"><span data-stu-id="305db-102">Create a new folder in a drive</span></span>

<span data-ttu-id="305db-103">Cree una carpeta o un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) con un elemento primario o una ruta de acceso especificados.</span><span class="sxs-lookup"><span data-stu-id="305db-103">Create a new folder or [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) with a specified parent item or path.</span></span>

## <a name="permissions"></a><span data-ttu-id="305db-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="305db-104">Permissions</span></span>

<span data-ttu-id="305db-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="305db-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="305db-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="305db-107">Permission type</span></span>      | <span data-ttu-id="305db-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="305db-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="305db-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="305db-109">Delegated (work or school account)</span></span> | <span data-ttu-id="305db-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="305db-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="305db-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="305db-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="305db-112">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="305db-112">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="305db-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="305db-113">Application</span></span> | <span data-ttu-id="305db-114">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="305db-114">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="305db-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="305db-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{parent-item-id}/children
POST /groups/{group-id}/drive/items/{parent-item-id}/children
POST /me/drive/items/{parent-item-id}/children
POST /sites/{site-id}/drive/items/{parent-item-id}/children
POST /users/{user-id}/drive/items/{parent-item-id}/children
```

## <a name="request-body"></a><span data-ttu-id="305db-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="305db-116">Request body</span></span>

<span data-ttu-id="305db-117">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [DriveItem](../resources/driveitem.md) que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="305db-117">In the request body, supply a JSON representation of the [DriveItem](../resources/driveitem.md) resource to create.</span></span>

## <a name="response"></a><span data-ttu-id="305db-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="305db-118">Response</span></span>

<span data-ttu-id="305db-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="305db-119">If successful, this method returns `201 Created` response code and a [Driveitem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="305db-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="305db-120">Example</span></span>

### <a name="request"></a><span data-ttu-id="305db-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="305db-121">Request</span></span>

<span data-ttu-id="305db-122">Aquí tiene un ejemplo de la solicitud para crear una carpeta en la carpeta raíz de OneDrive del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="305db-122">Here is an example of the request to create a new folder in the signed-in user's OneDrive root folder.</span></span>
<span data-ttu-id="305db-123">La propiedad `@microsoft.graph.conflictBehavior` usada indica que, si ya existe un elemento con el mismo nombre, el servicio debe elegir un nuevo nombre para la carpeta al crearla.</span><span class="sxs-lookup"><span data-stu-id="305db-123">The `@microsoft.graph.conflictBehavior` property used indicates that if an item already exists with the same name, the service should choose a new name for the folder while creating it.</span></span>

<!-- { "blockType": "request", "name": "create-folder", "scopes": "files.readwrite" } -->

```http
POST /me/drive/root/children
Content-Type: application/json

{
  "name": "New Folder",
  "folder": { },
  "@microsoft.graph.conflictBehavior": "rename"
}
```

### <a name="response"></a><span data-ttu-id="305db-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="305db-124">Response</span></span>

<span data-ttu-id="305db-125">Si se ejecuta correctamente, este método devuelve la carpeta que se acaba de crear como un recurso [DriveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="305db-125">If successful, this method returns the newly created folder as a [DriveItem][item-resource] resource.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "309EC495-3E92-431D-9124-F0299633171D"
    }
  },
  "createdDateTime": "2016-09-20T14:34:00Z",
  "eTag": "343F1FBD-E9B3-4DDE-BCA7-D61AEAFF44E5,1",
  "id": "ACEA49D1-1444-45A9-A1CB-68B1B28AE491",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "309EC495-3E92-431D-9124-F0299633171D"
    }
  },
  "lastModifiedDateTime": "2016-09-20T14:34:00Z",
  "name": "New Folder",
  "parentReference": {
    "driveId": "5FE38E3C-051C-4D55-9B83-8A437658275B",
    "id": "E67A8F34-B0AA-46E1-8FF7-0750A29553DF",
    "path": "/drive/root:/"
  },
  "size": 0,
  "folder": {
    "childCount": 0
  }
}
```

## <a name="error-response"></a><span data-ttu-id="305db-126">Respuesta de error</span><span class="sxs-lookup"><span data-stu-id="305db-126">Error response</span></span>

<span data-ttu-id="305db-127">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="305db-127">Read the [Error Responses][error-response] topic for more info about how errors are returned.</span></span>
[respuesta de error]: / gráfico/errores [elemento-recurso]:.. /Resources/driveitem.MD [carpeta faceta]:.. /Resources/Folder.MD
[error-response]: /graph/errors [item-resource]: ../resources/driveitem.md [folder-facet]: ../resources/folder.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a folder item in a drive.",
  "keywords": "create,folder,new item",
  "section": "documentation",
  "tocPath": "Items/Create folder"
} -->
