---
title: tipo de recurso mobileAppTroubleshootingAppPolicyCreationHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
ms.openlocfilehash: 7ca80443351e5c1b1232dc050cdf721ab7389351
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089465"
---
# <a name="mobileapptroubleshootingapppolicycreationhistory-resource-type"></a><span data-ttu-id="53153-103">tipo de recurso mobileAppTroubleshootingAppPolicyCreationHistory</span><span class="sxs-lookup"><span data-stu-id="53153-103">mobileAppTroubleshootingAppPolicyCreationHistory resource type</span></span>

> <span data-ttu-id="53153-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53153-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53153-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53153-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="53153-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53153-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53153-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="53153-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="53153-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="53153-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="53153-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53153-109">Properties</span></span>
|<span data-ttu-id="53153-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53153-110">Property</span></span>|<span data-ttu-id="53153-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="53153-111">Type</span></span>|<span data-ttu-id="53153-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="53153-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53153-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="53153-113">occurrenceDateTime</span></span>|<span data-ttu-id="53153-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53153-114">DateTimeOffset</span></span>|<span data-ttu-id="53153-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="53153-115">Time when the history item occurred.</span></span> <span data-ttu-id="53153-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="53153-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|
|<span data-ttu-id="53153-117">runState</span><span class="sxs-lookup"><span data-stu-id="53153-117">runState</span></span>|[<span data-ttu-id="53153-118">runState</span><span class="sxs-lookup"><span data-stu-id="53153-118">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="53153-119">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="53153-119">Status of the item.</span></span> <span data-ttu-id="53153-120">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="53153-120">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="53153-121">errorCode</span><span class="sxs-lookup"><span data-stu-id="53153-121">errorCode</span></span>|<span data-ttu-id="53153-122">String</span><span class="sxs-lookup"><span data-stu-id="53153-122">String</span></span>|<span data-ttu-id="53153-123">Código de error para el error, vacío si no hay error.</span><span class="sxs-lookup"><span data-stu-id="53153-123">Error code for the failure, empty if no failure.</span></span>|

## <a name="relationships"></a><span data-ttu-id="53153-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53153-124">Relationships</span></span>
<span data-ttu-id="53153-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="53153-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="53153-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53153-126">JSON Representation</span></span>
<span data-ttu-id="53153-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="53153-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingAppPolicyCreationHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingAppPolicyCreationHistory",
  "occurrenceDateTime": "String (timestamp)",
  "runState": "String",
  "errorCode": "String"
}
```





