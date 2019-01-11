---
title: tipo de recurso unsupportedDeviceConfigurationDetail
description: Una descripción de por qué una entidad no es compatible.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0a213961e6b816917b061bc56c792cf9a60e3a2a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839476"
---
# <a name="unsupporteddeviceconfigurationdetail-resource-type"></a><span data-ttu-id="7c35c-103">tipo de recurso unsupportedDeviceConfigurationDetail</span><span class="sxs-lookup"><span data-stu-id="7c35c-103">unsupportedDeviceConfigurationDetail resource type</span></span>

> <span data-ttu-id="7c35c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c35c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c35c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c35c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7c35c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7c35c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7c35c-107">Una descripción de por qué una entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="7c35c-107">A description of why an entity is unsupported.</span></span>
## <a name="properties"></a><span data-ttu-id="7c35c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c35c-108">Properties</span></span>
|<span data-ttu-id="7c35c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c35c-109">Property</span></span>|<span data-ttu-id="7c35c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c35c-110">Type</span></span>|<span data-ttu-id="7c35c-111">Description</span><span class="sxs-lookup"><span data-stu-id="7c35c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7c35c-112">message</span><span class="sxs-lookup"><span data-stu-id="7c35c-112">message</span></span>|<span data-ttu-id="7c35c-113">String</span><span class="sxs-lookup"><span data-stu-id="7c35c-113">String</span></span>|<span data-ttu-id="7c35c-114">Un mensaje que explica por qué una entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="7c35c-114">A message explaining why an entity is unsupported.</span></span>|
|<span data-ttu-id="7c35c-115">propertyName</span><span class="sxs-lookup"><span data-stu-id="7c35c-115">propertyName</span></span>|<span data-ttu-id="7c35c-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="7c35c-116">String</span></span>|<span data-ttu-id="7c35c-117">Si el mensaje está relacionado con una propiedad concreta en la entidad original y, a continuación, el nombre de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c35c-117">If message is related to a specific property in the original entity, then the name of that property.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7c35c-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7c35c-118">Relationships</span></span>
<span data-ttu-id="7c35c-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7c35c-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7c35c-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c35c-120">JSON Representation</span></span>
<span data-ttu-id="7c35c-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c35c-121">Here is a JSON representation of the resource.</span></span>
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





