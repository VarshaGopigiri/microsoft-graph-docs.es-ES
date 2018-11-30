---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: UploadSession
ms.openlocfilehash: d84b588c28791ab8f1cf6cef1be6af767fa18e47
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="uploadsession-resource"></a><span data-ttu-id="602bf-102">Recurso UploadSession</span><span class="sxs-lookup"><span data-stu-id="602bf-102">UploadSession resource</span></span>

<span data-ttu-id="602bf-103">El recurso **UploadSession** proporciona información sobre cómo cargar archivos grandes en las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="602bf-103">The **UploadSession** resource provides information about how to upload large files to OneDrive, OneDrive for Business, or SharePoint document libraries.</span></span>

## <a name="json-representation"></a><span data-ttu-id="602bf-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="602bf-104">JSON representation</span></span>

<span data-ttu-id="602bf-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="602bf-105">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "uploadUrl", "nextExpectedRanges" ],
  "@odata.type": "microsoft.graph.uploadSession"
}-->

```json
{
  "uploadUrl": "https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337",
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["0-"]
}
```

## <a name="properties"></a><span data-ttu-id="602bf-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="602bf-106">Properties</span></span>


| <span data-ttu-id="602bf-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="602bf-107">Property</span></span>       | <span data-ttu-id="602bf-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="602bf-108">Type</span></span>              |<span data-ttu-id="602bf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="602bf-109">Description</span></span>
|:-------------------|:------------------|:------------------------------------
| <span data-ttu-id="602bf-110">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="602bf-110">expirationDateTime</span></span> | <span data-ttu-id="602bf-111">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="602bf-111">DateTimeOffset</span></span>    | <span data-ttu-id="602bf-p101">La fecha y hora en UTC en que caducará la sesión de carga. Debe cargarse el archivo completo antes de esta fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="602bf-p101">The date and time in UTC that the upload session will expire. The complete file must be uploaded before this expiration time is reached.</span></span>
| <span data-ttu-id="602bf-114">nextExpectedRanges</span><span class="sxs-lookup"><span data-stu-id="602bf-114">nextExpectedRanges</span></span> | <span data-ttu-id="602bf-115">Colección string</span><span class="sxs-lookup"><span data-stu-id="602bf-115">String collection</span></span> | <span data-ttu-id="602bf-p102">Una colección de intervalos de bytes que el servidor no encuentra para el archivo. Estos intervalos están indexados con cero y tienen el formato "inicio-fin" (p. ej. "0-26" para indicar los 27 primeros bytes del archivo).</span><span class="sxs-lookup"><span data-stu-id="602bf-p102">A collection of byte ranges that the server is missing for the file. These ranges are zero indexed and of the format "start-end" (e.g. "0-26" to indicate the first 27 bytes of the file).</span></span>
| <span data-ttu-id="602bf-118">uploadUrl</span><span class="sxs-lookup"><span data-stu-id="602bf-118">uploadUrl</span></span>          | <span data-ttu-id="602bf-119">String</span><span class="sxs-lookup"><span data-stu-id="602bf-119">String</span></span>            | <span data-ttu-id="602bf-120">El extremo de la dirección URL que acepta las solicitudes PUT de los intervalos de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="602bf-120">The URL endpoint that accepts PUT requests for byte ranges of the file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="602bf-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="602bf-121">Additional Resources</span></span>

<span data-ttu-id="602bf-122">Consulte [Cargar archivos de gran tamaño con una sesión de carga](../api/driveitem_createuploadsession.md) para obtener más información sobre cómo cargar archivos mediante una sesión de carga.</span><span class="sxs-lookup"><span data-stu-id="602bf-122">See [Upload large files with an upload session](../api/driveitem_createuploadsession.md) for details on how to upload files using an upload session.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "UploadSession is used to provide information about large file uploads.",
  "section": "documentation",
  "tocPath": "Resources/UploadSession"
} -->
