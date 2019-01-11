---
title: tipo de recurso mfaDetail
description: 'Indica los detalles MFA para una sesión específica. Incluye el método de autenticación usado para iniciar sesión, así como detalles de autenticación (por ejemplo: teléfono, SMS o correo de voz) '
localization_priority: Normal
ms.openlocfilehash: 5069045fd202d443a94a80f7333f12ab5e707ada
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883744"
---
# <a name="mfadetail-resource-type"></a><span data-ttu-id="82206-104">tipo de recurso mfaDetail</span><span class="sxs-lookup"><span data-stu-id="82206-104">mfaDetail resource type</span></span>
<span data-ttu-id="82206-105">Indica los detalles MFA para una sesión específica.</span><span class="sxs-lookup"><span data-stu-id="82206-105">Indicates MFA details for a specific sign-in.</span></span> <span data-ttu-id="82206-106">Incluye el método de autenticación usado para iniciar sesión, así como detalles de autenticación (por ejemplo: teléfono, SMS o correo de voz)</span><span class="sxs-lookup"><span data-stu-id="82206-106">It includes the authentication method used for signing in as well as auth details (for example: Phone, SMS or voicemail)</span></span> 



## <a name="properties"></a><span data-ttu-id="82206-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82206-107">Properties</span></span>
| <span data-ttu-id="82206-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82206-108">Property</span></span>     | <span data-ttu-id="82206-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="82206-109">Type</span></span>   |<span data-ttu-id="82206-110">Description</span><span class="sxs-lookup"><span data-stu-id="82206-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="82206-111">authDetail</span><span class="sxs-lookup"><span data-stu-id="82206-111">authDetail</span></span>|<span data-ttu-id="82206-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="82206-112">String</span></span>|<span data-ttu-id="82206-113">Indica el detalle de la autenticación MFA para la actividad de inicio de sesión correspondiente cuando el MFA requerido es "Sí".</span><span class="sxs-lookup"><span data-stu-id="82206-113">Indicates the MFA auth detail for the corresponding Sign-in activity when the MFA Required is "Yes".</span></span>|
|<span data-ttu-id="82206-114">método authMethod</span><span class="sxs-lookup"><span data-stu-id="82206-114">authMethod</span></span>|<span data-ttu-id="82206-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="82206-115">String</span></span>|<span data-ttu-id="82206-116">Indica los métodos de autenticación MFA (SMS, teléfono, aplicación Authenticator son algunas del valor) para la actividad de inicio de sesión correspondiente cuando el campo MFA necesario es "Yes".</span><span class="sxs-lookup"><span data-stu-id="82206-116">Indicates the MFA Auth methods (SMS, Phone, Authenticator App are some of the value) for the corresponding sign-in activity when the MFA Required field is "Yes".</span></span>|

## <a name="json-representation"></a><span data-ttu-id="82206-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82206-117">JSON representation</span></span>

<span data-ttu-id="82206-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="82206-118">Here is a JSON representation of the resource.</span></span>

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
