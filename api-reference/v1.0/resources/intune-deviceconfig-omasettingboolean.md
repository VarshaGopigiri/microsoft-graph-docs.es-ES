---
title: Tipo de recurso omaSettingBoolean
description: Definición booleana de la configuración de OMA.
ms.openlocfilehash: 1c0cc1d90374b7720fd9ba95e7488a09167f7842
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029981"
---
# <a name="omasettingboolean-resource-type"></a><span data-ttu-id="9b028-103">Tipo de recurso omaSettingBoolean</span><span class="sxs-lookup"><span data-stu-id="9b028-103">omaSettingBoolean resource type</span></span>

> <span data-ttu-id="9b028-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b028-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b028-105">Definición booleana de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="9b028-105">OMA Settings Boolean definition.</span></span>

<span data-ttu-id="9b028-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="9b028-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="9b028-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b028-107">Properties</span></span>
|<span data-ttu-id="9b028-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b028-108">Property</span></span>|<span data-ttu-id="9b028-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b028-109">Type</span></span>|<span data-ttu-id="9b028-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b028-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b028-111">displayName</span><span class="sxs-lookup"><span data-stu-id="9b028-111">displayName</span></span>|<span data-ttu-id="9b028-112">cadena</span><span class="sxs-lookup"><span data-stu-id="9b028-112">String</span></span>|<span data-ttu-id="9b028-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="9b028-113">Display Name.</span></span> <span data-ttu-id="9b028-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="9b028-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="9b028-115">descripción</span><span class="sxs-lookup"><span data-stu-id="9b028-115">description</span></span>|<span data-ttu-id="9b028-116">String</span><span class="sxs-lookup"><span data-stu-id="9b028-116">String</span></span>|<span data-ttu-id="9b028-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="9b028-117">Description.</span></span> <span data-ttu-id="9b028-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="9b028-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="9b028-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="9b028-119">omaUri</span></span>|<span data-ttu-id="9b028-120">cadena</span><span class="sxs-lookup"><span data-stu-id="9b028-120">String</span></span>|<span data-ttu-id="9b028-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="9b028-121">OMA.</span></span> <span data-ttu-id="9b028-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="9b028-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="9b028-123">valor</span><span class="sxs-lookup"><span data-stu-id="9b028-123">value</span></span>|<span data-ttu-id="9b028-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="9b028-124">Boolean</span></span>|<span data-ttu-id="9b028-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="9b028-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9b028-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b028-126">Relationships</span></span>
<span data-ttu-id="9b028-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9b028-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9b028-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b028-128">JSON Representation</span></span>
<span data-ttu-id="9b028-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9b028-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingBoolean"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBoolean",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": true
}
```



