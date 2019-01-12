---
title: tipo de recurso windowsAutopilotSettings
description: El recurso windowsAutopilotSettings representa una cuenta de piloto automático de Windows a los datos de sincronización con el servicio de sincronización de datos de dispositivos de Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4bf9a39d6a5078362c966edde38ec98deec037b0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939556"
---
# <a name="windowsautopilotsettings-resource-type"></a><span data-ttu-id="679ce-103">tipo de recurso windowsAutopilotSettings</span><span class="sxs-lookup"><span data-stu-id="679ce-103">windowsAutopilotSettings resource type</span></span>

> <span data-ttu-id="679ce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="679ce-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="679ce-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="679ce-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="679ce-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="679ce-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="679ce-107">El recurso windowsAutopilotSettings representa una cuenta de piloto automático de Windows a los datos de sincronización con el servicio de sincronización de datos de dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="679ce-107">The windowsAutopilotSettings resource represents a Windows Autopilot Account to sync data with Windows device data sync service.</span></span>
## <a name="methods"></a><span data-ttu-id="679ce-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="679ce-108">Methods</span></span>
|<span data-ttu-id="679ce-109">Método</span><span class="sxs-lookup"><span data-stu-id="679ce-109">Method</span></span>|<span data-ttu-id="679ce-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="679ce-110">Return Type</span></span>|<span data-ttu-id="679ce-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="679ce-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="679ce-112">Obtener windowsAutopilotSettings</span><span class="sxs-lookup"><span data-stu-id="679ce-112">Get windowsAutopilotSettings</span></span>](../api/intune-enrollment-windowsautopilotsettings-get.md)|[<span data-ttu-id="679ce-113">windowsAutopilotSettings</span><span class="sxs-lookup"><span data-stu-id="679ce-113">windowsAutopilotSettings</span></span>](../resources/intune-enrollment-windowsautopilotsettings.md)|<span data-ttu-id="679ce-114">Leer las propiedades y las relaciones del objeto [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="679ce-114">Read properties and relationships of the [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) object.</span></span>|
|[<span data-ttu-id="679ce-115">Actualizar windowsAutopilotSettings</span><span class="sxs-lookup"><span data-stu-id="679ce-115">Update windowsAutopilotSettings</span></span>](../api/intune-enrollment-windowsautopilotsettings-update.md)|[<span data-ttu-id="679ce-116">windowsAutopilotSettings</span><span class="sxs-lookup"><span data-stu-id="679ce-116">windowsAutopilotSettings</span></span>](../resources/intune-enrollment-windowsautopilotsettings.md)|<span data-ttu-id="679ce-117">Actualizar las propiedades de un objeto [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="679ce-117">Update the properties of a [windowsAutopilotSettings](../resources/intune-enrollment-windowsautopilotsettings.md) object.</span></span>|
|[<span data-ttu-id="679ce-118">Acción sync</span><span class="sxs-lookup"><span data-stu-id="679ce-118">sync action</span></span>](../api/intune-enrollment-windowsautopilotsettings-sync.md)|<span data-ttu-id="679ce-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="679ce-119">None</span></span>|<span data-ttu-id="679ce-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="679ce-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="679ce-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="679ce-121">Properties</span></span>
|<span data-ttu-id="679ce-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="679ce-122">Property</span></span>|<span data-ttu-id="679ce-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="679ce-123">Type</span></span>|<span data-ttu-id="679ce-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="679ce-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="679ce-125">id</span><span class="sxs-lookup"><span data-stu-id="679ce-125">id</span></span>|<span data-ttu-id="679ce-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="679ce-126">String</span></span>|<span data-ttu-id="679ce-127">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="679ce-127">The GUID for the object</span></span>|
|<span data-ttu-id="679ce-128">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="679ce-128">lastSyncDateTime</span></span>|<span data-ttu-id="679ce-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="679ce-129">DateTimeOffset</span></span>|<span data-ttu-id="679ce-130">Datos de la última sincronización de la hora de fecha con el servicio DDS.</span><span class="sxs-lookup"><span data-stu-id="679ce-130">Last data sync date time with DDS service.</span></span>|
|<span data-ttu-id="679ce-131">lastManualSyncTriggerDateTime</span><span class="sxs-lookup"><span data-stu-id="679ce-131">lastManualSyncTriggerDateTime</span></span>|<span data-ttu-id="679ce-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="679ce-132">DateTimeOffset</span></span>|<span data-ttu-id="679ce-133">Datos de la última sincronización de la hora de fecha con el servicio DDS.</span><span class="sxs-lookup"><span data-stu-id="679ce-133">Last data sync date time with DDS service.</span></span>|
|<span data-ttu-id="679ce-134">syncStatus</span><span class="sxs-lookup"><span data-stu-id="679ce-134">syncStatus</span></span>|[<span data-ttu-id="679ce-135">windowsAutopilotSyncStatus</span><span class="sxs-lookup"><span data-stu-id="679ce-135">windowsAutopilotSyncStatus</span></span>](../resources/intune-enrollment-windowsautopilotsyncstatus.md)|<span data-ttu-id="679ce-136">Indica el estado de sincronización con el servicio de sincronización (DDS) de datos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="679ce-136">Indicates the status of sync with Device data sync (DDS) service.</span></span> <span data-ttu-id="679ce-137">Los valores posibles son: `unknown`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="679ce-137">Possible values are: `unknown`, `inProgress`, `completed`, `failed`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="679ce-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="679ce-138">Relationships</span></span>
<span data-ttu-id="679ce-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="679ce-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="679ce-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="679ce-140">JSON Representation</span></span>
<span data-ttu-id="679ce-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="679ce-141">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsAutopilotSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsAutopilotSettings",
  "id": "String (identifier)",
  "lastSyncDateTime": "String (timestamp)",
  "lastManualSyncTriggerDateTime": "String (timestamp)",
  "syncStatus": "String"
}
```





