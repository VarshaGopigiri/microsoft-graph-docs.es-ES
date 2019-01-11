---
title: tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType
description: Posibles valores de configuración de protección de credenciales.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7f59fed69647ead4ccdda0523ae80571aebcb57c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871585"
---
# <a name="deviceguardlocalsystemauthoritycredentialguardtype-enum-type"></a><span data-ttu-id="886d4-103">tipo de enumeración deviceGuardLocalSystemAuthorityCredentialGuardType</span><span class="sxs-lookup"><span data-stu-id="886d4-103">deviceGuardLocalSystemAuthorityCredentialGuardType enum type</span></span>

> <span data-ttu-id="886d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="886d4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="886d4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="886d4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="886d4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="886d4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="886d4-107">Posibles valores de configuración de protección de credenciales.</span><span class="sxs-lookup"><span data-stu-id="886d4-107">Possible values of Credential Guard settings.</span></span>
## <a name="members"></a><span data-ttu-id="886d4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="886d4-108">Members</span></span>
|<span data-ttu-id="886d4-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="886d4-109">Member</span></span>|<span data-ttu-id="886d4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="886d4-110">Value</span></span>|<span data-ttu-id="886d4-111">Description</span><span class="sxs-lookup"><span data-stu-id="886d4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="886d4-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="886d4-112">notConfigured</span></span>|<span data-ttu-id="886d4-113">0</span><span class="sxs-lookup"><span data-stu-id="886d4-113">0</span></span>|<span data-ttu-id="886d4-114">Desactiva el Guard credenciales de forma remota si ha configurado anteriormente sin bloqueo UEFI.</span><span class="sxs-lookup"><span data-stu-id="886d4-114">Turns off Credential Guard remotely if configured previously without UEFI Lock.</span></span>|
|<span data-ttu-id="886d4-115">enableWithUEFILock</span><span class="sxs-lookup"><span data-stu-id="886d4-115">enableWithUEFILock</span></span>|<span data-ttu-id="886d4-116">1</span><span class="sxs-lookup"><span data-stu-id="886d4-116">1</span></span>|<span data-ttu-id="886d4-117">Activa Guard de credenciales con bloqueo UEFI.</span><span class="sxs-lookup"><span data-stu-id="886d4-117">Turns on Credential Guard with UEFI lock.</span></span>|
|<span data-ttu-id="886d4-118">enableWithoutUEFILock</span><span class="sxs-lookup"><span data-stu-id="886d4-118">enableWithoutUEFILock</span></span>|<span data-ttu-id="886d4-119">2</span><span class="sxs-lookup"><span data-stu-id="886d4-119">2</span></span>|<span data-ttu-id="886d4-120">Sin bloqueo UEFI activa Guard de credenciales.</span><span class="sxs-lookup"><span data-stu-id="886d4-120">Turns on Credential Guard without UEFI lock.</span></span>|





