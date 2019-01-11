---
title: tipo de enumeración firewallPacketQueueingMethodType
description: Valores posibles para firewallPacketQueueingMethod
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1303287e521cf0b542047e8acaf122bc08a770a6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823222"
---
# <a name="firewallpacketqueueingmethodtype-enum-type"></a><span data-ttu-id="edf39-103">tipo de enumeración firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="edf39-103">firewallPacketQueueingMethodType enum type</span></span>

> <span data-ttu-id="edf39-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="edf39-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="edf39-105">Valores posibles para firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="edf39-105">Possible values for firewallPacketQueueingMethod</span></span>
## <a name="members"></a><span data-ttu-id="edf39-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="edf39-106">Members</span></span>
|<span data-ttu-id="edf39-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="edf39-107">Member</span></span>|<span data-ttu-id="edf39-108">Valor</span><span class="sxs-lookup"><span data-stu-id="edf39-108">Value</span></span>|<span data-ttu-id="edf39-109">Description</span><span class="sxs-lookup"><span data-stu-id="edf39-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="edf39-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="edf39-110">deviceDefault</span></span>|<span data-ttu-id="edf39-111">0</span><span class="sxs-lookup"><span data-stu-id="edf39-111">0</span></span>|<span data-ttu-id="edf39-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="edf39-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="edf39-113">deshabilitado</span><span class="sxs-lookup"><span data-stu-id="edf39-113">disabled</span></span>|<span data-ttu-id="edf39-114">1</span><span class="sxs-lookup"><span data-stu-id="edf39-114">1</span></span>|<span data-ttu-id="edf39-115">Deshabilitar la puesta en cola de paquetes</span><span class="sxs-lookup"><span data-stu-id="edf39-115">Disable packet queuing</span></span>|
|<span data-ttu-id="edf39-116">queueInbound</span><span class="sxs-lookup"><span data-stu-id="edf39-116">queueInbound</span></span>|<span data-ttu-id="edf39-117">2</span><span class="sxs-lookup"><span data-stu-id="edf39-117">2</span></span>|<span data-ttu-id="edf39-118">Poner en cola los paquetes cifrados entrantes</span><span class="sxs-lookup"><span data-stu-id="edf39-118">Queue inbound encrypted packets</span></span>|
|<span data-ttu-id="edf39-119">queueOutbound</span><span class="sxs-lookup"><span data-stu-id="edf39-119">queueOutbound</span></span>|<span data-ttu-id="edf39-120">3</span><span class="sxs-lookup"><span data-stu-id="edf39-120">3</span></span>|<span data-ttu-id="edf39-121">Cola descifra los paquetes salientes para desvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="edf39-121">Queue decrypted outbound packets for forwarding</span></span>|
|<span data-ttu-id="edf39-122">queueBoth</span><span class="sxs-lookup"><span data-stu-id="edf39-122">queueBoth</span></span>|<span data-ttu-id="edf39-123">4</span><span class="sxs-lookup"><span data-stu-id="edf39-123">4</span></span>|<span data-ttu-id="edf39-124">Paquetes entrantes y salientes en cola</span><span class="sxs-lookup"><span data-stu-id="edf39-124">Queue both inbound and outbound packets</span></span>|



