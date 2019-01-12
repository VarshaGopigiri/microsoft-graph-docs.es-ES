---
title: Tipo de recurso managedAppConfiguration
description: Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2bf4e8ce0d32bea7714ae489167dbb582043fa5a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936637"
---
# <a name="managedappconfiguration-resource-type"></a><span data-ttu-id="ce0ea-103">Tipo de recurso managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce0ea-103">managedAppConfiguration resource type</span></span>

> <span data-ttu-id="ce0ea-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce0ea-105">Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-105">Configuration used to deliver a set of custom settings as-is to apps for users to whom the configuration is scoped</span></span>

<span data-ttu-id="ce0ea-106">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ce0ea-106">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="ce0ea-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce0ea-107">Methods</span></span>
|<span data-ttu-id="ce0ea-108">Método</span><span class="sxs-lookup"><span data-stu-id="ce0ea-108">Method</span></span>|<span data-ttu-id="ce0ea-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce0ea-109">Return Type</span></span>|<span data-ttu-id="ce0ea-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce0ea-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ce0ea-111">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="ce0ea-111">List managedAppConfigurations</span></span>](../api/intune-mam-managedappconfiguration-list.md)|<span data-ttu-id="ce0ea-112">Colección [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce0ea-112">[managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) collection</span></span>|<span data-ttu-id="ce0ea-113">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-113">List properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="ce0ea-114">Obtener managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce0ea-114">Get managedAppConfiguration</span></span>](../api/intune-mam-managedappconfiguration-get.md)|[<span data-ttu-id="ce0ea-115">managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce0ea-115">managedAppConfiguration</span></span>](../resources/intune-mam-managedappconfiguration.md)|<span data-ttu-id="ce0ea-116">Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-116">Read properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ce0ea-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce0ea-117">Properties</span></span>
|<span data-ttu-id="ce0ea-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce0ea-118">Property</span></span>|<span data-ttu-id="ce0ea-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce0ea-119">Type</span></span>|<span data-ttu-id="ce0ea-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce0ea-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce0ea-121">displayName</span><span class="sxs-lookup"><span data-stu-id="ce0ea-121">displayName</span></span>|<span data-ttu-id="ce0ea-122">String</span><span class="sxs-lookup"><span data-stu-id="ce0ea-122">String</span></span>|<span data-ttu-id="ce0ea-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-123">Policy display name.</span></span> <span data-ttu-id="ce0ea-124">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-124">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="ce0ea-125">descripción</span><span class="sxs-lookup"><span data-stu-id="ce0ea-125">description</span></span>|<span data-ttu-id="ce0ea-126">String</span><span class="sxs-lookup"><span data-stu-id="ce0ea-126">String</span></span>|<span data-ttu-id="ce0ea-127">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-127">The policy's description.</span></span> <span data-ttu-id="ce0ea-128">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-128">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="ce0ea-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ce0ea-129">createdDateTime</span></span>|<span data-ttu-id="ce0ea-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce0ea-130">DateTimeOffset</span></span>|<span data-ttu-id="ce0ea-131">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-131">The date and time the policy was created.</span></span> <span data-ttu-id="ce0ea-132">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-132">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="ce0ea-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ce0ea-133">lastModifiedDateTime</span></span>|<span data-ttu-id="ce0ea-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce0ea-134">DateTimeOffset</span></span>|<span data-ttu-id="ce0ea-135">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-135">Last time the policy was modified.</span></span> <span data-ttu-id="ce0ea-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="ce0ea-137">id</span><span class="sxs-lookup"><span data-stu-id="ce0ea-137">id</span></span>|<span data-ttu-id="ce0ea-138">String</span><span class="sxs-lookup"><span data-stu-id="ce0ea-138">String</span></span>|<span data-ttu-id="ce0ea-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-139">Key of the entity.</span></span> <span data-ttu-id="ce0ea-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="ce0ea-141">version</span><span class="sxs-lookup"><span data-stu-id="ce0ea-141">version</span></span>|<span data-ttu-id="ce0ea-142">String</span><span class="sxs-lookup"><span data-stu-id="ce0ea-142">String</span></span>|<span data-ttu-id="ce0ea-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-143">Version of the entity.</span></span> <span data-ttu-id="ce0ea-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ea-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="ce0ea-145">customSettings</span><span class="sxs-lookup"><span data-stu-id="ce0ea-145">customSettings</span></span>|<span data-ttu-id="ce0ea-146">Colección [keyValuePair](../resources/intune-mam-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="ce0ea-146">[keyValuePair](../resources/intune-mam-keyvaluepair.md) collection</span></span>|<span data-ttu-id="ce0ea-147">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio</span><span class="sxs-lookup"><span data-stu-id="ce0ea-147">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service</span></span>|

## <a name="relationships"></a><span data-ttu-id="ce0ea-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ce0ea-148">Relationships</span></span>
<span data-ttu-id="ce0ea-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ce0ea-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ce0ea-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce0ea-150">JSON Representation</span></span>
<span data-ttu-id="ce0ea-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ce0ea-151">Here is a JSON representation of the resource.</span></span>
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



