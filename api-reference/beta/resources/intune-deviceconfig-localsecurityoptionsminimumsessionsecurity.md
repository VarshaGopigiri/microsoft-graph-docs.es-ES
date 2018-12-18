---
title: tipo de enumeración localSecurityOptionsMinimumSessionSecurity
description: Valores posibles para LocalSecurityOptionsMinimumSessionSecurity
author: tfitzmac
ms.openlocfilehash: 5feabd9c84ec42f55bb45b952be5af834fd84498
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350641"
---
# <a name="localsecurityoptionsminimumsessionsecurity-enum-type"></a><span data-ttu-id="c1895-103">tipo de enumeración localSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="c1895-103">localSecurityOptionsMinimumSessionSecurity enum type</span></span>

> <span data-ttu-id="c1895-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c1895-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c1895-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c1895-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c1895-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c1895-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c1895-107">Valores posibles para LocalSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="c1895-107">Possible values for LocalSecurityOptionsMinimumSessionSecurity</span></span>
## <a name="members"></a><span data-ttu-id="c1895-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1895-108">Members</span></span>
|<span data-ttu-id="c1895-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="c1895-109">Member</span></span>|<span data-ttu-id="c1895-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c1895-110">Value</span></span>|<span data-ttu-id="c1895-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1895-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c1895-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="c1895-112">none</span></span>|<span data-ttu-id="c1895-113">0</span><span class="sxs-lookup"><span data-stu-id="c1895-113">0</span></span>|<span data-ttu-id="c1895-114">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="c1895-114">Send LM & NTLM responses</span></span>|
|<span data-ttu-id="c1895-115">requireNtmlV2SessionSecurity</span><span class="sxs-lookup"><span data-stu-id="c1895-115">requireNtmlV2SessionSecurity</span></span>|<span data-ttu-id="c1895-116">1</span><span class="sxs-lookup"><span data-stu-id="c1895-116">1</span></span>|<span data-ttu-id="c1895-117">Enviar la seguridad de sesión LM & NTLM de usar NTLMv2 si negociar</span><span class="sxs-lookup"><span data-stu-id="c1895-117">Send LM & NTLM-use NTLMv2 session security if negotiated</span></span>|
|<span data-ttu-id="c1895-118">require128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="c1895-118">require128BitEncryption</span></span>|<span data-ttu-id="c1895-119">2</span><span class="sxs-lookup"><span data-stu-id="c1895-119">2</span></span>|<span data-ttu-id="c1895-120">Enviar respuestas de LM y NTLM</span><span class="sxs-lookup"><span data-stu-id="c1895-120">Send LM & NTLM responses only</span></span>|
|<span data-ttu-id="c1895-121">ntlmV2And128BitEncryption</span><span class="sxs-lookup"><span data-stu-id="c1895-121">ntlmV2And128BitEncryption</span></span>|<span data-ttu-id="c1895-122">3</span><span class="sxs-lookup"><span data-stu-id="c1895-122">3</span></span>|<span data-ttu-id="c1895-123">Enviar respuestas de LM & NTLMv2</span><span class="sxs-lookup"><span data-stu-id="c1895-123">Send LM & NTLMv2 responses only</span></span>|





