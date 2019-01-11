---
title: Tipo de recurso managedAppConfiguration
description: Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2b3acf921f76e34e21427364ef84d1647cc7d0f3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861323"
---
# <a name="managedappconfiguration-resource-type"></a><span data-ttu-id="2b3f2-103">Tipo de recurso managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b3f2-103">managedAppConfiguration resource type</span></span>

> <span data-ttu-id="2b3f2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b3f2-105">Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-105">Configuration used to deliver a set of custom settings as-is to apps for users to whom the configuration is scoped</span></span>

<span data-ttu-id="2b3f2-106">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="2b3f2-106">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="2b3f2-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b3f2-107">Methods</span></span>
|<span data-ttu-id="2b3f2-108">Método</span><span class="sxs-lookup"><span data-stu-id="2b3f2-108">Method</span></span>|<span data-ttu-id="2b3f2-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b3f2-109">Return Type</span></span>|<span data-ttu-id="2b3f2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b3f2-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="2b3f2-111">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b3f2-111">List managedAppConfigurations</span></span>](../api/intune-mam-managedappconfiguration-list.md)|<span data-ttu-id="2b3f2-112">Colección [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b3f2-112">[managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) collection</span></span>|<span data-ttu-id="2b3f2-113">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-113">List properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="2b3f2-114">Obtener managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b3f2-114">Get managedAppConfiguration</span></span>](../api/intune-mam-managedappconfiguration-get.md)|[<span data-ttu-id="2b3f2-115">managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b3f2-115">managedAppConfiguration</span></span>](../resources/intune-mam-managedappconfiguration.md)|<span data-ttu-id="2b3f2-116">Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-116">Read properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="2b3f2-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b3f2-117">Properties</span></span>
|<span data-ttu-id="2b3f2-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b3f2-118">Property</span></span>|<span data-ttu-id="2b3f2-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b3f2-119">Type</span></span>|<span data-ttu-id="2b3f2-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b3f2-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2b3f2-121">displayName</span><span class="sxs-lookup"><span data-stu-id="2b3f2-121">displayName</span></span>|<span data-ttu-id="2b3f2-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b3f2-122">String</span></span>|<span data-ttu-id="2b3f2-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-123">Policy display name.</span></span> <span data-ttu-id="2b3f2-124">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-124">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2b3f2-125">descripción</span><span class="sxs-lookup"><span data-stu-id="2b3f2-125">description</span></span>|<span data-ttu-id="2b3f2-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b3f2-126">String</span></span>|<span data-ttu-id="2b3f2-127">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-127">The policy's description.</span></span> <span data-ttu-id="2b3f2-128">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-128">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2b3f2-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2b3f2-129">createdDateTime</span></span>|<span data-ttu-id="2b3f2-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b3f2-130">DateTimeOffset</span></span>|<span data-ttu-id="2b3f2-131">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-131">The date and time the policy was created.</span></span> <span data-ttu-id="2b3f2-132">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-132">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2b3f2-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2b3f2-133">lastModifiedDateTime</span></span>|<span data-ttu-id="2b3f2-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b3f2-134">DateTimeOffset</span></span>|<span data-ttu-id="2b3f2-135">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-135">Last time the policy was modified.</span></span> <span data-ttu-id="2b3f2-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2b3f2-137">id</span><span class="sxs-lookup"><span data-stu-id="2b3f2-137">id</span></span>|<span data-ttu-id="2b3f2-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b3f2-138">String</span></span>|<span data-ttu-id="2b3f2-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-139">Key of the entity.</span></span> <span data-ttu-id="2b3f2-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2b3f2-141">version</span><span class="sxs-lookup"><span data-stu-id="2b3f2-141">version</span></span>|<span data-ttu-id="2b3f2-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b3f2-142">String</span></span>|<span data-ttu-id="2b3f2-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-143">Version of the entity.</span></span> <span data-ttu-id="2b3f2-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f2-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2b3f2-145">customSettings</span><span class="sxs-lookup"><span data-stu-id="2b3f2-145">customSettings</span></span>|<span data-ttu-id="2b3f2-146">Colección [keyValuePair](../resources/intune-mam-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="2b3f2-146">[keyValuePair](../resources/intune-mam-keyvaluepair.md) collection</span></span>|<span data-ttu-id="2b3f2-147">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio</span><span class="sxs-lookup"><span data-stu-id="2b3f2-147">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service</span></span>|

## <a name="relationships"></a><span data-ttu-id="2b3f2-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2b3f2-148">Relationships</span></span>
<span data-ttu-id="2b3f2-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2b3f2-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2b3f2-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2b3f2-150">JSON Representation</span></span>
<span data-ttu-id="2b3f2-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2b3f2-151">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppConfiguration",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ]
}
```



