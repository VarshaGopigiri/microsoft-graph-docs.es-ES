---
title: tipo de recurso windowsManagementApp
description: Entidad de aplicación de administración de Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 395148d4c870193d75f418d7dc30d2b2241bad01
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913502"
---
# <a name="windowsmanagementapp-resource-type"></a><span data-ttu-id="17457-103">tipo de recurso windowsManagementApp</span><span class="sxs-lookup"><span data-stu-id="17457-103">windowsManagementApp resource type</span></span>

> <span data-ttu-id="17457-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17457-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17457-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17457-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="17457-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17457-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17457-107">Entidad de aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="17457-107">Windows management app entity.</span></span>
## <a name="methods"></a><span data-ttu-id="17457-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="17457-108">Methods</span></span>
|<span data-ttu-id="17457-109">Método</span><span class="sxs-lookup"><span data-stu-id="17457-109">Method</span></span>|<span data-ttu-id="17457-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17457-110">Return Type</span></span>|<span data-ttu-id="17457-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="17457-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="17457-112">Obtener windowsManagementApp</span><span class="sxs-lookup"><span data-stu-id="17457-112">Get windowsManagementApp</span></span>](../api/intune-devices-windowsmanagementapp-get.md)|[<span data-ttu-id="17457-113">windowsManagementApp</span><span class="sxs-lookup"><span data-stu-id="17457-113">windowsManagementApp</span></span>](../resources/intune-devices-windowsmanagementapp.md)|<span data-ttu-id="17457-114">Leer las propiedades y las relaciones del objeto [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) .</span><span class="sxs-lookup"><span data-stu-id="17457-114">Read properties and relationships of the [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) object.</span></span>|
|[<span data-ttu-id="17457-115">Actualizar windowsManagementApp</span><span class="sxs-lookup"><span data-stu-id="17457-115">Update windowsManagementApp</span></span>](../api/intune-devices-windowsmanagementapp-update.md)|[<span data-ttu-id="17457-116">windowsManagementApp</span><span class="sxs-lookup"><span data-stu-id="17457-116">windowsManagementApp</span></span>](../resources/intune-devices-windowsmanagementapp.md)|<span data-ttu-id="17457-117">Actualizar las propiedades de un objeto [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) .</span><span class="sxs-lookup"><span data-stu-id="17457-117">Update the properties of a [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="17457-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17457-118">Properties</span></span>
|<span data-ttu-id="17457-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17457-119">Property</span></span>|<span data-ttu-id="17457-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="17457-120">Type</span></span>|<span data-ttu-id="17457-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="17457-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="17457-122">id</span><span class="sxs-lookup"><span data-stu-id="17457-122">id</span></span>|<span data-ttu-id="17457-123">String</span><span class="sxs-lookup"><span data-stu-id="17457-123">String</span></span>|<span data-ttu-id="17457-124">Identificador único para la aplicación de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="17457-124">Unique Identifier for the Windows management app</span></span>|
|<span data-ttu-id="17457-125">availableVersion</span><span class="sxs-lookup"><span data-stu-id="17457-125">availableVersion</span></span>|<span data-ttu-id="17457-126">String</span><span class="sxs-lookup"><span data-stu-id="17457-126">String</span></span>|<span data-ttu-id="17457-127">Versión disponible de Windows management app.</span><span class="sxs-lookup"><span data-stu-id="17457-127">Windows management app available version.</span></span>|

## <a name="relationships"></a><span data-ttu-id="17457-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17457-128">Relationships</span></span>
|<span data-ttu-id="17457-129">Relación</span><span class="sxs-lookup"><span data-stu-id="17457-129">Relationship</span></span>|<span data-ttu-id="17457-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="17457-130">Type</span></span>|<span data-ttu-id="17457-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="17457-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="17457-132">healthSummary</span><span class="sxs-lookup"><span data-stu-id="17457-132">healthSummary</span></span>|[<span data-ttu-id="17457-133">windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="17457-133">windowsManagementAppHealthSummary</span></span>](../resources/intune-devices-windowsmanagementapphealthsummary.md)|<span data-ttu-id="17457-134">Mantenimiento de resumen para la aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="17457-134">Health summary for Windows management app.</span></span>|
|<span data-ttu-id="17457-135">healthStates</span><span class="sxs-lookup"><span data-stu-id="17457-135">healthStates</span></span>|<span data-ttu-id="17457-136">colección de [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md)</span><span class="sxs-lookup"><span data-stu-id="17457-136">[windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) collection</span></span>|<span data-ttu-id="17457-137">La lista de Estados de mantenimiento para la aplicación de administración de Windows instalada.</span><span class="sxs-lookup"><span data-stu-id="17457-137">The list of health states for installed Windows management app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="17457-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17457-138">JSON Representation</span></span>
<span data-ttu-id="17457-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="17457-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsManagementApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsManagementApp",
  "id": "String (identifier)",
  "availableVersion": "String"
}
```





