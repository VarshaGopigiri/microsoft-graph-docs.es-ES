---
title: tipo de enumeración localSecurityOptionsAdministratorElevationPromptBehaviorType
description: Valores posibles para LocalSecurityOptionsAdministratorElevationPromptBehavior
author: tfitzmac
ms.openlocfilehash: 620e2030433bd0f7a72263fa16907ec18c86f5f8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308753"
---
# <a name="localsecurityoptionsadministratorelevationpromptbehaviortype-enum-type"></a><span data-ttu-id="5ebfa-103">tipo de enumeración localSecurityOptionsAdministratorElevationPromptBehaviorType</span><span class="sxs-lookup"><span data-stu-id="5ebfa-103">localSecurityOptionsAdministratorElevationPromptBehaviorType enum type</span></span>

> <span data-ttu-id="5ebfa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ebfa-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5ebfa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5ebfa-107">Valores posibles para LocalSecurityOptionsAdministratorElevationPromptBehavior</span><span class="sxs-lookup"><span data-stu-id="5ebfa-107">Possible values for LocalSecurityOptionsAdministratorElevationPromptBehavior</span></span>
## <a name="members"></a><span data-ttu-id="5ebfa-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ebfa-108">Members</span></span>
|<span data-ttu-id="5ebfa-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5ebfa-109">Member</span></span>|<span data-ttu-id="5ebfa-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebfa-110">Value</span></span>|<span data-ttu-id="5ebfa-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ebfa-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5ebfa-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="5ebfa-112">notConfigured</span></span>|<span data-ttu-id="5ebfa-113">0</span><span class="sxs-lookup"><span data-stu-id="5ebfa-113">0</span></span>|<span data-ttu-id="5ebfa-114">No configurado</span><span class="sxs-lookup"><span data-stu-id="5ebfa-114">Not Configured</span></span>|
|<span data-ttu-id="5ebfa-115">elevateWithoutPrompting</span><span class="sxs-lookup"><span data-stu-id="5ebfa-115">elevateWithoutPrompting</span></span>|<span data-ttu-id="5ebfa-116">1</span><span class="sxs-lookup"><span data-stu-id="5ebfa-116">1</span></span>|<span data-ttu-id="5ebfa-117">Elevar sin preguntar.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-117">Elevate without prompting.</span></span>|
|<span data-ttu-id="5ebfa-118">promptForCredentialsOnTheSecureDesktop</span><span class="sxs-lookup"><span data-stu-id="5ebfa-118">promptForCredentialsOnTheSecureDesktop</span></span>|<span data-ttu-id="5ebfa-119">2</span><span class="sxs-lookup"><span data-stu-id="5ebfa-119">2</span></span>|<span data-ttu-id="5ebfa-120">Símbolo del sistema para las credenciales en el escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="5ebfa-120">Prompt for credentials on the secure desktop</span></span>|
|<span data-ttu-id="5ebfa-121">promptForConsentOnTheSecureDesktop</span><span class="sxs-lookup"><span data-stu-id="5ebfa-121">promptForConsentOnTheSecureDesktop</span></span>|<span data-ttu-id="5ebfa-122">3</span><span class="sxs-lookup"><span data-stu-id="5ebfa-122">3</span></span>|<span data-ttu-id="5ebfa-123">Pedir consentimiento en el escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="5ebfa-123">Prompt for consent on the secure desktop</span></span>|
|<span data-ttu-id="5ebfa-124">promptForCredentials</span><span class="sxs-lookup"><span data-stu-id="5ebfa-124">promptForCredentials</span></span>|<span data-ttu-id="5ebfa-125">4</span><span class="sxs-lookup"><span data-stu-id="5ebfa-125">4</span></span>|<span data-ttu-id="5ebfa-126">Solicitud de credenciales</span><span class="sxs-lookup"><span data-stu-id="5ebfa-126">Prompt for credentials</span></span>|
|<span data-ttu-id="5ebfa-127">promptForConsent</span><span class="sxs-lookup"><span data-stu-id="5ebfa-127">promptForConsent</span></span>|<span data-ttu-id="5ebfa-128">5</span><span class="sxs-lookup"><span data-stu-id="5ebfa-128">5</span></span>|<span data-ttu-id="5ebfa-129">Solicitud de consentimiento</span><span class="sxs-lookup"><span data-stu-id="5ebfa-129">Prompt for consent</span></span>|
|<span data-ttu-id="5ebfa-130">promptForConsentForNonWindowsBinaries</span><span class="sxs-lookup"><span data-stu-id="5ebfa-130">promptForConsentForNonWindowsBinaries</span></span>|<span data-ttu-id="5ebfa-131">6</span><span class="sxs-lookup"><span data-stu-id="5ebfa-131">6</span></span>|<span data-ttu-id="5ebfa-132">Pedir consentimiento para archivos binarios que no son de Windows</span><span class="sxs-lookup"><span data-stu-id="5ebfa-132">Prompt for consent for non-Windows binaries</span></span>|





