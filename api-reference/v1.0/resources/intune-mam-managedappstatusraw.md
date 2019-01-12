---
title: Tipo de recurso managedAppStatusRaw
description: Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2370c0df7cb38059cb89b4ceab56893fbc23615c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961704"
---
# <a name="managedappstatusraw-resource-type"></a><span data-ttu-id="9407a-103">Tipo de recurso managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="9407a-103">managedAppStatusRaw resource type</span></span>

> <span data-ttu-id="9407a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9407a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9407a-105">Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.</span><span class="sxs-lookup"><span data-stu-id="9407a-105">Represents an un-typed status report about organizations app protection and configuration.</span></span>

<span data-ttu-id="9407a-106">Hereda de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="9407a-106">Inherits from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>

## <a name="methods"></a><span data-ttu-id="9407a-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9407a-107">Methods</span></span>
|<span data-ttu-id="9407a-108">Método</span><span class="sxs-lookup"><span data-stu-id="9407a-108">Method</span></span>|<span data-ttu-id="9407a-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9407a-109">Return Type</span></span>|<span data-ttu-id="9407a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9407a-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="9407a-111">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="9407a-111">List managedAppStatusRaws</span></span>](../api/intune-mam-managedappstatusraw-list.md)|<span data-ttu-id="9407a-112">Colección [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md)</span><span class="sxs-lookup"><span data-stu-id="9407a-112">[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) collection</span></span>|<span data-ttu-id="9407a-113">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="9407a-113">List properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects.</span></span>|
|[<span data-ttu-id="9407a-114">Obtener managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="9407a-114">Get managedAppStatusRaw</span></span>](../api/intune-mam-managedappstatusraw-get.md)|[<span data-ttu-id="9407a-115">managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="9407a-115">managedAppStatusRaw</span></span>](../resources/intune-mam-managedappstatusraw.md)|<span data-ttu-id="9407a-116">Lea las propiedades y las relaciones del objeto [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="9407a-116">Read properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="9407a-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9407a-117">Properties</span></span>
|<span data-ttu-id="9407a-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9407a-118">Property</span></span>|<span data-ttu-id="9407a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9407a-119">Type</span></span>|<span data-ttu-id="9407a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9407a-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9407a-121">displayName</span><span class="sxs-lookup"><span data-stu-id="9407a-121">displayName</span></span>|<span data-ttu-id="9407a-122">String</span><span class="sxs-lookup"><span data-stu-id="9407a-122">String</span></span>|<span data-ttu-id="9407a-123">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="9407a-123">Friendly name of the status report.</span></span> <span data-ttu-id="9407a-124">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="9407a-124">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="9407a-125">id</span><span class="sxs-lookup"><span data-stu-id="9407a-125">id</span></span>|<span data-ttu-id="9407a-126">String</span><span class="sxs-lookup"><span data-stu-id="9407a-126">String</span></span>|<span data-ttu-id="9407a-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9407a-127">Key of the entity.</span></span> <span data-ttu-id="9407a-128">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="9407a-128">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="9407a-129">version</span><span class="sxs-lookup"><span data-stu-id="9407a-129">version</span></span>|<span data-ttu-id="9407a-130">String</span><span class="sxs-lookup"><span data-stu-id="9407a-130">String</span></span>|<span data-ttu-id="9407a-131">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9407a-131">Version of the entity.</span></span> <span data-ttu-id="9407a-132">Heredado de [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="9407a-132">Inherited from [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span></span>|
|<span data-ttu-id="9407a-133">content</span><span class="sxs-lookup"><span data-stu-id="9407a-133">content</span></span>|[<span data-ttu-id="9407a-134">Json</span><span class="sxs-lookup"><span data-stu-id="9407a-134">Json</span></span>](../resources/intune-mam-json.md)|<span data-ttu-id="9407a-135">Contenido del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="9407a-135">Status report content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9407a-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9407a-136">Relationships</span></span>
<span data-ttu-id="9407a-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9407a-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9407a-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9407a-138">JSON Representation</span></span>
<span data-ttu-id="9407a-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9407a-139">Here is a JSON representation of the resource.</span></span>
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



