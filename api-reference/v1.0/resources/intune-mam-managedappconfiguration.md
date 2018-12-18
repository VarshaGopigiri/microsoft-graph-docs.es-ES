---
title: Tipo de recurso managedAppConfiguration
description: Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.
author: tfitzmac
ms.openlocfilehash: e4b20c642f49b2f110ced2f72a5a54a6583b561f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346910"
---
# <a name="managedappconfiguration-resource-type"></a><span data-ttu-id="559a8-103">Tipo de recurso managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="559a8-103">managedAppConfiguration resource type</span></span>

> <span data-ttu-id="559a8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="559a8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="559a8-105">Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.</span><span class="sxs-lookup"><span data-stu-id="559a8-105">Configuration used to deliver a set of custom settings as-is to apps for users to whom the configuration is scoped</span></span>

<span data-ttu-id="559a8-106">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="559a8-106">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="559a8-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="559a8-107">Methods</span></span>
|<span data-ttu-id="559a8-108">Método</span><span class="sxs-lookup"><span data-stu-id="559a8-108">Method</span></span>|<span data-ttu-id="559a8-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="559a8-109">Return Type</span></span>|<span data-ttu-id="559a8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="559a8-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="559a8-111">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="559a8-111">List managedAppConfigurations</span></span>](../api/intune-mam-managedappconfiguration-list.md)|<span data-ttu-id="559a8-112">Colección [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="559a8-112">[managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) collection</span></span>|<span data-ttu-id="559a8-113">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-113">List properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="559a8-114">Obtener managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="559a8-114">Get managedAppConfiguration</span></span>](../api/intune-mam-managedappconfiguration-get.md)|[<span data-ttu-id="559a8-115">managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="559a8-115">managedAppConfiguration</span></span>](../resources/intune-mam-managedappconfiguration.md)|<span data-ttu-id="559a8-116">Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-116">Read properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="559a8-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="559a8-117">Properties</span></span>
|<span data-ttu-id="559a8-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="559a8-118">Property</span></span>|<span data-ttu-id="559a8-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="559a8-119">Type</span></span>|<span data-ttu-id="559a8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="559a8-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="559a8-121">displayName</span><span class="sxs-lookup"><span data-stu-id="559a8-121">displayName</span></span>|<span data-ttu-id="559a8-122">String</span><span class="sxs-lookup"><span data-stu-id="559a8-122">String</span></span>|<span data-ttu-id="559a8-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="559a8-123">Policy display name.</span></span> <span data-ttu-id="559a8-124">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-124">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="559a8-125">descripción</span><span class="sxs-lookup"><span data-stu-id="559a8-125">description</span></span>|<span data-ttu-id="559a8-126">String</span><span class="sxs-lookup"><span data-stu-id="559a8-126">String</span></span>|<span data-ttu-id="559a8-127">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="559a8-127">The policy's description.</span></span> <span data-ttu-id="559a8-128">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-128">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="559a8-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="559a8-129">createdDateTime</span></span>|<span data-ttu-id="559a8-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="559a8-130">DateTimeOffset</span></span>|<span data-ttu-id="559a8-131">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="559a8-131">The date and time the policy was created.</span></span> <span data-ttu-id="559a8-132">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-132">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="559a8-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="559a8-133">lastModifiedDateTime</span></span>|<span data-ttu-id="559a8-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="559a8-134">DateTimeOffset</span></span>|<span data-ttu-id="559a8-135">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="559a8-135">Last time the policy was modified.</span></span> <span data-ttu-id="559a8-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="559a8-137">id</span><span class="sxs-lookup"><span data-stu-id="559a8-137">id</span></span>|<span data-ttu-id="559a8-138">String</span><span class="sxs-lookup"><span data-stu-id="559a8-138">String</span></span>|<span data-ttu-id="559a8-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="559a8-139">Key of the entity.</span></span> <span data-ttu-id="559a8-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="559a8-141">version</span><span class="sxs-lookup"><span data-stu-id="559a8-141">version</span></span>|<span data-ttu-id="559a8-142">String</span><span class="sxs-lookup"><span data-stu-id="559a8-142">String</span></span>|<span data-ttu-id="559a8-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="559a8-143">Version of the entity.</span></span> <span data-ttu-id="559a8-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="559a8-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="559a8-145">customSettings</span><span class="sxs-lookup"><span data-stu-id="559a8-145">customSettings</span></span>|<span data-ttu-id="559a8-146">Colección [keyValuePair](../resources/intune-mam-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="559a8-146">[keyValuePair](../resources/intune-mam-keyvaluepair.md) collection</span></span>|<span data-ttu-id="559a8-147">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio</span><span class="sxs-lookup"><span data-stu-id="559a8-147">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service</span></span>|

## <a name="relationships"></a><span data-ttu-id="559a8-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="559a8-148">Relationships</span></span>
<span data-ttu-id="559a8-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="559a8-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="559a8-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="559a8-150">JSON Representation</span></span>
<span data-ttu-id="559a8-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="559a8-151">Here is a JSON representation of the resource.</span></span>
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



