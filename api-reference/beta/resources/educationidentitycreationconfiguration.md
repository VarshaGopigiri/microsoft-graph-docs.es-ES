---
title: tipo de recurso educationIdentityCreationConfiguration
description: Define la configuración de creación de identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se crearán en el directorio.
ms.openlocfilehash: edbfa03bb574a1d8d9d4faaa2032ec82f6d20f66
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090163"
---
## <a name="educationidentitycreationconfiguration-resource-type"></a><span data-ttu-id="dc859-105">tipo de recurso educationIdentityCreationConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc859-105">educationIdentityCreationConfiguration resource type</span></span>

> <span data-ttu-id="dc859-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc859-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc859-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc859-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dc859-108">Define la configuración de creación de identidades de perfil de datos de school.</span><span class="sxs-lookup"><span data-stu-id="dc859-108">Defines the settings on creation of school data profile identities.</span></span> <span data-ttu-id="dc859-109">Estas identidades incluyen estudiantes y profesores.</span><span class="sxs-lookup"><span data-stu-id="dc859-109">These identities include students and teachers.</span></span> <span data-ttu-id="dc859-110">En función de esta configuración, los usuarios se crearán en el directorio.</span><span class="sxs-lookup"><span data-stu-id="dc859-110">Based on these settings, the users will be created in the directory.</span></span>

> <span data-ttu-id="dc859-111">**Nota:** Si ha activado para la sincronización entre local de Active Directory y Azure Active Directory (AD Azure) de sincronización de directorios, use el recurso [educationIdentityMatchingConfiguration](educationidentitymatchingconfiguration.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dc859-111">**Note:** If you have directory sync turned on to sync between on-premises Active Directory and Azure Active Directory (Azure AD), use the [educationIdentityMatchingConfiguration](educationidentitymatchingconfiguration.md) resource instead.</span></span>

<span data-ttu-id="dc859-112">Deriva de [educationIdentitySynchronizationConfiguration](educationidentitysynchronizationconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="dc859-112">Derived from [educationIdentitySynchronizationConfiguration](educationidentitysynchronizationconfiguration.md).</span></span>

## <a name="properties"></a><span data-ttu-id="dc859-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc859-113">Properties</span></span>

| <span data-ttu-id="dc859-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc859-114">Property</span></span> | <span data-ttu-id="dc859-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc859-115">Type</span></span> | <span data-ttu-id="dc859-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc859-116">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="dc859-117">**userDomains**</span><span class="sxs-lookup"><span data-stu-id="dc859-117">**userDomains**</span></span> | <span data-ttu-id="dc859-118">colección de [educationIdentityDomain](educationidentitydomain.md)</span><span class="sxs-lookup"><span data-stu-id="dc859-118">[educationIdentityDomain](educationidentitydomain.md) collection</span></span> |  <span data-ttu-id="dc859-119">Establece la lista de dominios que se usará por tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="dc859-119">Sets the list of domains to use per user type.</span></span>  |


## <a name="json-representation"></a><span data-ttu-id="dc859-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc859-120">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityCreationConfiguration"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationIdentityCreationConfiguration",
    "userDomains": [
        {
            "@odata.type": "#microsoft.graph.educationIdentityDomain",
        }
    ]
}
```