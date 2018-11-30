---
title: tipo de recurso managedDeviceModelsAndManufacturers
description: Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta
ms.openlocfilehash: c61026a6caa097e01e09a4343dd54f769c743460
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090945"
---
# <a name="manageddevicemodelsandmanufacturers-resource-type"></a><span data-ttu-id="5276d-103">tipo de recurso managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="5276d-103">managedDeviceModelsAndManufacturers resource type</span></span>

> <span data-ttu-id="5276d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5276d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5276d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5276d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5276d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5276d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5276d-107">Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="5276d-107">Models and Manufactures meatadata for managed devices in the account</span></span>
## <a name="properties"></a><span data-ttu-id="5276d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5276d-108">Properties</span></span>
|<span data-ttu-id="5276d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5276d-109">Property</span></span>|<span data-ttu-id="5276d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5276d-110">Type</span></span>|<span data-ttu-id="5276d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5276d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5276d-112">deviceModels</span><span class="sxs-lookup"><span data-stu-id="5276d-112">deviceModels</span></span>|<span data-ttu-id="5276d-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="5276d-113">String collection</span></span>|<span data-ttu-id="5276d-114">Lista de modelos para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="5276d-114">List of Models for managed devices in the account</span></span>|
|<span data-ttu-id="5276d-115">deviceManufacturers</span><span class="sxs-lookup"><span data-stu-id="5276d-115">deviceManufacturers</span></span>|<span data-ttu-id="5276d-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="5276d-116">String collection</span></span>|<span data-ttu-id="5276d-117">Lista de fabricantes de los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="5276d-117">List of Manufactures for managed devices in the account</span></span>|

## <a name="relationships"></a><span data-ttu-id="5276d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5276d-118">Relationships</span></span>
<span data-ttu-id="5276d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5276d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5276d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5276d-120">JSON Representation</span></span>
<span data-ttu-id="5276d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5276d-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceModelsAndManufacturers"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceModelsAndManufacturers",
  "deviceModels": [
    "String"
  ],
  "deviceManufacturers": [
    "String"
  ]
}
```





