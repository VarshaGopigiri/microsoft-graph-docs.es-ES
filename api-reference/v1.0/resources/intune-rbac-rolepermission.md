---
title: Tipo de recurso rolePermission
description: Todavía no documentado
ms.openlocfilehash: 16c78e2ee4475a717879d501aabeb5fe2ae0d481
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030201"
---
# <a name="rolepermission-resource-type"></a><span data-ttu-id="ff499-103">Tipo de recurso rolePermission</span><span class="sxs-lookup"><span data-stu-id="ff499-103">rolePermission resource type</span></span>

> <span data-ttu-id="ff499-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ff499-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ff499-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ff499-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="ff499-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff499-106">Properties</span></span>
|<span data-ttu-id="ff499-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff499-107">Property</span></span>|<span data-ttu-id="ff499-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff499-108">Type</span></span>|<span data-ttu-id="ff499-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff499-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ff499-110">resourceActions</span><span class="sxs-lookup"><span data-stu-id="ff499-110">resourceActions</span></span>|<span data-ttu-id="ff499-111">Colección [resourceAction](../resources/intune-rbac-resourceaction.md)</span><span class="sxs-lookup"><span data-stu-id="ff499-111">[resourceAction](../resources/intune-rbac-resourceaction.md) collection</span></span>|<span data-ttu-id="ff499-112">Acciones</span><span class="sxs-lookup"><span data-stu-id="ff499-112">Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="ff499-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff499-113">Relationships</span></span>
<span data-ttu-id="ff499-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ff499-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ff499-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff499-115">JSON Representation</span></span>
<span data-ttu-id="ff499-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff499-116">Here is a JSON representation of the resource.</span></span>
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


