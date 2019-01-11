---
title: tipo de recurso officeConfigurationGroupAssignmentTarget
description: Configuración de cliente de Office AAD grupo de destino de la asignación.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b2fe6a668c1f490c167fe61496af14cf2654cebb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814773"
---
# <a name="officeconfigurationgroupassignmenttarget-resource-type"></a><span data-ttu-id="14815-103">tipo de recurso officeConfigurationGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="14815-103">officeConfigurationGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="14815-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14815-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14815-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14815-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="14815-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="14815-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="14815-107">Configuración de cliente de Office AAD grupo de destino de la asignación.</span><span class="sxs-lookup"><span data-stu-id="14815-107">Office client configuration AAD group assignment target.</span></span>

<span data-ttu-id="14815-108">Hereda de [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="14815-108">Inherits from [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="14815-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14815-109">Properties</span></span>
|<span data-ttu-id="14815-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14815-110">Property</span></span>|<span data-ttu-id="14815-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="14815-111">Type</span></span>|<span data-ttu-id="14815-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="14815-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="14815-113">groupId</span><span class="sxs-lookup"><span data-stu-id="14815-113">groupId</span></span>|<span data-ttu-id="14815-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="14815-114">String</span></span>|<span data-ttu-id="14815-115">El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14815-115">The Id of the AAD group we are targeting the device configuration to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="14815-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="14815-116">Relationships</span></span>
<span data-ttu-id="14815-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="14815-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="14815-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14815-118">JSON Representation</span></span>
<span data-ttu-id="14815-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="14815-119">Here is a JSON representation of the resource.</span></span>
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



