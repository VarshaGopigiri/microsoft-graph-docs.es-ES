---
title: Tipo de recurso deviceComplianceActionItem
description: Configuración de la acción programada
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d697275780b686edc9a3b1eed42b6afb712163b0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866433"
---
# <a name="devicecomplianceactionitem-resource-type"></a><span data-ttu-id="812a8-103">Tipo de recurso deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-103">deviceComplianceActionItem resource type</span></span>

> <span data-ttu-id="812a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="812a8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="812a8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="812a8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="812a8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="812a8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="812a8-107">Configuración de la acción programada</span><span class="sxs-lookup"><span data-stu-id="812a8-107">Scheduled Action Configuration</span></span>
## <a name="methods"></a><span data-ttu-id="812a8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="812a8-108">Methods</span></span>
|<span data-ttu-id="812a8-109">Método</span><span class="sxs-lookup"><span data-stu-id="812a8-109">Method</span></span>|<span data-ttu-id="812a8-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="812a8-110">Return Type</span></span>|<span data-ttu-id="812a8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="812a8-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="812a8-112">Enumerar deviceComplianceActionItems</span><span class="sxs-lookup"><span data-stu-id="812a8-112">List deviceComplianceActionItems</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-list.md)|<span data-ttu-id="812a8-113">Colección [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)</span><span class="sxs-lookup"><span data-stu-id="812a8-113">[deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) collection</span></span>|<span data-ttu-id="812a8-114">Enumere las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="812a8-114">List properties and relationships of the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) objects.</span></span>|
|[<span data-ttu-id="812a8-115">Obtener deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-115">Get deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-get.md)|[<span data-ttu-id="812a8-116">deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-116">deviceComplianceActionItem</span></span>](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|<span data-ttu-id="812a8-117">Lea las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="812a8-117">Read properties and relationships of the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>|
|[<span data-ttu-id="812a8-118">Crear deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-118">Create deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-create.md)|[<span data-ttu-id="812a8-119">deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-119">deviceComplianceActionItem</span></span>](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|<span data-ttu-id="812a8-120">Cree un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="812a8-120">Create a new [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>|
|[<span data-ttu-id="812a8-121">Eliminar deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-121">Delete deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-delete.md)|<span data-ttu-id="812a8-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="812a8-122">None</span></span>|<span data-ttu-id="812a8-123">Elimina un [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="812a8-123">Deletes a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span></span>|
|[<span data-ttu-id="812a8-124">Actualizar deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-124">Update deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-update.md)|[<span data-ttu-id="812a8-125">deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="812a8-125">deviceComplianceActionItem</span></span>](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|<span data-ttu-id="812a8-126">Actualice las propiedades de un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="812a8-126">Update the properties of a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="812a8-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="812a8-127">Properties</span></span>
|<span data-ttu-id="812a8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="812a8-128">Property</span></span>|<span data-ttu-id="812a8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="812a8-129">Type</span></span>|<span data-ttu-id="812a8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="812a8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="812a8-131">id</span><span class="sxs-lookup"><span data-stu-id="812a8-131">id</span></span>|<span data-ttu-id="812a8-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="812a8-132">String</span></span>|<span data-ttu-id="812a8-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="812a8-133">Key of the entity.</span></span>|
|<span data-ttu-id="812a8-134">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="812a8-134">gracePeriodHours</span></span>|<span data-ttu-id="812a8-135">Int32</span><span class="sxs-lookup"><span data-stu-id="812a8-135">Int32</span></span>|<span data-ttu-id="812a8-136">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="812a8-136">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="812a8-137">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="812a8-137">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="812a8-138">actionType</span><span class="sxs-lookup"><span data-stu-id="812a8-138">actionType</span></span>|[<span data-ttu-id="812a8-139">deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="812a8-139">deviceComplianceActionType</span></span>](../resources/intune-deviceconfig-devicecomplianceactiontype.md)|<span data-ttu-id="812a8-140">¿Qué acción debe realizar.</span><span class="sxs-lookup"><span data-stu-id="812a8-140">What action to take.</span></span> <span data-ttu-id="812a8-141">Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification` y `remoteLock`.</span><span class="sxs-lookup"><span data-stu-id="812a8-141">Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification`, `remoteLock`.</span></span>|
|<span data-ttu-id="812a8-142">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="812a8-142">notificationTemplateId</span></span>|<span data-ttu-id="812a8-143">String</span><span class="sxs-lookup"><span data-stu-id="812a8-143">String</span></span>|<span data-ttu-id="812a8-144">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="812a8-144">What notification Message template to use</span></span>|
|<span data-ttu-id="812a8-145">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="812a8-145">notificationMessageCCList</span></span>|<span data-ttu-id="812a8-146">Colección string</span><span class="sxs-lookup"><span data-stu-id="812a8-146">String collection</span></span>|<span data-ttu-id="812a8-147">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="812a8-147">A list of group IDs to speicify who to CC this notification message to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="812a8-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="812a8-148">Relationships</span></span>
<span data-ttu-id="812a8-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="812a8-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="812a8-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="812a8-150">JSON Representation</span></span>
<span data-ttu-id="812a8-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="812a8-151">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceActionItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
  "id": "String (identifier)",
  "gracePeriodHours": 1024,
  "actionType": "String",
  "notificationTemplateId": "String",
  "notificationMessageCCList": [
    "String"
  ]
}
```





