---
title: Tipo de recurso groupAssignmentTarget
description: Representa una tarea de un grupo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 96aec1b72233cfe7d553b8f17feb9af382d89cde
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971679"
---
# <a name="groupassignmenttarget-resource-type"></a><span data-ttu-id="50d2f-103">Tipo de recurso groupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="50d2f-103">groupAssignmentTarget resource type</span></span>

> <span data-ttu-id="50d2f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50d2f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50d2f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50d2f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="50d2f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50d2f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50d2f-107">Representa una tarea de un grupo.</span><span class="sxs-lookup"><span data-stu-id="50d2f-107">Represents an assignment to a group.</span></span>

<span data-ttu-id="50d2f-108">Hereda de [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="50d2f-108">Inherits from [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="50d2f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50d2f-109">Properties</span></span>
|<span data-ttu-id="50d2f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50d2f-110">Property</span></span>|<span data-ttu-id="50d2f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="50d2f-111">Type</span></span>|<span data-ttu-id="50d2f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d2f-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50d2f-113">groupId</span><span class="sxs-lookup"><span data-stu-id="50d2f-113">groupId</span></span>|<span data-ttu-id="50d2f-114">cadena</span><span class="sxs-lookup"><span data-stu-id="50d2f-114">String</span></span>|<span data-ttu-id="50d2f-115">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="50d2f-115">The group Id that is the target of the assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="50d2f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="50d2f-116">Relationships</span></span>
<span data-ttu-id="50d2f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="50d2f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="50d2f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50d2f-118">JSON Representation</span></span>
<span data-ttu-id="50d2f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50d2f-119">Here is a JSON representation of the resource.</span></span>
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





