---
title: Tipo de recurso appConfigurationSettingItem
description: Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0590a22178935e9e8a6b4eb0e279b55d4f984222
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842157"
---
# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="eac75-103">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="eac75-103">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="eac75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eac75-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eac75-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eac75-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eac75-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eac75-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eac75-107">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac75-107">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="eac75-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eac75-108">Properties</span></span>
|<span data-ttu-id="eac75-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eac75-109">Property</span></span>|<span data-ttu-id="eac75-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="eac75-110">Type</span></span>|<span data-ttu-id="eac75-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="eac75-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eac75-112">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="eac75-112">appConfigKey</span></span>|<span data-ttu-id="eac75-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="eac75-113">String</span></span>|<span data-ttu-id="eac75-114">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac75-114">app configuration key.</span></span>|
|<span data-ttu-id="eac75-115">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="eac75-115">appConfigKeyType</span></span>|[<span data-ttu-id="eac75-116">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="eac75-116">mdmAppConfigKeyType</span></span>](../resources/intune-apps-mdmappconfigkeytype.md)|<span data-ttu-id="eac75-117">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac75-117">app configuration key type.</span></span> <span data-ttu-id="eac75-118">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="eac75-118">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="eac75-119">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="eac75-119">appConfigKeyValue</span></span>|<span data-ttu-id="eac75-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="eac75-120">String</span></span>|<span data-ttu-id="eac75-121">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac75-121">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="eac75-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eac75-122">Relationships</span></span>
<span data-ttu-id="eac75-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="eac75-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="eac75-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eac75-124">JSON Representation</span></span>
<span data-ttu-id="eac75-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="eac75-125">Here is a JSON representation of the resource.</span></span>
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





