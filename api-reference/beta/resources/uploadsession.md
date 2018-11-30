---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: UploadSession
ms.openlocfilehash: 27e3b448b54df0a5d35e2992391a554b73fd2c42
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091077"
---
# <a name="uploadsession-resource"></a><span data-ttu-id="413ac-102">Recurso UploadSession</span><span class="sxs-lookup"><span data-stu-id="413ac-102">UploadSession resource</span></span>

> <span data-ttu-id="413ac-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="413ac-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="413ac-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="413ac-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="413ac-105">El recurso **UploadSession** proporciona información sobre cómo cargar archivos grandes en las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="413ac-105">The **UploadSession** resource provides information about how to upload large files to OneDrive, OneDrive for Business, or SharePoint document libraries.</span></span>

## <a name="json-representation"></a><span data-ttu-id="413ac-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="413ac-106">JSON representation</span></span>

<span data-ttu-id="413ac-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="413ac-107">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="413ac-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="413ac-108">Properties</span></span>


| <span data-ttu-id="413ac-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="413ac-109">Property</span></span>       | <span data-ttu-id="413ac-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="413ac-110">Type</span></span>              |<span data-ttu-id="413ac-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="413ac-111">Description</span></span>
|:-------------------|:------------------|:------------------------------------
| <span data-ttu-id="413ac-112">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="413ac-112">expirationDateTime</span></span> | <span data-ttu-id="413ac-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="413ac-113">DateTimeOffset</span></span>    | <span data-ttu-id="413ac-p102">La fecha y hora en UTC en que caducará la sesión de carga. Debe cargarse el archivo completo antes de esta fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="413ac-p102">The date and time in UTC that the upload session will expire. The complete file must be uploaded before this expiration time is reached.</span></span>
| <span data-ttu-id="413ac-116">nextExpectedRanges</span><span class="sxs-lookup"><span data-stu-id="413ac-116">nextExpectedRanges</span></span> | <span data-ttu-id="413ac-117">Colección String</span><span class="sxs-lookup"><span data-stu-id="413ac-117">String collection</span></span> | <span data-ttu-id="413ac-p103">Una colección de intervalos de bytes que el servidor no encuentra para el archivo. Estos intervalos están indexados con cero y tienen el formato "inicio-fin" (p. ej. "0-26" para indicar los 27 primeros bytes del archivo).</span><span class="sxs-lookup"><span data-stu-id="413ac-p103">A collection of byte ranges that the server is missing for the file. These ranges are zero indexed and of the format "start-end" (e.g. "0-26" to indicate the first 27 bytes of the file).</span></span>
| <span data-ttu-id="413ac-120">uploadUrl</span><span class="sxs-lookup"><span data-stu-id="413ac-120">uploadUrl</span></span>          | <span data-ttu-id="413ac-121">String</span><span class="sxs-lookup"><span data-stu-id="413ac-121">String</span></span>            | <span data-ttu-id="413ac-122">El extremo de la dirección URL que acepta las solicitudes PUT de los intervalos de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="413ac-122">The URL endpoint that accepts PUT requests for byte ranges of the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="413ac-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="413ac-123">See also</span></span>

- [<span data-ttu-id="413ac-124">Cargar archivos de gran tamaño con una sesión de carga</span><span class="sxs-lookup"><span data-stu-id="413ac-124">Upload large files with an upload session</span></span>](../api/driveitem-createuploadsession.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "UploadSession is used to provide information about large file uploads.",
  "section": "documentation",
  "tocPath": "Resources/UploadSession"
} -->
