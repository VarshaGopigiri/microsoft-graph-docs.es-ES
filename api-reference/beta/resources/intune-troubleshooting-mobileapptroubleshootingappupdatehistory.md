---
title: tipo de recurso mobileAppTroubleshootingAppUpdateHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 26ca343f761853bba05fa9905737b7fddf6ab3ec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870682"
---
# <a name="mobileapptroubleshootingappupdatehistory-resource-type"></a><span data-ttu-id="2fdb6-103">tipo de recurso mobileAppTroubleshootingAppUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="2fdb6-103">mobileAppTroubleshootingAppUpdateHistory resource type</span></span>

> <span data-ttu-id="2fdb6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2fdb6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2fdb6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2fdb6-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="2fdb6-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="2fdb6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fdb6-109">Properties</span></span>
|<span data-ttu-id="2fdb6-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fdb6-110">Property</span></span>|<span data-ttu-id="2fdb6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fdb6-111">Type</span></span>|<span data-ttu-id="2fdb6-112">Description</span><span class="sxs-lookup"><span data-stu-id="2fdb6-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2fdb6-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="2fdb6-113">occurrenceDateTime</span></span>|<span data-ttu-id="2fdb6-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2fdb6-114">DateTimeOffset</span></span>|<span data-ttu-id="2fdb6-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-115">Time when the history item occurred.</span></span> <span data-ttu-id="2fdb6-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="2fdb6-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2fdb6-117">Relationships</span></span>
<span data-ttu-id="2fdb6-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2fdb6-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2fdb6-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2fdb6-119">JSON Representation</span></span>
<span data-ttu-id="2fdb6-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-120">Here is a JSON representation of the resource.</span></span>
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





