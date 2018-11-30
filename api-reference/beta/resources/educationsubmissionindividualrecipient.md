---
title: tipo de recurso educationSubmissionIndividualRecipient
description: 'Una subclase de educationSubmissionRecipient que indica que se ha asignado un envío a una persona en la clase.  '
ms.openlocfilehash: 4b74defc1a21427b6169e399262d827561178e5f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083857"
---
# <a name="educationsubmissionindividualrecipient-resource-type"></a><span data-ttu-id="fbe98-103">tipo de recurso educationSubmissionIndividualRecipient</span><span class="sxs-lookup"><span data-stu-id="fbe98-103">educationSubmissionIndividualRecipient resource type</span></span>

> <span data-ttu-id="fbe98-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fbe98-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fbe98-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fbe98-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fbe98-106">Una subclase de [educationSubmissionRecipient](educationsubmissionrecipient.md) que indica que se ha asignado un envío a una persona en la clase.</span><span class="sxs-lookup"><span data-stu-id="fbe98-106">A subclass of [educationSubmissionRecipient](educationsubmissionrecipient.md) that indicates that a submission is assigned to an individual in the class.</span></span>  


## <a name="properties"></a><span data-ttu-id="fbe98-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbe98-107">Properties</span></span>
| <span data-ttu-id="fbe98-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbe98-108">Property</span></span>     | <span data-ttu-id="fbe98-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbe98-109">Type</span></span>   |<span data-ttu-id="fbe98-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbe98-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fbe98-111">userId</span><span class="sxs-lookup"><span data-stu-id="fbe98-111">userId</span></span>|<span data-ttu-id="fbe98-112">String</span><span class="sxs-lookup"><span data-stu-id="fbe98-112">String</span></span>|<span data-ttu-id="fbe98-113">Identificador de usuario del usuario a quien se asigna el envío.</span><span class="sxs-lookup"><span data-stu-id="fbe98-113">User ID of the user to whom the submission is assigned.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fbe98-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fbe98-114">JSON representation</span></span>

<span data-ttu-id="fbe98-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fbe98-115">The following is a JSON representation of the resource.</span></span>

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