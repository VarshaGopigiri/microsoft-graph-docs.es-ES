---
title: tipo de enumeración eapType
description: Tipos de configuración de protocolo de autenticación (EAP) extensible.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1e894e10356711fd4522ff816750e986d8b8e57d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957812"
---
# <a name="eaptype-enum-type"></a><span data-ttu-id="b2a94-103">tipo de enumeración eapType</span><span class="sxs-lookup"><span data-stu-id="b2a94-103">eapType enum type</span></span>

> <span data-ttu-id="b2a94-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2a94-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2a94-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2a94-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b2a94-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2a94-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2a94-107">Tipos de configuración de protocolo de autenticación (EAP) extensible.</span><span class="sxs-lookup"><span data-stu-id="b2a94-107">Extensible Authentication Protocol (EAP) configuration types.</span></span>
## <a name="members"></a><span data-ttu-id="b2a94-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2a94-108">Members</span></span>
|<span data-ttu-id="b2a94-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b2a94-109">Member</span></span>|<span data-ttu-id="b2a94-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b2a94-110">Value</span></span>|<span data-ttu-id="b2a94-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2a94-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2a94-112">eapTls</span><span class="sxs-lookup"><span data-stu-id="b2a94-112">eapTls</span></span>|<span data-ttu-id="b2a94-113">13</span><span class="sxs-lookup"><span data-stu-id="b2a94-113">13</span></span>|<span data-ttu-id="b2a94-114">EAP-Transport Layer Security (EAP-TLS).</span><span class="sxs-lookup"><span data-stu-id="b2a94-114">EAP-Transport Layer Security (EAP-TLS).</span></span>|
|<span data-ttu-id="b2a94-115">salto</span><span class="sxs-lookup"><span data-stu-id="b2a94-115">leap</span></span>|<span data-ttu-id="b2a94-116">17</span><span class="sxs-lookup"><span data-stu-id="b2a94-116">17</span></span>|<span data-ttu-id="b2a94-117">Protocolo de autenticación Extensible ligero (LEAP).</span><span class="sxs-lookup"><span data-stu-id="b2a94-117">Lightweight Extensible Authentication Protocol (LEAP).</span></span>|
|<span data-ttu-id="b2a94-118">eapSim</span><span class="sxs-lookup"><span data-stu-id="b2a94-118">eapSim</span></span>|<span data-ttu-id="b2a94-119">18</span><span class="sxs-lookup"><span data-stu-id="b2a94-119">18</span></span>|<span data-ttu-id="b2a94-120">EAP para el módulo de identidad de suscriptor GSM (EAP-SIM).</span><span class="sxs-lookup"><span data-stu-id="b2a94-120">EAP for GSM Subscriber Identity Module (EAP-SIM).</span></span>|
|<span data-ttu-id="b2a94-121">eapTtls</span><span class="sxs-lookup"><span data-stu-id="b2a94-121">eapTtls</span></span>|<span data-ttu-id="b2a94-122">21</span><span class="sxs-lookup"><span data-stu-id="b2a94-122">21</span></span>|<span data-ttu-id="b2a94-123">Seguridad de la capa de transporte de túnel EAP (EAP-TTLS).</span><span class="sxs-lookup"><span data-stu-id="b2a94-123">EAP-Tunneled Transport Layer Security (EAP-TTLS).</span></span>|
|<span data-ttu-id="b2a94-124">PEAP</span><span class="sxs-lookup"><span data-stu-id="b2a94-124">peap</span></span>|<span data-ttu-id="b2a94-125">25</span><span class="sxs-lookup"><span data-stu-id="b2a94-125">25</span></span>|<span data-ttu-id="b2a94-126">Protegido el protocolo de autenticación Extensible (PEAP).</span><span class="sxs-lookup"><span data-stu-id="b2a94-126">Protected Extensible Authentication Protocol (PEAP).</span></span>|
|<span data-ttu-id="b2a94-127">eapFast</span><span class="sxs-lookup"><span data-stu-id="b2a94-127">eapFast</span></span>|<span data-ttu-id="b2a94-128">43</span><span class="sxs-lookup"><span data-stu-id="b2a94-128">43</span></span>|<span data-ttu-id="b2a94-129">Autenticación EAP Flexible mediante túnel seguro (EAP-FAST).</span><span class="sxs-lookup"><span data-stu-id="b2a94-129">EAP-Flexible Authentication via Secure Tunneling (EAP-FAST).</span></span>|





