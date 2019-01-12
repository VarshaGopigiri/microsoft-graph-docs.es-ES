---
title: tipo de enumeración firewallPacketQueueingMethodType
description: Valores posibles para firewallPacketQueueingMethod
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3700df6d2eaf0dd0d2dde8a3f4a90be2e3684951
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940102"
---
# <a name="firewallpacketqueueingmethodtype-enum-type"></a><span data-ttu-id="12ed7-103">tipo de enumeración firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="12ed7-103">firewallPacketQueueingMethodType enum type</span></span>

> <span data-ttu-id="12ed7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12ed7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12ed7-105">Valores posibles para firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="12ed7-105">Possible values for firewallPacketQueueingMethod</span></span>
## <a name="members"></a><span data-ttu-id="12ed7-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="12ed7-106">Members</span></span>
|<span data-ttu-id="12ed7-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="12ed7-107">Member</span></span>|<span data-ttu-id="12ed7-108">Valor</span><span class="sxs-lookup"><span data-stu-id="12ed7-108">Value</span></span>|<span data-ttu-id="12ed7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="12ed7-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12ed7-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="12ed7-110">deviceDefault</span></span>|<span data-ttu-id="12ed7-111">0</span><span class="sxs-lookup"><span data-stu-id="12ed7-111">0</span></span>|<span data-ttu-id="12ed7-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="12ed7-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="12ed7-113">deshabilitado</span><span class="sxs-lookup"><span data-stu-id="12ed7-113">disabled</span></span>|<span data-ttu-id="12ed7-114">1</span><span class="sxs-lookup"><span data-stu-id="12ed7-114">1</span></span>|<span data-ttu-id="12ed7-115">Deshabilitar la puesta en cola de paquetes</span><span class="sxs-lookup"><span data-stu-id="12ed7-115">Disable packet queuing</span></span>|
|<span data-ttu-id="12ed7-116">queueInbound</span><span class="sxs-lookup"><span data-stu-id="12ed7-116">queueInbound</span></span>|<span data-ttu-id="12ed7-117">2</span><span class="sxs-lookup"><span data-stu-id="12ed7-117">2</span></span>|<span data-ttu-id="12ed7-118">Poner en cola los paquetes cifrados entrantes</span><span class="sxs-lookup"><span data-stu-id="12ed7-118">Queue inbound encrypted packets</span></span>|
|<span data-ttu-id="12ed7-119">queueOutbound</span><span class="sxs-lookup"><span data-stu-id="12ed7-119">queueOutbound</span></span>|<span data-ttu-id="12ed7-120">3</span><span class="sxs-lookup"><span data-stu-id="12ed7-120">3</span></span>|<span data-ttu-id="12ed7-121">Cola descifra los paquetes salientes para desvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="12ed7-121">Queue decrypted outbound packets for forwarding</span></span>|
|<span data-ttu-id="12ed7-122">queueBoth</span><span class="sxs-lookup"><span data-stu-id="12ed7-122">queueBoth</span></span>|<span data-ttu-id="12ed7-123">4</span><span class="sxs-lookup"><span data-stu-id="12ed7-123">4</span></span>|<span data-ttu-id="12ed7-124">Paquetes entrantes y salientes en cola</span><span class="sxs-lookup"><span data-stu-id="12ed7-124">Queue both inbound and outbound packets</span></span>|



