---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 822c996d788fd5edb5c92f876c725b771b051c15
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952485"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a><span data-ttu-id="04a94-103">tipo de enumeración localSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="04a94-103">localSecurityOptionsMinimumSessionSecurity enum type</span></span>

> <span data-ttu-id="04a94-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04a94-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04a94-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04a94-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="04a94-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04a94-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04a94-107">Valores posibles para LocalSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="04a94-107">Possible values for LocalSecurityOptionsMinimumSessionSecurity</span></span>
## <a name="members"></a><span data-ttu-id="04a94-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="04a94-108">Members</span></span>
|<span data-ttu-id="04a94-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="04a94-109">Member</span></span>|<span data-ttu-id="04a94-110">Valor</span><span class="sxs-lookup"><span data-stu-id="04a94-110">Value</span></span>|<span data-ttu-id="04a94-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="04a94-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04a94-112">none</span><span class="sxs-lookup"><span data-stu-id="04a94-112">none</span></span>|<span data-ttu-id="04a94-113">0</span><span class="sxs-lookup"><span data-stu-id="04a94-113">0</span></span>|<span data-ttu-id="04a94-114">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="04a94-114">Send LM & NTLM responses</span></span>|
|<span data-ttu-id="04a94-115">requireNtmlV2SessionSecurity</span><span class="sxs-lookup"><span data-stu-id="04a94-115">requireNtmlV2SessionSecurity</span></span>|<span data-ttu-id="04a94-116">1</span><span class="sxs-lookup"><span data-stu-id="04a94-116">1</span></span>|<span data-ttu-id="04a94-117">Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar</span><span class="sxs-lookup"><span data-stu-id="04a94-117">Send LM & NTLM-use NTLMv2 session security if negotiated</span></span>|
|<span data-ttu-id="04a94-118">require128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="04a94-118">require128BitEncryption</span></span>|<span data-ttu-id="04a94-119">2</span><span class="sxs-lookup"><span data-stu-id="04a94-119">2</span></span>|<span data-ttu-id="04a94-120">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="04a94-120">Send LM & NTLM responses only</span></span>|
|<span data-ttu-id="04a94-121">ntlmV2And128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="04a94-121">ntlmV2And128BitEncryption</span></span>|<span data-ttu-id="04a94-122">3</span><span class="sxs-lookup"><span data-stu-id="04a94-122">3</span></span>|<span data-ttu-id="04a94-123">Enviar respuestas de LM & NTLMv2</span><span class="sxs-lookup"><span data-stu-id="04a94-123">Send LM & NTLMv2 responses only</span></span>|





