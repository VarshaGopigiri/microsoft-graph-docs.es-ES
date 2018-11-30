---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Create a new folder
ms.openlocfilehash: 7f1df04ecf6948ee30ddda9486058db19ae36412
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086921"
---
# <a name="create-a-new-folder-in-a-drive"></a><span data-ttu-id="c2288-102">Crear una carpeta en una unidad</span><span class="sxs-lookup"><span data-stu-id="c2288-102">Create a new folder in a drive</span></span>

> <span data-ttu-id="c2288-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2288-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2288-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2288-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c2288-105">Cree una carpeta o un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) con un elemento primario o una ruta de acceso especificados.</span><span class="sxs-lookup"><span data-stu-id="c2288-105">Create a new folder or [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) with a specified parent item or path.</span></span>

## <a name="permissions"></a><span data-ttu-id="c2288-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2288-106">Permissions</span></span>

<span data-ttu-id="c2288-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2288-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2288-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2288-109">Permission type</span></span>      | <span data-ttu-id="c2288-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2288-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2288-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2288-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c2288-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2288-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="c2288-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2288-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2288-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2288-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="c2288-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2288-115">Application</span></span> | <span data-ttu-id="c2288-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2288-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2288-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2288-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{parent-item-id}/children
POST /groups/{group-id}/drive/items/{parent-item-id}/children
POST /me/drive/items/{parent-item-id}/children
POST /sites/{site-id}/drive/items/{parent-item-id}/children
POST /users/{user-id}/drive/items/{parent-item-id}/children
```

## <a name="request-body"></a><span data-ttu-id="c2288-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2288-118">Request body</span></span>

<span data-ttu-id="c2288-119">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [DriveItem](../resources/driveitem.md) que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="c2288-119">In the request body, supply a JSON representation of the [DriveItem](../resources/driveitem.md) resource to create.</span></span>

## <a name="response"></a><span data-ttu-id="c2288-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2288-120">Response</span></span>

<span data-ttu-id="c2288-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2288-121">If successful, this method returns `201 Created` response code and a [Driveitem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2288-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2288-122">Example</span></span>

### <a name="request"></a><span data-ttu-id="c2288-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2288-123">Request</span></span>

<span data-ttu-id="c2288-124">Aquí tiene un ejemplo de la solicitud para crear una carpeta en la carpeta raíz de OneDrive del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="c2288-124">Here is an example of the request to create a new folder in the signed-in user's OneDrive root folder.</span></span>
<span data-ttu-id="c2288-125">La propiedad `@microsoft.graph.conflictBehavior` usada indica que, si ya existe un elemento con el mismo nombre, el servicio debe elegir un nuevo nombre para la carpeta al crearla.</span><span class="sxs-lookup"><span data-stu-id="c2288-125">The `@microsoft.graph.conflictBehavior` property used indicates that if an item already exists with the same name, the service should choose a new name for the folder while creating it.</span></span>

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

### <a name="response"></a><span data-ttu-id="c2288-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2288-126">Response</span></span>

<span data-ttu-id="c2288-127">Si se ejecuta correctamente, este método devuelve la carpeta que se acaba de crear como un recurso [DriveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="c2288-127">If successful, this method returns the newly created folder as a [DriveItem][item-resource] resource.</span></span>

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

## <a name="error-response"></a><span data-ttu-id="c2288-128">Respuesta de error</span><span class="sxs-lookup"><span data-stu-id="c2288-128">Error response</span></span>

<span data-ttu-id="c2288-129">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="c2288-129">Read the [Error Responses][error-response] topic for more info about how errors are returned.</span></span>
[respuesta de error]: / gráfico/errores [elemento-recurso]:.. /Resources/driveitem.MD [carpeta faceta]:.. /Resources/Folder.MD
[error-response]: /graph/errors [item-resource]: ../resources/driveitem.md [folder-facet]: ../resources/folder.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a folder item in a drive.",
  "keywords": "create,folder,new item",
  "section": "documentation",
  "tocPath": "Items/Create folder"
} -->
