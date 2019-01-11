---
title: tipo de recurso deviceAndAppManagementAssignedRoleIds
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1ae87f1a8430ef2539fe10e813390b0fbd68b267
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846343"
---
# <a name="deviceandappmanagementassignedroleids-resource-type"></a><span data-ttu-id="4b1bf-103">tipo de recurso deviceAndAppManagementAssignedRoleIds</span><span class="sxs-lookup"><span data-stu-id="4b1bf-103">deviceAndAppManagementAssignedRoleIds resource type</span></span>

> <span data-ttu-id="4b1bf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b1bf-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b1bf-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b1bf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4b1bf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4b1bf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4b1bf-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4b1bf-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="4b1bf-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b1bf-108">Properties</span></span>
|<span data-ttu-id="4b1bf-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b1bf-109">Property</span></span>|<span data-ttu-id="4b1bf-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b1bf-110">Type</span></span>|<span data-ttu-id="4b1bf-111">Description</span><span class="sxs-lookup"><span data-stu-id="4b1bf-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4b1bf-112">roleDefinitionIds</span><span class="sxs-lookup"><span data-stu-id="4b1bf-112">roleDefinitionIds</span></span>|<span data-ttu-id="4b1bf-113">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="4b1bf-113">Guid collection</span></span>|<span data-ttu-id="4b1bf-114">Identificadores de definición de rol para las definiciones de roles asignados a un usuario específicas.</span><span class="sxs-lookup"><span data-stu-id="4b1bf-114">Role Definition IDs for the specifc Role Definitions assigned to a user.</span></span>|
|<span data-ttu-id="4b1bf-115">roleAssignmentIds</span><span class="sxs-lookup"><span data-stu-id="4b1bf-115">roleAssignmentIds</span></span>|<span data-ttu-id="4b1bf-116">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="4b1bf-116">Guid collection</span></span>|<span data-ttu-id="4b1bf-117">Identificadores de asignación de rol para las asignaciones de roles asignados a un usuario específicas.</span><span class="sxs-lookup"><span data-stu-id="4b1bf-117">Role Assignment IDs for the specifc Role Assignments assigned to a user.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4b1bf-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4b1bf-118">Relationships</span></span>
<span data-ttu-id="4b1bf-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4b1bf-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4b1bf-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b1bf-120">JSON Representation</span></span>
<span data-ttu-id="4b1bf-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4b1bf-121">Here is a JSON representation of the resource.</span></span>
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





