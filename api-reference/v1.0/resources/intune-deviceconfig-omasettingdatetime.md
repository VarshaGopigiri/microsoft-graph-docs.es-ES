---
title: Tipo de recurso omaSettingDateTime
description: Definición de DateTime de la configuración de OMA.
ms.openlocfilehash: b4ea11c22acb2a4119c2de1934f1ae66c2310658
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029306"
---
# <a name="omasettingdatetime-resource-type"></a><span data-ttu-id="4bff9-103">Tipo de recurso omaSettingDateTime</span><span class="sxs-lookup"><span data-stu-id="4bff9-103">omaSettingDateTime resource type</span></span>

> <span data-ttu-id="4bff9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4bff9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4bff9-105">Definición de DateTime de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="4bff9-105">OMA Settings DateTime definition.</span></span>

<span data-ttu-id="4bff9-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4bff9-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="4bff9-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bff9-107">Properties</span></span>
|<span data-ttu-id="4bff9-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bff9-108">Property</span></span>|<span data-ttu-id="4bff9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bff9-109">Type</span></span>|<span data-ttu-id="4bff9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bff9-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4bff9-111">displayName</span><span class="sxs-lookup"><span data-stu-id="4bff9-111">displayName</span></span>|<span data-ttu-id="4bff9-112">cadena</span><span class="sxs-lookup"><span data-stu-id="4bff9-112">String</span></span>|<span data-ttu-id="4bff9-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="4bff9-113">Display Name.</span></span> <span data-ttu-id="4bff9-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4bff9-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="4bff9-115">descripción</span><span class="sxs-lookup"><span data-stu-id="4bff9-115">description</span></span>|<span data-ttu-id="4bff9-116">String</span><span class="sxs-lookup"><span data-stu-id="4bff9-116">String</span></span>|<span data-ttu-id="4bff9-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="4bff9-117">Description.</span></span> <span data-ttu-id="4bff9-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4bff9-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="4bff9-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="4bff9-119">omaUri</span></span>|<span data-ttu-id="4bff9-120">cadena</span><span class="sxs-lookup"><span data-stu-id="4bff9-120">String</span></span>|<span data-ttu-id="4bff9-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="4bff9-121">OMA.</span></span> <span data-ttu-id="4bff9-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4bff9-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="4bff9-123">value</span><span class="sxs-lookup"><span data-stu-id="4bff9-123">value</span></span>|<span data-ttu-id="4bff9-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4bff9-124">DateTimeOffset</span></span>|<span data-ttu-id="4bff9-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="4bff9-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4bff9-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4bff9-126">Relationships</span></span>
<span data-ttu-id="4bff9-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4bff9-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4bff9-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4bff9-128">JSON Representation</span></span>
<span data-ttu-id="4bff9-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4bff9-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingDateTime"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingDateTime",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String (timestamp)"
}
```



