---
title: tipo de enumeración firewallPacketQueueingMethodType
description: Valores posibles para firewallPacketQueueingMethod
ms.openlocfilehash: 70643e300f1a6cc151edeae849e5ae7c5f977750
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030802"
---
# <a name="firewallpacketqueueingmethodtype-enum-type"></a><span data-ttu-id="20f1a-103">tipo de enumeración firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="20f1a-103">firewallPacketQueueingMethodType enum type</span></span>

> <span data-ttu-id="20f1a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="20f1a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="20f1a-105">Valores posibles para firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="20f1a-105">Possible values for firewallPacketQueueingMethod</span></span>
## <a name="members"></a><span data-ttu-id="20f1a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="20f1a-106">Members</span></span>
|<span data-ttu-id="20f1a-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="20f1a-107">Member</span></span>|<span data-ttu-id="20f1a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="20f1a-108">Value</span></span>|<span data-ttu-id="20f1a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="20f1a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="20f1a-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="20f1a-110">deviceDefault</span></span>|<span data-ttu-id="20f1a-111">0</span><span class="sxs-lookup"><span data-stu-id="20f1a-111">0</span></span>|<span data-ttu-id="20f1a-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="20f1a-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="20f1a-113">deshabilitado</span><span class="sxs-lookup"><span data-stu-id="20f1a-113">disabled</span></span>|<span data-ttu-id="20f1a-114">1</span><span class="sxs-lookup"><span data-stu-id="20f1a-114">1</span></span>|<span data-ttu-id="20f1a-115">Deshabilitar la puesta en cola de paquetes</span><span class="sxs-lookup"><span data-stu-id="20f1a-115">Disable packet queuing</span></span>|
|<span data-ttu-id="20f1a-116">queueInbound</span><span class="sxs-lookup"><span data-stu-id="20f1a-116">queueInbound</span></span>|<span data-ttu-id="20f1a-117">2</span><span class="sxs-lookup"><span data-stu-id="20f1a-117">2</span></span>|<span data-ttu-id="20f1a-118">Poner en cola los paquetes cifrados entrantes</span><span class="sxs-lookup"><span data-stu-id="20f1a-118">Queue inbound encrypted packets</span></span>|
|<span data-ttu-id="20f1a-119">queueOutbound</span><span class="sxs-lookup"><span data-stu-id="20f1a-119">queueOutbound</span></span>|<span data-ttu-id="20f1a-120">3</span><span class="sxs-lookup"><span data-stu-id="20f1a-120">3</span></span>|<span data-ttu-id="20f1a-121">Cola descifra los paquetes salientes para desvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="20f1a-121">Queue decrypted outbound packets for forwarding</span></span>|
|<span data-ttu-id="20f1a-122">queueBoth</span><span class="sxs-lookup"><span data-stu-id="20f1a-122">queueBoth</span></span>|<span data-ttu-id="20f1a-123">4</span><span class="sxs-lookup"><span data-stu-id="20f1a-123">4</span></span>|<span data-ttu-id="20f1a-124">Paquetes entrantes y salientes en cola</span><span class="sxs-lookup"><span data-stu-id="20f1a-124">Queue both inbound and outbound packets</span></span>|



