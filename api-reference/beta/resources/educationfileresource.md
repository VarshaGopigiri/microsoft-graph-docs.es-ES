---
title: tipo de recurso educationFileResource
description: Una subclase de educationResource que representa un objeto de archivo que está asociado con la asignación o el envío.  En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema. El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.
ms.openlocfilehash: b3ba77b6b9243d987ad1137afe6d2206e47dadaf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087219"
---
# <a name="educationfileresource-resource-type"></a><span data-ttu-id="2da58-105">tipo de recurso educationFileResource</span><span class="sxs-lookup"><span data-stu-id="2da58-105">educationFileResource resource type</span></span>

> <span data-ttu-id="2da58-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2da58-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2da58-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2da58-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2da58-108">Una subclase de [educationResource](educationresource.md) que representa un objeto de archivo que está asociado con la asignación o el envío.</span><span class="sxs-lookup"><span data-stu-id="2da58-108">A subclass of [educationResource](educationresource.md) that represents a file object that is associated with the assignment or submission.</span></span>  <span data-ttu-id="2da58-109">En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="2da58-109">In this case, the file is not one of the special files (Word, Excel, and so on) but is a file that does not have special handling within the system.</span></span> <span data-ttu-id="2da58-110">El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.</span><span class="sxs-lookup"><span data-stu-id="2da58-110">The file resource must be stored in the **resourceFolder** that is associated with the assignment or submission this resource is attached to.</span></span>

## <a name="properties"></a><span data-ttu-id="2da58-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2da58-111">Properties</span></span>
| <span data-ttu-id="2da58-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2da58-112">Property</span></span>     | <span data-ttu-id="2da58-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="2da58-113">Type</span></span>   |<span data-ttu-id="2da58-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2da58-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2da58-115">fileUrl</span><span class="sxs-lookup"><span data-stu-id="2da58-115">fileUrl</span></span>|<span data-ttu-id="2da58-116">String</span><span class="sxs-lookup"><span data-stu-id="2da58-116">String</span></span>|<span data-ttu-id="2da58-117">Ubicación en el disco del recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="2da58-117">Location on disk of the file resource.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2da58-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2da58-118">JSON representation</span></span>

<span data-ttu-id="2da58-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2da58-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFileResource"
}-->

```json
{
  "fileUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationFileResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->