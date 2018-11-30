---
title: Tipo de recurso auditResource
description: Una clase que contiene las propiedades del recurso de auditoría.
ms.openlocfilehash: a3825418c1406bbe9fcce7feeba96217342c735e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088742"
---
# <a name="auditresource-resource-type"></a><span data-ttu-id="579d4-103">Tipo de recurso auditResource</span><span class="sxs-lookup"><span data-stu-id="579d4-103">auditResource resource type</span></span>

> <span data-ttu-id="579d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="579d4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="579d4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="579d4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="579d4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="579d4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="579d4-107">Una clase que contiene las propiedades del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="579d4-107">A class containing the properties for Audit Resource.</span></span>
## <a name="properties"></a><span data-ttu-id="579d4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="579d4-108">Properties</span></span>
|<span data-ttu-id="579d4-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="579d4-109">Property</span></span>|<span data-ttu-id="579d4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="579d4-110">Type</span></span>|<span data-ttu-id="579d4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="579d4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="579d4-112">displayName</span><span class="sxs-lookup"><span data-stu-id="579d4-112">displayName</span></span>|<span data-ttu-id="579d4-113">cadena</span><span class="sxs-lookup"><span data-stu-id="579d4-113">String</span></span>|<span data-ttu-id="579d4-114">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="579d4-114">Display name.</span></span>|
|<span data-ttu-id="579d4-115">modifiedProperties</span><span class="sxs-lookup"><span data-stu-id="579d4-115">modifiedProperties</span></span>|<span data-ttu-id="579d4-116">Colección [auditProperty](../resources/intune-auditing-auditproperty.md)</span><span class="sxs-lookup"><span data-stu-id="579d4-116">[auditProperty](../resources/intune-auditing-auditproperty.md) collection</span></span>|<span data-ttu-id="579d4-117">Lista de propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="579d4-117">List of modified properties.</span></span>|
|<span data-ttu-id="579d4-118">tipo</span><span class="sxs-lookup"><span data-stu-id="579d4-118">type</span></span>|<span data-ttu-id="579d4-119">cadena</span><span class="sxs-lookup"><span data-stu-id="579d4-119">String</span></span>|<span data-ttu-id="579d4-120">Tipo del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="579d4-120">Audit resource's type.</span></span>|
|<span data-ttu-id="579d4-121">resourceId</span><span class="sxs-lookup"><span data-stu-id="579d4-121">resourceId</span></span>|<span data-ttu-id="579d4-122">cadena</span><span class="sxs-lookup"><span data-stu-id="579d4-122">String</span></span>|<span data-ttu-id="579d4-123">Identificador del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="579d4-123">Audit resource's Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="579d4-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="579d4-124">Relationships</span></span>
<span data-ttu-id="579d4-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="579d4-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="579d4-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="579d4-126">JSON Representation</span></span>
<span data-ttu-id="579d4-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="579d4-127">Here is a JSON representation of the resource.</span></span>
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





