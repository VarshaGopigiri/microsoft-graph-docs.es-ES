---
title: Tipo de recurso appConfigurationSettingItem
description: Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
ms.openlocfilehash: bd08b325fd04e8e4a742da515d052d453cfb58a7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030411"
---
# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="88e00-103">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="88e00-103">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="88e00-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="88e00-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="88e00-105">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88e00-105">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="88e00-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88e00-106">Properties</span></span>
|<span data-ttu-id="88e00-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88e00-107">Property</span></span>|<span data-ttu-id="88e00-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="88e00-108">Type</span></span>|<span data-ttu-id="88e00-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="88e00-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="88e00-110">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="88e00-110">appConfigKey</span></span>|<span data-ttu-id="88e00-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="88e00-111">String</span></span>|<span data-ttu-id="88e00-112">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88e00-112">app configuration key.</span></span>|
|<span data-ttu-id="88e00-113">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="88e00-113">appConfigKeyType</span></span>|[<span data-ttu-id="88e00-114">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="88e00-114">mdmAppConfigKeyType</span></span>](../resources/intune-apps-mdmappconfigkeytype.md)|<span data-ttu-id="88e00-115">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88e00-115">app configuration key type.</span></span> <span data-ttu-id="88e00-116">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="88e00-116">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="88e00-117">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="88e00-117">appConfigKeyValue</span></span>|<span data-ttu-id="88e00-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="88e00-118">String</span></span>|<span data-ttu-id="88e00-119">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88e00-119">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="88e00-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="88e00-120">Relationships</span></span>
<span data-ttu-id="88e00-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="88e00-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="88e00-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="88e00-122">JSON Representation</span></span>
<span data-ttu-id="88e00-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="88e00-123">Here is a JSON representation of the resource.</span></span>
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



