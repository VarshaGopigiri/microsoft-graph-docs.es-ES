---
title: Tipo de recurso appConfigurationSettingItem
description: Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
author: tfitzmac
ms.openlocfilehash: b75579e56602ad5359bc32d52312931342b42a6b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353581"
---
# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="72780-103">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="72780-103">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="72780-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="72780-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="72780-105">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72780-105">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="72780-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72780-106">Properties</span></span>
|<span data-ttu-id="72780-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72780-107">Property</span></span>|<span data-ttu-id="72780-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="72780-108">Type</span></span>|<span data-ttu-id="72780-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="72780-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72780-110">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="72780-110">appConfigKey</span></span>|<span data-ttu-id="72780-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="72780-111">String</span></span>|<span data-ttu-id="72780-112">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72780-112">app configuration key.</span></span>|
|<span data-ttu-id="72780-113">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="72780-113">appConfigKeyType</span></span>|[<span data-ttu-id="72780-114">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="72780-114">mdmAppConfigKeyType</span></span>](../resources/intune-apps-mdmappconfigkeytype.md)|<span data-ttu-id="72780-115">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72780-115">app configuration key type.</span></span> <span data-ttu-id="72780-116">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="72780-116">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="72780-117">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="72780-117">appConfigKeyValue</span></span>|<span data-ttu-id="72780-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="72780-118">String</span></span>|<span data-ttu-id="72780-119">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72780-119">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="72780-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="72780-120">Relationships</span></span>
<span data-ttu-id="72780-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="72780-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="72780-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="72780-122">JSON Representation</span></span>
<span data-ttu-id="72780-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="72780-123">Here is a JSON representation of the resource.</span></span>
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



