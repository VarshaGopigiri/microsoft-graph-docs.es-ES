---
title: Tipo de recurso remoteAssistancePartner
description: Los recursos remoteAssistPartner representan los metadatos y el estado de un servicio de partner de asistencia remota específico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 52badd2ad146f23fba70ab545a459b124e7fae2c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821718"
---
# <a name="remoteassistancepartner-resource-type"></a><span data-ttu-id="9c154-103">Tipo de recurso remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-103">remoteAssistancePartner resource type</span></span>

> <span data-ttu-id="9c154-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9c154-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9c154-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9c154-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9c154-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9c154-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9c154-107">Los recursos remoteAssistPartner representan los metadatos y el estado de un servicio de partner de asistencia remota específico.</span><span class="sxs-lookup"><span data-stu-id="9c154-107">remoteAssistPartner resources represent the metadata and status of a given Remote Assistance partner service.</span></span>
## <a name="methods"></a><span data-ttu-id="9c154-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c154-108">Methods</span></span>
|<span data-ttu-id="9c154-109">Método</span><span class="sxs-lookup"><span data-stu-id="9c154-109">Method</span></span>|<span data-ttu-id="9c154-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c154-110">Return Type</span></span>|<span data-ttu-id="9c154-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c154-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="9c154-112">Enumerar remoteAssistancePartners</span><span class="sxs-lookup"><span data-stu-id="9c154-112">List remoteAssistancePartners</span></span>](../api/intune-remoteassistance-remoteassistancepartner-list.md)|<span data-ttu-id="9c154-113">Colección [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md)</span><span class="sxs-lookup"><span data-stu-id="9c154-113">[remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) collection</span></span>|<span data-ttu-id="9c154-114">Enumere las propiedades y las relaciones de los objetos [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="9c154-114">List properties and relationships of the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) objects.</span></span>|
|[<span data-ttu-id="9c154-115">Obtener remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-115">Get remoteAssistancePartner</span></span>](../api/intune-remoteassistance-remoteassistancepartner-get.md)|[<span data-ttu-id="9c154-116">remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-116">remoteAssistancePartner</span></span>](../resources/intune-remoteassistance-remoteassistancepartner.md)|<span data-ttu-id="9c154-117">Lea las propiedades y las relaciones del objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="9c154-117">Read properties and relationships of the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>|
|[<span data-ttu-id="9c154-118">Crear remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-118">Create remoteAssistancePartner</span></span>](../api/intune-remoteassistance-remoteassistancepartner-create.md)|[<span data-ttu-id="9c154-119">remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-119">remoteAssistancePartner</span></span>](../resources/intune-remoteassistance-remoteassistancepartner.md)|<span data-ttu-id="9c154-120">Cree un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="9c154-120">Create a new [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>|
|[<span data-ttu-id="9c154-121">Eliminar remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-121">Delete remoteAssistancePartner</span></span>](../api/intune-remoteassistance-remoteassistancepartner-delete.md)|<span data-ttu-id="9c154-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9c154-122">None</span></span>|<span data-ttu-id="9c154-123">Elimina un [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="9c154-123">Deletes a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span></span>|
|[<span data-ttu-id="9c154-124">Actualizar remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-124">Update remoteAssistancePartner</span></span>](../api/intune-remoteassistance-remoteassistancepartner-update.md)|[<span data-ttu-id="9c154-125">remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="9c154-125">remoteAssistancePartner</span></span>](../resources/intune-remoteassistance-remoteassistancepartner.md)|<span data-ttu-id="9c154-126">Actualice las propiedades de un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="9c154-126">Update the properties of a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>|
|[<span data-ttu-id="9c154-127">Acción beginOnboarding</span><span class="sxs-lookup"><span data-stu-id="9c154-127">beginOnboarding action</span></span>](../api/intune-remoteassistance-remoteassistancepartner-beginonboarding.md)|<span data-ttu-id="9c154-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9c154-128">None</span></span>|<span data-ttu-id="9c154-129">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9c154-129">Not yet documented</span></span>|
|[<span data-ttu-id="9c154-130">Acción disconnect</span><span class="sxs-lookup"><span data-stu-id="9c154-130">disconnect action</span></span>](../api/intune-remoteassistance-remoteassistancepartner-disconnect.md)|<span data-ttu-id="9c154-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9c154-131">None</span></span>|<span data-ttu-id="9c154-132">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9c154-132">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="9c154-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c154-133">Properties</span></span>
|<span data-ttu-id="9c154-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c154-134">Property</span></span>|<span data-ttu-id="9c154-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c154-135">Type</span></span>|<span data-ttu-id="9c154-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c154-136">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9c154-137">id</span><span class="sxs-lookup"><span data-stu-id="9c154-137">id</span></span>|<span data-ttu-id="9c154-138">String</span><span class="sxs-lookup"><span data-stu-id="9c154-138">String</span></span>|<span data-ttu-id="9c154-139">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="9c154-139">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="9c154-140">displayName</span><span class="sxs-lookup"><span data-stu-id="9c154-140">displayName</span></span>|<span data-ttu-id="9c154-141">String</span><span class="sxs-lookup"><span data-stu-id="9c154-141">String</span></span>|<span data-ttu-id="9c154-142">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="9c154-142">Display name of the partner.</span></span>|
|<span data-ttu-id="9c154-143">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="9c154-143">onboardingUrl</span></span>|<span data-ttu-id="9c154-144">String</span><span class="sxs-lookup"><span data-stu-id="9c154-144">String</span></span>|<span data-ttu-id="9c154-145">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="9c154-145">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="9c154-146">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="9c154-146">onboardingStatus</span></span>|[<span data-ttu-id="9c154-147">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="9c154-147">remoteAssistanceOnboardingStatus</span></span>](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|<span data-ttu-id="9c154-148">TBD.</span><span class="sxs-lookup"><span data-stu-id="9c154-148">TBD.</span></span> <span data-ttu-id="9c154-149">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="9c154-149">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="9c154-150">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="9c154-150">lastConnectionDateTime</span></span>|<span data-ttu-id="9c154-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9c154-151">DateTimeOffset</span></span>|<span data-ttu-id="9c154-152">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="9c154-152">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9c154-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9c154-153">Relationships</span></span>
<span data-ttu-id="9c154-154">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9c154-154">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9c154-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9c154-155">JSON Representation</span></span>
<span data-ttu-id="9c154-156">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9c154-156">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.remoteAssistancePartner"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "id": "String (identifier)",
  "displayName": "String",
  "onboardingUrl": "String",
  "onboardingStatus": "String",
  "lastConnectionDateTime": "String (timestamp)"
}
```





