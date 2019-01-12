---
title: tipo de recurso managedDeviceModelsAndManufacturers
description: Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8a1769f82153fd8184807877c484a4dc31ebda1a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927530"
---
# <a name="manageddevicemodelsandmanufacturers-resource-type"></a><span data-ttu-id="52711-103">tipo de recurso managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="52711-103">managedDeviceModelsAndManufacturers resource type</span></span>

> <span data-ttu-id="52711-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52711-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52711-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52711-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="52711-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52711-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52711-107">Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="52711-107">Models and Manufactures meatadata for managed devices in the account</span></span>
## <a name="properties"></a><span data-ttu-id="52711-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52711-108">Properties</span></span>
|<span data-ttu-id="52711-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52711-109">Property</span></span>|<span data-ttu-id="52711-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="52711-110">Type</span></span>|<span data-ttu-id="52711-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="52711-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="52711-112">deviceModels</span><span class="sxs-lookup"><span data-stu-id="52711-112">deviceModels</span></span>|<span data-ttu-id="52711-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="52711-113">String collection</span></span>|<span data-ttu-id="52711-114">Lista de modelos para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="52711-114">List of Models for managed devices in the account</span></span>|
|<span data-ttu-id="52711-115">deviceManufacturers</span><span class="sxs-lookup"><span data-stu-id="52711-115">deviceManufacturers</span></span>|<span data-ttu-id="52711-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="52711-116">String collection</span></span>|<span data-ttu-id="52711-117">Lista de fabricantes de los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="52711-117">List of Manufactures for managed devices in the account</span></span>|

## <a name="relationships"></a><span data-ttu-id="52711-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="52711-118">Relationships</span></span>
<span data-ttu-id="52711-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="52711-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="52711-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="52711-120">JSON Representation</span></span>
<span data-ttu-id="52711-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="52711-121">Here is a JSON representation of the resource.</span></span>
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





