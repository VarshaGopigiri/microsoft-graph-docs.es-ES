---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
ms.openlocfilehash: ab87690e611effa239a8471612dbb201ea6b75b8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087192"
---
# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="67e1a-103">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="67e1a-103">managedAppPolicy resource type</span></span>

> <span data-ttu-id="67e1a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="67e1a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="67e1a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="67e1a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="67e1a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="67e1a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="67e1a-107">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="67e1a-107">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="67e1a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="67e1a-108">Methods</span></span>
|<span data-ttu-id="67e1a-109">Método</span><span class="sxs-lookup"><span data-stu-id="67e1a-109">Method</span></span>|<span data-ttu-id="67e1a-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67e1a-110">Return Type</span></span>|<span data-ttu-id="67e1a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="67e1a-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="67e1a-112">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="67e1a-112">List managedAppPolicies</span></span>](../api/intune-mam-managedapppolicy-list.md)|<span data-ttu-id="67e1a-113">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="67e1a-113">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="67e1a-114">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="67e1a-114">List properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="67e1a-115">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="67e1a-115">Get managedAppPolicy</span></span>](../api/intune-mam-managedapppolicy-get.md)|[<span data-ttu-id="67e1a-116">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="67e1a-116">managedAppPolicy</span></span>](../resources/intune-mam-managedapppolicy.md)|<span data-ttu-id="67e1a-117">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="67e1a-117">Read properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="67e1a-118">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="67e1a-118">targetApps action</span></span>](../api/intune-mam-managedapppolicy-targetapps.md)|<span data-ttu-id="67e1a-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="67e1a-119">None</span></span>|<span data-ttu-id="67e1a-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="67e1a-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="67e1a-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67e1a-121">Properties</span></span>
|<span data-ttu-id="67e1a-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67e1a-122">Property</span></span>|<span data-ttu-id="67e1a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="67e1a-123">Type</span></span>|<span data-ttu-id="67e1a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="67e1a-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="67e1a-125">displayName</span><span class="sxs-lookup"><span data-stu-id="67e1a-125">displayName</span></span>|<span data-ttu-id="67e1a-126">String</span><span class="sxs-lookup"><span data-stu-id="67e1a-126">String</span></span>|<span data-ttu-id="67e1a-127">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="67e1a-127">Policy display name.</span></span>|
|<span data-ttu-id="67e1a-128">descripción</span><span class="sxs-lookup"><span data-stu-id="67e1a-128">description</span></span>|<span data-ttu-id="67e1a-129">String</span><span class="sxs-lookup"><span data-stu-id="67e1a-129">String</span></span>|<span data-ttu-id="67e1a-130">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="67e1a-130">The policy's description.</span></span>|
|<span data-ttu-id="67e1a-131">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="67e1a-131">createdDateTime</span></span>|<span data-ttu-id="67e1a-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="67e1a-132">DateTimeOffset</span></span>|<span data-ttu-id="67e1a-133">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="67e1a-133">The date and time the policy was created.</span></span>|
|<span data-ttu-id="67e1a-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="67e1a-134">lastModifiedDateTime</span></span>|<span data-ttu-id="67e1a-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="67e1a-135">DateTimeOffset</span></span>|<span data-ttu-id="67e1a-136">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="67e1a-136">Last time the policy was modified.</span></span>|
|<span data-ttu-id="67e1a-137">id</span><span class="sxs-lookup"><span data-stu-id="67e1a-137">id</span></span>|<span data-ttu-id="67e1a-138">String</span><span class="sxs-lookup"><span data-stu-id="67e1a-138">String</span></span>|<span data-ttu-id="67e1a-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="67e1a-139">Key of the entity.</span></span>|
|<span data-ttu-id="67e1a-140">version</span><span class="sxs-lookup"><span data-stu-id="67e1a-140">version</span></span>|<span data-ttu-id="67e1a-141">String</span><span class="sxs-lookup"><span data-stu-id="67e1a-141">String</span></span>|<span data-ttu-id="67e1a-142">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="67e1a-142">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="67e1a-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="67e1a-143">Relationships</span></span>
<span data-ttu-id="67e1a-144">Ninguna</span><span class="sxs-lookup"><span data-stu-id="67e1a-144">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="67e1a-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67e1a-145">JSON Representation</span></span>
<span data-ttu-id="67e1a-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="67e1a-146">Here is a JSON representation of the resource.</span></span>
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





