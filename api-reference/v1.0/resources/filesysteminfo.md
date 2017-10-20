---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FileSystemInfo
ms.openlocfilehash: 9a5214f9c5e161de0be66ac634c7c5538b203772
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="filesysteminfo-facet"></a><span data-ttu-id="6c993-102">Faceta FileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="6c993-102">FileSystemInfo facet</span></span>

<span data-ttu-id="6c993-103">El recurso **FileSystemInfo** contiene propiedades que aparecen en el sistema de archivos local del dispositivo de la versión local de un elemento.</span><span class="sxs-lookup"><span data-stu-id="6c993-103">The **FileSystemInfo** resource contains properties that are reported by the device's local file system for the local version of an item. This facet can be used to specify the last modified date or created date of the item as it was on the local device.</span></span>
<span data-ttu-id="6c993-104">Esta faceta se puede usar para especificar la fecha de la última modificación o de creación del elemento tal y como estaba en el dispositivo local.</span><span class="sxs-lookup"><span data-stu-id="6c993-104">The FileSystemInfo facet contains properties that are reported by the device's local file system for the local version of an item. This facet can be used to specify the last modified date or created date of the item as it was on the local device.</span></span>

<span data-ttu-id="6c993-105">Está disponible en la propiedad fileSystemInfo de los recursos [driveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="6c993-105">It is available on the fileSystemInfo property of [driveItem][item-resource] resources.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6c993-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6c993-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "lastAccessedDateTime"
  ],
  "@odata.type": "microsoft.graph.fileSystemInfo"
}-->

```json
{
  "createdDateTime" : "datetime",
  "lastAccessedDateTime": "datetime",
  "lastModifiedDateTime" : "datetime"
}
```

## <a name="properties"></a><span data-ttu-id="6c993-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c993-107">Properties</span></span>

| <span data-ttu-id="6c993-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c993-108">Property</span></span>                 | <span data-ttu-id="6c993-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c993-109">Type</span></span>           | <span data-ttu-id="6c993-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c993-110">Description</span></span>                                                                                                          |
| :----------------------- | :------------- | :------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="6c993-111">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="6c993-111">**createdDateTime**</span></span>      | <span data-ttu-id="6c993-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c993-112">DateTimeOffset</span></span> | <span data-ttu-id="6c993-113">La fecha y la hora UTC de creación del archivo en un cliente.</span><span class="sxs-lookup"><span data-stu-id="6c993-113">The UTC date and time the file was created on a client.</span></span>                                                              |
| <span data-ttu-id="6c993-114">**lastAccessedDateTime**</span><span class="sxs-lookup"><span data-stu-id="6c993-114">**lastAccessedDateTime**</span></span> | <span data-ttu-id="6c993-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c993-115">DateTimeOffset</span></span> | <span data-ttu-id="6c993-116">La fecha y la hora UTC del último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="6c993-116">The UTC date and time the file was last accessed on a client.</span></span> <span data-ttu-id="6c993-117">Solo disponible para la [lista de archivos recientes](../api/drive_recent.md).</span><span class="sxs-lookup"><span data-stu-id="6c993-117">Available for the [recent file list](../api/drive_recent.md) only.</span></span> |
| <span data-ttu-id="6c993-118">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="6c993-118">**lastModifiedDateTime**</span></span> | <span data-ttu-id="6c993-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c993-119">DateTimeOffset</span></span> | <span data-ttu-id="6c993-120">La fecha y la hora UTC en que se ha modificado por última vez el archivo en un cliente.</span><span class="sxs-lookup"><span data-stu-id="6c993-120">The UTC date and time the file was last modified on a client.</span></span>                                                        |

## <a name="notes"></a><span data-ttu-id="6c993-121">Notas</span><span class="sxs-lookup"><span data-stu-id="6c993-121">Notes</span></span>

<span data-ttu-id="6c993-122">Los valores de **createdDateTime** y **lastModifiedDateTime** varían de las mismas propiedades en el recurso [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="6c993-122">Values for **createdDateTime** and **lastModifiedDateTime** vary from the same properties on the [DriveItem](driveitem.md) resource.</span></span>
<span data-ttu-id="6c993-123">Los valores del recurso DriveItem son la fecha y hora de creación y modificación como se ve desde el servicio.</span><span class="sxs-lookup"><span data-stu-id="6c993-123">The properties on the driveItem resource are the created and modified date and time from the perspective of when the service saw the file.</span></span>
<span data-ttu-id="6c993-124">Los valores almacenados en el recurso **FileSystemInfo** los proporciona el cliente.</span><span class="sxs-lookup"><span data-stu-id="6c993-124">The values stored in the **FileSystemInfo** facet are provided by the client are are the values displayed to the user if they exist.</span></span>

<span data-ttu-id="6c993-125">Por ejemplo, si un archivo se ha creado en el dispositivo el lunes, pero no se ha cargado al servicio hasta el martes, el cliente que carga el archivo debe escribir la faceta `fileSystemInfo` para incluir la fecha de creación del lunes.</span><span class="sxs-lookup"><span data-stu-id="6c993-125">For example, if a file was created on the device on Monday, but not uploaded to the service until Tuesday, the client that uploads the file should write the `fileSystemInfo` facet to include the created date on Monday. When the item metadata is retrieved, the created date for the item will reflect Tuesday, but the  facet will show the original created date on Monday.</span></span> <span data-ttu-id="6c993-126">Cuando se recuperan los metadatos del elemento, la fecha de creación del elemento reflejará el martes, pero la faceta `fileSystemInfo` mostrará la fecha de creación original del lunes.</span><span class="sxs-lookup"><span data-stu-id="6c993-126">When the item metadata is retrieved, the created date for the item will reflect Tuesday, but the `fileSystemInfo` facet will show the original created date on Monday.</span></span>

<span data-ttu-id="6c993-p105">Estas propiedades son de lectura y escritura. Si está cargando un archivo y conoce los valores del cliente local de estos campos, debe incluirlos en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c993-p105">These properties are read/write. If you are uploading a file and know the local client values for these fields, you should include them in the request.</span></span>

<span data-ttu-id="6c993-129">Si se actualiza el contenido del archivo y no se proporcionan estas propiedades, **lastModifiedDateTime** se restablece a la hora actual de forma automática.</span><span class="sxs-lookup"><span data-stu-id="6c993-129">If the file's content is updated and these properties are not provided, **lastModifiedDateTime** automatically resets to the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c993-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c993-130">Remarks</span></span>

* <span data-ttu-id="6c993-131">**lastAccessedDateTime** no está disponible para elementos en SharePoint Online u OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="6c993-131">**lastAccessedDateTime** is not available for items in SharePoint online, OneDrive for Business, or SharePoint Server 2016.</span></span>

<span data-ttu-id="6c993-132">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="6c993-132">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "The fileSystemInfo facet provides information about date created and modified by clients.",
  "keywords": "fileSystemInfo,client,system info,onedrive",
  "section": "documentation",
  "tocPath": "Facets/FileSystemInfo"
} -->
