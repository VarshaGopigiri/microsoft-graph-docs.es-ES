---
title: tipo de recurso deviceAndAppManagementAssignedRoleIds
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 034120b891812a43c6c1683f61e52f071dc89816
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353385"
---
# <a name="deviceandappmanagementassignedroleids-resource-type"></a><span data-ttu-id="fb953-103">tipo de recurso deviceAndAppManagementAssignedRoleIds</span><span class="sxs-lookup"><span data-stu-id="fb953-103">deviceAndAppManagementAssignedRoleIds resource type</span></span>

> <span data-ttu-id="fb953-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb953-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb953-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb953-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fb953-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb953-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb953-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fb953-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="fb953-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb953-108">Properties</span></span>
|<span data-ttu-id="fb953-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb953-109">Property</span></span>|<span data-ttu-id="fb953-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb953-110">Type</span></span>|<span data-ttu-id="fb953-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb953-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb953-112">roleDefinitionIds</span><span class="sxs-lookup"><span data-stu-id="fb953-112">roleDefinitionIds</span></span>|<span data-ttu-id="fb953-113">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="fb953-113">Guid collection</span></span>|<span data-ttu-id="fb953-114">Identificadores de definición de rol para las definiciones de roles asignados a un usuario específicas.</span><span class="sxs-lookup"><span data-stu-id="fb953-114">Role Definition IDs for the specifc Role Definitions assigned to a user.</span></span>|
|<span data-ttu-id="fb953-115">roleAssignmentIds</span><span class="sxs-lookup"><span data-stu-id="fb953-115">roleAssignmentIds</span></span>|<span data-ttu-id="fb953-116">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="fb953-116">Guid collection</span></span>|<span data-ttu-id="fb953-117">Identificadores de asignación de rol para las asignaciones de roles asignados a un usuario específicas.</span><span class="sxs-lookup"><span data-stu-id="fb953-117">Role Assignment IDs for the specifc Role Assignments assigned to a user.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fb953-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fb953-118">Relationships</span></span>
<span data-ttu-id="fb953-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fb953-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fb953-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb953-120">JSON Representation</span></span>
<span data-ttu-id="fb953-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fb953-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceAndAppManagementAssignedRoleIds"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementAssignedRoleIds",
  "roleDefinitionIds": [
    "Guid"
  ],
  "roleAssignmentIds": [
    "Guid"
  ]
}
```





