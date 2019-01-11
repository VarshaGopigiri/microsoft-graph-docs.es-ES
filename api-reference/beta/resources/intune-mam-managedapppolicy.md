---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3cea81d492e708c1d21039c6286fe01e70a590b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840736"
---
# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="50b8e-103">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="50b8e-103">managedAppPolicy resource type</span></span>

> <span data-ttu-id="50b8e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50b8e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50b8e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50b8e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="50b8e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50b8e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50b8e-107">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="50b8e-107">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="50b8e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="50b8e-108">Methods</span></span>
|<span data-ttu-id="50b8e-109">Método</span><span class="sxs-lookup"><span data-stu-id="50b8e-109">Method</span></span>|<span data-ttu-id="50b8e-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50b8e-110">Return Type</span></span>|<span data-ttu-id="50b8e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="50b8e-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="50b8e-112">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="50b8e-112">List managedAppPolicies</span></span>](../api/intune-mam-managedapppolicy-list.md)|<span data-ttu-id="50b8e-113">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="50b8e-113">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="50b8e-114">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="50b8e-114">List properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="50b8e-115">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="50b8e-115">Get managedAppPolicy</span></span>](../api/intune-mam-managedapppolicy-get.md)|[<span data-ttu-id="50b8e-116">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="50b8e-116">managedAppPolicy</span></span>](../resources/intune-mam-managedapppolicy.md)|<span data-ttu-id="50b8e-117">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="50b8e-117">Read properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="50b8e-118">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="50b8e-118">targetApps action</span></span>](../api/intune-mam-managedapppolicy-targetapps.md)|<span data-ttu-id="50b8e-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="50b8e-119">None</span></span>|<span data-ttu-id="50b8e-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="50b8e-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="50b8e-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50b8e-121">Properties</span></span>
|<span data-ttu-id="50b8e-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50b8e-122">Property</span></span>|<span data-ttu-id="50b8e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="50b8e-123">Type</span></span>|<span data-ttu-id="50b8e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="50b8e-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50b8e-125">displayName</span><span class="sxs-lookup"><span data-stu-id="50b8e-125">displayName</span></span>|<span data-ttu-id="50b8e-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b8e-126">String</span></span>|<span data-ttu-id="50b8e-127">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="50b8e-127">Policy display name.</span></span>|
|<span data-ttu-id="50b8e-128">descripción</span><span class="sxs-lookup"><span data-stu-id="50b8e-128">description</span></span>|<span data-ttu-id="50b8e-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b8e-129">String</span></span>|<span data-ttu-id="50b8e-130">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="50b8e-130">The policy's description.</span></span>|
|<span data-ttu-id="50b8e-131">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="50b8e-131">createdDateTime</span></span>|<span data-ttu-id="50b8e-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50b8e-132">DateTimeOffset</span></span>|<span data-ttu-id="50b8e-133">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="50b8e-133">The date and time the policy was created.</span></span>|
|<span data-ttu-id="50b8e-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="50b8e-134">lastModifiedDateTime</span></span>|<span data-ttu-id="50b8e-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50b8e-135">DateTimeOffset</span></span>|<span data-ttu-id="50b8e-136">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="50b8e-136">Last time the policy was modified.</span></span>|
|<span data-ttu-id="50b8e-137">id</span><span class="sxs-lookup"><span data-stu-id="50b8e-137">id</span></span>|<span data-ttu-id="50b8e-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b8e-138">String</span></span>|<span data-ttu-id="50b8e-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="50b8e-139">Key of the entity.</span></span>|
|<span data-ttu-id="50b8e-140">version</span><span class="sxs-lookup"><span data-stu-id="50b8e-140">version</span></span>|<span data-ttu-id="50b8e-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b8e-141">String</span></span>|<span data-ttu-id="50b8e-142">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="50b8e-142">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="50b8e-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="50b8e-143">Relationships</span></span>
<span data-ttu-id="50b8e-144">Ninguna</span><span class="sxs-lookup"><span data-stu-id="50b8e-144">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="50b8e-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50b8e-145">JSON Representation</span></span>
<span data-ttu-id="50b8e-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50b8e-146">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicy",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String"
}
```





