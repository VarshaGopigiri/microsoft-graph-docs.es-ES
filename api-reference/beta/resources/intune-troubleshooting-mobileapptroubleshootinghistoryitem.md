---
title: tipo de recurso mobileAppTroubleshootingHistoryItem
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
ms.openlocfilehash: 132039a0b6e457ebd2ca3e545f6f15dd4ad7ac58
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329529"
---
# <a name="mobileapptroubleshootinghistoryitem-resource-type"></a><span data-ttu-id="a2ffa-103">tipo de recurso mobileAppTroubleshootingHistoryItem</span><span class="sxs-lookup"><span data-stu-id="a2ffa-103">mobileAppTroubleshootingHistoryItem resource type</span></span>

> <span data-ttu-id="a2ffa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2ffa-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2ffa-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2ffa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a2ffa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2ffa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2ffa-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="a2ffa-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>
## <a name="properties"></a><span data-ttu-id="a2ffa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2ffa-108">Properties</span></span>
|<span data-ttu-id="a2ffa-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2ffa-109">Property</span></span>|<span data-ttu-id="a2ffa-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2ffa-110">Type</span></span>|<span data-ttu-id="a2ffa-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2ffa-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2ffa-112">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="a2ffa-112">occurrenceDateTime</span></span>|<span data-ttu-id="a2ffa-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a2ffa-113">DateTimeOffset</span></span>|<span data-ttu-id="a2ffa-114">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="a2ffa-114">Time when the history item occurred.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a2ffa-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a2ffa-115">Relationships</span></span>
<span data-ttu-id="a2ffa-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a2ffa-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a2ffa-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2ffa-117">JSON Representation</span></span>
<span data-ttu-id="a2ffa-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a2ffa-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingHistoryItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingHistoryItem",
  "occurrenceDateTime": "String (timestamp)"
}
```





