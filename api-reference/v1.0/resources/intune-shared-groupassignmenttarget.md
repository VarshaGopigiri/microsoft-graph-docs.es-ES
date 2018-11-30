---
title: Tipo de recurso groupAssignmentTarget
description: Representa una tarea de un grupo.
ms.openlocfilehash: 0ebb41b1f737a20a37d322bac7ab5ae6ab2a248f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030852"
---
# <a name="groupassignmenttarget-resource-type"></a><span data-ttu-id="84538-103">Tipo de recurso groupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="84538-103">groupAssignmentTarget resource type</span></span>

> <span data-ttu-id="84538-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84538-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84538-105">Representa una tarea de un grupo.</span><span class="sxs-lookup"><span data-stu-id="84538-105">Represents an assignment to a group.</span></span>

<span data-ttu-id="84538-106">Hereda de [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="84538-106">Inherits from [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="84538-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84538-107">Properties</span></span>
|<span data-ttu-id="84538-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84538-108">Property</span></span>|<span data-ttu-id="84538-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="84538-109">Type</span></span>|<span data-ttu-id="84538-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="84538-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84538-111">groupId</span><span class="sxs-lookup"><span data-stu-id="84538-111">groupId</span></span>|<span data-ttu-id="84538-112">cadena</span><span class="sxs-lookup"><span data-stu-id="84538-112">String</span></span>|<span data-ttu-id="84538-113">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="84538-113">The group Id that is the target of the assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="84538-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="84538-114">Relationships</span></span>
<span data-ttu-id="84538-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="84538-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="84538-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84538-116">JSON Representation</span></span>
<span data-ttu-id="84538-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="84538-117">Here is a JSON representation of the resource.</span></span>
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



