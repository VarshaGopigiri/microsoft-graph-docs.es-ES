---
title: tipo de recurso mobileAppTroubleshootingAppTargetHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9da17e4a03d1a28c32215b8616dad2ea3700ef4f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969425"
---
# <a name="mobileapptroubleshootingapptargethistory-resource-type"></a><span data-ttu-id="cdffd-103">tipo de recurso mobileAppTroubleshootingAppTargetHistory</span><span class="sxs-lookup"><span data-stu-id="cdffd-103">mobileAppTroubleshootingAppTargetHistory resource type</span></span>

> <span data-ttu-id="cdffd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cdffd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cdffd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cdffd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cdffd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cdffd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cdffd-107">Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="cdffd-107">History Item contained in the Mobile App Troubleshooting Event.</span></span>

<span data-ttu-id="cdffd-108">Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="cdffd-108">Inherits from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="cdffd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cdffd-109">Properties</span></span>
|<span data-ttu-id="cdffd-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cdffd-110">Property</span></span>|<span data-ttu-id="cdffd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdffd-111">Type</span></span>|<span data-ttu-id="cdffd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdffd-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cdffd-113">occurrenceDateTime</span><span class="sxs-lookup"><span data-stu-id="cdffd-113">occurrenceDateTime</span></span>|<span data-ttu-id="cdffd-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cdffd-114">DateTimeOffset</span></span>|<span data-ttu-id="cdffd-115">Tiempo que se produjo el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="cdffd-115">Time when the history item occurred.</span></span> <span data-ttu-id="cdffd-116">Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="cdffd-116">Inherited from [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span></span>|
|<span data-ttu-id="cdffd-117">securityGroupId</span><span class="sxs-lookup"><span data-stu-id="cdffd-117">securityGroupId</span></span>|<span data-ttu-id="cdffd-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="cdffd-118">String</span></span>|<span data-ttu-id="cdffd-119">Identificador de grupo de seguridad AAD a la que se ha destinado.</span><span class="sxs-lookup"><span data-stu-id="cdffd-119">AAD security group id to which it was targeted.</span></span>|
|<span data-ttu-id="cdffd-120">runState</span><span class="sxs-lookup"><span data-stu-id="cdffd-120">runState</span></span>|[<span data-ttu-id="cdffd-121">runState</span><span class="sxs-lookup"><span data-stu-id="cdffd-121">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="cdffd-122">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="cdffd-122">Status of the item.</span></span> <span data-ttu-id="cdffd-123">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="cdffd-123">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="cdffd-124">errorCode</span><span class="sxs-lookup"><span data-stu-id="cdffd-124">errorCode</span></span>|<span data-ttu-id="cdffd-125">String</span><span class="sxs-lookup"><span data-stu-id="cdffd-125">String</span></span>|<span data-ttu-id="cdffd-126">Código de error para el error, vacío si no hay error.</span><span class="sxs-lookup"><span data-stu-id="cdffd-126">Error code for the failure, empty if no failure.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cdffd-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cdffd-127">Relationships</span></span>
<span data-ttu-id="cdffd-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cdffd-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cdffd-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cdffd-129">JSON Representation</span></span>
<span data-ttu-id="cdffd-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cdffd-130">Here is a JSON representation of the resource.</span></span>
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





