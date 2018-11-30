---
title: tipo de recurso educationIdentityMatchingConfiguration
description: Define la configuración para que coincidan con las identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se actualizará en el directorio.
ms.openlocfilehash: b189735340c121a56c48ae21518989cf8e1634f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090286"
---
## <a name="educationidentitymatchingconfiguration-resource-type"></a><span data-ttu-id="303c5-105">tipo de recurso educationIdentityMatchingConfiguration</span><span class="sxs-lookup"><span data-stu-id="303c5-105">educationIdentityMatchingConfiguration resource type</span></span>

> <span data-ttu-id="303c5-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="303c5-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="303c5-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="303c5-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="303c5-108">Define la configuración para que coincidan con las identidades de perfil de datos de school.</span><span class="sxs-lookup"><span data-stu-id="303c5-108">Defines the settings for matching school data profile identities.</span></span> <span data-ttu-id="303c5-109">Estas identidades incluyen estudiantes y profesores.</span><span class="sxs-lookup"><span data-stu-id="303c5-109">These identities include students and teachers.</span></span> <span data-ttu-id="303c5-110">En función de esta configuración, los usuarios se actualizará en el directorio.</span><span class="sxs-lookup"><span data-stu-id="303c5-110">Based on these settings, the users will be updated in the directory.</span></span>

> <span data-ttu-id="303c5-111">**Nota:** Ningún usuario se crea cuando se selecciona este recurso.</span><span class="sxs-lookup"><span data-stu-id="303c5-111">**Note:** No users are created when this resource is selected.</span></span>

## <a name="properties"></a><span data-ttu-id="303c5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="303c5-112">Properties</span></span>

| <span data-ttu-id="303c5-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="303c5-113">Property</span></span> | <span data-ttu-id="303c5-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="303c5-114">Type</span></span> | <span data-ttu-id="303c5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="303c5-115">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="303c5-116">**matchingOptions**</span><span class="sxs-lookup"><span data-stu-id="303c5-116">**matchingOptions**</span></span> | <span data-ttu-id="303c5-117">colección de [educationIdentityMatchingOptions](educationidentitymatchingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="303c5-117">[educationIdentityMatchingOptions](educationidentitymatchingoptions.md) collection</span></span> | <span data-ttu-id="303c5-118">Asignación entre la cuenta de usuario y las opciones para usar para identificar de forma única al usuario que actualice.</span><span class="sxs-lookup"><span data-stu-id="303c5-118">Mapping between the user account and the options to use to uniquely identify the user to update.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="303c5-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="303c5-119">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityMatchingConfiguration"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationIdentityMatchingConfiguration",
    "matchingOptions": [
        {
            "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
            "sourcePropertyName": "String",
            "targetPropertyName": "String",
            "targetDomain": "String"
        }
    ]
}
```
