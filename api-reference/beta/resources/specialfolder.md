---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SpecialFolder
localization_priority: Normal
ms.openlocfilehash: 2e57956f30e35e9c9276e0fd55d718f22a2c58d0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828675"
---
# <a name="specialfolder-resource-type"></a><span data-ttu-id="d9906-102">Tipo de recurso SpecialFolder</span><span class="sxs-lookup"><span data-stu-id="d9906-102">SpecialFolder resource type</span></span>

> <span data-ttu-id="d9906-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9906-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9906-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9906-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d9906-105">El recurso **SpecialFolder** agrupa en una sola estructura los elementos de datos relacionados con carpetas especiales.</span><span class="sxs-lookup"><span data-stu-id="d9906-105">The **SpecialFolder** resource groups special folder-related data items into a single structure.</span></span>

<span data-ttu-id="d9906-106">Si un objeto **DriveItem** tiene una faceta **specialFolder** que no es NULL, el elemento representa una carpeta especial (con nombre).</span><span class="sxs-lookup"><span data-stu-id="d9906-106">If a **DriveItem** has a non-null **specialFolder** facet, the item represents a special (named) folder.</span></span>
<span data-ttu-id="d9906-107">Se puede obtener acceso a las carpetas especiales directamente a través de la [colección de carpetas especiales](../api/drive-get-specialfolder.md).</span><span class="sxs-lookup"><span data-stu-id="d9906-107">Special folders can be accessed directly via the [special folders collection](../api/drive-get-specialfolder.md).</span></span>

<span data-ttu-id="d9906-p103">Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá devolviendo esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="d9906-p103">Special folders provide simple aliases to access well-known folders without the need to look up the folder by path (which would require localization), or reference the folder with an ID. If a special folder is renamed or moved to another location within the drive, this syntax will continue to return that folder.</span></span>

<span data-ttu-id="d9906-p104">Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="d9906-p104">Special folders are automatically created the first time an application attempts to write to one, if it doesn't already exist. If a user deletes one, it is recreated when written to again.</span></span>

<span data-ttu-id="d9906-112">**Nota:** Si la aplicación solo ha solicitado el ámbito **Files.Read** y solicita una carpeta especial que no existe, la respuesta será un error `403 Forbidden`.</span><span class="sxs-lookup"><span data-stu-id="d9906-112">**Note:** If your app has only requested **Files.Read** scope and requests a special folder that doesn't exist, the response will be a `403 Forbidden` error.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d9906-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9906-113">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.specialFolder"
}-->
```json
{
  "name": "string"
}
```

## <a name="properties"></a><span data-ttu-id="d9906-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9906-114">Properties</span></span>

| <span data-ttu-id="d9906-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9906-115">Property</span></span>  | <span data-ttu-id="d9906-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9906-116">Type</span></span>   | <span data-ttu-id="d9906-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9906-117">Description</span></span>                                                            |
|:----------|:-------|:-----------------------------------------------------------------------|
| <span data-ttu-id="d9906-118">name</span><span class="sxs-lookup"><span data-stu-id="d9906-118">name</span></span>      | <span data-ttu-id="d9906-119">string</span><span class="sxs-lookup"><span data-stu-id="d9906-119">string</span></span> | <span data-ttu-id="d9906-120">El identificador único de este elemento en la colección `/drive/special`</span><span class="sxs-lookup"><span data-stu-id="d9906-120">The unique identifier for this item in the `/drive/special` collection</span></span> |

## <a name="special-folders"></a><span data-ttu-id="d9906-121">Carpetas especiales</span><span class="sxs-lookup"><span data-stu-id="d9906-121">Special folders</span></span>

<span data-ttu-id="d9906-122">Estas son las carpetas especiales disponibles en OneDrive Personal y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="d9906-122">Here are the special folders available in OneDrive Personal and OneDrive for Business.</span></span>

| <span data-ttu-id="d9906-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9906-123">Name</span></span>        | <span data-ttu-id="d9906-124">Id. de carpeta</span><span class="sxs-lookup"><span data-stu-id="d9906-124">Folder id</span></span>    | <span data-ttu-id="d9906-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9906-125">Description</span></span>                                                              |
|:------------|:-------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="d9906-126">Raíz de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d9906-126">App Root</span></span>    | `approot`    | <span data-ttu-id="d9906-p105">La carpeta personal de la aplicación. Normalmente en `/Apps/{Application Name}`</span><span class="sxs-lookup"><span data-stu-id="d9906-p105">The application's personal folder. Usually in `/Apps/{Application Name}`</span></span> |
| <span data-ttu-id="d9906-129">Álbum de cámara</span><span class="sxs-lookup"><span data-stu-id="d9906-129">Camera Roll</span></span> | `cameraroll` | <span data-ttu-id="d9906-p106">La carpeta de copia de seguridad del álbum de cámara. No está disponible en OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="d9906-p106">The Camera Roll Backup folder. Not available in OneDrive for Business.</span></span>   |
| <span data-ttu-id="d9906-132">Documentos</span><span class="sxs-lookup"><span data-stu-id="d9906-132">Documents</span></span>   | `documents`  | <span data-ttu-id="d9906-133">La carpeta Documentos.</span><span class="sxs-lookup"><span data-stu-id="d9906-133">The Documents folder.</span></span>                                                    |
| <span data-ttu-id="d9906-134">Música</span><span class="sxs-lookup"><span data-stu-id="d9906-134">Music</span></span>       | `music`      | <span data-ttu-id="d9906-p107">La carpeta Música. No está disponible en OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="d9906-p107">The Music folder. Not available in OneDrive for Business.</span></span>                |
| <span data-ttu-id="d9906-137">Fotos</span><span class="sxs-lookup"><span data-stu-id="d9906-137">Photos</span></span>      | `photos`     | <span data-ttu-id="d9906-138">La carpeta Fotos.</span><span class="sxs-lookup"><span data-stu-id="d9906-138">The Photos folder.</span></span>                                                       |

## <a name="remarks"></a><span data-ttu-id="d9906-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9906-139">Remarks</span></span> 

<span data-ttu-id="d9906-140">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="d9906-140">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The SpecialFolder facet provides information about folders accessible as special folders.",
  "keywords": "special folder,item,facet",
  "section": "documentation",
  "tocPath": ""
}-->
