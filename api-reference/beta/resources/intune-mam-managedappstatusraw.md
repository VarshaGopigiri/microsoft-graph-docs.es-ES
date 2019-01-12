---
title: Tipo de recurso managedAppStatusRaw
description: Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4497f0dc1b7be59b08c7b07d9cd381746544ef47
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922119"
---
# <a name="managedappstatusraw-resource-type"></a><span data-ttu-id="85e9d-103">Tipo de recurso managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="85e9d-103">managedAppStatusRaw resource type</span></span>

> <span data-ttu-id="85e9d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="85e9d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="85e9d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="85e9d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="85e9d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="85e9d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="85e9d-107">Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.</span><span class="sxs-lookup"><span data-stu-id="85e9d-107">Represents an un-typed status report about organizations app protection and configuration.</span></span>

<span data-ttu-id="85e9d-108">Hereda de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="85e9d-108">Inherits from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>

## <a name="methods"></a><span data-ttu-id="85e9d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="85e9d-109">Methods</span></span>
|<span data-ttu-id="85e9d-110">Método</span><span class="sxs-lookup"><span data-stu-id="85e9d-110">Method</span></span>|<span data-ttu-id="85e9d-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85e9d-111">Return Type</span></span>|<span data-ttu-id="85e9d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="85e9d-112">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="85e9d-113">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="85e9d-113">List managedAppStatusRaws</span></span>](../api/intune-mam-managedappstatusraw-list.md)|<span data-ttu-id="85e9d-114">Colección [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md)</span><span class="sxs-lookup"><span data-stu-id="85e9d-114">[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) collection</span></span>|<span data-ttu-id="85e9d-115">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="85e9d-115">List properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects.</span></span>|
|[<span data-ttu-id="85e9d-116">Obtener managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="85e9d-116">Get managedAppStatusRaw</span></span>](../api/intune-mam-managedappstatusraw-get.md)|[<span data-ttu-id="85e9d-117">managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="85e9d-117">managedAppStatusRaw</span></span>](../resources/intune-mam-managedappstatusraw.md)|<span data-ttu-id="85e9d-118">Lea las propiedades y las relaciones del objeto [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="85e9d-118">Read properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="85e9d-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85e9d-119">Properties</span></span>
|<span data-ttu-id="85e9d-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85e9d-120">Property</span></span>|<span data-ttu-id="85e9d-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="85e9d-121">Type</span></span>|<span data-ttu-id="85e9d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="85e9d-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="85e9d-123">displayName</span><span class="sxs-lookup"><span data-stu-id="85e9d-123">displayName</span></span>|<span data-ttu-id="85e9d-124">String</span><span class="sxs-lookup"><span data-stu-id="85e9d-124">String</span></span>|<span data-ttu-id="85e9d-125">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="85e9d-125">Friendly name of the status report.</span></span> <span data-ttu-id="85e9d-126">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="85e9d-126">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="85e9d-127">id</span><span class="sxs-lookup"><span data-stu-id="85e9d-127">id</span></span>|<span data-ttu-id="85e9d-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="85e9d-128">String</span></span>|<span data-ttu-id="85e9d-129">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="85e9d-129">Key of the entity.</span></span> <span data-ttu-id="85e9d-130">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="85e9d-130">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="85e9d-131">version</span><span class="sxs-lookup"><span data-stu-id="85e9d-131">version</span></span>|<span data-ttu-id="85e9d-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="85e9d-132">String</span></span>|<span data-ttu-id="85e9d-133">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="85e9d-133">Version of the entity.</span></span> <span data-ttu-id="85e9d-134">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="85e9d-134">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="85e9d-135">content</span><span class="sxs-lookup"><span data-stu-id="85e9d-135">content</span></span>|[<span data-ttu-id="85e9d-136">Json</span><span class="sxs-lookup"><span data-stu-id="85e9d-136">Json</span></span>](../resources/intune-mam-json.md)|<span data-ttu-id="85e9d-137">Contenido del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="85e9d-137">Status report content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="85e9d-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="85e9d-138">Relationships</span></span>
<span data-ttu-id="85e9d-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="85e9d-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="85e9d-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="85e9d-140">JSON Representation</span></span>
<span data-ttu-id="85e9d-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="85e9d-141">Here is a JSON representation of the resource.</span></span>
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





