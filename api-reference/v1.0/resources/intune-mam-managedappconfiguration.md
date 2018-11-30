---
title: Tipo de recurso managedAppConfiguration
description: Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.
ms.openlocfilehash: 42544aeacda4494a7757a15bef75a493d96fe0cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032488"
---
# <a name="managedappconfiguration-resource-type"></a><span data-ttu-id="396d6-103">Tipo de recurso managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="396d6-103">managedAppConfiguration resource type</span></span>

> <span data-ttu-id="396d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="396d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="396d6-105">Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.</span><span class="sxs-lookup"><span data-stu-id="396d6-105">Configuration used to deliver a set of custom settings as-is to apps for users to whom the configuration is scoped</span></span>

<span data-ttu-id="396d6-106">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="396d6-106">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="396d6-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="396d6-107">Methods</span></span>
|<span data-ttu-id="396d6-108">Método</span><span class="sxs-lookup"><span data-stu-id="396d6-108">Method</span></span>|<span data-ttu-id="396d6-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="396d6-109">Return Type</span></span>|<span data-ttu-id="396d6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="396d6-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="396d6-111">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="396d6-111">List managedAppConfigurations</span></span>](../api/intune-mam-managedappconfiguration-list.md)|<span data-ttu-id="396d6-112">Colección [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="396d6-112">[managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) collection</span></span>|<span data-ttu-id="396d6-113">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-113">List properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="396d6-114">Obtener managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="396d6-114">Get managedAppConfiguration</span></span>](../api/intune-mam-managedappconfiguration-get.md)|[<span data-ttu-id="396d6-115">managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="396d6-115">managedAppConfiguration</span></span>](../resources/intune-mam-managedappconfiguration.md)|<span data-ttu-id="396d6-116">Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-116">Read properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="396d6-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="396d6-117">Properties</span></span>
|<span data-ttu-id="396d6-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="396d6-118">Property</span></span>|<span data-ttu-id="396d6-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="396d6-119">Type</span></span>|<span data-ttu-id="396d6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="396d6-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="396d6-121">displayName</span><span class="sxs-lookup"><span data-stu-id="396d6-121">displayName</span></span>|<span data-ttu-id="396d6-122">String</span><span class="sxs-lookup"><span data-stu-id="396d6-122">String</span></span>|<span data-ttu-id="396d6-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="396d6-123">Policy display name.</span></span> <span data-ttu-id="396d6-124">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-124">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="396d6-125">descripción</span><span class="sxs-lookup"><span data-stu-id="396d6-125">description</span></span>|<span data-ttu-id="396d6-126">String</span><span class="sxs-lookup"><span data-stu-id="396d6-126">String</span></span>|<span data-ttu-id="396d6-127">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="396d6-127">The policy's description.</span></span> <span data-ttu-id="396d6-128">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-128">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="396d6-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="396d6-129">createdDateTime</span></span>|<span data-ttu-id="396d6-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="396d6-130">DateTimeOffset</span></span>|<span data-ttu-id="396d6-131">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="396d6-131">The date and time the policy was created.</span></span> <span data-ttu-id="396d6-132">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-132">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="396d6-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="396d6-133">lastModifiedDateTime</span></span>|<span data-ttu-id="396d6-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="396d6-134">DateTimeOffset</span></span>|<span data-ttu-id="396d6-135">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="396d6-135">Last time the policy was modified.</span></span> <span data-ttu-id="396d6-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="396d6-137">id</span><span class="sxs-lookup"><span data-stu-id="396d6-137">id</span></span>|<span data-ttu-id="396d6-138">String</span><span class="sxs-lookup"><span data-stu-id="396d6-138">String</span></span>|<span data-ttu-id="396d6-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="396d6-139">Key of the entity.</span></span> <span data-ttu-id="396d6-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="396d6-141">version</span><span class="sxs-lookup"><span data-stu-id="396d6-141">version</span></span>|<span data-ttu-id="396d6-142">String</span><span class="sxs-lookup"><span data-stu-id="396d6-142">String</span></span>|<span data-ttu-id="396d6-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="396d6-143">Version of the entity.</span></span> <span data-ttu-id="396d6-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="396d6-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="396d6-145">customSettings</span><span class="sxs-lookup"><span data-stu-id="396d6-145">customSettings</span></span>|<span data-ttu-id="396d6-146">Colección [keyValuePair](../resources/intune-mam-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="396d6-146">[keyValuePair](../resources/intune-mam-keyvaluepair.md) collection</span></span>|<span data-ttu-id="396d6-147">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio</span><span class="sxs-lookup"><span data-stu-id="396d6-147">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service</span></span>|

## <a name="relationships"></a><span data-ttu-id="396d6-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="396d6-148">Relationships</span></span>
<span data-ttu-id="396d6-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="396d6-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="396d6-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="396d6-150">JSON Representation</span></span>
<span data-ttu-id="396d6-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="396d6-151">Here is a JSON representation of the resource.</span></span>
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



