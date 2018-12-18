---
title: tipo de recurso educationSubmissionIndividualRecipient
description: 'Una subclase de educationSubmissionRecipient que indica que se ha asignado un envío a una persona en la clase.  '
author: dipakboyed
ms.openlocfilehash: 3447c91fe4f387508a3afdf80a7337786d46f860
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318805"
---
# <a name="educationsubmissionindividualrecipient-resource-type"></a><span data-ttu-id="7663f-103">tipo de recurso educationSubmissionIndividualRecipient</span><span class="sxs-lookup"><span data-stu-id="7663f-103">educationSubmissionIndividualRecipient resource type</span></span>

> <span data-ttu-id="7663f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7663f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7663f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7663f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7663f-106">Una subclase de [educationSubmissionRecipient](educationsubmissionrecipient.md) que indica que se ha asignado un envío a una persona en la clase.</span><span class="sxs-lookup"><span data-stu-id="7663f-106">A subclass of [educationSubmissionRecipient](educationsubmissionrecipient.md) that indicates that a submission is assigned to an individual in the class.</span></span>  


## <a name="properties"></a><span data-ttu-id="7663f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7663f-107">Properties</span></span>
| <span data-ttu-id="7663f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7663f-108">Property</span></span>     | <span data-ttu-id="7663f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7663f-109">Type</span></span>   |<span data-ttu-id="7663f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7663f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7663f-111">userId</span><span class="sxs-lookup"><span data-stu-id="7663f-111">userId</span></span>|<span data-ttu-id="7663f-112">String</span><span class="sxs-lookup"><span data-stu-id="7663f-112">String</span></span>|<span data-ttu-id="7663f-113">Identificador de usuario del usuario a quien se asigna el envío.</span><span class="sxs-lookup"><span data-stu-id="7663f-113">User ID of the user to whom the submission is assigned.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7663f-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7663f-114">JSON representation</span></span>

<span data-ttu-id="7663f-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7663f-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmissionIndividualRecipient"
}-->

```json
{
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmissionIndividualRecipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->