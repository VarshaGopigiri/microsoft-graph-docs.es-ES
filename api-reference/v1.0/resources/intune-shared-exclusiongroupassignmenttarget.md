---
title: Tipo de recurso exclusionGroupAssignmentTarget
description: Representa un grupo que debería excluirse de una tarea.
author: tfitzmac
ms.openlocfilehash: 8193ac714f7f68dc371454c809c3eaa3176f8453
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304518"
---
# <a name="exclusiongroupassignmenttarget-resource-type"></a><span data-ttu-id="396ca-103">Tipo de recurso exclusionGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="396ca-103">exclusionGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="396ca-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="396ca-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="396ca-105">Representa un grupo que debería excluirse de una tarea.</span><span class="sxs-lookup"><span data-stu-id="396ca-105">Represents a group that should be excluded from an assignment.</span></span>

<span data-ttu-id="396ca-106">Hereda de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="396ca-106">Inherits from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="396ca-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="396ca-107">Properties</span></span>
|<span data-ttu-id="396ca-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="396ca-108">Property</span></span>|<span data-ttu-id="396ca-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="396ca-109">Type</span></span>|<span data-ttu-id="396ca-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="396ca-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="396ca-111">groupId</span><span class="sxs-lookup"><span data-stu-id="396ca-111">groupId</span></span>|<span data-ttu-id="396ca-112">cadena</span><span class="sxs-lookup"><span data-stu-id="396ca-112">String</span></span>|<span data-ttu-id="396ca-113">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="396ca-113">The group Id that is the target of the assignment.</span></span> <span data-ttu-id="396ca-114">Heredado de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="396ca-114">Inherited from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="396ca-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="396ca-115">Relationships</span></span>
<span data-ttu-id="396ca-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="396ca-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="396ca-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="396ca-117">JSON Representation</span></span>
<span data-ttu-id="396ca-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="396ca-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.exclusionGroupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.exclusionGroupAssignmentTarget",
  "groupId": "String"
}
```



