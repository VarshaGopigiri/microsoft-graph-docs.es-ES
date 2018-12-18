---
title: Tipo de recurso rolePermission
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: c33af6af3bc06a53bd24ddf97576551a5eea6e9c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349108"
---
# <a name="rolepermission-resource-type"></a><span data-ttu-id="c57e6-103">Tipo de recurso rolePermission</span><span class="sxs-lookup"><span data-stu-id="c57e6-103">rolePermission resource type</span></span>

> <span data-ttu-id="c57e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c57e6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c57e6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c57e6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c57e6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c57e6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c57e6-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c57e6-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="c57e6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c57e6-108">Properties</span></span>
|<span data-ttu-id="c57e6-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c57e6-109">Property</span></span>|<span data-ttu-id="c57e6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c57e6-110">Type</span></span>|<span data-ttu-id="c57e6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c57e6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c57e6-112">actions</span><span class="sxs-lookup"><span data-stu-id="c57e6-112">actions</span></span>|<span data-ttu-id="c57e6-113">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="c57e6-113">String collection</span></span>|<span data-ttu-id="c57e6-114">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="c57e6-114">Allowed Actions</span></span>|
|<span data-ttu-id="c57e6-115">resourceActions</span><span class="sxs-lookup"><span data-stu-id="c57e6-115">resourceActions</span></span>|<span data-ttu-id="c57e6-116">Colección [resourceAction](../resources/intune-rbac-resourceaction.md)</span><span class="sxs-lookup"><span data-stu-id="c57e6-116">[resourceAction](../resources/intune-rbac-resourceaction.md) collection</span></span>|<span data-ttu-id="c57e6-117">Acciones</span><span class="sxs-lookup"><span data-stu-id="c57e6-117">Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="c57e6-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c57e6-118">Relationships</span></span>
<span data-ttu-id="c57e6-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c57e6-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c57e6-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c57e6-120">JSON Representation</span></span>
<span data-ttu-id="c57e6-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c57e6-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.rolePermission"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.rolePermission",
  "actions": [
    "String"
  ],
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





