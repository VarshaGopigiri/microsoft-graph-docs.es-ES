---
title: Tipo de recurso auditResource
description: Una clase que contiene las propiedades del recurso de auditoría.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7f8fc3a96b3d17759e1e65eaa17c6571e4cec347
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844740"
---
# <a name="auditresource-resource-type"></a><span data-ttu-id="74341-103">Tipo de recurso auditResource</span><span class="sxs-lookup"><span data-stu-id="74341-103">auditResource resource type</span></span>

> <span data-ttu-id="74341-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74341-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74341-105">Una clase que contiene las propiedades del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="74341-105">A class containing the properties for Audit Resource.</span></span>
## <a name="properties"></a><span data-ttu-id="74341-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74341-106">Properties</span></span>
|<span data-ttu-id="74341-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74341-107">Property</span></span>|<span data-ttu-id="74341-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="74341-108">Type</span></span>|<span data-ttu-id="74341-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="74341-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="74341-110">displayName</span><span class="sxs-lookup"><span data-stu-id="74341-110">displayName</span></span>|<span data-ttu-id="74341-111">cadena</span><span class="sxs-lookup"><span data-stu-id="74341-111">String</span></span>|<span data-ttu-id="74341-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="74341-112">Display name.</span></span>|
|<span data-ttu-id="74341-113">modifiedProperties</span><span class="sxs-lookup"><span data-stu-id="74341-113">modifiedProperties</span></span>|<span data-ttu-id="74341-114">Colección [auditProperty](../resources/intune-auditing-auditproperty.md)</span><span class="sxs-lookup"><span data-stu-id="74341-114">[auditProperty](../resources/intune-auditing-auditproperty.md) collection</span></span>|<span data-ttu-id="74341-115">Lista de propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="74341-115">List of modified properties.</span></span>|
|<span data-ttu-id="74341-116">tipo</span><span class="sxs-lookup"><span data-stu-id="74341-116">type</span></span>|<span data-ttu-id="74341-117">cadena</span><span class="sxs-lookup"><span data-stu-id="74341-117">String</span></span>|<span data-ttu-id="74341-118">Tipo del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="74341-118">Audit resource's type.</span></span>|
|<span data-ttu-id="74341-119">resourceId</span><span class="sxs-lookup"><span data-stu-id="74341-119">resourceId</span></span>|<span data-ttu-id="74341-120">cadena</span><span class="sxs-lookup"><span data-stu-id="74341-120">String</span></span>|<span data-ttu-id="74341-121">Identificador del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="74341-121">Audit resource's Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="74341-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="74341-122">Relationships</span></span>
<span data-ttu-id="74341-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="74341-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="74341-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="74341-124">JSON Representation</span></span>
<span data-ttu-id="74341-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="74341-125">Here is a JSON representation of the resource.</span></span>
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



