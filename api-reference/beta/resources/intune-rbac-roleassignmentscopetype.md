---
title: tipo de enumeración roleAssignmentScopeType
description: Especifica el tipo de ámbito para una asignación de roles.
author: tfitzmac
ms.openlocfilehash: 0a3286b3b7bc583323204ca39ff85e01869ddbe7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343130"
---
# <a name="roleassignmentscopetype-enum-type"></a><span data-ttu-id="173c4-103">tipo de enumeración roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="173c4-103">roleAssignmentScopeType enum type</span></span>

> <span data-ttu-id="173c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="173c4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="173c4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="173c4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="173c4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="173c4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="173c4-107">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="173c4-107">Specifies the type of scope for a Role Assignment.</span></span>
## <a name="members"></a><span data-ttu-id="173c4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="173c4-108">Members</span></span>
|<span data-ttu-id="173c4-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="173c4-109">Member</span></span>|<span data-ttu-id="173c4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="173c4-110">Value</span></span>|<span data-ttu-id="173c4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="173c4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="173c4-112">resourceScope</span><span class="sxs-lookup"><span data-stu-id="173c4-112">resourceScope</span></span>|<span data-ttu-id="173c4-113">0</span><span class="sxs-lookup"><span data-stu-id="173c4-113">0</span></span>|<span data-ttu-id="173c4-114">Permitir que las asignaciones para el ResourceScopes especificado.</span><span class="sxs-lookup"><span data-stu-id="173c4-114">Allow assignments to the specified ResourceScopes.</span></span>|
|<span data-ttu-id="173c4-115">allDevices</span><span class="sxs-lookup"><span data-stu-id="173c4-115">allDevices</span></span>|<span data-ttu-id="173c4-116">1</span><span class="sxs-lookup"><span data-stu-id="173c4-116">1</span></span>|<span data-ttu-id="173c4-117">Permitir que las asignaciones a todos los dispositivos de Intune.</span><span class="sxs-lookup"><span data-stu-id="173c4-117">Allow assignments to all Intune devices.</span></span>|
|<span data-ttu-id="173c4-118">allLicensedUsers</span><span class="sxs-lookup"><span data-stu-id="173c4-118">allLicensedUsers</span></span>|<span data-ttu-id="173c4-119">2</span><span class="sxs-lookup"><span data-stu-id="173c4-119">2</span></span>|<span data-ttu-id="173c4-120">Permitir que las asignaciones a todos los usuarios de Intune con licencia.</span><span class="sxs-lookup"><span data-stu-id="173c4-120">Allow assignments to all Intune licensed users.</span></span>|
|<span data-ttu-id="173c4-121">allDevicesAndLicensedUsers</span><span class="sxs-lookup"><span data-stu-id="173c4-121">allDevicesAndLicensedUsers</span></span>|<span data-ttu-id="173c4-122">3</span><span class="sxs-lookup"><span data-stu-id="173c4-122">3</span></span>|<span data-ttu-id="173c4-123">Permitir que las asignaciones a todos los dispositivos Intune y los usuarios con licencia.</span><span class="sxs-lookup"><span data-stu-id="173c4-123">Allow assignments to all Intune devices and licensed users.</span></span>|





