---
title: tipo de recurso mobileAppTroubleshootingAppStateHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 65ee72ed0c265f2e989e82dfdcc28d27605d4753
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885571"
---
# <a name="mobileapptroubleshootingappstatehistory-resource-type"></a><span data-ttu-id="39e86-103">tipo de recurso mobileAppTroubleshootingAppStateHistory</span><span class="sxs-lookup"><span data-stu-id="39e86-103">mobileAppTroubleshootingAppStateHistory resource type</span></span>

> <span data-ttu-id="39e86-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39e86-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39e86-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39e86-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="39e86-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39e86-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39e86-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="39e86-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="39e86-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="39e86-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="39e86-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39e86-109">Properties</span></span>
|<span data-ttu-id="39e86-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39e86-110">Property</span></span>|<span data-ttu-id="39e86-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="39e86-111">Type</span></span>|<span data-ttu-id="39e86-112">Description</span><span class="sxs-lookup"><span data-stu-id="39e86-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39e86-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="39e86-113">occurrenceDateTime</span></span>|<span data-ttu-id="39e86-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39e86-114">DateTimeOffset</span></span>|<span data-ttu-id="39e86-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="39e86-115">Time when the history item occurred.</span></span> <span data-ttu-id="39e86-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="39e86-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|
|<span data-ttu-id="39e86-117">actionType</span><span class="sxs-lookup"><span data-stu-id="39e86-117">actionType</span></span>|[<span data-ttu-id="39e86-118">mobileAppActionType</span><span class="sxs-lookup"><span data-stu-id="39e86-118">mobileAppActionType</span></span>](../resources/intune-troubleshooting-mobileappactiontype.md)|<span data-ttu-id="39e86-119">Identificador de grupo de seguridad AAD a la que se ha destinado.</span><span class="sxs-lookup"><span data-stu-id="39e86-119">AAD security group id to which it was targeted.</span></span> <span data-ttu-id="39e86-120">Los valores posibles son: `unknown`, `installCommandSent`, `installed`, `uninstalled` y `userRequestedInstall`.</span><span class="sxs-lookup"><span data-stu-id="39e86-120">Possible values are: `unknown`, `installCommandSent`, `installed`, `uninstalled`, `userRequestedInstall`.</span></span>|
|<span data-ttu-id="39e86-121">runState</span><span class="sxs-lookup"><span data-stu-id="39e86-121">runState</span></span>|[<span data-ttu-id="39e86-122">runState</span><span class="sxs-lookup"><span data-stu-id="39e86-122">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="39e86-123">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="39e86-123">Status of the item.</span></span> <span data-ttu-id="39e86-124">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="39e86-124">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="39e86-125">errorCode</span><span class="sxs-lookup"><span data-stu-id="39e86-125">errorCode</span></span>|<span data-ttu-id="39e86-126">String</span><span class="sxs-lookup"><span data-stu-id="39e86-126">String</span></span>|<span data-ttu-id="39e86-127">Código de error para el error, vacío si no hay error.</span><span class="sxs-lookup"><span data-stu-id="39e86-127">Error code for the failure, empty if no failure.</span></span>|

## <a name="relationships"></a><span data-ttu-id="39e86-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="39e86-128">Relationships</span></span>
<span data-ttu-id="39e86-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="39e86-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="39e86-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="39e86-130">JSON Representation</span></span>
<span data-ttu-id="39e86-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="39e86-131">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingAppStateHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingAppStateHistory",
  "occurrenceDateTime": "String (timestamp)",
  "actionType": "String",
  "runState": "String",
  "errorCode": "String"
}
```





