---
title: Tipo de recurso managedAppPolicy
description: El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 45a8365bb7a1ea97c156921cfbd923ba9b52dd1b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937505"
---
# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="63033-103">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="63033-103">managedAppPolicy resource type</span></span>

> <span data-ttu-id="63033-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63033-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63033-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63033-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63033-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63033-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63033-107">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="63033-107">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="63033-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="63033-108">Methods</span></span>
|<span data-ttu-id="63033-109">Método</span><span class="sxs-lookup"><span data-stu-id="63033-109">Method</span></span>|<span data-ttu-id="63033-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63033-110">Return Type</span></span>|<span data-ttu-id="63033-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="63033-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="63033-112">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="63033-112">List managedAppPolicies</span></span>](../api/intune-mam-managedapppolicy-list.md)|<span data-ttu-id="63033-113">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="63033-113">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="63033-114">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63033-114">List properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="63033-115">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="63033-115">Get managedAppPolicy</span></span>](../api/intune-mam-managedapppolicy-get.md)|[<span data-ttu-id="63033-116">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="63033-116">managedAppPolicy</span></span>](../resources/intune-mam-managedapppolicy.md)|<span data-ttu-id="63033-117">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63033-117">Read properties and relationships of the [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="63033-118">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="63033-118">targetApps action</span></span>](../api/intune-mam-managedapppolicy-targetapps.md)|<span data-ttu-id="63033-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="63033-119">None</span></span>|<span data-ttu-id="63033-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63033-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="63033-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63033-121">Properties</span></span>
|<span data-ttu-id="63033-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63033-122">Property</span></span>|<span data-ttu-id="63033-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="63033-123">Type</span></span>|<span data-ttu-id="63033-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="63033-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63033-125">displayName</span><span class="sxs-lookup"><span data-stu-id="63033-125">displayName</span></span>|<span data-ttu-id="63033-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="63033-126">String</span></span>|<span data-ttu-id="63033-127">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="63033-127">Policy display name.</span></span>|
|<span data-ttu-id="63033-128">descripción</span><span class="sxs-lookup"><span data-stu-id="63033-128">description</span></span>|<span data-ttu-id="63033-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="63033-129">String</span></span>|<span data-ttu-id="63033-130">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="63033-130">The policy's description.</span></span>|
|<span data-ttu-id="63033-131">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="63033-131">createdDateTime</span></span>|<span data-ttu-id="63033-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63033-132">DateTimeOffset</span></span>|<span data-ttu-id="63033-133">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="63033-133">The date and time the policy was created.</span></span>|
|<span data-ttu-id="63033-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="63033-134">lastModifiedDateTime</span></span>|<span data-ttu-id="63033-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63033-135">DateTimeOffset</span></span>|<span data-ttu-id="63033-136">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="63033-136">Last time the policy was modified.</span></span>|
|<span data-ttu-id="63033-137">id</span><span class="sxs-lookup"><span data-stu-id="63033-137">id</span></span>|<span data-ttu-id="63033-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="63033-138">String</span></span>|<span data-ttu-id="63033-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63033-139">Key of the entity.</span></span>|
|<span data-ttu-id="63033-140">version</span><span class="sxs-lookup"><span data-stu-id="63033-140">version</span></span>|<span data-ttu-id="63033-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="63033-141">String</span></span>|<span data-ttu-id="63033-142">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63033-142">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="63033-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="63033-143">Relationships</span></span>
<span data-ttu-id="63033-144">Ninguna</span><span class="sxs-lookup"><span data-stu-id="63033-144">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="63033-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="63033-145">JSON Representation</span></span>
<span data-ttu-id="63033-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="63033-146">Here is a JSON representation of the resource.</span></span>
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





