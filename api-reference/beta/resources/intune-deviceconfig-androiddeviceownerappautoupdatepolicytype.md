---
title: tipo de enumeración androidDeviceOwnerAppAutoUpdatePolicyType
description: Valores posibles del propietario del dispositivo Android, para los Estados de automático de la aplicación del dispositivo actualizan la directiva.
localization_priority: Normal
ms.openlocfilehash: 721d08220553bf6acfaac0f84bf0d71725c39ba6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834121"
---
# <a name="androiddeviceownerappautoupdatepolicytype-enum-type"></a><span data-ttu-id="96a3c-103">tipo de enumeración androidDeviceOwnerAppAutoUpdatePolicyType</span><span class="sxs-lookup"><span data-stu-id="96a3c-103">androidDeviceOwnerAppAutoUpdatePolicyType enum type</span></span>

> <span data-ttu-id="96a3c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96a3c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96a3c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96a3c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="96a3c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="96a3c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="96a3c-107">Valores posibles del propietario del dispositivo Android, para los Estados de automático de la aplicación del dispositivo actualizan la directiva.</span><span class="sxs-lookup"><span data-stu-id="96a3c-107">Android Device Owner possible values for states of the device's app auto update policy.</span></span>
## <a name="members"></a><span data-ttu-id="96a3c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="96a3c-108">Members</span></span>
|<span data-ttu-id="96a3c-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="96a3c-109">Member</span></span>|<span data-ttu-id="96a3c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="96a3c-110">Value</span></span>|<span data-ttu-id="96a3c-111">Description</span><span class="sxs-lookup"><span data-stu-id="96a3c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="96a3c-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="96a3c-112">notConfigured</span></span>|<span data-ttu-id="96a3c-113">0</span><span class="sxs-lookup"><span data-stu-id="96a3c-113">0</span></span>|<span data-ttu-id="96a3c-114">No configurado; Este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="96a3c-114">Not configured; this value is ignored.</span></span>|
|<span data-ttu-id="96a3c-115">userChoice</span><span class="sxs-lookup"><span data-stu-id="96a3c-115">userChoice</span></span>|<span data-ttu-id="96a3c-116">1</span><span class="sxs-lookup"><span data-stu-id="96a3c-116">1</span></span>|<span data-ttu-id="96a3c-117">El usuario puede controlar las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="96a3c-117">The user can control auto-updates.</span></span>|
|<span data-ttu-id="96a3c-118">nunca</span><span class="sxs-lookup"><span data-stu-id="96a3c-118">never</span></span>|<span data-ttu-id="96a3c-119">2</span><span class="sxs-lookup"><span data-stu-id="96a3c-119">2</span></span>|<span data-ttu-id="96a3c-120">Aplicaciones nunca se actualizan por automático.</span><span class="sxs-lookup"><span data-stu-id="96a3c-120">Apps are never auto-updated.</span></span>|
|<span data-ttu-id="96a3c-121">wiFiOnly</span><span class="sxs-lookup"><span data-stu-id="96a3c-121">wiFiOnly</span></span>|<span data-ttu-id="96a3c-122">3</span><span class="sxs-lookup"><span data-stu-id="96a3c-122">3</span></span>|<span data-ttu-id="96a3c-123">Aplicaciones que se actualiza automáticamente a través de Wi-Fi solo están.</span><span class="sxs-lookup"><span data-stu-id="96a3c-123">Apps are auto-updated over Wi-Fi only.</span></span>|
|<span data-ttu-id="96a3c-124">siempre</span><span class="sxs-lookup"><span data-stu-id="96a3c-124">always</span></span>|<span data-ttu-id="96a3c-125">4</span><span class="sxs-lookup"><span data-stu-id="96a3c-125">4</span></span>|<span data-ttu-id="96a3c-126">Aplicaciones están actualizadas de forma automática en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="96a3c-126">Apps are auto-updated at any time.</span></span> <span data-ttu-id="96a3c-127">Es posible que se aplican los cargos de datos.</span><span class="sxs-lookup"><span data-stu-id="96a3c-127">Data charges may apply.</span></span>|





