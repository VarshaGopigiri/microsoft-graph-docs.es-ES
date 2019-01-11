---
title: tipo de recurso educationWordResource
description: 'Una subclase de educationResource. Éste es un recurso de documento de Word. Se debe cargar el archivo de palabras en el directorio **fileResource** asociado con el '
localization_priority: Normal
ms.openlocfilehash: 0fa366a6fb6de70d10a010cf5e0e11ffd26a3b94
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805141"
---
# <a name="educationwordresource-resource-type"></a><span data-ttu-id="9dec8-105">tipo de recurso educationWordResource</span><span class="sxs-lookup"><span data-stu-id="9dec8-105">educationWordResource resource type</span></span>

> <span data-ttu-id="9dec8-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9dec8-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9dec8-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9dec8-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9dec8-108">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="9dec8-108">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="9dec8-109">Éste es un recurso de documento de Word.</span><span class="sxs-lookup"><span data-stu-id="9dec8-109">This is a Word document resource.</span></span> <span data-ttu-id="9dec8-110">En el directorio **fileResource** asociado con la asignación o el envío, se debe cargar el archivo de Word.</span><span class="sxs-lookup"><span data-stu-id="9dec8-110">The Word file must be uploaded in the **fileResource** directory associated with the assignment or submission.</span></span>


## <a name="properties"></a><span data-ttu-id="9dec8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9dec8-111">Properties</span></span>
| <span data-ttu-id="9dec8-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9dec8-112">Property</span></span>     | <span data-ttu-id="9dec8-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="9dec8-113">Type</span></span>   |<span data-ttu-id="9dec8-114">Description</span><span class="sxs-lookup"><span data-stu-id="9dec8-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9dec8-115">fileUrl</span><span class="sxs-lookup"><span data-stu-id="9dec8-115">fileUrl</span></span>|<span data-ttu-id="9dec8-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="9dec8-116">String</span></span>|<span data-ttu-id="9dec8-117">Ubicación del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="9dec8-117">Location of the file on disk.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9dec8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9dec8-118">JSON representation</span></span>

<span data-ttu-id="9dec8-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9dec8-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationWordResource"
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
  "description": "educationWordResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
