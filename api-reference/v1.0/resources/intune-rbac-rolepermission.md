---
title: Tipo de recurso rolePermission
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3e284198b7b2e6ad3fe120bd1c17c96a1872b793
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816607"
---
# <a name="rolepermission-resource-type"></a><span data-ttu-id="fbf41-103">Tipo de recurso rolePermission</span><span class="sxs-lookup"><span data-stu-id="fbf41-103">rolePermission resource type</span></span>

> <span data-ttu-id="fbf41-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fbf41-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fbf41-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fbf41-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="fbf41-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbf41-106">Properties</span></span>
|<span data-ttu-id="fbf41-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbf41-107">Property</span></span>|<span data-ttu-id="fbf41-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbf41-108">Type</span></span>|<span data-ttu-id="fbf41-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbf41-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fbf41-110">resourceActions</span><span class="sxs-lookup"><span data-stu-id="fbf41-110">resourceActions</span></span>|<span data-ttu-id="fbf41-111">Colección [resourceAction](../resources/intune-rbac-resourceaction.md)</span><span class="sxs-lookup"><span data-stu-id="fbf41-111">[resourceAction](../resources/intune-rbac-resourceaction.md) collection</span></span>|<span data-ttu-id="fbf41-112">Acciones</span><span class="sxs-lookup"><span data-stu-id="fbf41-112">Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="fbf41-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fbf41-113">Relationships</span></span>
<span data-ttu-id="fbf41-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fbf41-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fbf41-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fbf41-115">JSON Representation</span></span>
<span data-ttu-id="fbf41-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fbf41-116">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.rolePermission"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.rolePermission",
  "resourceActions": [
    {
      "@odata.type": "microsoft.graph.resourceAction",
      "allowedResourceActions": [
        "String"
      ],
      "notAllowedResourceActions": [
        "String"
      ]
    }
  ]
}
```



