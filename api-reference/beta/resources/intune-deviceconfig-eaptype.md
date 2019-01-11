---
title: tipo de enumeración eapType
description: Tipos de configuración de protocolo de autenticación (EAP) extensible.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 92c1cddd42f16556cbba51be7eb06a0f75c537a3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828899"
---
# <a name="eaptype-enum-type"></a><span data-ttu-id="dc3e9-103">tipo de enumeración eapType</span><span class="sxs-lookup"><span data-stu-id="dc3e9-103">eapType enum type</span></span>

> <span data-ttu-id="dc3e9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc3e9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc3e9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc3e9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dc3e9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dc3e9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dc3e9-107">Tipos de configuración de protocolo de autenticación (EAP) extensible.</span><span class="sxs-lookup"><span data-stu-id="dc3e9-107">Extensible Authentication Protocol (EAP) configuration types.</span></span>
## <a name="members"></a><span data-ttu-id="dc3e9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc3e9-108">Members</span></span>
|<span data-ttu-id="dc3e9-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="dc3e9-109">Member</span></span>|<span data-ttu-id="dc3e9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="dc3e9-110">Value</span></span>|<span data-ttu-id="dc3e9-111">Description</span><span class="sxs-lookup"><span data-stu-id="dc3e9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dc3e9-112">eapTls</span><span class="sxs-lookup"><span data-stu-id="dc3e9-112">eapTls</span></span>|<span data-ttu-id="dc3e9-113">13</span><span class="sxs-lookup"><span data-stu-id="dc3e9-113">13</span></span>|<span data-ttu-id="dc3e9-114">EAP-Transport Layer Security (EAP-TLS).</span><span class="sxs-lookup"><span data-stu-id="dc3e9-114">EAP-Transport Layer Security (EAP-TLS).</span></span>|
|<span data-ttu-id="dc3e9-115">salto</span><span class="sxs-lookup"><span data-stu-id="dc3e9-115">leap</span></span>|<span data-ttu-id="dc3e9-116">17</span><span class="sxs-lookup"><span data-stu-id="dc3e9-116">17</span></span>|<span data-ttu-id="dc3e9-117">Protocolo de autenticación Extensible ligero (LEAP).</span><span class="sxs-lookup"><span data-stu-id="dc3e9-117">Lightweight Extensible Authentication Protocol (LEAP).</span></span>|
|<span data-ttu-id="dc3e9-118">eapSim</span><span class="sxs-lookup"><span data-stu-id="dc3e9-118">eapSim</span></span>|<span data-ttu-id="dc3e9-119">18</span><span class="sxs-lookup"><span data-stu-id="dc3e9-119">18</span></span>|<span data-ttu-id="dc3e9-120">EAP para el módulo de identidad de suscriptor GSM (EAP-SIM).</span><span class="sxs-lookup"><span data-stu-id="dc3e9-120">EAP for GSM Subscriber Identity Module (EAP-SIM).</span></span>|
|<span data-ttu-id="dc3e9-121">eapTtls</span><span class="sxs-lookup"><span data-stu-id="dc3e9-121">eapTtls</span></span>|<span data-ttu-id="dc3e9-122">21</span><span class="sxs-lookup"><span data-stu-id="dc3e9-122">21</span></span>|<span data-ttu-id="dc3e9-123">Seguridad de la capa de transporte de túnel EAP (EAP-TTLS).</span><span class="sxs-lookup"><span data-stu-id="dc3e9-123">EAP-Tunneled Transport Layer Security (EAP-TTLS).</span></span>|
|<span data-ttu-id="dc3e9-124">PEAP</span><span class="sxs-lookup"><span data-stu-id="dc3e9-124">peap</span></span>|<span data-ttu-id="dc3e9-125">25</span><span class="sxs-lookup"><span data-stu-id="dc3e9-125">25</span></span>|<span data-ttu-id="dc3e9-126">Protegido el protocolo de autenticación Extensible (PEAP).</span><span class="sxs-lookup"><span data-stu-id="dc3e9-126">Protected Extensible Authentication Protocol (PEAP).</span></span>|
|<span data-ttu-id="dc3e9-127">eapFast</span><span class="sxs-lookup"><span data-stu-id="dc3e9-127">eapFast</span></span>|<span data-ttu-id="dc3e9-128">43</span><span class="sxs-lookup"><span data-stu-id="dc3e9-128">43</span></span>|<span data-ttu-id="dc3e9-129">Autenticación EAP Flexible mediante túnel seguro (EAP-FAST).</span><span class="sxs-lookup"><span data-stu-id="dc3e9-129">EAP-Flexible Authentication via Secure Tunneling (EAP-FAST).</span></span>|





