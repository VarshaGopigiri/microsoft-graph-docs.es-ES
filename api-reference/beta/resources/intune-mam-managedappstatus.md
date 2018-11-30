---
title: Tipo de recurso managedAppStatus
description: Representa el estado de protección y configuración de la aplicación para la organización.
ms.openlocfilehash: 659e89acb6741c7a3f7aad072bb658ce52e9e5cc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089453"
---
# <a name="managedappstatus-resource-type"></a><span data-ttu-id="6e012-103">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="6e012-103">managedAppStatus resource type</span></span>

> <span data-ttu-id="6e012-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e012-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e012-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e012-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6e012-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e012-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e012-107">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="6e012-107">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="6e012-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e012-108">Methods</span></span>
|<span data-ttu-id="6e012-109">Método</span><span class="sxs-lookup"><span data-stu-id="6e012-109">Method</span></span>|<span data-ttu-id="6e012-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e012-110">Return Type</span></span>|<span data-ttu-id="6e012-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e012-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="6e012-112">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="6e012-112">List managedAppStatuses</span></span>](../api/intune-mam-managedappstatus-list.md)|<span data-ttu-id="6e012-113">Colección [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="6e012-113">[managedAppStatus](../resources/intune-mam-managedappstatus.md) collection</span></span>|<span data-ttu-id="6e012-114">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="6e012-114">List properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="6e012-115">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="6e012-115">Get managedAppStatus</span></span>](../api/intune-mam-managedappstatus-get.md)|[<span data-ttu-id="6e012-116">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="6e012-116">managedAppStatus</span></span>](../resources/intune-mam-managedappstatus.md)|<span data-ttu-id="6e012-117">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="6e012-117">Read properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="6e012-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e012-118">Properties</span></span>
|<span data-ttu-id="6e012-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e012-119">Property</span></span>|<span data-ttu-id="6e012-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e012-120">Type</span></span>|<span data-ttu-id="6e012-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e012-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6e012-122">displayName</span><span class="sxs-lookup"><span data-stu-id="6e012-122">displayName</span></span>|<span data-ttu-id="6e012-123">String</span><span class="sxs-lookup"><span data-stu-id="6e012-123">String</span></span>|<span data-ttu-id="6e012-124">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="6e012-124">Friendly name of the status report.</span></span>|
|<span data-ttu-id="6e012-125">id</span><span class="sxs-lookup"><span data-stu-id="6e012-125">id</span></span>|<span data-ttu-id="6e012-126">String</span><span class="sxs-lookup"><span data-stu-id="6e012-126">String</span></span>|<span data-ttu-id="6e012-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6e012-127">Key of the entity.</span></span>|
|<span data-ttu-id="6e012-128">version</span><span class="sxs-lookup"><span data-stu-id="6e012-128">version</span></span>|<span data-ttu-id="6e012-129">String</span><span class="sxs-lookup"><span data-stu-id="6e012-129">String</span></span>|<span data-ttu-id="6e012-130">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6e012-130">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6e012-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6e012-131">Relationships</span></span>
<span data-ttu-id="6e012-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6e012-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6e012-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6e012-133">JSON Representation</span></span>
<span data-ttu-id="6e012-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6e012-134">Here is a JSON representation of the resource.</span></span>
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





