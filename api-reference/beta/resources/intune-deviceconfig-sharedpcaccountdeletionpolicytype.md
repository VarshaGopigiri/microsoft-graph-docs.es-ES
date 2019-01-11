---
title: tipo de enumeración sharedPCAccountDeletionPolicyType
description: Valores posibles para cuando se eliminan las cuentas en un equipo compartido.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d7f51f76e6164c973b213eb53526d5961bb2b627
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861036"
---
# <a name="sharedpcaccountdeletionpolicytype-enum-type"></a><span data-ttu-id="5dbf8-103">tipo de enumeración sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="5dbf8-103">sharedPCAccountDeletionPolicyType enum type</span></span>

> <span data-ttu-id="5dbf8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5dbf8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5dbf8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5dbf8-107">Valores posibles para cuando se eliminan las cuentas en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-107">Possible values for when accounts are deleted on a shared PC.</span></span>
## <a name="members"></a><span data-ttu-id="5dbf8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5dbf8-108">Members</span></span>
|<span data-ttu-id="5dbf8-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5dbf8-109">Member</span></span>|<span data-ttu-id="5dbf8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5dbf8-110">Value</span></span>|<span data-ttu-id="5dbf8-111">Description</span><span class="sxs-lookup"><span data-stu-id="5dbf8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5dbf8-112">inmediato</span><span class="sxs-lookup"><span data-stu-id="5dbf8-112">immediate</span></span>|<span data-ttu-id="5dbf8-113">0</span><span class="sxs-lookup"><span data-stu-id="5dbf8-113">0</span></span>|<span data-ttu-id="5dbf8-114">Eliminar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-114">Delete immediately.</span></span>|
|<span data-ttu-id="5dbf8-115">diskSpaceThreshold</span><span class="sxs-lookup"><span data-stu-id="5dbf8-115">diskSpaceThreshold</span></span>|<span data-ttu-id="5dbf8-116">1</span><span class="sxs-lookup"><span data-stu-id="5dbf8-116">1</span></span>|<span data-ttu-id="5dbf8-117">Eliminar en el umbral de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-117">Delete at disk space threshold.</span></span>|
|<span data-ttu-id="5dbf8-118">diskSpaceThresholdOrInactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="5dbf8-118">diskSpaceThresholdOrInactiveThreshold</span></span>|<span data-ttu-id="5dbf8-119">2</span><span class="sxs-lookup"><span data-stu-id="5dbf8-119">2</span></span>|<span data-ttu-id="5dbf8-120">Eliminar en el umbral de espacio en disco o umbral inactivo.</span><span class="sxs-lookup"><span data-stu-id="5dbf8-120">Delete at disk space threshold or inactive threshold.</span></span>|





