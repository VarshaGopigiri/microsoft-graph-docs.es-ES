---
title: Tipo de recurso managedAppConfiguration
description: Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.
author: tfitzmac
ms.openlocfilehash: ffbbb5758fd8192e5acc5c674caa6f5acecdcf3c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358523"
---
# <a name="managedappconfiguration-resource-type"></a><span data-ttu-id="2fede-103">Tipo de recurso managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fede-103">managedAppConfiguration resource type</span></span>

> <span data-ttu-id="2fede-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2fede-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2fede-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2fede-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2fede-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2fede-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2fede-107">Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.</span><span class="sxs-lookup"><span data-stu-id="2fede-107">Configuration used to deliver a set of custom settings as-is to apps for users to whom the configuration is scoped</span></span>

<span data-ttu-id="2fede-108">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="2fede-108">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="2fede-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2fede-109">Methods</span></span>
|<span data-ttu-id="2fede-110">Método</span><span class="sxs-lookup"><span data-stu-id="2fede-110">Method</span></span>|<span data-ttu-id="2fede-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fede-111">Return Type</span></span>|<span data-ttu-id="2fede-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fede-112">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="2fede-113">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="2fede-113">List managedAppConfigurations</span></span>](../api/intune-mam-managedappconfiguration-list.md)|<span data-ttu-id="2fede-114">Colección [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2fede-114">[managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) collection</span></span>|<span data-ttu-id="2fede-115">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-115">List properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="2fede-116">Obtener managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fede-116">Get managedAppConfiguration</span></span>](../api/intune-mam-managedappconfiguration-get.md)|[<span data-ttu-id="2fede-117">managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fede-117">managedAppConfiguration</span></span>](../resources/intune-mam-managedappconfiguration.md)|<span data-ttu-id="2fede-118">Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-118">Read properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="2fede-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fede-119">Properties</span></span>
|<span data-ttu-id="2fede-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fede-120">Property</span></span>|<span data-ttu-id="2fede-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fede-121">Type</span></span>|<span data-ttu-id="2fede-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fede-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2fede-123">displayName</span><span class="sxs-lookup"><span data-stu-id="2fede-123">displayName</span></span>|<span data-ttu-id="2fede-124">String</span><span class="sxs-lookup"><span data-stu-id="2fede-124">String</span></span>|<span data-ttu-id="2fede-125">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2fede-125">Policy display name.</span></span> <span data-ttu-id="2fede-126">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-126">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2fede-127">descripción</span><span class="sxs-lookup"><span data-stu-id="2fede-127">description</span></span>|<span data-ttu-id="2fede-128">String</span><span class="sxs-lookup"><span data-stu-id="2fede-128">String</span></span>|<span data-ttu-id="2fede-129">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2fede-129">The policy's description.</span></span> <span data-ttu-id="2fede-130">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-130">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2fede-131">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2fede-131">createdDateTime</span></span>|<span data-ttu-id="2fede-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2fede-132">DateTimeOffset</span></span>|<span data-ttu-id="2fede-133">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2fede-133">The date and time the policy was created.</span></span> <span data-ttu-id="2fede-134">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-134">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2fede-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2fede-135">lastModifiedDateTime</span></span>|<span data-ttu-id="2fede-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2fede-136">DateTimeOffset</span></span>|<span data-ttu-id="2fede-137">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="2fede-137">Last time the policy was modified.</span></span> <span data-ttu-id="2fede-138">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-138">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2fede-139">id</span><span class="sxs-lookup"><span data-stu-id="2fede-139">id</span></span>|<span data-ttu-id="2fede-140">String</span><span class="sxs-lookup"><span data-stu-id="2fede-140">String</span></span>|<span data-ttu-id="2fede-141">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2fede-141">Key of the entity.</span></span> <span data-ttu-id="2fede-142">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-142">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2fede-143">version</span><span class="sxs-lookup"><span data-stu-id="2fede-143">version</span></span>|<span data-ttu-id="2fede-144">String</span><span class="sxs-lookup"><span data-stu-id="2fede-144">String</span></span>|<span data-ttu-id="2fede-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2fede-145">Version of the entity.</span></span> <span data-ttu-id="2fede-146">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2fede-146">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="2fede-147">customSettings</span><span class="sxs-lookup"><span data-stu-id="2fede-147">customSettings</span></span>|<span data-ttu-id="2fede-148">Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="2fede-148">[keyValuePair](../resources/intune-shared-keyvaluepair.md) collection</span></span>|<span data-ttu-id="2fede-149">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio</span><span class="sxs-lookup"><span data-stu-id="2fede-149">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service</span></span>|

## <a name="relationships"></a><span data-ttu-id="2fede-150">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2fede-150">Relationships</span></span>
<span data-ttu-id="2fede-151">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2fede-151">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2fede-152">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2fede-152">JSON Representation</span></span>
<span data-ttu-id="2fede-153">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2fede-153">Here is a JSON representation of the resource.</span></span>
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





