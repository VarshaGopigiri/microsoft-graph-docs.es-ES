---
title: Tipo de recurso appConfigurationSettingItem
description: Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ddb7b503ff14e6499342fafc2d0cf5ab8e670138
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960339"
---
# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="2508b-103">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="2508b-103">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="2508b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2508b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2508b-105">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2508b-105">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="2508b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2508b-106">Properties</span></span>
|<span data-ttu-id="2508b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2508b-107">Property</span></span>|<span data-ttu-id="2508b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2508b-108">Type</span></span>|<span data-ttu-id="2508b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2508b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2508b-110">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="2508b-110">appConfigKey</span></span>|<span data-ttu-id="2508b-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="2508b-111">String</span></span>|<span data-ttu-id="2508b-112">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2508b-112">app configuration key.</span></span>|
|<span data-ttu-id="2508b-113">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="2508b-113">appConfigKeyType</span></span>|[<span data-ttu-id="2508b-114">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="2508b-114">mdmAppConfigKeyType</span></span>](../resources/intune-apps-mdmappconfigkeytype.md)|<span data-ttu-id="2508b-115">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2508b-115">app configuration key type.</span></span> <span data-ttu-id="2508b-116">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="2508b-116">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="2508b-117">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="2508b-117">appConfigKeyValue</span></span>|<span data-ttu-id="2508b-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="2508b-118">String</span></span>|<span data-ttu-id="2508b-119">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2508b-119">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2508b-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2508b-120">Relationships</span></span>
<span data-ttu-id="2508b-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2508b-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2508b-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2508b-122">JSON Representation</span></span>
<span data-ttu-id="2508b-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2508b-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appConfigurationSettingItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appConfigurationSettingItem",
  "appConfigKey": "String",
  "appConfigKeyType": "String",
  "appConfigKeyValue": "String"
}
```



