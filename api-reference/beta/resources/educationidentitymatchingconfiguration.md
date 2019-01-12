---
title: tipo de recurso educationIdentityMatchingConfiguration
description: Define la configuración para que coincidan con las identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se actualizará en el directorio.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 9ee9f58c2f69882361ee105a1d7531bb5756e165
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977552"
---
## <a name="educationidentitymatchingconfiguration-resource-type"></a><span data-ttu-id="96943-105">tipo de recurso educationIdentityMatchingConfiguration</span><span class="sxs-lookup"><span data-stu-id="96943-105">educationIdentityMatchingConfiguration resource type</span></span>

> <span data-ttu-id="96943-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96943-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96943-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96943-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="96943-108">Define la configuración para que coincidan con las identidades de perfil de datos de school.</span><span class="sxs-lookup"><span data-stu-id="96943-108">Defines the settings for matching school data profile identities.</span></span> <span data-ttu-id="96943-109">Estas identidades incluyen estudiantes y profesores.</span><span class="sxs-lookup"><span data-stu-id="96943-109">These identities include students and teachers.</span></span> <span data-ttu-id="96943-110">En función de esta configuración, los usuarios se actualizará en el directorio.</span><span class="sxs-lookup"><span data-stu-id="96943-110">Based on these settings, the users will be updated in the directory.</span></span>

> <span data-ttu-id="96943-111">**Nota:** Ningún usuario se crea cuando se selecciona este recurso.</span><span class="sxs-lookup"><span data-stu-id="96943-111">**Note:** No users are created when this resource is selected.</span></span>

## <a name="properties"></a><span data-ttu-id="96943-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96943-112">Properties</span></span>

| <span data-ttu-id="96943-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96943-113">Property</span></span> | <span data-ttu-id="96943-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="96943-114">Type</span></span> | <span data-ttu-id="96943-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="96943-115">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="96943-116">**matchingOptions**</span><span class="sxs-lookup"><span data-stu-id="96943-116">**matchingOptions**</span></span> | <span data-ttu-id="96943-117">colección de [educationIdentityMatchingOptions](educationidentitymatchingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="96943-117">[educationIdentityMatchingOptions](educationidentitymatchingoptions.md) collection</span></span> | <span data-ttu-id="96943-118">Asignación entre la cuenta de usuario y las opciones para usar para identificar de forma única al usuario que actualice.</span><span class="sxs-lookup"><span data-stu-id="96943-118">Mapping between the user account and the options to use to uniquely identify the user to update.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="96943-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96943-119">JSON representation</span></span>
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
