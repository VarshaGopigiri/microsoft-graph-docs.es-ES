---
title: tipo de recurso unsupportedDeviceConfigurationDetail
description: Una descripción de por qué una entidad no es compatible.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6b82dcf28652cbe54a4932a641579101cb392639
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949776"
---
# <a name="unsupporteddeviceconfigurationdetail-resource-type"></a><span data-ttu-id="8d81b-103">tipo de recurso unsupportedDeviceConfigurationDetail</span><span class="sxs-lookup"><span data-stu-id="8d81b-103">unsupportedDeviceConfigurationDetail resource type</span></span>

> <span data-ttu-id="8d81b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d81b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d81b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d81b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8d81b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d81b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d81b-107">Una descripción de por qué una entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8d81b-107">A description of why an entity is unsupported.</span></span>
## <a name="properties"></a><span data-ttu-id="8d81b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d81b-108">Properties</span></span>
|<span data-ttu-id="8d81b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d81b-109">Property</span></span>|<span data-ttu-id="8d81b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d81b-110">Type</span></span>|<span data-ttu-id="8d81b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d81b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d81b-112">message</span><span class="sxs-lookup"><span data-stu-id="8d81b-112">message</span></span>|<span data-ttu-id="8d81b-113">String</span><span class="sxs-lookup"><span data-stu-id="8d81b-113">String</span></span>|<span data-ttu-id="8d81b-114">Un mensaje que explica por qué una entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8d81b-114">A message explaining why an entity is unsupported.</span></span>|
|<span data-ttu-id="8d81b-115">propertyName</span><span class="sxs-lookup"><span data-stu-id="8d81b-115">propertyName</span></span>|<span data-ttu-id="8d81b-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="8d81b-116">String</span></span>|<span data-ttu-id="8d81b-117">Si el mensaje está relacionado con una propiedad concreta en la entidad original y, a continuación, el nombre de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="8d81b-117">If message is related to a specific property in the original entity, then the name of that property.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d81b-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d81b-118">Relationships</span></span>
<span data-ttu-id="8d81b-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d81b-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d81b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d81b-120">JSON Representation</span></span>
<span data-ttu-id="8d81b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d81b-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.unsupportedDeviceConfigurationDetail"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.unsupportedDeviceConfigurationDetail",
  "message": "String",
  "propertyName": "String"
}
```





