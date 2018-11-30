---
title: tipo de recurso officeConfigurationGroupAssignmentTarget
description: Configuración de cliente de Office AAD grupo de destino de la asignación.
ms.openlocfilehash: 263e48bfc5800231a9f36159e802f65294e6ac02
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088994"
---
# <a name="officeconfigurationgroupassignmenttarget-resource-type"></a><span data-ttu-id="e15e5-103">tipo de recurso officeConfigurationGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="e15e5-103">officeConfigurationGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="e15e5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e15e5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e15e5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e15e5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e15e5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e15e5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e15e5-107">Configuración de cliente de Office AAD grupo de destino de la asignación.</span><span class="sxs-lookup"><span data-stu-id="e15e5-107">Office client configuration AAD group assignment target.</span></span>

<span data-ttu-id="e15e5-108">Hereda de [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="e15e5-108">Inherits from [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e15e5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e15e5-109">Properties</span></span>
|<span data-ttu-id="e15e5-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e15e5-110">Property</span></span>|<span data-ttu-id="e15e5-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e15e5-111">Type</span></span>|<span data-ttu-id="e15e5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e15e5-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e15e5-113">groupId</span><span class="sxs-lookup"><span data-stu-id="e15e5-113">groupId</span></span>|<span data-ttu-id="e15e5-114">String</span><span class="sxs-lookup"><span data-stu-id="e15e5-114">String</span></span>|<span data-ttu-id="e15e5-115">El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e15e5-115">The Id of the AAD group we are targeting the device configuration to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e15e5-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e15e5-116">Relationships</span></span>
<span data-ttu-id="e15e5-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e15e5-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e15e5-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e15e5-118">JSON Representation</span></span>
<span data-ttu-id="e15e5-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e15e5-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeConfigurationGroupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeConfigurationGroupAssignmentTarget",
  "groupId": "String"
}
```



