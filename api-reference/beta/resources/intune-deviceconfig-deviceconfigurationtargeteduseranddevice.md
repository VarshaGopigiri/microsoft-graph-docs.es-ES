---
title: tipo de recurso deviceConfigurationTargetedUserAndDevice
description: Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 234cc9c909875d835ba54709f30f1ca306eb0954
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947970"
---
# <a name="deviceconfigurationtargeteduseranddevice-resource-type"></a><span data-ttu-id="eb145-103">tipo de recurso deviceConfigurationTargetedUserAndDevice</span><span class="sxs-lookup"><span data-stu-id="eb145-103">deviceConfigurationTargetedUserAndDevice resource type</span></span>

> <span data-ttu-id="eb145-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb145-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb145-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb145-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eb145-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb145-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb145-107">Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb145-107">Conflict summary for a set of device configuration policies.</span></span>
## <a name="properties"></a><span data-ttu-id="eb145-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb145-108">Properties</span></span>
|<span data-ttu-id="eb145-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb145-109">Property</span></span>|<span data-ttu-id="eb145-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb145-110">Type</span></span>|<span data-ttu-id="eb145-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb145-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eb145-112">deviceId</span><span class="sxs-lookup"><span data-stu-id="eb145-112">deviceId</span></span>|<span data-ttu-id="eb145-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb145-113">String</span></span>|<span data-ttu-id="eb145-114">El identificador del dispositivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="eb145-114">The id of the device in the checkin.</span></span>|
|<span data-ttu-id="eb145-115">deviceName</span><span class="sxs-lookup"><span data-stu-id="eb145-115">deviceName</span></span>|<span data-ttu-id="eb145-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb145-116">String</span></span>|<span data-ttu-id="eb145-117">El nombre del dispositivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="eb145-117">The name of the device in the checkin.</span></span>|
|<span data-ttu-id="eb145-118">userId</span><span class="sxs-lookup"><span data-stu-id="eb145-118">userId</span></span>|<span data-ttu-id="eb145-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb145-119">String</span></span>|<span data-ttu-id="eb145-120">El identificador del usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="eb145-120">The id of the user in the checkin.</span></span>|
|<span data-ttu-id="eb145-121">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="eb145-121">userDisplayName</span></span>|<span data-ttu-id="eb145-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb145-122">String</span></span>|<span data-ttu-id="eb145-123">El nombre para mostrar del usuario en el registro</span><span class="sxs-lookup"><span data-stu-id="eb145-123">The display name of the user in the checkin</span></span>|
|<span data-ttu-id="eb145-124">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="eb145-124">userPrincipalName</span></span>|<span data-ttu-id="eb145-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb145-125">String</span></span>|<span data-ttu-id="eb145-126">El UPN del usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="eb145-126">The UPN of the user in the checkin.</span></span>|
|<span data-ttu-id="eb145-127">lastCheckinDateTime</span><span class="sxs-lookup"><span data-stu-id="eb145-127">lastCheckinDateTime</span></span>|<span data-ttu-id="eb145-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eb145-128">DateTimeOffset</span></span>|<span data-ttu-id="eb145-129">Última hora de protección para este par de usuario/dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb145-129">Last checkin time for this user/device pair.</span></span>|

## <a name="relationships"></a><span data-ttu-id="eb145-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eb145-130">Relationships</span></span>
<span data-ttu-id="eb145-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="eb145-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="eb145-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eb145-132">JSON Representation</span></span>
<span data-ttu-id="eb145-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="eb145-133">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceConfigurationTargetedUserAndDevice"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationTargetedUserAndDevice",
  "deviceId": "String",
  "deviceName": "String",
  "userId": "String",
  "userDisplayName": "String",
  "userPrincipalName": "String",
  "lastCheckinDateTime": "String (timestamp)"
}
```





