---
title: tipo de recurso mobileAppTroubleshootingAppUpdateHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c938aa30667f28e65285cfdb365f4b0eab55104a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922273"
---
# <a name="mobileapptroubleshootingappupdatehistory-resource-type"></a><span data-ttu-id="8465b-103">tipo de recurso mobileAppTroubleshootingAppUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="8465b-103">mobileAppTroubleshootingAppUpdateHistory resource type</span></span>

> <span data-ttu-id="8465b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8465b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8465b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8465b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8465b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8465b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8465b-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="8465b-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="8465b-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="8465b-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8465b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8465b-109">Properties</span></span>
|<span data-ttu-id="8465b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8465b-110">Property</span></span>|<span data-ttu-id="8465b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8465b-111">Type</span></span>|<span data-ttu-id="8465b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8465b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8465b-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="8465b-113">occurrenceDateTime</span></span>|<span data-ttu-id="8465b-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8465b-114">DateTimeOffset</span></span>|<span data-ttu-id="8465b-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="8465b-115">Time when the history item occurred.</span></span> <span data-ttu-id="8465b-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="8465b-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="8465b-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8465b-117">Relationships</span></span>
<span data-ttu-id="8465b-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8465b-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8465b-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8465b-119">JSON Representation</span></span>
<span data-ttu-id="8465b-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8465b-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingAppUpdateHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingAppUpdateHistory",
  "occurrenceDateTime": "String (timestamp)"
}
```





