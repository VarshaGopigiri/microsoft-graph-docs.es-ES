---
title: Tipo de recurso exclusionGroupAssignmentTarget
description: Representa un grupo que debería excluirse de una tarea.
author: tfitzmac
ms.openlocfilehash: 783231c451668169ba85e8ce1cfecd669b5c0b7d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343186"
---
# <a name="exclusiongroupassignmenttarget-resource-type"></a><span data-ttu-id="cfbc0-103">Tipo de recurso exclusionGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="cfbc0-103">exclusionGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="cfbc0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cfbc0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cfbc0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cfbc0-107">Representa un grupo que debería excluirse de una tarea.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-107">Represents a group that should be excluded from an assignment.</span></span>

<span data-ttu-id="cfbc0-108">Hereda de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="cfbc0-108">Inherits from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="cfbc0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cfbc0-109">Properties</span></span>
|<span data-ttu-id="cfbc0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cfbc0-110">Property</span></span>|<span data-ttu-id="cfbc0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cfbc0-111">Type</span></span>|<span data-ttu-id="cfbc0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfbc0-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cfbc0-113">groupId</span><span class="sxs-lookup"><span data-stu-id="cfbc0-113">groupId</span></span>|<span data-ttu-id="cfbc0-114">cadena</span><span class="sxs-lookup"><span data-stu-id="cfbc0-114">String</span></span>|<span data-ttu-id="cfbc0-115">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-115">The group Id that is the target of the assignment.</span></span> <span data-ttu-id="cfbc0-116">Heredado de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="cfbc0-116">Inherited from [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="cfbc0-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cfbc0-117">Relationships</span></span>
<span data-ttu-id="cfbc0-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cfbc0-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cfbc0-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cfbc0-119">JSON Representation</span></span>
<span data-ttu-id="cfbc0-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-120">Here is a JSON representation of the resource.</span></span>
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





