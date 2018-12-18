---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
author: tfitzmac
ms.openlocfilehash: b1efe085bc2fc43804049ff4b091e10c458b9a98
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310552"
---
# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="53d22-103">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="53d22-103">managedAppPolicy resource type</span></span>

> <span data-ttu-id="53d22-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53d22-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53d22-105">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="53d22-105">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="53d22-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="53d22-106">Methods</span></span>
|<span data-ttu-id="53d22-107">Método</span><span class="sxs-lookup"><span data-stu-id="53d22-107">Method</span></span>|<span data-ttu-id="53d22-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d22-108">Return Type</span></span>|<span data-ttu-id="53d22-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="53d22-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="53d22-110">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="53d22-110">List managedAppPolicies</span></span>](../api/intune-mam-managedapppolicy-list.md)|<span data-ttu-id="53d22-111">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="53d22-111">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="53d22-112">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="53d22-112">List properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="53d22-113">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="53d22-113">Get managedAppPolicy</span></span>](../api/intune-mam-managedapppolicy-get.md)|[<span data-ttu-id="53d22-114">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="53d22-114">managedAppPolicy</span></span>](../resources/intune-mam-managedapppolicy.md)|<span data-ttu-id="53d22-115">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="53d22-115">Read properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="53d22-116">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="53d22-116">targetApps action</span></span>](../api/intune-mam-managedapppolicy-targetapps.md)|<span data-ttu-id="53d22-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="53d22-117">None</span></span>|<span data-ttu-id="53d22-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="53d22-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="53d22-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53d22-119">Properties</span></span>
|<span data-ttu-id="53d22-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53d22-120">Property</span></span>|<span data-ttu-id="53d22-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="53d22-121">Type</span></span>|<span data-ttu-id="53d22-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="53d22-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53d22-123">displayName</span><span class="sxs-lookup"><span data-stu-id="53d22-123">displayName</span></span>|<span data-ttu-id="53d22-124">String</span><span class="sxs-lookup"><span data-stu-id="53d22-124">String</span></span>|<span data-ttu-id="53d22-125">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="53d22-125">Policy display name.</span></span>|
|<span data-ttu-id="53d22-126">descripción</span><span class="sxs-lookup"><span data-stu-id="53d22-126">description</span></span>|<span data-ttu-id="53d22-127">String</span><span class="sxs-lookup"><span data-stu-id="53d22-127">String</span></span>|<span data-ttu-id="53d22-128">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="53d22-128">The policy's description.</span></span>|
|<span data-ttu-id="53d22-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="53d22-129">createdDateTime</span></span>|<span data-ttu-id="53d22-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53d22-130">DateTimeOffset</span></span>|<span data-ttu-id="53d22-131">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="53d22-131">The date and time the policy was created.</span></span>|
|<span data-ttu-id="53d22-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53d22-132">lastModifiedDateTime</span></span>|<span data-ttu-id="53d22-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53d22-133">DateTimeOffset</span></span>|<span data-ttu-id="53d22-134">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="53d22-134">Last time the policy was modified.</span></span>|
|<span data-ttu-id="53d22-135">id</span><span class="sxs-lookup"><span data-stu-id="53d22-135">id</span></span>|<span data-ttu-id="53d22-136">String</span><span class="sxs-lookup"><span data-stu-id="53d22-136">String</span></span>|<span data-ttu-id="53d22-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="53d22-137">Key of the entity.</span></span>|
|<span data-ttu-id="53d22-138">version</span><span class="sxs-lookup"><span data-stu-id="53d22-138">version</span></span>|<span data-ttu-id="53d22-139">String</span><span class="sxs-lookup"><span data-stu-id="53d22-139">String</span></span>|<span data-ttu-id="53d22-140">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="53d22-140">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="53d22-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53d22-141">Relationships</span></span>
<span data-ttu-id="53d22-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="53d22-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="53d22-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53d22-143">JSON Representation</span></span>
<span data-ttu-id="53d22-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="53d22-144">Here is a JSON representation of the resource.</span></span>
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



