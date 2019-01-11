---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5766e3a467a157bac0d876fd0178dc3ba1cb94e2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888085"
---
# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="dc8bd-103">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="dc8bd-103">managedAppPolicy resource type</span></span>

> <span data-ttu-id="dc8bd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dc8bd-105">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-105">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="dc8bd-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc8bd-106">Methods</span></span>
|<span data-ttu-id="dc8bd-107">Método</span><span class="sxs-lookup"><span data-stu-id="dc8bd-107">Method</span></span>|<span data-ttu-id="dc8bd-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc8bd-108">Return Type</span></span>|<span data-ttu-id="dc8bd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc8bd-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="dc8bd-110">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="dc8bd-110">List managedAppPolicies</span></span>](../api/intune-mam-managedapppolicy-list.md)|<span data-ttu-id="dc8bd-111">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="dc8bd-111">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="dc8bd-112">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="dc8bd-112">List properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="dc8bd-113">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="dc8bd-113">Get managedAppPolicy</span></span>](../api/intune-mam-managedapppolicy-get.md)|[<span data-ttu-id="dc8bd-114">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="dc8bd-114">managedAppPolicy</span></span>](../resources/intune-mam-managedapppolicy.md)|<span data-ttu-id="dc8bd-115">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="dc8bd-115">Read properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="dc8bd-116">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="dc8bd-116">targetApps action</span></span>](../api/intune-mam-managedapppolicy-targetapps.md)|<span data-ttu-id="dc8bd-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dc8bd-117">None</span></span>|<span data-ttu-id="dc8bd-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dc8bd-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="dc8bd-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc8bd-119">Properties</span></span>
|<span data-ttu-id="dc8bd-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc8bd-120">Property</span></span>|<span data-ttu-id="dc8bd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc8bd-121">Type</span></span>|<span data-ttu-id="dc8bd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc8bd-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dc8bd-123">displayName</span><span class="sxs-lookup"><span data-stu-id="dc8bd-123">displayName</span></span>|<span data-ttu-id="dc8bd-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="dc8bd-124">String</span></span>|<span data-ttu-id="dc8bd-125">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-125">Policy display name.</span></span>|
|<span data-ttu-id="dc8bd-126">descripción</span><span class="sxs-lookup"><span data-stu-id="dc8bd-126">description</span></span>|<span data-ttu-id="dc8bd-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="dc8bd-127">String</span></span>|<span data-ttu-id="dc8bd-128">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-128">The policy's description.</span></span>|
|<span data-ttu-id="dc8bd-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="dc8bd-129">createdDateTime</span></span>|<span data-ttu-id="dc8bd-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dc8bd-130">DateTimeOffset</span></span>|<span data-ttu-id="dc8bd-131">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-131">The date and time the policy was created.</span></span>|
|<span data-ttu-id="dc8bd-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="dc8bd-132">lastModifiedDateTime</span></span>|<span data-ttu-id="dc8bd-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dc8bd-133">DateTimeOffset</span></span>|<span data-ttu-id="dc8bd-134">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-134">Last time the policy was modified.</span></span>|
|<span data-ttu-id="dc8bd-135">id</span><span class="sxs-lookup"><span data-stu-id="dc8bd-135">id</span></span>|<span data-ttu-id="dc8bd-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="dc8bd-136">String</span></span>|<span data-ttu-id="dc8bd-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-137">Key of the entity.</span></span>|
|<span data-ttu-id="dc8bd-138">version</span><span class="sxs-lookup"><span data-stu-id="dc8bd-138">version</span></span>|<span data-ttu-id="dc8bd-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="dc8bd-139">String</span></span>|<span data-ttu-id="dc8bd-140">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-140">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dc8bd-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dc8bd-141">Relationships</span></span>
<span data-ttu-id="dc8bd-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="dc8bd-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="dc8bd-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc8bd-143">JSON Representation</span></span>
<span data-ttu-id="dc8bd-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-144">Here is a JSON representation of the resource.</span></span>
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



