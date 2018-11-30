---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
ms.openlocfilehash: 969c7d6576c613f5214bfc3b8a5a1ad36722f0df
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089000"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a><span data-ttu-id="4f375-103">tipo de enumeración localSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="4f375-103">localSecurityOptionsMinimumSessionSecurity enum type</span></span>

> <span data-ttu-id="4f375-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4f375-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4f375-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4f375-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4f375-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4f375-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4f375-107">Valores posibles para LocalSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="4f375-107">Possible values for LocalSecurityOptionsMinimumSessionSecurity</span></span>
## <a name="members"></a><span data-ttu-id="4f375-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f375-108">Members</span></span>
|<span data-ttu-id="4f375-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="4f375-109">Member</span></span>|<span data-ttu-id="4f375-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4f375-110">Value</span></span>|<span data-ttu-id="4f375-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f375-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4f375-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="4f375-112">none</span></span>|<span data-ttu-id="4f375-113">0</span><span class="sxs-lookup"><span data-stu-id="4f375-113">0</span></span>|<span data-ttu-id="4f375-114">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="4f375-114">Send LM & NTLM responses</span></span>|
|<span data-ttu-id="4f375-115">requireNtmlV2SessionSecurity</span><span class="sxs-lookup"><span data-stu-id="4f375-115">requireNtmlV2SessionSecurity</span></span>|<span data-ttu-id="4f375-116">1</span><span class="sxs-lookup"><span data-stu-id="4f375-116">1</span></span>|<span data-ttu-id="4f375-117">Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar</span><span class="sxs-lookup"><span data-stu-id="4f375-117">Send LM & NTLM-use NTLMv2 session security if negotiated</span></span>|
|<span data-ttu-id="4f375-118">require128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="4f375-118">require128BitEncryption</span></span>|<span data-ttu-id="4f375-119">2</span><span class="sxs-lookup"><span data-stu-id="4f375-119">2</span></span>|<span data-ttu-id="4f375-120">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="4f375-120">Send LM & NTLM responses only</span></span>|
|<span data-ttu-id="4f375-121">ntlmV2And128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="4f375-121">ntlmV2And128BitEncryption</span></span>|<span data-ttu-id="4f375-122">3</span><span class="sxs-lookup"><span data-stu-id="4f375-122">3</span></span>|<span data-ttu-id="4f375-123">Enviar respuestas de LM & NTLMv2</span><span class="sxs-lookup"><span data-stu-id="4f375-123">Send LM & NTLMv2 responses only</span></span>|





