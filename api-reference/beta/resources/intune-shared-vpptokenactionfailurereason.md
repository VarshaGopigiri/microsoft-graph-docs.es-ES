---
title: tipo de enumeración vppTokenActionFailureReason
description: Error de acción de token de posibles tipos de razones para un programa de compra de volumen de Apple.
author: tfitzmac
ms.openlocfilehash: f36b92238b097f50990bbdb2f3c3584b2ff48901
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320968"
---
# <a name="vpptokenactionfailurereason-enum-type"></a><span data-ttu-id="af35f-103">tipo de enumeración vppTokenActionFailureReason</span><span class="sxs-lookup"><span data-stu-id="af35f-103">vppTokenActionFailureReason enum type</span></span>

> <span data-ttu-id="af35f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af35f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af35f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af35f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="af35f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="af35f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="af35f-107">Error de acción de token de posibles tipos de razones para un programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="af35f-107">Possible types of reasons for an Apple Volume Purchase Program token action failure.</span></span>
## <a name="members"></a><span data-ttu-id="af35f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="af35f-108">Members</span></span>
|<span data-ttu-id="af35f-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="af35f-109">Member</span></span>|<span data-ttu-id="af35f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="af35f-110">Value</span></span>|<span data-ttu-id="af35f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="af35f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="af35f-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="af35f-112">none</span></span>|<span data-ttu-id="af35f-113">0</span><span class="sxs-lookup"><span data-stu-id="af35f-113">0</span></span>|<span data-ttu-id="af35f-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af35f-114">None.</span></span>|
|<span data-ttu-id="af35f-115">appleFailure</span><span class="sxs-lookup"><span data-stu-id="af35f-115">appleFailure</span></span>|<span data-ttu-id="af35f-116">1</span><span class="sxs-lookup"><span data-stu-id="af35f-116">1</span></span>|<span data-ttu-id="af35f-117">Se ha producido un error en el servicio de Apple.</span><span class="sxs-lookup"><span data-stu-id="af35f-117">There was an error on Apple's service.</span></span>|
|<span data-ttu-id="af35f-118">Error interno</span><span class="sxs-lookup"><span data-stu-id="af35f-118">internalError</span></span>|<span data-ttu-id="af35f-119">2</span><span class="sxs-lookup"><span data-stu-id="af35f-119">2</span></span>|<span data-ttu-id="af35f-120">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="af35f-120">There was an internal error.</span></span>|
|<span data-ttu-id="af35f-121">expiredVppToken</span><span class="sxs-lookup"><span data-stu-id="af35f-121">expiredVppToken</span></span>|<span data-ttu-id="af35f-122">3</span><span class="sxs-lookup"><span data-stu-id="af35f-122">3</span></span>|<span data-ttu-id="af35f-123">Se ha producido un error debido a que el token del programa de compra de volumen de Apple ha caducado.</span><span class="sxs-lookup"><span data-stu-id="af35f-123">There was an error because the Apple Volume Purchase Program token was expired.</span></span>|
|<span data-ttu-id="af35f-124">expiredApplePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="af35f-124">expiredApplePushNotificationCertificate</span></span>|<span data-ttu-id="af35f-125">4</span><span class="sxs-lookup"><span data-stu-id="af35f-125">4</span></span>|<span data-ttu-id="af35f-126">Se ha producido un error debido a que el certificado de la notificación de inserción de Apple volumen compra programa caducado.</span><span class="sxs-lookup"><span data-stu-id="af35f-126">There was an error because the Apple Volume Purchase Program Push Notification certificate expired.</span></span>|





