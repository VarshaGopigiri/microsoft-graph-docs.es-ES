---
title: tipo de recurso educationExcelResource
description: 'Una subclase de educationResource. Este tipo de recurso representa un documento de Excel.  '
ms.openlocfilehash: cdd86cf1048863ac3def2ae6be13c3f39b37e642
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090156"
---
# <a name="educationexcelresource-resource-type"></a><span data-ttu-id="67375-104">tipo de recurso educationExcelResource</span><span class="sxs-lookup"><span data-stu-id="67375-104">educationExcelResource resource type</span></span>

> <span data-ttu-id="67375-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="67375-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="67375-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="67375-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="67375-107">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="67375-107">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="67375-108">Este tipo de recurso representa un documento de Excel.</span><span class="sxs-lookup"><span data-stu-id="67375-108">This resource type represents an Excel document.</span></span>  
 
><span data-ttu-id="67375-109">**Nota:** El archivo de Excel debe estar en la carpeta de recursos asociada con el objeto de asignación o el envío al que pertenece este recurso.</span><span class="sxs-lookup"><span data-stu-id="67375-109">**Note:** The Excel file must be in the resource folder associated with the assignment or submission object to which this resource belongs.</span></span>


## <a name="properties"></a><span data-ttu-id="67375-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67375-110">Properties</span></span>
| <span data-ttu-id="67375-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67375-111">Property</span></span>     | <span data-ttu-id="67375-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="67375-112">Type</span></span>   |<span data-ttu-id="67375-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="67375-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="67375-114">fileUrl</span><span class="sxs-lookup"><span data-stu-id="67375-114">fileUrl</span></span>|<span data-ttu-id="67375-115">String</span><span class="sxs-lookup"><span data-stu-id="67375-115">String</span></span>|<span data-ttu-id="67375-116">Puntero al objeto de archivo de Excel.</span><span class="sxs-lookup"><span data-stu-id="67375-116">Pointer to the Excel file object.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="67375-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67375-117">JSON representation</span></span>

<span data-ttu-id="67375-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="67375-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationExcelResource"
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
  "description": "educationExcelResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->