---
title: Tipo de recurso omaSettingInteger
description: Definición del entero de la configuración de OMA.
ms.openlocfilehash: 36c22b423161d9f3c58c3085fb7b040c663d460b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032091"
---
# <a name="omasettinginteger-resource-type"></a><span data-ttu-id="678ed-103">Tipo de recurso omaSettingInteger</span><span class="sxs-lookup"><span data-stu-id="678ed-103">omaSettingInteger resource type</span></span>

> <span data-ttu-id="678ed-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="678ed-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="678ed-105">Definición del entero de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="678ed-105">OMA Settings Integer definition.</span></span>

<span data-ttu-id="678ed-106">Hereda de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="678ed-106">Inherits from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="678ed-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="678ed-107">Properties</span></span>
|<span data-ttu-id="678ed-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="678ed-108">Property</span></span>|<span data-ttu-id="678ed-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="678ed-109">Type</span></span>|<span data-ttu-id="678ed-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="678ed-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="678ed-111">displayName</span><span class="sxs-lookup"><span data-stu-id="678ed-111">displayName</span></span>|<span data-ttu-id="678ed-112">cadena</span><span class="sxs-lookup"><span data-stu-id="678ed-112">String</span></span>|<span data-ttu-id="678ed-113">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="678ed-113">Display Name.</span></span> <span data-ttu-id="678ed-114">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="678ed-114">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="678ed-115">descripción</span><span class="sxs-lookup"><span data-stu-id="678ed-115">description</span></span>|<span data-ttu-id="678ed-116">String</span><span class="sxs-lookup"><span data-stu-id="678ed-116">String</span></span>|<span data-ttu-id="678ed-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="678ed-117">Description.</span></span> <span data-ttu-id="678ed-118">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="678ed-118">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="678ed-119">omaUri</span><span class="sxs-lookup"><span data-stu-id="678ed-119">omaUri</span></span>|<span data-ttu-id="678ed-120">cadena</span><span class="sxs-lookup"><span data-stu-id="678ed-120">String</span></span>|<span data-ttu-id="678ed-121">OMA.</span><span class="sxs-lookup"><span data-stu-id="678ed-121">OMA.</span></span> <span data-ttu-id="678ed-122">Heredado de [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="678ed-122">Inherited from [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span></span>|
|<span data-ttu-id="678ed-123">valor</span><span class="sxs-lookup"><span data-stu-id="678ed-123">value</span></span>|<span data-ttu-id="678ed-124">Int32</span><span class="sxs-lookup"><span data-stu-id="678ed-124">Int32</span></span>|<span data-ttu-id="678ed-125">Valor.</span><span class="sxs-lookup"><span data-stu-id="678ed-125">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="678ed-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="678ed-126">Relationships</span></span>
<span data-ttu-id="678ed-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="678ed-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="678ed-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="678ed-128">JSON Representation</span></span>
<span data-ttu-id="678ed-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="678ed-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingInteger"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingInteger",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": 1024
}
```



