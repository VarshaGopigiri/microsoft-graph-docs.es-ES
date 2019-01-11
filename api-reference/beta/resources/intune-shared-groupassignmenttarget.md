---
title: Tipo de recurso groupAssignmentTarget
description: Representa una tarea de un grupo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f344c0ed718f32352901af63da32c11ca02e2db6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849815"
---
# <a name="groupassignmenttarget-resource-type"></a><span data-ttu-id="cd755-103">Tipo de recurso groupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="cd755-103">groupAssignmentTarget resource type</span></span>

> <span data-ttu-id="cd755-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd755-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd755-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd755-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cd755-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd755-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd755-107">Representa una tarea de un grupo.</span><span class="sxs-lookup"><span data-stu-id="cd755-107">Represents an assignment to a group.</span></span>

<span data-ttu-id="cd755-108">Hereda de [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="cd755-108">Inherits from [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="cd755-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd755-109">Properties</span></span>
|<span data-ttu-id="cd755-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd755-110">Property</span></span>|<span data-ttu-id="cd755-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd755-111">Type</span></span>|<span data-ttu-id="cd755-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd755-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cd755-113">groupId</span><span class="sxs-lookup"><span data-stu-id="cd755-113">groupId</span></span>|<span data-ttu-id="cd755-114">cadena</span><span class="sxs-lookup"><span data-stu-id="cd755-114">String</span></span>|<span data-ttu-id="cd755-115">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cd755-115">The group Id that is the target of the assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cd755-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cd755-116">Relationships</span></span>
<span data-ttu-id="cd755-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cd755-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cd755-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd755-118">JSON Representation</span></span>
<span data-ttu-id="cd755-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cd755-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.groupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupAssignmentTarget",
  "groupId": "String"
}
```





