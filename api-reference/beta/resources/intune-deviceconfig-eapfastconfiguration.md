---
title: tipo de enumeración eapFastConfiguration
description: Configuraciones disponibles para la configuración de EAP-FAST.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 499d6595980bcb6bca1ea93687399e8988a3bed7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811091"
---
# <a name="eapfastconfiguration-enum-type"></a><span data-ttu-id="227ad-103">tipo de enumeración eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="227ad-103">eapFastConfiguration enum type</span></span>

> <span data-ttu-id="227ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="227ad-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="227ad-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="227ad-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="227ad-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="227ad-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="227ad-107">Configuraciones disponibles para la configuración de EAP-FAST.</span><span class="sxs-lookup"><span data-stu-id="227ad-107">Available settings for EAP-FAST Configuration.</span></span>
## <a name="members"></a><span data-ttu-id="227ad-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="227ad-108">Members</span></span>
|<span data-ttu-id="227ad-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="227ad-109">Member</span></span>|<span data-ttu-id="227ad-110">Valor</span><span class="sxs-lookup"><span data-stu-id="227ad-110">Value</span></span>|<span data-ttu-id="227ad-111">Description</span><span class="sxs-lookup"><span data-stu-id="227ad-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="227ad-112">noProtectedAccessCredential</span><span class="sxs-lookup"><span data-stu-id="227ad-112">noProtectedAccessCredential</span></span>|<span data-ttu-id="227ad-113">0</span><span class="sxs-lookup"><span data-stu-id="227ad-113">0</span></span>|<span data-ttu-id="227ad-114">Usar EAP-FAST sin credenciales de acceso protegido (PAC).</span><span class="sxs-lookup"><span data-stu-id="227ad-114">Use EAP-FAST without Protected Access Credential (PAC).</span></span>|
|<span data-ttu-id="227ad-115">useProtectedAccessCredential</span><span class="sxs-lookup"><span data-stu-id="227ad-115">useProtectedAccessCredential</span></span>|<span data-ttu-id="227ad-116">1</span><span class="sxs-lookup"><span data-stu-id="227ad-116">1</span></span>|<span data-ttu-id="227ad-117">Uso protegida credenciales de acceso (PAC).</span><span class="sxs-lookup"><span data-stu-id="227ad-117">Use Protected Access Credential (PAC).</span></span>|
|<span data-ttu-id="227ad-118">useProtectedAccessCredentialAndProvision</span><span class="sxs-lookup"><span data-stu-id="227ad-118">useProtectedAccessCredentialAndProvision</span></span>|<span data-ttu-id="227ad-119">2</span><span class="sxs-lookup"><span data-stu-id="227ad-119">2</span></span>|<span data-ttu-id="227ad-120">Uso de acceso protegido (PAC) de credenciales y aprovisionamiento PAC.</span><span class="sxs-lookup"><span data-stu-id="227ad-120">Use Protected Access Credential (PAC) and Provision PAC.</span></span>|
|<span data-ttu-id="227ad-121">useProtectedAccessCredentialAndProvisionAnonymously</span><span class="sxs-lookup"><span data-stu-id="227ad-121">useProtectedAccessCredentialAndProvisionAnonymously</span></span>|<span data-ttu-id="227ad-122">3</span><span class="sxs-lookup"><span data-stu-id="227ad-122">3</span></span>|<span data-ttu-id="227ad-123">Use acceso credencial protegido (PAC), PAC de aprovisionamiento y hacerlo de forma anónima.</span><span class="sxs-lookup"><span data-stu-id="227ad-123">Use Protected Access Credential (PAC), Provision PAC, and do so anonymously.</span></span>|





