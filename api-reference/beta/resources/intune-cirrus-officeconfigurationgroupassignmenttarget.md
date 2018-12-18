---
title: tipo de recurso officeConfigurationGroupAssignmentTarget
description: Configuración de cliente de Office AAD grupo de destino de la asignación.
author: tfitzmac
ms.openlocfilehash: 82008de6e5cb64885e9e2d5804a00956da2ff434
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335871"
---
# <a name="officeconfigurationgroupassignmenttarget-resource-type"></a><span data-ttu-id="8d141-103">tipo de recurso officeConfigurationGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="8d141-103">officeConfigurationGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="8d141-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d141-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d141-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d141-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8d141-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d141-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d141-107">Configuración de cliente de Office AAD grupo de destino de la asignación.</span><span class="sxs-lookup"><span data-stu-id="8d141-107">Office client configuration AAD group assignment target.</span></span>

<span data-ttu-id="8d141-108">Hereda de [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="8d141-108">Inherits from [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8d141-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d141-109">Properties</span></span>
|<span data-ttu-id="8d141-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d141-110">Property</span></span>|<span data-ttu-id="8d141-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d141-111">Type</span></span>|<span data-ttu-id="8d141-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d141-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d141-113">groupId</span><span class="sxs-lookup"><span data-stu-id="8d141-113">groupId</span></span>|<span data-ttu-id="8d141-114">String</span><span class="sxs-lookup"><span data-stu-id="8d141-114">String</span></span>|<span data-ttu-id="8d141-115">El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d141-115">The Id of the AAD group we are targeting the device configuration to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d141-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d141-116">Relationships</span></span>
<span data-ttu-id="8d141-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d141-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d141-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d141-118">JSON Representation</span></span>
<span data-ttu-id="8d141-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d141-119">Here is a JSON representation of the resource.</span></span>
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



