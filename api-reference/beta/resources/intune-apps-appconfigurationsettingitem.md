---
title: Tipo de recurso appConfigurationSettingItem
description: Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
author: tfitzmac
ms.openlocfilehash: 9a9020acc63c445d919564865c44d9c57a5ff57a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320947"
---
# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="edf53-103">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="edf53-103">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="edf53-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="edf53-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="edf53-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="edf53-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="edf53-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="edf53-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="edf53-107">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edf53-107">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="edf53-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="edf53-108">Properties</span></span>
|<span data-ttu-id="edf53-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="edf53-109">Property</span></span>|<span data-ttu-id="edf53-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="edf53-110">Type</span></span>|<span data-ttu-id="edf53-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="edf53-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="edf53-112">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="edf53-112">appConfigKey</span></span>|<span data-ttu-id="edf53-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="edf53-113">String</span></span>|<span data-ttu-id="edf53-114">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edf53-114">app configuration key.</span></span>|
|<span data-ttu-id="edf53-115">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="edf53-115">appConfigKeyType</span></span>|[<span data-ttu-id="edf53-116">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="edf53-116">mdmAppConfigKeyType</span></span>](../resources/intune-apps-mdmappconfigkeytype.md)|<span data-ttu-id="edf53-117">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edf53-117">app configuration key type.</span></span> <span data-ttu-id="edf53-118">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="edf53-118">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="edf53-119">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="edf53-119">appConfigKeyValue</span></span>|<span data-ttu-id="edf53-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="edf53-120">String</span></span>|<span data-ttu-id="edf53-121">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edf53-121">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="edf53-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="edf53-122">Relationships</span></span>
<span data-ttu-id="edf53-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="edf53-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="edf53-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="edf53-124">JSON Representation</span></span>
<span data-ttu-id="edf53-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="edf53-125">Here is a JSON representation of the resource.</span></span>
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





