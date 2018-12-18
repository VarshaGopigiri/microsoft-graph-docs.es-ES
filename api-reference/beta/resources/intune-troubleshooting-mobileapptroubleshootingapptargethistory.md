---
title: tipo de recurso mobileAppTroubleshootingAppTargetHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
ms.openlocfilehash: cdb901d4c532b57025837a2fb0cc0975ceba3f8c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312736"
---
# <a name="mobileapptroubleshootingapptargethistory-resource-type"></a><span data-ttu-id="ab9b5-103">tipo de recurso mobileAppTroubleshootingAppTargetHistory</span><span class="sxs-lookup"><span data-stu-id="ab9b5-103">mobileAppTroubleshootingAppTargetHistory resource type</span></span>

> <span data-ttu-id="ab9b5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab9b5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab9b5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab9b5-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="ab9b5-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="ab9b5-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ab9b5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab9b5-109">Properties</span></span>
|<span data-ttu-id="ab9b5-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab9b5-110">Property</span></span>|<span data-ttu-id="ab9b5-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab9b5-111">Type</span></span>|<span data-ttu-id="ab9b5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab9b5-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab9b5-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="ab9b5-113">occurrenceDateTime</span></span>|<span data-ttu-id="ab9b5-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab9b5-114">DateTimeOffset</span></span>|<span data-ttu-id="ab9b5-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-115">Time when the history item occurred.</span></span> <span data-ttu-id="ab9b5-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="ab9b5-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|
|<span data-ttu-id="ab9b5-117">securityGroupId</span><span class="sxs-lookup"><span data-stu-id="ab9b5-117">securityGroupId</span></span>|<span data-ttu-id="ab9b5-118">String</span><span class="sxs-lookup"><span data-stu-id="ab9b5-118">String</span></span>|<span data-ttu-id="ab9b5-119">Identificador de grupo de seguridad AAD a la que se ha destinado.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-119">AAD security group id to which it was targeted.</span></span>|
|<span data-ttu-id="ab9b5-120">runState</span><span class="sxs-lookup"><span data-stu-id="ab9b5-120">runState</span></span>|[<span data-ttu-id="ab9b5-121">runState</span><span class="sxs-lookup"><span data-stu-id="ab9b5-121">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="ab9b5-122">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-122">Status of the item.</span></span> <span data-ttu-id="ab9b5-123">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-123">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="ab9b5-124">errorCode</span><span class="sxs-lookup"><span data-stu-id="ab9b5-124">errorCode</span></span>|<span data-ttu-id="ab9b5-125">String</span><span class="sxs-lookup"><span data-stu-id="ab9b5-125">String</span></span>|<span data-ttu-id="ab9b5-126">Código de error para el error, vacío si no hay error.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-126">Error code for the failure, empty if no failure.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ab9b5-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ab9b5-127">Relationships</span></span>
<span data-ttu-id="ab9b5-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ab9b5-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ab9b5-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab9b5-129">JSON Representation</span></span>
<span data-ttu-id="ab9b5-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ab9b5-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingAppTargetHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingAppTargetHistory",
  "occurrenceDateTime": "String (timestamp)",
  "securityGroupId": "String",
  "runState": "String",
  "errorCode": "String"
}
```





