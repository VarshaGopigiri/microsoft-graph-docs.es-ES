---
title: tipo de recurso educationIdentityDomain
description: 'Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario. El recurso de dominio forma parte de la configuración de creación de identidad. '
ms.openlocfilehash: 8298e1eb38ae70f982719ee3a7d6588cd181bdd8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088351"
---
# <a name="educationidentitydomain-resource-type"></a><span data-ttu-id="4fed1-104">tipo de recurso educationIdentityDomain</span><span class="sxs-lookup"><span data-stu-id="4fed1-104">educationIdentityDomain resource type</span></span>

> <span data-ttu-id="4fed1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4fed1-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4fed1-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4fed1-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4fed1-107">Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="4fed1-107">Represents the mapping between an education user type and the domain the user's account belongs to.</span></span> <span data-ttu-id="4fed1-108">El recurso de dominio forma parte de la [configuración de creación de identidad](educationidentitycreationconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4fed1-108">The domain resource is part of the [identity creation configuration](educationidentitycreationconfiguration.md).</span></span> 

## <a name="properties"></a><span data-ttu-id="4fed1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fed1-109">Properties</span></span>

| <span data-ttu-id="4fed1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4fed1-110">Property</span></span> | <span data-ttu-id="4fed1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fed1-111">Type</span></span> | <span data-ttu-id="4fed1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fed1-112">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="4fed1-113">**appliesTo**</span><span class="sxs-lookup"><span data-stu-id="4fed1-113">**appliesTo**</span></span> | <span data-ttu-id="4fed1-114">string</span><span class="sxs-lookup"><span data-stu-id="4fed1-114">string</span></span> |  <span data-ttu-id="4fed1-115">El tipo de función de usuario para asignar a la licencia.</span><span class="sxs-lookup"><span data-stu-id="4fed1-115">The user role type to assign to license.</span></span> <span data-ttu-id="4fed1-116">Los valores posibles son: `student` y `teacher`.</span><span class="sxs-lookup"><span data-stu-id="4fed1-116">Possible values are: `student`, `teacher`.</span></span>      |
| <span data-ttu-id="4fed1-117">**name**</span><span class="sxs-lookup"><span data-stu-id="4fed1-117">**name**</span></span> | <span data-ttu-id="4fed1-118">string</span><span class="sxs-lookup"><span data-stu-id="4fed1-118">string</span></span> |  <span data-ttu-id="4fed1-119">Representa el dominio para la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="4fed1-119">Represents the domain for the user account.</span></span>         |

## <a name="json-representation"></a><span data-ttu-id="4fed1-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4fed1-120">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityDomain"
}-->

```json
{
    "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
    "name": "String"
}
```