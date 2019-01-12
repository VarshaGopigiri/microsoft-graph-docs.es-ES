---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5054566f0ee80940165ba19f8f0da197b5e4f3c0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981108"
---
# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="a4a88-103">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="a4a88-103">managedAppPolicy resource type</span></span>

> <span data-ttu-id="a4a88-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4a88-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4a88-105">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a4a88-105">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="a4a88-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4a88-106">Methods</span></span>
|<span data-ttu-id="a4a88-107">Método</span><span class="sxs-lookup"><span data-stu-id="a4a88-107">Method</span></span>|<span data-ttu-id="a4a88-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4a88-108">Return Type</span></span>|<span data-ttu-id="a4a88-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4a88-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a4a88-110">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="a4a88-110">List managedAppPolicies</span></span>](../api/intune-mam-managedapppolicy-list.md)|<span data-ttu-id="a4a88-111">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a4a88-111">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="a4a88-112">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a4a88-112">List properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="a4a88-113">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="a4a88-113">Get managedAppPolicy</span></span>](../api/intune-mam-managedapppolicy-get.md)|[<span data-ttu-id="a4a88-114">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="a4a88-114">managedAppPolicy</span></span>](../resources/intune-mam-managedapppolicy.md)|<span data-ttu-id="a4a88-115">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a4a88-115">Read properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="a4a88-116">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="a4a88-116">targetApps action</span></span>](../api/intune-mam-managedapppolicy-targetapps.md)|<span data-ttu-id="a4a88-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a4a88-117">None</span></span>|<span data-ttu-id="a4a88-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a4a88-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="a4a88-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4a88-119">Properties</span></span>
|<span data-ttu-id="a4a88-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4a88-120">Property</span></span>|<span data-ttu-id="a4a88-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4a88-121">Type</span></span>|<span data-ttu-id="a4a88-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4a88-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4a88-123">displayName</span><span class="sxs-lookup"><span data-stu-id="a4a88-123">displayName</span></span>|<span data-ttu-id="a4a88-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a88-124">String</span></span>|<span data-ttu-id="a4a88-125">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="a4a88-125">Policy display name.</span></span>|
|<span data-ttu-id="a4a88-126">descripción</span><span class="sxs-lookup"><span data-stu-id="a4a88-126">description</span></span>|<span data-ttu-id="a4a88-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a88-127">String</span></span>|<span data-ttu-id="a4a88-128">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="a4a88-128">The policy's description.</span></span>|
|<span data-ttu-id="a4a88-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a4a88-129">createdDateTime</span></span>|<span data-ttu-id="a4a88-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4a88-130">DateTimeOffset</span></span>|<span data-ttu-id="a4a88-131">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="a4a88-131">The date and time the policy was created.</span></span>|
|<span data-ttu-id="a4a88-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a4a88-132">lastModifiedDateTime</span></span>|<span data-ttu-id="a4a88-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4a88-133">DateTimeOffset</span></span>|<span data-ttu-id="a4a88-134">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="a4a88-134">Last time the policy was modified.</span></span>|
|<span data-ttu-id="a4a88-135">id</span><span class="sxs-lookup"><span data-stu-id="a4a88-135">id</span></span>|<span data-ttu-id="a4a88-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a88-136">String</span></span>|<span data-ttu-id="a4a88-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a4a88-137">Key of the entity.</span></span>|
|<span data-ttu-id="a4a88-138">version</span><span class="sxs-lookup"><span data-stu-id="a4a88-138">version</span></span>|<span data-ttu-id="a4a88-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a88-139">String</span></span>|<span data-ttu-id="a4a88-140">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a4a88-140">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a4a88-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a4a88-141">Relationships</span></span>
<span data-ttu-id="a4a88-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a4a88-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a4a88-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a4a88-143">JSON Representation</span></span>
<span data-ttu-id="a4a88-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a4a88-144">Here is a JSON representation of the resource.</span></span>
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



