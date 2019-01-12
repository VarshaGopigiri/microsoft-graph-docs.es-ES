---
title: Tipo de recurso rolePermission
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b8b9ba237052fef2b4caa8123d147ea1782fa9b9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932808"
---
# <a name="rolepermission-resource-type"></a><span data-ttu-id="c61ff-103">Tipo de recurso rolePermission</span><span class="sxs-lookup"><span data-stu-id="c61ff-103">rolePermission resource type</span></span>

> <span data-ttu-id="c61ff-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c61ff-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c61ff-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c61ff-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="c61ff-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c61ff-106">Properties</span></span>
|<span data-ttu-id="c61ff-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c61ff-107">Property</span></span>|<span data-ttu-id="c61ff-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c61ff-108">Type</span></span>|<span data-ttu-id="c61ff-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c61ff-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c61ff-110">resourceActions</span><span class="sxs-lookup"><span data-stu-id="c61ff-110">resourceActions</span></span>|<span data-ttu-id="c61ff-111">Colección [resourceAction](../resources/intune-rbac-resourceaction.md)</span><span class="sxs-lookup"><span data-stu-id="c61ff-111">[resourceAction](../resources/intune-rbac-resourceaction.md) collection</span></span>|<span data-ttu-id="c61ff-112">Acciones</span><span class="sxs-lookup"><span data-stu-id="c61ff-112">Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="c61ff-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c61ff-113">Relationships</span></span>
<span data-ttu-id="c61ff-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c61ff-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c61ff-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c61ff-115">JSON Representation</span></span>
<span data-ttu-id="c61ff-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c61ff-116">Here is a JSON representation of the resource.</span></span>
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



