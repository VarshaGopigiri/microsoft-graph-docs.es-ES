---
title: tipo de enumeración vppTokenActionFailureReason
description: Error de acción de token de posibles tipos de razones para un programa de compra de volumen de Apple.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f488302b7fc701e8a419357ad7d6cbbb6015759b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883723"
---
# <a name="vpptokenactionfailurereason-enum-type"></a><span data-ttu-id="a17e6-103">tipo de enumeración vppTokenActionFailureReason</span><span class="sxs-lookup"><span data-stu-id="a17e6-103">vppTokenActionFailureReason enum type</span></span>

> <span data-ttu-id="a17e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a17e6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a17e6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a17e6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a17e6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a17e6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a17e6-107">Error de acción de token de posibles tipos de razones para un programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="a17e6-107">Possible types of reasons for an Apple Volume Purchase Program token action failure.</span></span>
## <a name="members"></a><span data-ttu-id="a17e6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a17e6-108">Members</span></span>
|<span data-ttu-id="a17e6-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a17e6-109">Member</span></span>|<span data-ttu-id="a17e6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a17e6-110">Value</span></span>|<span data-ttu-id="a17e6-111">Description</span><span class="sxs-lookup"><span data-stu-id="a17e6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a17e6-112">none</span><span class="sxs-lookup"><span data-stu-id="a17e6-112">none</span></span>|<span data-ttu-id="a17e6-113">0</span><span class="sxs-lookup"><span data-stu-id="a17e6-113">0</span></span>|<span data-ttu-id="a17e6-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a17e6-114">None.</span></span>|
|<span data-ttu-id="a17e6-115">appleFailure</span><span class="sxs-lookup"><span data-stu-id="a17e6-115">appleFailure</span></span>|<span data-ttu-id="a17e6-116">1</span><span class="sxs-lookup"><span data-stu-id="a17e6-116">1</span></span>|<span data-ttu-id="a17e6-117">Se ha producido un error en el servicio de Apple.</span><span class="sxs-lookup"><span data-stu-id="a17e6-117">There was an error on Apple's service.</span></span>|
|<span data-ttu-id="a17e6-118">Error interno</span><span class="sxs-lookup"><span data-stu-id="a17e6-118">internalError</span></span>|<span data-ttu-id="a17e6-119">2</span><span class="sxs-lookup"><span data-stu-id="a17e6-119">2</span></span>|<span data-ttu-id="a17e6-120">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="a17e6-120">There was an internal error.</span></span>|
|<span data-ttu-id="a17e6-121">expiredVppToken</span><span class="sxs-lookup"><span data-stu-id="a17e6-121">expiredVppToken</span></span>|<span data-ttu-id="a17e6-122">3</span><span class="sxs-lookup"><span data-stu-id="a17e6-122">3</span></span>|<span data-ttu-id="a17e6-123">Se ha producido un error debido a que el token del programa de compra de volumen de Apple ha caducado.</span><span class="sxs-lookup"><span data-stu-id="a17e6-123">There was an error because the Apple Volume Purchase Program token was expired.</span></span>|
|<span data-ttu-id="a17e6-124">expiredApplePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="a17e6-124">expiredApplePushNotificationCertificate</span></span>|<span data-ttu-id="a17e6-125">4</span><span class="sxs-lookup"><span data-stu-id="a17e6-125">4</span></span>|<span data-ttu-id="a17e6-126">Se ha producido un error debido a que el certificado de la notificación de inserción de Apple volumen compra programa caducado.</span><span class="sxs-lookup"><span data-stu-id="a17e6-126">There was an error because the Apple Volume Purchase Program Push Notification certificate expired.</span></span>|





