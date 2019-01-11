---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: fb6912e7d3bba42364849165cceb28050ddacfae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833239"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a><span data-ttu-id="cf751-103">tipo de enumeración localSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="cf751-103">localSecurityOptionsMinimumSessionSecurity enum type</span></span>

> <span data-ttu-id="cf751-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cf751-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cf751-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cf751-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cf751-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf751-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf751-107">Valores posibles para LocalSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="cf751-107">Possible values for LocalSecurityOptionsMinimumSessionSecurity</span></span>
## <a name="members"></a><span data-ttu-id="cf751-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf751-108">Members</span></span>
|<span data-ttu-id="cf751-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="cf751-109">Member</span></span>|<span data-ttu-id="cf751-110">Valor</span><span class="sxs-lookup"><span data-stu-id="cf751-110">Value</span></span>|<span data-ttu-id="cf751-111">Description</span><span class="sxs-lookup"><span data-stu-id="cf751-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf751-112">none</span><span class="sxs-lookup"><span data-stu-id="cf751-112">none</span></span>|<span data-ttu-id="cf751-113">0</span><span class="sxs-lookup"><span data-stu-id="cf751-113">0</span></span>|<span data-ttu-id="cf751-114">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="cf751-114">Send LM & NTLM responses</span></span>|
|<span data-ttu-id="cf751-115">requireNtmlV2SessionSecurity</span><span class="sxs-lookup"><span data-stu-id="cf751-115">requireNtmlV2SessionSecurity</span></span>|<span data-ttu-id="cf751-116">1</span><span class="sxs-lookup"><span data-stu-id="cf751-116">1</span></span>|<span data-ttu-id="cf751-117">Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar</span><span class="sxs-lookup"><span data-stu-id="cf751-117">Send LM & NTLM-use NTLMv2 session security if negotiated</span></span>|
|<span data-ttu-id="cf751-118">require128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="cf751-118">require128BitEncryption</span></span>|<span data-ttu-id="cf751-119">2</span><span class="sxs-lookup"><span data-stu-id="cf751-119">2</span></span>|<span data-ttu-id="cf751-120">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="cf751-120">Send LM & NTLM responses only</span></span>|
|<span data-ttu-id="cf751-121">ntlmV2And128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="cf751-121">ntlmV2And128BitEncryption</span></span>|<span data-ttu-id="cf751-122">3</span><span class="sxs-lookup"><span data-stu-id="cf751-122">3</span></span>|<span data-ttu-id="cf751-123">Enviar respuestas de LM & NTLMv2</span><span class="sxs-lookup"><span data-stu-id="cf751-123">Send LM & NTLMv2 responses only</span></span>|





