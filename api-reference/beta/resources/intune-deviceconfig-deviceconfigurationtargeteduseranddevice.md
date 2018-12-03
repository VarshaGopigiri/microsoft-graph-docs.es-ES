---
title: tipo de recurso deviceConfigurationTargetedUserAndDevice
description: Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.
ms.openlocfilehash: 6f79a8fe24e06d2bdafa81c30cabf8158b4e5773
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083982"
---
# <a name="deviceconfigurationtargeteduseranddevice-resource-type"></a><span data-ttu-id="ab14f-103">tipo de recurso deviceConfigurationTargetedUserAndDevice</span><span class="sxs-lookup"><span data-stu-id="ab14f-103">deviceConfigurationTargetedUserAndDevice resource type</span></span>

> <span data-ttu-id="ab14f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab14f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab14f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab14f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab14f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab14f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab14f-107">Conflicto de resumen para un conjunto de directivas de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab14f-107">Conflict summary for a set of device configuration policies.</span></span>
## <a name="properties"></a><span data-ttu-id="ab14f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab14f-108">Properties</span></span>
|<span data-ttu-id="ab14f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab14f-109">Property</span></span>|<span data-ttu-id="ab14f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab14f-110">Type</span></span>|<span data-ttu-id="ab14f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab14f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab14f-112">deviceId</span><span class="sxs-lookup"><span data-stu-id="ab14f-112">deviceId</span></span>|<span data-ttu-id="ab14f-113">String</span><span class="sxs-lookup"><span data-stu-id="ab14f-113">String</span></span>|<span data-ttu-id="ab14f-114">El identificador del dispositivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="ab14f-114">The id of the device in the checkin.</span></span>|
|<span data-ttu-id="ab14f-115">deviceName</span><span class="sxs-lookup"><span data-stu-id="ab14f-115">deviceName</span></span>|<span data-ttu-id="ab14f-116">String</span><span class="sxs-lookup"><span data-stu-id="ab14f-116">String</span></span>|<span data-ttu-id="ab14f-117">El nombre del dispositivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="ab14f-117">The name of the device in the checkin.</span></span>|
|<span data-ttu-id="ab14f-118">userId</span><span class="sxs-lookup"><span data-stu-id="ab14f-118">userId</span></span>|<span data-ttu-id="ab14f-119">String</span><span class="sxs-lookup"><span data-stu-id="ab14f-119">String</span></span>|<span data-ttu-id="ab14f-120">El identificador del usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="ab14f-120">The id of the user in the checkin.</span></span>|
|<span data-ttu-id="ab14f-121">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="ab14f-121">userDisplayName</span></span>|<span data-ttu-id="ab14f-122">String</span><span class="sxs-lookup"><span data-stu-id="ab14f-122">String</span></span>|<span data-ttu-id="ab14f-123">El nombre para mostrar del usuario en el registro</span><span class="sxs-lookup"><span data-stu-id="ab14f-123">The display name of the user in the checkin</span></span>|
|<span data-ttu-id="ab14f-124">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ab14f-124">userPrincipalName</span></span>|<span data-ttu-id="ab14f-125">String</span><span class="sxs-lookup"><span data-stu-id="ab14f-125">String</span></span>|<span data-ttu-id="ab14f-126">El UPN del usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="ab14f-126">The UPN of the user in the checkin.</span></span>|
|<span data-ttu-id="ab14f-127">lastCheckinDateTime</span><span class="sxs-lookup"><span data-stu-id="ab14f-127">lastCheckinDateTime</span></span>|<span data-ttu-id="ab14f-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab14f-128">DateTimeOffset</span></span>|<span data-ttu-id="ab14f-129">Última hora de protección para este par de usuario/dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab14f-129">Last checkin time for this user/device pair.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ab14f-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ab14f-130">Relationships</span></span>
<span data-ttu-id="ab14f-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ab14f-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ab14f-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab14f-132">JSON Representation</span></span>
<span data-ttu-id="ab14f-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ab14f-133">Here is a JSON representation of the resource.</span></span>
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




