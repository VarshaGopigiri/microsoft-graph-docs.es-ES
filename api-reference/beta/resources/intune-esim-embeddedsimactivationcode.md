---
title: tipo de recurso embeddedSIMActivationCode
description: El código de activación SIM incrustado como proporcionada por el operador móvil.
ms.openlocfilehash: ad0b5d9ff2ac06387d81354cf74f2784d4838600
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089093"
---
# <a name="embeddedsimactivationcode-resource-type"></a><span data-ttu-id="47160-103">tipo de recurso embeddedSIMActivationCode</span><span class="sxs-lookup"><span data-stu-id="47160-103">embeddedSIMActivationCode resource type</span></span>

> <span data-ttu-id="47160-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47160-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47160-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47160-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="47160-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47160-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47160-107">El código de activación SIM incrustado como proporcionada por el operador móvil.</span><span class="sxs-lookup"><span data-stu-id="47160-107">The embedded SIM activation code as provided by the mobile operator.</span></span>
## <a name="properties"></a><span data-ttu-id="47160-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47160-108">Properties</span></span>
|<span data-ttu-id="47160-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="47160-109">Property</span></span>|<span data-ttu-id="47160-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="47160-110">Type</span></span>|<span data-ttu-id="47160-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="47160-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="47160-112">integratedCircuitCardIdentifier</span><span class="sxs-lookup"><span data-stu-id="47160-112">integratedCircuitCardIdentifier</span></span>|<span data-ttu-id="47160-113">String</span><span class="sxs-lookup"><span data-stu-id="47160-113">String</span></span>|<span data-ttu-id="47160-114">El identificador de tarjeta de circuito integrado (ICCID) para este de código de activación de SIM incrustado como proporcionado por el operador de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="47160-114">The Integrated Circuit Card Identifier (ICCID) for this embedded SIM activation code as provided by the mobile operator.</span></span>
<span data-ttu-id="47160-115">La entrada debe coincidir con la siguiente expresión regular: ' ^\[0-9\]{19}\[0-9\]?$ '.</span><span class="sxs-lookup"><span data-stu-id="47160-115">The input must match the following regular expression: '^\[0-9\]{19}\[0-9\]?$'.</span></span>|
|<span data-ttu-id="47160-116">matchingIdentifier</span><span class="sxs-lookup"><span data-stu-id="47160-116">matchingIdentifier</span></span>|<span data-ttu-id="47160-117">String</span><span class="sxs-lookup"><span data-stu-id="47160-117">String</span></span>|<span data-ttu-id="47160-118">MatchingIdentifier (MatchingID) tal como se especifica en la GSMA asociación SGP.22 RSP especificación técnica sección 4.1.</span><span class="sxs-lookup"><span data-stu-id="47160-118">The MatchingIdentifier (MatchingID) as specified in the GSMA Association SGP.22 RSP Technical Specification section 4.1.</span></span>
<span data-ttu-id="47160-119">La entrada debe coincidir con la siguiente expresión regular: ' ^\[a-zA-Z0-9\-\]\* $'.</span><span class="sxs-lookup"><span data-stu-id="47160-119">The input must match the following regular expression: '^\[a-zA-Z0-9\-\]\*$'.</span></span>|
|<span data-ttu-id="47160-120">smdpPlusServerAddress</span><span class="sxs-lookup"><span data-stu-id="47160-120">smdpPlusServerAddress</span></span>|<span data-ttu-id="47160-121">String</span><span class="sxs-lookup"><span data-stu-id="47160-121">String</span></span>|<span data-ttu-id="47160-122">El nombre de dominio completo de la SM-DP + servidor tal como se especifica en la especificación técnica de GSM asociación SPG.22 RSP.</span><span class="sxs-lookup"><span data-stu-id="47160-122">The fully qualified domain name of the SM-DP+ server as specified in the GSM Association SPG .22 RSP Technical Specification.</span></span>
<span data-ttu-id="47160-123">La entrada debe coincidir con la siguiente expresión regular: ' ^ (\[a-zA-Z0-9\]+(-\[a-zA-Z0-9\]+) \*\.) +\[a-zA-Z\]{2,}$'.</span><span class="sxs-lookup"><span data-stu-id="47160-123">The input must match the following regular expression: '^(\[a-zA-Z0-9\]+(-\[a-zA-Z0-9\]+)\*\.)+\[a-zA-Z\]{2,}$'.</span></span>|

## <a name="relationships"></a><span data-ttu-id="47160-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="47160-124">Relationships</span></span>
<span data-ttu-id="47160-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="47160-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="47160-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="47160-126">JSON Representation</span></span>
<span data-ttu-id="47160-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="47160-127">Here is a JSON representation of the resource.</span></span>
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





