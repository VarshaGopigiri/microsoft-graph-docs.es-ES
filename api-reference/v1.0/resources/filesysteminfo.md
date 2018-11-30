---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FileSystemInfo
ms.openlocfilehash: 2a2e31754e64d18f8fce873212d7c582e6611e60
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031625"
---
# <a name="filesysteminfo-facet"></a><span data-ttu-id="b8c65-102">Faceta FileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="b8c65-102">FileSystemInfo facet</span></span>

<span data-ttu-id="b8c65-p101">El recurso **FileSystemInfo** contiene propiedades que aparecen en el sistema de archivos local del dispositivo de la versión local de un elemento. Esta faceta se puede usar para especificar la fecha de la última modificación o de creación del elemento tal y como estaba en el dispositivo local.</span><span class="sxs-lookup"><span data-stu-id="b8c65-p101">The **FileSystemInfo** resource contains properties that are reported by the device's local file system for the local version of an item. This facet can be used to specify the last modified date or created date of the item as it was on the local device.</span></span>

<span data-ttu-id="b8c65-105">Está disponible en la propiedad fileSystemInfo de los recursos [driveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="b8c65-105">It is available on the fileSystemInfo property of [driveItem][item-resource] resources.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b8c65-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b8c65-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="b8c65-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8c65-107">Properties</span></span>

| <span data-ttu-id="b8c65-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8c65-108">Property</span></span>                 | <span data-ttu-id="b8c65-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c65-109">Type</span></span>           | <span data-ttu-id="b8c65-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8c65-110">Description</span></span>                                                                                                          |
| :----------------------- | :------------- | :------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="b8c65-111">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="b8c65-111">**createdDateTime**</span></span>      | <span data-ttu-id="b8c65-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8c65-112">DateTimeOffset</span></span> | <span data-ttu-id="b8c65-113">La fecha y la hora UTC de creación del archivo en un cliente.</span><span class="sxs-lookup"><span data-stu-id="b8c65-113">The UTC date and time the file was created on a client.</span></span>                                                              |
| <span data-ttu-id="b8c65-114">**lastAccessedDateTime**</span><span class="sxs-lookup"><span data-stu-id="b8c65-114">**lastAccessedDateTime**</span></span> | <span data-ttu-id="b8c65-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8c65-115">DateTimeOffset</span></span> | <span data-ttu-id="b8c65-p102">La fecha y la hora UTC del último acceso al archivo. Solo disponible para la [lista de archivos recientes](../api/drive-recent.md).</span><span class="sxs-lookup"><span data-stu-id="b8c65-p102">The UTC date and time the file was last accessed. Available for the [recent file list](../api/drive-recent.md) only.</span></span> |
| <span data-ttu-id="b8c65-118">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="b8c65-118">**lastModifiedDateTime**</span></span> | <span data-ttu-id="b8c65-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8c65-119">DateTimeOffset</span></span> | <span data-ttu-id="b8c65-120">La fecha y la hora UTC en que se ha modificado por última vez el archivo en un cliente.</span><span class="sxs-lookup"><span data-stu-id="b8c65-120">The UTC date and time the file was last modified on a client.</span></span>                                                        |

## <a name="notes"></a><span data-ttu-id="b8c65-121">Notas</span><span class="sxs-lookup"><span data-stu-id="b8c65-121">Notes</span></span>

<span data-ttu-id="b8c65-p103">Los valores de **createdDateTime** y **lastModifiedDateTime** varían de las mismas propiedades en el recurso [DriveItem](driveitem.md). Los valores del recurso DriveItem son la fecha y hora de creación y modificación como se ve desde el servicio. Los valores almacenados en el recurso **FileSystemInfo** los proporciona el cliente.</span><span class="sxs-lookup"><span data-stu-id="b8c65-p103">Values for **createdDateTime** and **lastModifiedDateTime** vary from the same properties on the [DriveItem](driveitem.md) resource. The values on the DriveItem resource are the created and modified date and time as seen from the service. The values stored in the **FileSystemInfo** resource are provided by the client.</span></span>

<span data-ttu-id="b8c65-p104">Por ejemplo, si un archivo se ha creado en el dispositivo el lunes, pero no se ha cargado al servicio hasta el martes, el cliente que carga el archivo debe escribir la faceta `fileSystemInfo` para incluir la fecha de creación del lunes. Cuando se recuperan los metadatos del elemento, la fecha de creación del elemento reflejará el martes, pero la faceta `fileSystemInfo` mostrará la fecha de creación original del lunes.</span><span class="sxs-lookup"><span data-stu-id="b8c65-p104">For example, if a file was created on the device on Monday, but not uploaded to the service until Tuesday, the client that uploads the file should write the `fileSystemInfo` facet to include the created date on Monday. When the item metadata is retrieved, the created date for the item will reflect Tuesday, but the `fileSystemInfo` facet will show the original created date on Monday.</span></span>

<span data-ttu-id="b8c65-p105">Estas propiedades son de lectura y escritura. Si está cargando un archivo y conoce los valores del cliente local de estos campos, debe incluirlos en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8c65-p105">These properties are read/write. If you are uploading a file and know the local client values for these fields, you should include them in the request.</span></span>

<span data-ttu-id="b8c65-129">Si se actualiza el contenido del archivo y no se proporcionan estas propiedades, **lastModifiedDateTime** se restablece a la hora actual de forma automática.</span><span class="sxs-lookup"><span data-stu-id="b8c65-129">If the file's content is updated and these properties are not provided, **lastModifiedDateTime** automatically resets to the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c65-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8c65-130">Remarks</span></span>

* <span data-ttu-id="b8c65-131">**lastAccessedDateTime** no está disponible para elementos en SharePoint Online u OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="b8c65-131">**lastAccessedDateTime** is not available for items in SharePoint online or OneDrive for Business.</span></span>

<span data-ttu-id="b8c65-132">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="b8c65-132">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "The fileSystemInfo facet provides information about date created and modified by clients.",
  "keywords": "fileSystemInfo,client,system info,onedrive",
  "section": "documentation",
  "tocPath": "Facets/FileSystemInfo"
} -->
