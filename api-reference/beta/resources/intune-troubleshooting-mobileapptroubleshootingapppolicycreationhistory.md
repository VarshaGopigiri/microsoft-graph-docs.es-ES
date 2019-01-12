---
title: tipo de recurso mobileAppTroubleshootingAppPolicyCreationHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0ee2088856c9c47771b3e647615f82fe26dfd552
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924394"
---
# <a name="mobileapptroubleshootingapppolicycreationhistory-resource-type"></a><span data-ttu-id="ec103-103">tipo de recurso mobileAppTroubleshootingAppPolicyCreationHistory</span><span class="sxs-lookup"><span data-stu-id="ec103-103">mobileAppTroubleshootingAppPolicyCreationHistory resource type</span></span>

> <span data-ttu-id="ec103-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec103-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec103-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec103-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ec103-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec103-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec103-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="ec103-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="ec103-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="ec103-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ec103-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec103-109">Properties</span></span>
|<span data-ttu-id="ec103-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec103-110">Property</span></span>|<span data-ttu-id="ec103-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec103-111">Type</span></span>|<span data-ttu-id="ec103-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec103-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec103-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="ec103-113">occurrenceDateTime</span></span>|<span data-ttu-id="ec103-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ec103-114">DateTimeOffset</span></span>|<span data-ttu-id="ec103-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="ec103-115">Time when the history item occurred.</span></span> <span data-ttu-id="ec103-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="ec103-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|
|<span data-ttu-id="ec103-117">runState</span><span class="sxs-lookup"><span data-stu-id="ec103-117">runState</span></span>|[<span data-ttu-id="ec103-118">runState</span><span class="sxs-lookup"><span data-stu-id="ec103-118">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="ec103-119">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ec103-119">Status of the item.</span></span> <span data-ttu-id="ec103-120">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="ec103-120">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="ec103-121">errorCode</span><span class="sxs-lookup"><span data-stu-id="ec103-121">errorCode</span></span>|<span data-ttu-id="ec103-122">String</span><span class="sxs-lookup"><span data-stu-id="ec103-122">String</span></span>|<span data-ttu-id="ec103-123">Código de error para el error, vacío si no hay error.</span><span class="sxs-lookup"><span data-stu-id="ec103-123">Error code for the failure, empty if no failure.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ec103-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ec103-124">Relationships</span></span>
<span data-ttu-id="ec103-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ec103-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ec103-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec103-126">JSON Representation</span></span>
<span data-ttu-id="ec103-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ec103-127">Here is a JSON representation of the resource.</span></span>
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





