---
title: Tipo de recurso deviceComplianceActionItem
description: Configuración de la acción programada
ms.openlocfilehash: dc84ee71e6544bf089f3470d607772c2242f7278
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085209"
---
# <a name="devicecomplianceactionitem-resource-type"></a><span data-ttu-id="adcaf-103">Tipo de recurso deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-103">deviceComplianceActionItem resource type</span></span>

> <span data-ttu-id="adcaf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="adcaf-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="adcaf-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="adcaf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="adcaf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="adcaf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="adcaf-107">Configuración de la acción programada</span><span class="sxs-lookup"><span data-stu-id="adcaf-107">Scheduled Action Configuration</span></span>
## <a name="methods"></a><span data-ttu-id="adcaf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="adcaf-108">Methods</span></span>
|<span data-ttu-id="adcaf-109">Método</span><span class="sxs-lookup"><span data-stu-id="adcaf-109">Method</span></span>|<span data-ttu-id="adcaf-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="adcaf-110">Return Type</span></span>|<span data-ttu-id="adcaf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="adcaf-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="adcaf-112">Enumerar deviceComplianceActionItems</span><span class="sxs-lookup"><span data-stu-id="adcaf-112">List deviceComplianceActionItems</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-list.md)|<span data-ttu-id="adcaf-113">Colección [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)</span><span class="sxs-lookup"><span data-stu-id="adcaf-113">[deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) collection</span></span>|<span data-ttu-id="adcaf-114">Enumere las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="adcaf-114">List properties and relationships of the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) objects.</span></span>|
|[<span data-ttu-id="adcaf-115">Obtener deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-115">Get deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-get.md)|[<span data-ttu-id="adcaf-116">deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-116">deviceComplianceActionItem</span></span>](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|<span data-ttu-id="adcaf-117">Lea las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="adcaf-117">Read properties and relationships of the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>|
|[<span data-ttu-id="adcaf-118">Crear deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-118">Create deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-create.md)|[<span data-ttu-id="adcaf-119">deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-119">deviceComplianceActionItem</span></span>](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|<span data-ttu-id="adcaf-120">Cree un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="adcaf-120">Create a new [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>|
|[<span data-ttu-id="adcaf-121">Eliminar deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-121">Delete deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-delete.md)|<span data-ttu-id="adcaf-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="adcaf-122">None</span></span>|<span data-ttu-id="adcaf-123">Elimina un [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="adcaf-123">Deletes a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span></span>|
|[<span data-ttu-id="adcaf-124">Actualizar deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-124">Update deviceComplianceActionItem</span></span>](../api/intune-deviceconfig-devicecomplianceactionitem-update.md)|[<span data-ttu-id="adcaf-125">deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="adcaf-125">deviceComplianceActionItem</span></span>](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|<span data-ttu-id="adcaf-126">Actualice las propiedades de un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="adcaf-126">Update the properties of a [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="adcaf-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="adcaf-127">Properties</span></span>
|<span data-ttu-id="adcaf-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="adcaf-128">Property</span></span>|<span data-ttu-id="adcaf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="adcaf-129">Type</span></span>|<span data-ttu-id="adcaf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="adcaf-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="adcaf-131">id</span><span class="sxs-lookup"><span data-stu-id="adcaf-131">id</span></span>|<span data-ttu-id="adcaf-132">String</span><span class="sxs-lookup"><span data-stu-id="adcaf-132">String</span></span>|<span data-ttu-id="adcaf-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="adcaf-133">Key of the entity.</span></span>|
|<span data-ttu-id="adcaf-134">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="adcaf-134">gracePeriodHours</span></span>|<span data-ttu-id="adcaf-135">Int32</span><span class="sxs-lookup"><span data-stu-id="adcaf-135">Int32</span></span>|<span data-ttu-id="adcaf-136">Número de horas de espera hasta que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="adcaf-136">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="adcaf-137">Valores válidos de 0 a 8760</span><span class="sxs-lookup"><span data-stu-id="adcaf-137">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="adcaf-138">actionType</span><span class="sxs-lookup"><span data-stu-id="adcaf-138">actionType</span></span>|[<span data-ttu-id="adcaf-139">deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="adcaf-139">deviceComplianceActionType</span></span>](../resources/intune-deviceconfig-devicecomplianceactiontype.md)|<span data-ttu-id="adcaf-140">¿Qué acción debe realizar.</span><span class="sxs-lookup"><span data-stu-id="adcaf-140">What action to take.</span></span> <span data-ttu-id="adcaf-141">Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification` y `remoteLock`.</span><span class="sxs-lookup"><span data-stu-id="adcaf-141">Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`, `pushNotification`, `remoteLock`.</span></span>|
|<span data-ttu-id="adcaf-142">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="adcaf-142">notificationTemplateId</span></span>|<span data-ttu-id="adcaf-143">String</span><span class="sxs-lookup"><span data-stu-id="adcaf-143">String</span></span>|<span data-ttu-id="adcaf-144">Qué plantilla de mensaje de notificación usar</span><span class="sxs-lookup"><span data-stu-id="adcaf-144">What notification Message template to use</span></span>|
|<span data-ttu-id="adcaf-145">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="adcaf-145">notificationMessageCCList</span></span>|<span data-ttu-id="adcaf-146">Colección string</span><span class="sxs-lookup"><span data-stu-id="adcaf-146">String collection</span></span>|<span data-ttu-id="adcaf-147">Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="adcaf-147">A list of group IDs to speicify who to CC this notification message to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="adcaf-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="adcaf-148">Relationships</span></span>
<span data-ttu-id="adcaf-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="adcaf-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="adcaf-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="adcaf-150">JSON Representation</span></span>
<span data-ttu-id="adcaf-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="adcaf-151">Here is a JSON representation of the resource.</span></span>
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





