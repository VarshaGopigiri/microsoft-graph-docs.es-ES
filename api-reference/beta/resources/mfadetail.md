---
title: tipo de recurso mfaDetail
description: 'Indica los detalles MFA para una sesión específica. Incluye el método de autenticación usado para iniciar sesión, así como detalles de autenticación (por ejemplo: teléfono, SMS o correo de voz) '
ms.openlocfilehash: a377c8648ebc8a6e3eb10fb6b0b87df066f8f2cc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086421"
---
# <a name="mfadetail-resource-type"></a><span data-ttu-id="5db47-104">tipo de recurso mfaDetail</span><span class="sxs-lookup"><span data-stu-id="5db47-104">mfaDetail resource type</span></span>
<span data-ttu-id="5db47-105">Indica los detalles MFA para una sesión específica.</span><span class="sxs-lookup"><span data-stu-id="5db47-105">Indicates MFA details for a specific sign-in.</span></span> <span data-ttu-id="5db47-106">Incluye el método de autenticación usado para iniciar sesión, así como detalles de autenticación (por ejemplo: teléfono, SMS o correo de voz)</span><span class="sxs-lookup"><span data-stu-id="5db47-106">It includes the authentication method used for signing in as well as auth details (for example: Phone, SMS or voicemail)</span></span> 



## <a name="properties"></a><span data-ttu-id="5db47-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5db47-107">Properties</span></span>
| <span data-ttu-id="5db47-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5db47-108">Property</span></span>     | <span data-ttu-id="5db47-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5db47-109">Type</span></span>   |<span data-ttu-id="5db47-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5db47-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5db47-111">authDetail</span><span class="sxs-lookup"><span data-stu-id="5db47-111">authDetail</span></span>|<span data-ttu-id="5db47-112">String</span><span class="sxs-lookup"><span data-stu-id="5db47-112">String</span></span>|<span data-ttu-id="5db47-113">Indica el detalle de la autenticación MFA para la actividad de inicio de sesión correspondiente cuando el MFA requerido es "Sí".</span><span class="sxs-lookup"><span data-stu-id="5db47-113">Indicates the MFA auth detail for the corresponding Sign-in activity when the MFA Required is "Yes".</span></span>|
|<span data-ttu-id="5db47-114">método authMethod</span><span class="sxs-lookup"><span data-stu-id="5db47-114">authMethod</span></span>|<span data-ttu-id="5db47-115">String</span><span class="sxs-lookup"><span data-stu-id="5db47-115">String</span></span>|<span data-ttu-id="5db47-116">Indica los métodos de autenticación MFA (SMS, teléfono, aplicación Authenticator son algunas del valor) para la actividad de inicio de sesión correspondiente cuando el campo MFA necesario es "Yes".</span><span class="sxs-lookup"><span data-stu-id="5db47-116">Indicates the MFA Auth methods (SMS, Phone, Authenticator App are some of the value) for the corresponding sign-in activity when the MFA Required field is "Yes".</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5db47-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5db47-117">JSON representation</span></span>

<span data-ttu-id="5db47-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5db47-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mfaDetail"
}-->

```json
{
  "authDetail": "String",
  "authMethod": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mfaDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->