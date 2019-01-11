---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtenga carpetas especiales.
localization_priority: Normal
ms.openlocfilehash: c63f3ae585db0aff812e16eb9f125d19e77a806c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887958"
---
# <a name="get-a-special-folder-by-name"></a><span data-ttu-id="97730-102">Obtener una carpeta especial por su nombre</span><span class="sxs-lookup"><span data-stu-id="97730-102">Get a special folder by name</span></span>

> <span data-ttu-id="97730-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="97730-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="97730-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="97730-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="97730-105">Use la colección especial para acceder a una carpeta especial por su nombre.</span><span class="sxs-lookup"><span data-stu-id="97730-105">Use the special collection to access a special folder by name.</span></span>

<span data-ttu-id="97730-p102">Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas en OneDrive sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá encontrando esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="97730-p102">Special folders provide simple aliases to access well-known folders in OneDrive without the need to look up the folder by path (which would require localization), or reference the folder with an ID. If a special folder is renamed or moved to another location within the drive, this syntax will continue to find that folder.</span></span>

<span data-ttu-id="97730-p103">Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="97730-p103">Special folders are automatically created the first time an application attempts to write to one, if it doesn't already exist. If a user deletes one, it is recreated when written to again.</span></span>

> <span data-ttu-id="97730-110">**Nota:**  Si tiene permisos de solo lectura y solicita una carpeta especial que no existe, recibirá un error `403 Forbidden`.</span><span class="sxs-lookup"><span data-stu-id="97730-110">**Note:**  If you have read-only permissions and request a special folder that doesn't exist, you'll receive a `403 Forbidden` error.</span></span>

## <a name="permissions"></a><span data-ttu-id="97730-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="97730-111">Permissions</span></span>

<span data-ttu-id="97730-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97730-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|            <span data-ttu-id="97730-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97730-114">Permission type</span></span>             |                                           <span data-ttu-id="97730-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97730-115">Permissions (from least to most privileged)</span></span>                                            |
| :------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="97730-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97730-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="97730-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97730-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>                            |
| <span data-ttu-id="97730-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97730-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="97730-119">Files.ReadWrite.AppFolder, Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97730-119">Files.ReadWrite.AppFolder, Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |
| <span data-ttu-id="97730-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97730-120">Application</span></span>                            | <span data-ttu-id="97730-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97730-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>                                                         |

## <a name="http-request"></a><span data-ttu-id="97730-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97730-122">HTTP Request</span></span>

<!-- { "blockType": "request", "name": "get-special-folder", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}
```

### <a name="special-folder-names"></a><span data-ttu-id="97730-123">Nombres de carpetas especiales</span><span class="sxs-lookup"><span data-stu-id="97730-123">Special folder names</span></span>

<span data-ttu-id="97730-124">Los siguientes nombres de carpetas especiales están disponibles en OneDrive y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="97730-124">The follow special folder names are available in OneDrive and OneDrive for Business.</span></span>

| <span data-ttu-id="97730-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="97730-125">Name</span></span>        | <span data-ttu-id="97730-126">Id. de carpeta</span><span class="sxs-lookup"><span data-stu-id="97730-126">Folder id</span></span>    | <span data-ttu-id="97730-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="97730-127">Description</span></span>                                                              |
|:------------|:-------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="97730-128">Documentos</span><span class="sxs-lookup"><span data-stu-id="97730-128">Documents</span></span>   | `documents`  | <span data-ttu-id="97730-129">La carpeta Documentos.</span><span class="sxs-lookup"><span data-stu-id="97730-129">The Documents folder.</span></span>                                                    |
| <span data-ttu-id="97730-130">Fotos</span><span class="sxs-lookup"><span data-stu-id="97730-130">Photos</span></span>      | `photos`     | <span data-ttu-id="97730-131">La carpeta Fotos.</span><span class="sxs-lookup"><span data-stu-id="97730-131">The Photos folder.</span></span>                                                       |
| <span data-ttu-id="97730-132">Álbum de cámara</span><span class="sxs-lookup"><span data-stu-id="97730-132">Camera Roll</span></span> | `cameraroll` | <span data-ttu-id="97730-133">La carpeta de copia de seguridad del álbum de cámara.</span><span class="sxs-lookup"><span data-stu-id="97730-133">The Camera Roll Backup folder.</span></span>                                           |
| <span data-ttu-id="97730-134">Raíz de la aplicación</span><span class="sxs-lookup"><span data-stu-id="97730-134">App Root</span></span>    | `approot`    | <span data-ttu-id="97730-p105">La carpeta personal de la aplicación. Normalmente en `/Apps/{Application Name}`</span><span class="sxs-lookup"><span data-stu-id="97730-p105">The application's personal folder. Usually in `/Apps/{Application Name}`</span></span> |
| <span data-ttu-id="97730-137">Música</span><span class="sxs-lookup"><span data-stu-id="97730-137">Music</span></span>       | `music`      | <span data-ttu-id="97730-138">La carpeta Música.</span><span class="sxs-lookup"><span data-stu-id="97730-138">The Music folder.</span></span>                                                        |


### <a name="optional-query-parameters"></a><span data-ttu-id="97730-139">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="97730-139">Optional query parameters</span></span>

<span data-ttu-id="97730-140">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand` y `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97730-140">This method supports the `$expand` and `$select` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="97730-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97730-141">Response</span></span>

<span data-ttu-id="97730-142">Este método devuelve un código de respuesta `200 OK` y un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97730-142">This method returns a `200 OK` response code and a [driveItem](../resources/driveitem.md) object in the response body.</span></span>

<span data-ttu-id="97730-143">Puede usar este método de direccionamiento de una carpeta especial junto con llamadas adicionales a las propiedades o relaciones en el objeto driveItem.</span><span class="sxs-lookup"><span data-stu-id="97730-143">You can use this method of addressing a special folder inline with additional calls to properties or relationships on the driveItem.</span></span>

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

## <a name="get-children-of-a-special-folder"></a><span data-ttu-id="97730-144">Obtener elementos secundarios de una carpeta especial</span><span class="sxs-lookup"><span data-stu-id="97730-144">Get children of a special folder</span></span>

<span data-ttu-id="97730-145">Para solicitar los elementos secundarios de una carpeta especial, puede solicitar la colección `children` o usar la opción [expand](/graph/query-parameters) para expandir la colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="97730-145">To request the children of a special folder, you can request the `children` collection or use the [expand](/graph/query-parameters) option to expand the children collection.</span></span>

### <a name="http-request"></a><span data-ttu-id="97730-146">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97730-146">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-special-children", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}/children
```

### <a name="response"></a><span data-ttu-id="97730-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97730-147">Response</span></span>

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

## <a name="remarks"></a><span data-ttu-id="97730-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97730-148">Remarks</span></span>

> <span data-ttu-id="97730-149">**Nota:** Los objetos DriveItems con la faceta `specialFolder` indican que el elemento es una carpeta especial y se puede obtener acceso a ella mediante la colección `special`.</span><span class="sxs-lookup"><span data-stu-id="97730-149">**Note:** DriveItems with the `specialFolder` facet indicate the item is a special folder and can be accessed via the `special` collection.</span></span>

<span data-ttu-id="97730-150">Si la aplicación tiene permisos de solo lectura, la solicitud para obtener una carpeta especial o los elementos secundarios de una carpeta especial puede producir un error `404 Not Found` o `403 Forbidden` si la carpeta especial todavía no existe.</span><span class="sxs-lookup"><span data-stu-id="97730-150">If your app has read-only permissions, the request to get a special folder or the children of a special folder may fail with a `404 Not Found` or a `403 Forbidden` error if the special folder does not already exist.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Access known folders in OneDrive through the special folder collection",
  "keywords": "known folders",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Special folders"
} -->
