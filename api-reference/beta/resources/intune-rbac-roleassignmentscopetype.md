---
title: tipo de enumeración roleAssignmentScopeType
description: Especifica el tipo de ámbito para una asignación de roles.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 738579fbd8bcda9ac438ada2f7746e020396d225
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871543"
---
# <a name="roleassignmentscopetype-enum-type"></a><span data-ttu-id="d2636-103">tipo de enumeración roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="d2636-103">roleAssignmentScopeType enum type</span></span>

> <span data-ttu-id="d2636-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2636-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2636-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2636-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d2636-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2636-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2636-107">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="d2636-107">Specifies the type of scope for a Role Assignment.</span></span>
## <a name="members"></a><span data-ttu-id="d2636-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2636-108">Members</span></span>
|<span data-ttu-id="d2636-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d2636-109">Member</span></span>|<span data-ttu-id="d2636-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d2636-110">Value</span></span>|<span data-ttu-id="d2636-111">Description</span><span class="sxs-lookup"><span data-stu-id="d2636-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2636-112">resourceScope</span><span class="sxs-lookup"><span data-stu-id="d2636-112">resourceScope</span></span>|<span data-ttu-id="d2636-113">0</span><span class="sxs-lookup"><span data-stu-id="d2636-113">0</span></span>|<span data-ttu-id="d2636-114">Permitir que las asignaciones para el ResourceScopes especificado.</span><span class="sxs-lookup"><span data-stu-id="d2636-114">Allow assignments to the specified ResourceScopes.</span></span>|
|<span data-ttu-id="d2636-115">allDevices</span><span class="sxs-lookup"><span data-stu-id="d2636-115">allDevices</span></span>|<span data-ttu-id="d2636-116">1</span><span class="sxs-lookup"><span data-stu-id="d2636-116">1</span></span>|<span data-ttu-id="d2636-117">Permitir que las asignaciones a todos los dispositivos de Intune.</span><span class="sxs-lookup"><span data-stu-id="d2636-117">Allow assignments to all Intune devices.</span></span>|
|<span data-ttu-id="d2636-118">allLicensedUsers</span><span class="sxs-lookup"><span data-stu-id="d2636-118">allLicensedUsers</span></span>|<span data-ttu-id="d2636-119">2</span><span class="sxs-lookup"><span data-stu-id="d2636-119">2</span></span>|<span data-ttu-id="d2636-120">Permitir que las asignaciones a todos los usuarios de Intune con licencia.</span><span class="sxs-lookup"><span data-stu-id="d2636-120">Allow assignments to all Intune licensed users.</span></span>|
|<span data-ttu-id="d2636-121">allDevicesAndLicensedUsers</span><span class="sxs-lookup"><span data-stu-id="d2636-121">allDevicesAndLicensedUsers</span></span>|<span data-ttu-id="d2636-122">3</span><span class="sxs-lookup"><span data-stu-id="d2636-122">3</span></span>|<span data-ttu-id="d2636-123">Permitir que las asignaciones a todos los dispositivos Intune y los usuarios con licencia.</span><span class="sxs-lookup"><span data-stu-id="d2636-123">Allow assignments to all Intune devices and licensed users.</span></span>|





