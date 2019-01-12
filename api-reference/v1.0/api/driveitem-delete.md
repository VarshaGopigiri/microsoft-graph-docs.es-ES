---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminar un archivo o carpeta
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 39c7706fab229e52c394c30c6daf478a1fefd581
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966870"
---
# <a name="delete-a-driveitem"></a><span data-ttu-id="722cf-102">Delete a DriveItem</span><span class="sxs-lookup"><span data-stu-id="722cf-102">Delete a DriveItem</span></span>

<span data-ttu-id="722cf-p101">Elimina un [DriveItem](../resources/driveitem.md) mediante su identificador o la ruta de acceso. Tenga en cuenta que si elimina elementos con este método moverá los elementos a la Papelera de reciclaje en lugar de eliminarlos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="722cf-p101">Delete a [DriveItem](../resources/driveitem.md) by using its ID or path. Note that deleting items using this method will move the items to the recycle bin instead of permanently deleting the item.</span></span>

## <a name="permissions"></a><span data-ttu-id="722cf-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="722cf-105">Permissions</span></span>

<span data-ttu-id="722cf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="722cf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="722cf-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="722cf-108">Permission type</span></span>      | <span data-ttu-id="722cf-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="722cf-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="722cf-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="722cf-110">Delegated (work or school account)</span></span> | <span data-ttu-id="722cf-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="722cf-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="722cf-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="722cf-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="722cf-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="722cf-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="722cf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="722cf-114">Application</span></span> | <span data-ttu-id="722cf-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="722cf-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="722cf-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="722cf-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /drives/{drive-id}/items/{item-id}
DELETE /groups/{group-id}/drive/items/{item-id}
DELETE /me/drive/items/{item-id}
DELETE /sites/{siteId}/drive/items/{itemId}
DELETE /users/{userId}/drive/items/{itemId}
```

## <a name="optional-request-headers"></a><span data-ttu-id="722cf-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="722cf-117">Optional request headers</span></span>

| <span data-ttu-id="722cf-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="722cf-118">Name</span></span>          | <span data-ttu-id="722cf-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="722cf-119">Type</span></span>   | <span data-ttu-id="722cf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="722cf-120">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="722cf-121">if-match</span><span class="sxs-lookup"><span data-stu-id="722cf-121">if-match</span></span>      | <span data-ttu-id="722cf-122">String</span><span class="sxs-lookup"><span data-stu-id="722cf-122">String</span></span> | <span data-ttu-id="722cf-123">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="722cf-123">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="example"></a><span data-ttu-id="722cf-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="722cf-124">Example</span></span>

<span data-ttu-id="722cf-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="722cf-125">Here is an example of how to call this API.</span></span>

<!-- { "blockType": "request", "name": "delete-item", "scopes": "files.readwrite", "tags": "service.graph" } -->

```http
DELETE /me/drive/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="722cf-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="722cf-126">Response</span></span>

<span data-ttu-id="722cf-127">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="722cf-127">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

### <a name="error-responses"></a><span data-ttu-id="722cf-128">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="722cf-128">Error responses</span></span>

<span data-ttu-id="722cf-129">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="722cf-129">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Delete a DriveItem from a drive",
  "keywords": "delete,existing item,onedrive",
  "section": "documentation",
  "tocPath": "Items/Delete"
} -->
