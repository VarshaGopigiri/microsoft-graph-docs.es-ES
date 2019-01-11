---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtenga carpetas especiales.
localization_priority: Normal
ms.openlocfilehash: 9975f02a0f9740b27eab7786995a9dd794cb3f80
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836725"
---
# <a name="get-a-special-folder-by-name"></a><span data-ttu-id="bf6b0-102">Obtener una carpeta especial por su nombre</span><span class="sxs-lookup"><span data-stu-id="bf6b0-102">Get a special folder by name</span></span>

<span data-ttu-id="bf6b0-103">Use la colección especial para acceder a una carpeta especial por su nombre.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-103">Use the special collection to access a special folder by name.</span></span>

<span data-ttu-id="bf6b0-p101">Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas en OneDrive sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá encontrando esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-p101">Special folders provide simple aliases to access well-known folders in OneDrive without the need to look up the folder by path (which would require localization), or reference the folder with an ID. If a special folder is renamed or moved to another location within the drive, this syntax will continue to find that folder.</span></span>

<span data-ttu-id="bf6b0-p102">Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-p102">Special folders are automatically created the first time an application attempts to write to one, if it doesn't already exist. If a user deletes one, it is recreated when written to again.</span></span>

> <span data-ttu-id="bf6b0-108">**Nota:**  Si tiene permisos de solo lectura y solicita una carpeta especial que no existe, recibirá un error `403 Forbidden`.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-108">**Note:**  If you have read-only permissions and request a special folder that doesn't exist, you'll receive a `403 Forbidden` error.</span></span>

## <a name="permissions"></a><span data-ttu-id="bf6b0-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf6b0-109">Permissions</span></span>

<span data-ttu-id="bf6b0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf6b0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="bf6b0-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf6b0-112">Permission type</span></span>             |                                           <span data-ttu-id="bf6b0-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf6b0-113">Permissions (from least to most privileged)</span></span>                                            |
| :------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="bf6b0-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf6b0-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="bf6b0-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf6b0-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>                            |
| <span data-ttu-id="bf6b0-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf6b0-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf6b0-117">Files.ReadWrite.AppFolder, Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf6b0-117">Files.ReadWrite.AppFolder, Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |
| <span data-ttu-id="bf6b0-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf6b0-118">Application</span></span>                            | <span data-ttu-id="bf6b0-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf6b0-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>                                                         |

## <a name="http-request"></a><span data-ttu-id="bf6b0-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf6b0-120">HTTP Request</span></span>

<!-- { "blockType": "request", "name": "get-special-folder", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}
```

### <a name="special-folder-names"></a><span data-ttu-id="bf6b0-121">Nombres de carpetas especiales</span><span class="sxs-lookup"><span data-stu-id="bf6b0-121">Special folder names</span></span>

<span data-ttu-id="bf6b0-122">Los siguientes nombres de carpetas especiales están disponibles en OneDrive y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-122">The follow special folder names are available in OneDrive and OneDrive for Business.</span></span>

| <span data-ttu-id="bf6b0-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf6b0-123">Name</span></span>        | <span data-ttu-id="bf6b0-124">Id. de carpeta</span><span class="sxs-lookup"><span data-stu-id="bf6b0-124">Folder id</span></span>    | <span data-ttu-id="bf6b0-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf6b0-125">Description</span></span>                                                              |
|:------------|:-------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="bf6b0-126">Documentos</span><span class="sxs-lookup"><span data-stu-id="bf6b0-126">Documents</span></span>   | `documents`  | <span data-ttu-id="bf6b0-127">La carpeta Documentos.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-127">The Documents folder.</span></span>                                                    |
| <span data-ttu-id="bf6b0-128">Fotos</span><span class="sxs-lookup"><span data-stu-id="bf6b0-128">Photos</span></span>      | `photos`     | <span data-ttu-id="bf6b0-129">La carpeta Fotos.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-129">The Photos folder.</span></span>                                                       |
| <span data-ttu-id="bf6b0-130">Álbum de cámara</span><span class="sxs-lookup"><span data-stu-id="bf6b0-130">Camera Roll</span></span> | `cameraroll` | <span data-ttu-id="bf6b0-131">La carpeta de copia de seguridad del álbum de cámara.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-131">The Camera Roll Backup folder.</span></span>                                           |
| <span data-ttu-id="bf6b0-132">Raíz de la aplicación</span><span class="sxs-lookup"><span data-stu-id="bf6b0-132">App Root</span></span>    | `approot`    | <span data-ttu-id="bf6b0-p104">La carpeta personal de la aplicación. Normalmente en `/Apps/{Application Name}`</span><span class="sxs-lookup"><span data-stu-id="bf6b0-p104">The application's personal folder. Usually in `/Apps/{Application Name}`</span></span> |
| <span data-ttu-id="bf6b0-135">Música</span><span class="sxs-lookup"><span data-stu-id="bf6b0-135">Music</span></span>       | `music`      | <span data-ttu-id="bf6b0-136">La carpeta Música.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-136">The Music folder.</span></span>                                                        |


### <a name="optional-query-parameters"></a><span data-ttu-id="bf6b0-137">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bf6b0-137">Optional query parameters</span></span>

<span data-ttu-id="bf6b0-138">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand` y `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-138">This method supports the `$expand` and `$select` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="bf6b0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf6b0-139">Response</span></span>

<span data-ttu-id="bf6b0-140">Este método devuelve un código de respuesta `200 OK` y un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-140">This method returns a `200 OK` response code and a [driveItem](../resources/driveitem.md) object in the response body.</span></span>

<span data-ttu-id="bf6b0-141">Puede usar este método de direccionamiento de una carpeta especial junto con llamadas adicionales a las propiedades o relaciones en el objeto driveItem.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-141">You can use this method of addressing a special folder inline with additional calls to properties or relationships on the driveItem.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "0123456789abc",
  "name": "Documents",
  "eTag": "012345819293.1",
  "specialFolder": {
    "name": "documents"
  }
}
```

## <a name="get-children-of-a-special-folder"></a><span data-ttu-id="bf6b0-142">Obtener elementos secundarios de una carpeta especial</span><span class="sxs-lookup"><span data-stu-id="bf6b0-142">Get children of a special folder</span></span>

<span data-ttu-id="bf6b0-143">Para solicitar los elementos secundarios de una carpeta especial, puede solicitar la colección `children` o usar la opción [expand](/graph/query-parameters) para expandir la colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-143">To request the children of a special folder, you can request the `children` collection or use the [expand](/graph/query-parameters) option to expand the children collection.</span></span>

### <a name="http-request"></a><span data-ttu-id="bf6b0-144">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf6b0-144">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-special-children", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/special/{special-folder-name}/children
```

### <a name="response"></a><span data-ttu-id="bf6b0-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf6b0-145">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048 },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="bf6b0-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf6b0-146">Remarks</span></span>

> <span data-ttu-id="bf6b0-147">**Nota:** Los objetos DriveItems con la faceta `specialFolder` indican que el elemento es una carpeta especial y se puede obtener acceso a ella mediante la colección `special`.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-147">**Note:** DriveItems with the `specialFolder` facet indicate the item is a special folder and can be accessed via the `special` collection.</span></span>

<span data-ttu-id="bf6b0-148">Si la aplicación tiene permisos de solo lectura, la solicitud para obtener una carpeta especial o los elementos secundarios de una carpeta especial puede producir un error `404 Not Found` o `403 Forbidden` si la carpeta especial todavía no existe.</span><span class="sxs-lookup"><span data-stu-id="bf6b0-148">If your app has read-only permissions, the request to get a special folder or the children of a special folder may fail with a `404 Not Found` or a `403 Forbidden` error if the special folder does not already exist.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Access known folders in OneDrive through the special folder collection",
  "keywords": "known folders",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Special folders"
} -->
