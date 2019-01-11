---
title: Tipo de recurso groupAssignmentTarget
description: Representa una tarea de un grupo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7218fc69564ea08a7302cfb0af7856360cd9a330
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809047"
---
# <a name="groupassignmenttarget-resource-type"></a><span data-ttu-id="f6146-103">Tipo de recurso groupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="f6146-103">groupAssignmentTarget resource type</span></span>

> <span data-ttu-id="f6146-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6146-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6146-105">Representa una tarea de un grupo.</span><span class="sxs-lookup"><span data-stu-id="f6146-105">Represents an assignment to a group.</span></span>

<span data-ttu-id="f6146-106">Hereda de [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="f6146-106">Inherits from [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="f6146-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6146-107">Properties</span></span>
|<span data-ttu-id="f6146-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6146-108">Property</span></span>|<span data-ttu-id="f6146-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6146-109">Type</span></span>|<span data-ttu-id="f6146-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6146-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6146-111">groupId</span><span class="sxs-lookup"><span data-stu-id="f6146-111">groupId</span></span>|<span data-ttu-id="f6146-112">cadena</span><span class="sxs-lookup"><span data-stu-id="f6146-112">String</span></span>|<span data-ttu-id="f6146-113">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f6146-113">The group Id that is the target of the assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f6146-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f6146-114">Relationships</span></span>
<span data-ttu-id="f6146-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f6146-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f6146-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6146-116">JSON Representation</span></span>
<span data-ttu-id="f6146-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6146-117">Here is a JSON representation of the resource.</span></span>
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



