---
title: Tipo de recurso managedAppStatus
description: Representa el estado de protección y configuración de la aplicación para la organización.
author: tfitzmac
ms.openlocfilehash: e23b20b53d7ad89a4bbd0df8510a66e0f7da581d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331595"
---
# <a name="managedappstatus-resource-type"></a><span data-ttu-id="ffcb2-103">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="ffcb2-103">managedAppStatus resource type</span></span>

> <span data-ttu-id="ffcb2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffcb2-105">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-105">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="ffcb2-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffcb2-106">Methods</span></span>
|<span data-ttu-id="ffcb2-107">Método</span><span class="sxs-lookup"><span data-stu-id="ffcb2-107">Method</span></span>|<span data-ttu-id="ffcb2-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffcb2-108">Return Type</span></span>|<span data-ttu-id="ffcb2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffcb2-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ffcb2-110">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="ffcb2-110">List managedAppStatuses</span></span>](../api/intune-mam-managedappstatus-list.md)|<span data-ttu-id="ffcb2-111">Colección [managedAppStatus](../resources/intune-mam-managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="ffcb2-111">[managedAppStatus](../resources/intune-mam-managedappstatus.md) collection</span></span>|<span data-ttu-id="ffcb2-112">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ffcb2-112">List properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="ffcb2-113">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="ffcb2-113">Get managedAppStatus</span></span>](../api/intune-mam-managedappstatus-get.md)|[<span data-ttu-id="ffcb2-114">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="ffcb2-114">managedAppStatus</span></span>](../resources/intune-mam-managedappstatus.md)|<span data-ttu-id="ffcb2-115">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune-mam-managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ffcb2-115">Read properties and relationships of the [managedAppStatus](../resources/intune-mam-managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ffcb2-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffcb2-116">Properties</span></span>
|<span data-ttu-id="ffcb2-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffcb2-117">Property</span></span>|<span data-ttu-id="ffcb2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffcb2-118">Type</span></span>|<span data-ttu-id="ffcb2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffcb2-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ffcb2-120">displayName</span><span class="sxs-lookup"><span data-stu-id="ffcb2-120">displayName</span></span>|<span data-ttu-id="ffcb2-121">String</span><span class="sxs-lookup"><span data-stu-id="ffcb2-121">String</span></span>|<span data-ttu-id="ffcb2-122">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-122">Friendly name of the status report.</span></span>|
|<span data-ttu-id="ffcb2-123">id</span><span class="sxs-lookup"><span data-stu-id="ffcb2-123">id</span></span>|<span data-ttu-id="ffcb2-124">String</span><span class="sxs-lookup"><span data-stu-id="ffcb2-124">String</span></span>|<span data-ttu-id="ffcb2-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-125">Key of the entity.</span></span>|
|<span data-ttu-id="ffcb2-126">version</span><span class="sxs-lookup"><span data-stu-id="ffcb2-126">version</span></span>|<span data-ttu-id="ffcb2-127">String</span><span class="sxs-lookup"><span data-stu-id="ffcb2-127">String</span></span>|<span data-ttu-id="ffcb2-128">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-128">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ffcb2-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ffcb2-129">Relationships</span></span>
<span data-ttu-id="ffcb2-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ffcb2-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ffcb2-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ffcb2-131">JSON Representation</span></span>
<span data-ttu-id="ffcb2-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-132">Here is a JSON representation of the resource.</span></span>
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



