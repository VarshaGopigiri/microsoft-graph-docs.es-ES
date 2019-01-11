---
title: Tipo de recurso managedAppStatus
description: Representa el estado de protección y configuración de la aplicación para la organización.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 05b2117f441fd60f92970cc506245d177a618fce
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840750"
---
# <a name="managedappstatus-resource-type"></a><span data-ttu-id="ca5bc-103">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="ca5bc-103">managedAppStatus resource type</span></span>

> <span data-ttu-id="ca5bc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ca5bc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ca5bc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca5bc-107">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-107">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="ca5bc-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca5bc-108">Methods</span></span>
|<span data-ttu-id="ca5bc-109">Método</span><span class="sxs-lookup"><span data-stu-id="ca5bc-109">Method</span></span>|<span data-ttu-id="ca5bc-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca5bc-110">Return Type</span></span>|<span data-ttu-id="ca5bc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca5bc-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ca5bc-112">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="ca5bc-112">List managedAppStatuses</span></span>](../api/intune-mam-managedappstatus-list.md)|<span data-ttu-id="ca5bc-113">Colección [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="ca5bc-113">[managedAppStatus](../resources/intune-mam-managedappstatus.md) collection</span></span>|<span data-ttu-id="ca5bc-114">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ca5bc-114">List properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="ca5bc-115">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="ca5bc-115">Get managedAppStatus</span></span>](../api/intune-mam-managedappstatus-get.md)|[<span data-ttu-id="ca5bc-116">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="ca5bc-116">managedAppStatus</span></span>](../resources/intune-mam-managedappstatus.md)|<span data-ttu-id="ca5bc-117">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ca5bc-117">Read properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ca5bc-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca5bc-118">Properties</span></span>
|<span data-ttu-id="ca5bc-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca5bc-119">Property</span></span>|<span data-ttu-id="ca5bc-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca5bc-120">Type</span></span>|<span data-ttu-id="ca5bc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca5bc-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca5bc-122">displayName</span><span class="sxs-lookup"><span data-stu-id="ca5bc-122">displayName</span></span>|<span data-ttu-id="ca5bc-123">String</span><span class="sxs-lookup"><span data-stu-id="ca5bc-123">String</span></span>|<span data-ttu-id="ca5bc-124">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-124">Friendly name of the status report.</span></span>|
|<span data-ttu-id="ca5bc-125">id</span><span class="sxs-lookup"><span data-stu-id="ca5bc-125">id</span></span>|<span data-ttu-id="ca5bc-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca5bc-126">String</span></span>|<span data-ttu-id="ca5bc-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-127">Key of the entity.</span></span>|
|<span data-ttu-id="ca5bc-128">version</span><span class="sxs-lookup"><span data-stu-id="ca5bc-128">version</span></span>|<span data-ttu-id="ca5bc-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca5bc-129">String</span></span>|<span data-ttu-id="ca5bc-130">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-130">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ca5bc-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ca5bc-131">Relationships</span></span>
<span data-ttu-id="ca5bc-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ca5bc-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ca5bc-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca5bc-133">JSON Representation</span></span>
<span data-ttu-id="ca5bc-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca5bc-134">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatus",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String"
}
```





