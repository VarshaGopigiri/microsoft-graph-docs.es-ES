---
title: Tipo de recurso managedAppStatusRaw
description: Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 19c00f6d6bc1eb642320f77d9b5dfcc2fe842b1e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856857"
---
# <a name="managedappstatusraw-resource-type"></a><span data-ttu-id="4271f-103">Tipo de recurso managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="4271f-103">managedAppStatusRaw resource type</span></span>

> <span data-ttu-id="4271f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4271f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4271f-105">Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.</span><span class="sxs-lookup"><span data-stu-id="4271f-105">Represents an un-typed status report about organizations app protection and configuration.</span></span>

<span data-ttu-id="4271f-106">Hereda de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="4271f-106">Inherits from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>

## <a name="methods"></a><span data-ttu-id="4271f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="4271f-107">Methods</span></span>
|<span data-ttu-id="4271f-108">Método</span><span class="sxs-lookup"><span data-stu-id="4271f-108">Method</span></span>|<span data-ttu-id="4271f-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4271f-109">Return Type</span></span>|<span data-ttu-id="4271f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4271f-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="4271f-111">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="4271f-111">List managedAppStatusRaws</span></span>](../api/intune-mam-managedappstatusraw-list.md)|<span data-ttu-id="4271f-112">Colección [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md)</span><span class="sxs-lookup"><span data-stu-id="4271f-112">[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) collection</span></span>|<span data-ttu-id="4271f-113">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="4271f-113">List properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects.</span></span>|
|[<span data-ttu-id="4271f-114">Obtener managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="4271f-114">Get managedAppStatusRaw</span></span>](../api/intune-mam-managedappstatusraw-get.md)|[<span data-ttu-id="4271f-115">managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="4271f-115">managedAppStatusRaw</span></span>](../resources/intune-mam-managedappstatusraw.md)|<span data-ttu-id="4271f-116">Lea las propiedades y las relaciones del objeto [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="4271f-116">Read properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="4271f-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4271f-117">Properties</span></span>
|<span data-ttu-id="4271f-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4271f-118">Property</span></span>|<span data-ttu-id="4271f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="4271f-119">Type</span></span>|<span data-ttu-id="4271f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4271f-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4271f-121">displayName</span><span class="sxs-lookup"><span data-stu-id="4271f-121">displayName</span></span>|<span data-ttu-id="4271f-122">String</span><span class="sxs-lookup"><span data-stu-id="4271f-122">String</span></span>|<span data-ttu-id="4271f-123">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="4271f-123">Friendly name of the status report.</span></span> <span data-ttu-id="4271f-124">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="4271f-124">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="4271f-125">id</span><span class="sxs-lookup"><span data-stu-id="4271f-125">id</span></span>|<span data-ttu-id="4271f-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="4271f-126">String</span></span>|<span data-ttu-id="4271f-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4271f-127">Key of the entity.</span></span> <span data-ttu-id="4271f-128">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="4271f-128">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="4271f-129">version</span><span class="sxs-lookup"><span data-stu-id="4271f-129">version</span></span>|<span data-ttu-id="4271f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="4271f-130">String</span></span>|<span data-ttu-id="4271f-131">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4271f-131">Version of the entity.</span></span> <span data-ttu-id="4271f-132">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="4271f-132">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="4271f-133">content</span><span class="sxs-lookup"><span data-stu-id="4271f-133">content</span></span>|[<span data-ttu-id="4271f-134">Json</span><span class="sxs-lookup"><span data-stu-id="4271f-134">Json</span></span>](../resources/intune-mam-json.md)|<span data-ttu-id="4271f-135">Contenido del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="4271f-135">Status report content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4271f-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4271f-136">Relationships</span></span>
<span data-ttu-id="4271f-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4271f-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4271f-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4271f-138">JSON Representation</span></span>
<span data-ttu-id="4271f-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4271f-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppStatusRaw"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```



