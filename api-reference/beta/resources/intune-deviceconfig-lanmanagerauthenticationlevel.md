---
title: tipo de enumeración lanManagerAuthenticationLevel
description: Valores posibles para LanManagerAuthenticationLevel
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fd88deb7684301023a75905d12a59ce25bad750f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911997"
---
# <a name="lanmanagerauthenticationlevel-enum-type"></a><span data-ttu-id="87a43-103">tipo de enumeración lanManagerAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="87a43-103">lanManagerAuthenticationLevel enum type</span></span>

> <span data-ttu-id="87a43-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="87a43-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="87a43-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="87a43-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="87a43-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="87a43-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="87a43-107">Valores posibles para LanManagerAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="87a43-107">Possible values for LanManagerAuthenticationLevel</span></span>
## <a name="members"></a><span data-ttu-id="87a43-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="87a43-108">Members</span></span>
|<span data-ttu-id="87a43-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="87a43-109">Member</span></span>|<span data-ttu-id="87a43-110">Valor</span><span class="sxs-lookup"><span data-stu-id="87a43-110">Value</span></span>|<span data-ttu-id="87a43-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="87a43-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="87a43-112">lmAndNltm</span><span class="sxs-lookup"><span data-stu-id="87a43-112">lmAndNltm</span></span>|<span data-ttu-id="87a43-113">0</span><span class="sxs-lookup"><span data-stu-id="87a43-113">0</span></span>|<span data-ttu-id="87a43-114">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="87a43-114">Send LM & NTLM responses</span></span>|
|<span data-ttu-id="87a43-115">lmNtlmAndNtlmV2</span><span class="sxs-lookup"><span data-stu-id="87a43-115">lmNtlmAndNtlmV2</span></span>|<span data-ttu-id="87a43-116">1</span><span class="sxs-lookup"><span data-stu-id="87a43-116">1</span></span>|<span data-ttu-id="87a43-117">Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar</span><span class="sxs-lookup"><span data-stu-id="87a43-117">Send LM & NTLM-use NTLMv2 session security if negotiated</span></span>|
|<span data-ttu-id="87a43-118">lmAndNtlmOnly</span><span class="sxs-lookup"><span data-stu-id="87a43-118">lmAndNtlmOnly</span></span>|<span data-ttu-id="87a43-119">2</span><span class="sxs-lookup"><span data-stu-id="87a43-119">2</span></span>|<span data-ttu-id="87a43-120">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="87a43-120">Send LM & NTLM responses only</span></span>|
|<span data-ttu-id="87a43-121">lmAndNtlmV2</span><span class="sxs-lookup"><span data-stu-id="87a43-121">lmAndNtlmV2</span></span>|<span data-ttu-id="87a43-122">3</span><span class="sxs-lookup"><span data-stu-id="87a43-122">3</span></span>|<span data-ttu-id="87a43-123">Enviar respuestas de LM & NTLMv2</span><span class="sxs-lookup"><span data-stu-id="87a43-123">Send LM & NTLMv2 responses only</span></span>|
|<span data-ttu-id="87a43-124">lmNtlmV2AndNotLm</span><span class="sxs-lookup"><span data-stu-id="87a43-124">lmNtlmV2AndNotLm</span></span>|<span data-ttu-id="87a43-125">4</span><span class="sxs-lookup"><span data-stu-id="87a43-125">4</span></span>|<span data-ttu-id="87a43-126">Enviar respuestas de LM y NTLMv2 únicamente.</span><span class="sxs-lookup"><span data-stu-id="87a43-126">Send LM & NTLMv2 responses only.</span></span> <span data-ttu-id="87a43-127">Rechazar LM</span><span class="sxs-lookup"><span data-stu-id="87a43-127">Refuse LM</span></span>|
|<span data-ttu-id="87a43-128">lmNtlmV2AndNotLmOrNtm</span><span class="sxs-lookup"><span data-stu-id="87a43-128">lmNtlmV2AndNotLmOrNtm</span></span>|<span data-ttu-id="87a43-129">5</span><span class="sxs-lookup"><span data-stu-id="87a43-129">5</span></span>|<span data-ttu-id="87a43-130">Enviar respuestas de LM y NTLMv2 únicamente.</span><span class="sxs-lookup"><span data-stu-id="87a43-130">Send LM & NTLMv2 responses only.</span></span> <span data-ttu-id="87a43-131">Rechazar LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="87a43-131">Refuse LM & NTLM</span></span>|





