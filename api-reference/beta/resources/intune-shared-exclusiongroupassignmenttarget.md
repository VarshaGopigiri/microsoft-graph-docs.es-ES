---
title: Tipo de recurso exclusionGroupAssignmentTarget
description: Representa un grupo que debería excluirse de una tarea.
ms.openlocfilehash: c5d104af3e87d285f0157a6fe6edbc46949f97bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089449"
---
# <a name="exclusiongroupassignmenttarget-resource-type"></a><span data-ttu-id="b7b86-103">Tipo de recurso exclusionGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="b7b86-103">exclusionGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="b7b86-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b7b86-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b7b86-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b7b86-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b7b86-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b7b86-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b7b86-107">Representa un grupo que debería excluirse de una tarea.</span><span class="sxs-lookup"><span data-stu-id="b7b86-107">Represents a group that should be excluded from an assignment.</span></span>

<span data-ttu-id="b7b86-108">Hereda de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="b7b86-108">Inherits from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="b7b86-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7b86-109">Properties</span></span>
|<span data-ttu-id="b7b86-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b7b86-110">Property</span></span>|<span data-ttu-id="b7b86-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7b86-111">Type</span></span>|<span data-ttu-id="b7b86-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7b86-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b7b86-113">groupId</span><span class="sxs-lookup"><span data-stu-id="b7b86-113">groupId</span></span>|<span data-ttu-id="b7b86-114">cadena</span><span class="sxs-lookup"><span data-stu-id="b7b86-114">String</span></span>|<span data-ttu-id="b7b86-115">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b7b86-115">The group Id that is the target of the assignment.</span></span> <span data-ttu-id="b7b86-116">Heredado de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="b7b86-116">Inherited from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="b7b86-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b7b86-117">Relationships</span></span>
<span data-ttu-id="b7b86-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b7b86-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b7b86-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b7b86-119">JSON Representation</span></span>
<span data-ttu-id="b7b86-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b7b86-120">Here is a JSON representation of the resource.</span></span>
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




