---
title: tipo de recurso mobileAppTroubleshootingDeviceCheckinHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
ms.openlocfilehash: b8050a6d99eeca008477059c9d39a40dbda906a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089247"
---
# <a name="mobileapptroubleshootingdevicecheckinhistory-resource-type"></a><span data-ttu-id="e5298-103">tipo de recurso mobileAppTroubleshootingDeviceCheckinHistory</span><span class="sxs-lookup"><span data-stu-id="e5298-103">mobileAppTroubleshootingDeviceCheckinHistory resource type</span></span>

> <span data-ttu-id="e5298-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5298-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5298-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5298-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e5298-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e5298-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e5298-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="e5298-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="e5298-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="e5298-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e5298-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5298-109">Properties</span></span>
|<span data-ttu-id="e5298-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5298-110">Property</span></span>|<span data-ttu-id="e5298-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5298-111">Type</span></span>|<span data-ttu-id="e5298-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5298-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e5298-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="e5298-113">occurrenceDateTime</span></span>|<span data-ttu-id="e5298-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e5298-114">DateTimeOffset</span></span>|<span data-ttu-id="e5298-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="e5298-115">Time when the history item occurred.</span></span> <span data-ttu-id="e5298-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="e5298-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="e5298-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e5298-117">Relationships</span></span>
<span data-ttu-id="e5298-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e5298-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e5298-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5298-119">JSON Representation</span></span>
<span data-ttu-id="e5298-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e5298-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingDeviceCheckinHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingDeviceCheckinHistory",
  "occurrenceDateTime": "String (timestamp)"
}
```




