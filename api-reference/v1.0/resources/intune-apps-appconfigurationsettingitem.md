---
title: Tipo de recurso appConfigurationSettingItem
description: Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 900a16544b0166263b7d40c428c2c4cbaf5a0bb6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830425"
---
# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="e0812-103">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="e0812-103">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="e0812-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e0812-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e0812-105">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0812-105">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="e0812-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0812-106">Properties</span></span>
|<span data-ttu-id="e0812-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0812-107">Property</span></span>|<span data-ttu-id="e0812-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0812-108">Type</span></span>|<span data-ttu-id="e0812-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0812-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e0812-110">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="e0812-110">appConfigKey</span></span>|<span data-ttu-id="e0812-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="e0812-111">String</span></span>|<span data-ttu-id="e0812-112">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0812-112">app configuration key.</span></span>|
|<span data-ttu-id="e0812-113">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="e0812-113">appConfigKeyType</span></span>|[<span data-ttu-id="e0812-114">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="e0812-114">mdmAppConfigKeyType</span></span>](../resources/intune-apps-mdmappconfigkeytype.md)|<span data-ttu-id="e0812-115">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0812-115">app configuration key type.</span></span> <span data-ttu-id="e0812-116">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="e0812-116">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="e0812-117">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="e0812-117">appConfigKeyValue</span></span>|<span data-ttu-id="e0812-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="e0812-118">String</span></span>|<span data-ttu-id="e0812-119">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0812-119">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e0812-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e0812-120">Relationships</span></span>
<span data-ttu-id="e0812-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e0812-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e0812-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0812-122">JSON Representation</span></span>
<span data-ttu-id="e0812-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e0812-123">Here is a JSON representation of the resource.</span></span>
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



