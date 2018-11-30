---
title: tipo de recurso educationPowerPointResource
description: 'Una subclase de educationResource. Éste es un recurso de PowerPoint. Se debe cargar el archivo de PowerPoint en el directorio **fileResource** asociado con el '
ms.openlocfilehash: a83a78449ecb7c64f62557ddfa642ab02b55c206
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088543"
---
# <a name="educationpowerpointresource-resource-type"></a><span data-ttu-id="3afad-105">tipo de recurso educationPowerPointResource</span><span class="sxs-lookup"><span data-stu-id="3afad-105">educationPowerPointResource resource type</span></span>

> <span data-ttu-id="3afad-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3afad-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3afad-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3afad-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3afad-108">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="3afad-108">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="3afad-109">Éste es un recurso de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="3afad-109">This is a PowerPoint resource.</span></span> <span data-ttu-id="3afad-110">En el directorio **fileResource** asociado con la asignación o el envío, se debe cargar el archivo de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="3afad-110">The PowerPoint file must be uploaded in the **fileResource** directory associated with the assignment or submission.</span></span>


## <a name="properties"></a><span data-ttu-id="3afad-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3afad-111">Properties</span></span>
| <span data-ttu-id="3afad-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3afad-112">Property</span></span>     | <span data-ttu-id="3afad-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="3afad-113">Type</span></span>   |<span data-ttu-id="3afad-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3afad-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3afad-115">fileUrl</span><span class="sxs-lookup"><span data-stu-id="3afad-115">fileUrl</span></span>|<span data-ttu-id="3afad-116">String</span><span class="sxs-lookup"><span data-stu-id="3afad-116">String</span></span>|<span data-ttu-id="3afad-117">Ubicación del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="3afad-117">Location of the file on disk.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3afad-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3afad-118">JSON representation</span></span>

<span data-ttu-id="3afad-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3afad-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationPowerPointResource"
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
  "description": "educationPowerPointResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->