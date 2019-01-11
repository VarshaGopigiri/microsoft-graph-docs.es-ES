---
title: Tipo de recurso exclusionGroupAssignmentTarget
description: Representa un grupo que debería excluirse de una tarea.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ad844205e0cb5f5b4d0b86d71212e2d9c2ca223e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826456"
---
# <a name="exclusiongroupassignmenttarget-resource-type"></a><span data-ttu-id="d58ce-103">Tipo de recurso exclusionGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="d58ce-103">exclusionGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="d58ce-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d58ce-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d58ce-105">Representa un grupo que debería excluirse de una tarea.</span><span class="sxs-lookup"><span data-stu-id="d58ce-105">Represents a group that should be excluded from an assignment.</span></span>

<span data-ttu-id="d58ce-106">Hereda de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="d58ce-106">Inherits from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="d58ce-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d58ce-107">Properties</span></span>
|<span data-ttu-id="d58ce-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d58ce-108">Property</span></span>|<span data-ttu-id="d58ce-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d58ce-109">Type</span></span>|<span data-ttu-id="d58ce-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d58ce-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d58ce-111">groupId</span><span class="sxs-lookup"><span data-stu-id="d58ce-111">groupId</span></span>|<span data-ttu-id="d58ce-112">cadena</span><span class="sxs-lookup"><span data-stu-id="d58ce-112">String</span></span>|<span data-ttu-id="d58ce-113">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d58ce-113">The group Id that is the target of the assignment.</span></span> <span data-ttu-id="d58ce-114">Heredado de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="d58ce-114">Inherited from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="d58ce-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d58ce-115">Relationships</span></span>
<span data-ttu-id="d58ce-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d58ce-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d58ce-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d58ce-117">JSON Representation</span></span>
<span data-ttu-id="d58ce-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d58ce-118">Here is a JSON representation of the resource.</span></span>
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



