---
title: tipo de recurso deviceConfigurationTargetedUserAndDevice
description: Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 46355f78f23060ecc901c3f98f0e3f7d13101d1e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809628"
---
# <a name="deviceconfigurationtargeteduseranddevice-resource-type"></a><span data-ttu-id="b506c-103">tipo de recurso deviceConfigurationTargetedUserAndDevice</span><span class="sxs-lookup"><span data-stu-id="b506c-103">deviceConfigurationTargetedUserAndDevice resource type</span></span>

> <span data-ttu-id="b506c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b506c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b506c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b506c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b506c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b506c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b506c-107">Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b506c-107">Conflict summary for a set of device configuration policies.</span></span>
## <a name="properties"></a><span data-ttu-id="b506c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b506c-108">Properties</span></span>
|<span data-ttu-id="b506c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b506c-109">Property</span></span>|<span data-ttu-id="b506c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b506c-110">Type</span></span>|<span data-ttu-id="b506c-111">Description</span><span class="sxs-lookup"><span data-stu-id="b506c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b506c-112">deviceId</span><span class="sxs-lookup"><span data-stu-id="b506c-112">deviceId</span></span>|<span data-ttu-id="b506c-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="b506c-113">String</span></span>|<span data-ttu-id="b506c-114">El identificador del dispositivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="b506c-114">The id of the device in the checkin.</span></span>|
|<span data-ttu-id="b506c-115">deviceName</span><span class="sxs-lookup"><span data-stu-id="b506c-115">deviceName</span></span>|<span data-ttu-id="b506c-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="b506c-116">String</span></span>|<span data-ttu-id="b506c-117">El nombre del dispositivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="b506c-117">The name of the device in the checkin.</span></span>|
|<span data-ttu-id="b506c-118">userId</span><span class="sxs-lookup"><span data-stu-id="b506c-118">userId</span></span>|<span data-ttu-id="b506c-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="b506c-119">String</span></span>|<span data-ttu-id="b506c-120">El identificador del usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="b506c-120">The id of the user in the checkin.</span></span>|
|<span data-ttu-id="b506c-121">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="b506c-121">userDisplayName</span></span>|<span data-ttu-id="b506c-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="b506c-122">String</span></span>|<span data-ttu-id="b506c-123">El nombre para mostrar del usuario en el registro</span><span class="sxs-lookup"><span data-stu-id="b506c-123">The display name of the user in the checkin</span></span>|
|<span data-ttu-id="b506c-124">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b506c-124">userPrincipalName</span></span>|<span data-ttu-id="b506c-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="b506c-125">String</span></span>|<span data-ttu-id="b506c-126">El UPN del usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="b506c-126">The UPN of the user in the checkin.</span></span>|
|<span data-ttu-id="b506c-127">lastCheckinDateTime</span><span class="sxs-lookup"><span data-stu-id="b506c-127">lastCheckinDateTime</span></span>|<span data-ttu-id="b506c-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b506c-128">DateTimeOffset</span></span>|<span data-ttu-id="b506c-129">Última hora de protección para este par de usuario/dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b506c-129">Last checkin time for this user/device pair.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b506c-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b506c-130">Relationships</span></span>
<span data-ttu-id="b506c-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b506c-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b506c-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b506c-132">JSON Representation</span></span>
<span data-ttu-id="b506c-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b506c-133">Here is a JSON representation of the resource.</span></span>
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





