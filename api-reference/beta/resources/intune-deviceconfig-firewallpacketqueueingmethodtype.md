---
title: tipo de enumeración firewallPacketQueueingMethodType
description: Valores posibles para firewallPacketQueueingMethod
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9538db02afc108573338556c8899495ca9c1f26c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957798"
---
# <a name="firewallpacketqueueingmethodtype-enum-type"></a><span data-ttu-id="7c853-103">tipo de enumeración firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="7c853-103">firewallPacketQueueingMethodType enum type</span></span>

> <span data-ttu-id="7c853-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c853-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c853-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c853-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7c853-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7c853-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7c853-107">Valores posibles para firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="7c853-107">Possible values for firewallPacketQueueingMethod</span></span>
## <a name="members"></a><span data-ttu-id="7c853-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c853-108">Members</span></span>
|<span data-ttu-id="7c853-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="7c853-109">Member</span></span>|<span data-ttu-id="7c853-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7c853-110">Value</span></span>|<span data-ttu-id="7c853-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c853-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7c853-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="7c853-112">deviceDefault</span></span>|<span data-ttu-id="7c853-113">0</span><span class="sxs-lookup"><span data-stu-id="7c853-113">0</span></span>|<span data-ttu-id="7c853-114">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="7c853-114">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="7c853-115">deshabilitado</span><span class="sxs-lookup"><span data-stu-id="7c853-115">disabled</span></span>|<span data-ttu-id="7c853-116">1</span><span class="sxs-lookup"><span data-stu-id="7c853-116">1</span></span>|<span data-ttu-id="7c853-117">Deshabilitar la puesta en cola de paquetes</span><span class="sxs-lookup"><span data-stu-id="7c853-117">Disable packet queuing</span></span>|
|<span data-ttu-id="7c853-118">queueInbound</span><span class="sxs-lookup"><span data-stu-id="7c853-118">queueInbound</span></span>|<span data-ttu-id="7c853-119">2</span><span class="sxs-lookup"><span data-stu-id="7c853-119">2</span></span>|<span data-ttu-id="7c853-120">Poner en cola los paquetes cifrados entrantes</span><span class="sxs-lookup"><span data-stu-id="7c853-120">Queue inbound encrypted packets</span></span>|
|<span data-ttu-id="7c853-121">queueOutbound</span><span class="sxs-lookup"><span data-stu-id="7c853-121">queueOutbound</span></span>|<span data-ttu-id="7c853-122">3</span><span class="sxs-lookup"><span data-stu-id="7c853-122">3</span></span>|<span data-ttu-id="7c853-123">Cola descifra los paquetes salientes para desvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="7c853-123">Queue decrypted outbound packets for forwarding</span></span>|
|<span data-ttu-id="7c853-124">queueBoth</span><span class="sxs-lookup"><span data-stu-id="7c853-124">queueBoth</span></span>|<span data-ttu-id="7c853-125">4</span><span class="sxs-lookup"><span data-stu-id="7c853-125">4</span></span>|<span data-ttu-id="7c853-126">Paquetes entrantes y salientes en cola</span><span class="sxs-lookup"><span data-stu-id="7c853-126">Queue both inbound and outbound packets</span></span>|





