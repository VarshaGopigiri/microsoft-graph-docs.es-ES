---
title: tipo de recurso embeddedSIMActivationCode
description: El código de activación SIM incrustado como proporcionada por el operador móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: af8bf020953dbc014f42aa6d363d3ca9e30db8a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987408"
---
# <a name="embeddedsimactivationcode-resource-type"></a><span data-ttu-id="4bbfa-103">tipo de recurso embeddedSIMActivationCode</span><span class="sxs-lookup"><span data-stu-id="4bbfa-103">embeddedSIMActivationCode resource type</span></span>

> <span data-ttu-id="4bbfa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4bbfa-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4bbfa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4bbfa-107">El código de activación SIM incrustado como proporcionada por el operador móvil.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-107">The embedded SIM activation code as provided by the mobile operator.</span></span>
## <a name="properties"></a><span data-ttu-id="4bbfa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bbfa-108">Properties</span></span>
|<span data-ttu-id="4bbfa-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bbfa-109">Property</span></span>|<span data-ttu-id="4bbfa-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bbfa-110">Type</span></span>|<span data-ttu-id="4bbfa-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bbfa-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4bbfa-112">integratedCircuitCardIdentifier</span><span class="sxs-lookup"><span data-stu-id="4bbfa-112">integratedCircuitCardIdentifier</span></span>|<span data-ttu-id="4bbfa-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bbfa-113">String</span></span>|<span data-ttu-id="4bbfa-114">El identificador de tarjeta de circuito integrado (ICCID) para este de código de activación de SIM incrustado como proporcionado por el operador de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-114">The Integrated Circuit Card Identifier (ICCID) for this embedded SIM activation code as provided by the mobile operator.</span></span>
<span data-ttu-id="4bbfa-115">La entrada debe coincidir con la siguiente expresión regular: ' ^\[0-9\]{19}\[0-9\]?$ '.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-115">The input must match the following regular expression: '^\[0-9\]{19}\[0-9\]?$'.</span></span>|
|<span data-ttu-id="4bbfa-116">matchingIdentifier</span><span class="sxs-lookup"><span data-stu-id="4bbfa-116">matchingIdentifier</span></span>|<span data-ttu-id="4bbfa-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bbfa-117">String</span></span>|<span data-ttu-id="4bbfa-118">MatchingIdentifier (MatchingID) tal como se especifica en la GSMA asociación SGP.22 RSP especificación técnica sección 4.1.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-118">The MatchingIdentifier (MatchingID) as specified in the GSMA Association SGP.22 RSP Technical Specification section 4.1.</span></span>
<span data-ttu-id="4bbfa-119">La entrada debe coincidir con la siguiente expresión regular: ' ^\[a-zA-Z0-9\-\]\* $'.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-119">The input must match the following regular expression: '^\[a-zA-Z0-9\-\]\*$'.</span></span>|
|<span data-ttu-id="4bbfa-120">smdpPlusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4bbfa-120">smdpPlusServerAddress</span></span>|<span data-ttu-id="4bbfa-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bbfa-121">String</span></span>|<span data-ttu-id="4bbfa-122">El nombre de dominio completo de la SM-DP + servidor tal como se especifica en la especificación técnica de GSM asociación SPG.22 RSP.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-122">The fully qualified domain name of the SM-DP+ server as specified in the GSM Association SPG .22 RSP Technical Specification.</span></span>
<span data-ttu-id="4bbfa-123">La entrada debe coincidir con la siguiente expresión regular: ' ^ (\[a-zA-Z0-9\]+(-\[a-zA-Z0-9\]+) \*\.) +\[a-zA-Z\]{2,}$'.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-123">The input must match the following regular expression: '^(\[a-zA-Z0-9\]+(-\[a-zA-Z0-9\]+)\*\.)+\[a-zA-Z\]{2,}$'.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4bbfa-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4bbfa-124">Relationships</span></span>
<span data-ttu-id="4bbfa-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4bbfa-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4bbfa-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4bbfa-126">JSON Representation</span></span>
<span data-ttu-id="4bbfa-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4bbfa-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.embeddedSIMActivationCode"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCode",
  "integratedCircuitCardIdentifier": "String",
  "matchingIdentifier": "String",
  "smdpPlusServerAddress": "String"
}
```





