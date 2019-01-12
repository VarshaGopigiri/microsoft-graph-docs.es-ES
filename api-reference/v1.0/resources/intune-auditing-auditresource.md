---
title: Tipo de recurso auditResource
description: Una clase que contiene las propiedades del recurso de auditoría.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4778e01076e2af1c18edb16a2587f65396cc6466
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977257"
---
# <a name="auditresource-resource-type"></a><span data-ttu-id="229f1-103">Tipo de recurso auditResource</span><span class="sxs-lookup"><span data-stu-id="229f1-103">auditResource resource type</span></span>

> <span data-ttu-id="229f1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="229f1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="229f1-105">Una clase que contiene las propiedades del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="229f1-105">A class containing the properties for Audit Resource.</span></span>
## <a name="properties"></a><span data-ttu-id="229f1-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="229f1-106">Properties</span></span>
|<span data-ttu-id="229f1-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="229f1-107">Property</span></span>|<span data-ttu-id="229f1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="229f1-108">Type</span></span>|<span data-ttu-id="229f1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="229f1-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="229f1-110">displayName</span><span class="sxs-lookup"><span data-stu-id="229f1-110">displayName</span></span>|<span data-ttu-id="229f1-111">cadena</span><span class="sxs-lookup"><span data-stu-id="229f1-111">String</span></span>|<span data-ttu-id="229f1-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="229f1-112">Display name.</span></span>|
|<span data-ttu-id="229f1-113">modifiedProperties</span><span class="sxs-lookup"><span data-stu-id="229f1-113">modifiedProperties</span></span>|<span data-ttu-id="229f1-114">Colección [auditProperty](../resources/intune-auditing-auditproperty.md)</span><span class="sxs-lookup"><span data-stu-id="229f1-114">[auditProperty](../resources/intune-auditing-auditproperty.md) collection</span></span>|<span data-ttu-id="229f1-115">Lista de propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="229f1-115">List of modified properties.</span></span>|
|<span data-ttu-id="229f1-116">tipo</span><span class="sxs-lookup"><span data-stu-id="229f1-116">type</span></span>|<span data-ttu-id="229f1-117">cadena</span><span class="sxs-lookup"><span data-stu-id="229f1-117">String</span></span>|<span data-ttu-id="229f1-118">Tipo del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="229f1-118">Audit resource's type.</span></span>|
|<span data-ttu-id="229f1-119">resourceId</span><span class="sxs-lookup"><span data-stu-id="229f1-119">resourceId</span></span>|<span data-ttu-id="229f1-120">cadena</span><span class="sxs-lookup"><span data-stu-id="229f1-120">String</span></span>|<span data-ttu-id="229f1-121">Identificador del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="229f1-121">Audit resource's Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="229f1-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="229f1-122">Relationships</span></span>
<span data-ttu-id="229f1-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="229f1-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="229f1-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="229f1-124">JSON Representation</span></span>
<span data-ttu-id="229f1-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="229f1-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditResource"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditResource",
  "displayName": "String",
  "modifiedProperties": [
    {
      "@odata.type": "microsoft.graph.auditProperty",
      "displayName": "String",
      "oldValue": "String",
      "newValue": "String"
    }
  ],
  "type": "String",
  "resourceId": "String"
}
```



