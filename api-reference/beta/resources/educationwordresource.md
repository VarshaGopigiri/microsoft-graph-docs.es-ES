---
title: tipo de recurso educationWordResource
description: 'Una subclase de educationResource. Éste es un recurso de documento de Word. Se debe cargar el archivo de palabras en el directorio **fileResource** asociado con el '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: d67f77774b9d3c428fcfd98006115f0459989fdc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948320"
---
# <a name="educationwordresource-resource-type"></a><span data-ttu-id="9279e-105">tipo de recurso educationWordResource</span><span class="sxs-lookup"><span data-stu-id="9279e-105">educationWordResource resource type</span></span>

> <span data-ttu-id="9279e-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9279e-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9279e-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9279e-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9279e-108">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="9279e-108">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="9279e-109">Éste es un recurso de documento de Word.</span><span class="sxs-lookup"><span data-stu-id="9279e-109">This is a Word document resource.</span></span> <span data-ttu-id="9279e-110">En el directorio **fileResource** asociado con la asignación o el envío, se debe cargar el archivo de Word.</span><span class="sxs-lookup"><span data-stu-id="9279e-110">The Word file must be uploaded in the **fileResource** directory associated with the assignment or submission.</span></span>


## <a name="properties"></a><span data-ttu-id="9279e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9279e-111">Properties</span></span>
| <span data-ttu-id="9279e-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9279e-112">Property</span></span>     | <span data-ttu-id="9279e-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="9279e-113">Type</span></span>   |<span data-ttu-id="9279e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9279e-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9279e-115">fileUrl</span><span class="sxs-lookup"><span data-stu-id="9279e-115">fileUrl</span></span>|<span data-ttu-id="9279e-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="9279e-116">String</span></span>|<span data-ttu-id="9279e-117">Ubicación del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="9279e-117">Location of the file on disk.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9279e-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9279e-118">JSON representation</span></span>

<span data-ttu-id="9279e-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9279e-119">The following is a JSON representation of the resource.</span></span>

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
