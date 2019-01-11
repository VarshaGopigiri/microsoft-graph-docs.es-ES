---
title: Tipo de recurso managedAppStatus
description: Representa el estado de protección y configuración de la aplicación para la organización.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 13bf28c0244a3288b949ebf718e3d5ce97ceb60c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890387"
---
# <a name="managedappstatus-resource-type"></a><span data-ttu-id="69659-103">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="69659-103">managedAppStatus resource type</span></span>

> <span data-ttu-id="69659-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="69659-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="69659-105">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="69659-105">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="69659-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="69659-106">Methods</span></span>
|<span data-ttu-id="69659-107">Método</span><span class="sxs-lookup"><span data-stu-id="69659-107">Method</span></span>|<span data-ttu-id="69659-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69659-108">Return Type</span></span>|<span data-ttu-id="69659-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="69659-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="69659-110">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="69659-110">List managedAppStatuses</span></span>](../api/intune-mam-managedappstatus-list.md)|<span data-ttu-id="69659-111">Colección [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="69659-111">[managedAppStatus](../resources/intune-mam-managedappstatus.md) collection</span></span>|<span data-ttu-id="69659-112">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="69659-112">List properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="69659-113">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="69659-113">Get managedAppStatus</span></span>](../api/intune-mam-managedappstatus-get.md)|[<span data-ttu-id="69659-114">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="69659-114">managedAppStatus</span></span>](../resources/intune-mam-managedappstatus.md)|<span data-ttu-id="69659-115">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="69659-115">Read properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="69659-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69659-116">Properties</span></span>
|<span data-ttu-id="69659-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69659-117">Property</span></span>|<span data-ttu-id="69659-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="69659-118">Type</span></span>|<span data-ttu-id="69659-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="69659-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="69659-120">displayName</span><span class="sxs-lookup"><span data-stu-id="69659-120">displayName</span></span>|<span data-ttu-id="69659-121">String</span><span class="sxs-lookup"><span data-stu-id="69659-121">String</span></span>|<span data-ttu-id="69659-122">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="69659-122">Friendly name of the status report.</span></span>|
|<span data-ttu-id="69659-123">id</span><span class="sxs-lookup"><span data-stu-id="69659-123">id</span></span>|<span data-ttu-id="69659-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="69659-124">String</span></span>|<span data-ttu-id="69659-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="69659-125">Key of the entity.</span></span>|
|<span data-ttu-id="69659-126">version</span><span class="sxs-lookup"><span data-stu-id="69659-126">version</span></span>|<span data-ttu-id="69659-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="69659-127">String</span></span>|<span data-ttu-id="69659-128">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="69659-128">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="69659-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="69659-129">Relationships</span></span>
<span data-ttu-id="69659-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="69659-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="69659-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="69659-131">JSON Representation</span></span>
<span data-ttu-id="69659-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="69659-132">Here is a JSON representation of the resource.</span></span>
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



