---
title: Tipo de recurso auditResource
description: Una clase que contiene las propiedades del recurso de auditoría.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ac7da99203631696b8c93fbde62db906143ffe38
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952247"
---
# <a name="auditresource-resource-type"></a><span data-ttu-id="6138d-103">Tipo de recurso auditResource</span><span class="sxs-lookup"><span data-stu-id="6138d-103">auditResource resource type</span></span>

> <span data-ttu-id="6138d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6138d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6138d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6138d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6138d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6138d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6138d-107">Una clase que contiene las propiedades del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="6138d-107">A class containing the properties for Audit Resource.</span></span>
## <a name="properties"></a><span data-ttu-id="6138d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6138d-108">Properties</span></span>
|<span data-ttu-id="6138d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6138d-109">Property</span></span>|<span data-ttu-id="6138d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6138d-110">Type</span></span>|<span data-ttu-id="6138d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6138d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6138d-112">displayName</span><span class="sxs-lookup"><span data-stu-id="6138d-112">displayName</span></span>|<span data-ttu-id="6138d-113">cadena</span><span class="sxs-lookup"><span data-stu-id="6138d-113">String</span></span>|<span data-ttu-id="6138d-114">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6138d-114">Display name.</span></span>|
|<span data-ttu-id="6138d-115">modifiedProperties</span><span class="sxs-lookup"><span data-stu-id="6138d-115">modifiedProperties</span></span>|<span data-ttu-id="6138d-116">Colección [auditProperty](../resources/intune-auditing-auditproperty.md)</span><span class="sxs-lookup"><span data-stu-id="6138d-116">[auditProperty](../resources/intune-auditing-auditproperty.md) collection</span></span>|<span data-ttu-id="6138d-117">Lista de propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="6138d-117">List of modified properties.</span></span>|
|<span data-ttu-id="6138d-118">tipo</span><span class="sxs-lookup"><span data-stu-id="6138d-118">type</span></span>|<span data-ttu-id="6138d-119">cadena</span><span class="sxs-lookup"><span data-stu-id="6138d-119">String</span></span>|<span data-ttu-id="6138d-120">Tipo del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="6138d-120">Audit resource's type.</span></span>|
|<span data-ttu-id="6138d-121">resourceId</span><span class="sxs-lookup"><span data-stu-id="6138d-121">resourceId</span></span>|<span data-ttu-id="6138d-122">cadena</span><span class="sxs-lookup"><span data-stu-id="6138d-122">String</span></span>|<span data-ttu-id="6138d-123">Identificador del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="6138d-123">Audit resource's Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6138d-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6138d-124">Relationships</span></span>
<span data-ttu-id="6138d-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6138d-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6138d-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6138d-126">JSON Representation</span></span>
<span data-ttu-id="6138d-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6138d-127">Here is a JSON representation of the resource.</span></span>
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





