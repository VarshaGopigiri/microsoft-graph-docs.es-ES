---
title: tipo de enumeración eapFastConfiguration
description: Configuraciones disponibles para la configuración de EAP-FAST.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 65165929d388ed57f2651a0d277996e56d2f046e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954459"
---
# <a name="eapfastconfiguration-enum-type"></a><span data-ttu-id="80c4f-103">tipo de enumeración eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="80c4f-103">eapFastConfiguration enum type</span></span>

> <span data-ttu-id="80c4f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="80c4f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="80c4f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="80c4f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="80c4f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80c4f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80c4f-107">Configuraciones disponibles para la configuración de EAP-FAST.</span><span class="sxs-lookup"><span data-stu-id="80c4f-107">Available settings for EAP-FAST Configuration.</span></span>
## <a name="members"></a><span data-ttu-id="80c4f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="80c4f-108">Members</span></span>
|<span data-ttu-id="80c4f-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="80c4f-109">Member</span></span>|<span data-ttu-id="80c4f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="80c4f-110">Value</span></span>|<span data-ttu-id="80c4f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="80c4f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80c4f-112">noProtectedAccessCredential</span><span class="sxs-lookup"><span data-stu-id="80c4f-112">noProtectedAccessCredential</span></span>|<span data-ttu-id="80c4f-113">0</span><span class="sxs-lookup"><span data-stu-id="80c4f-113">0</span></span>|<span data-ttu-id="80c4f-114">Usar EAP-FAST sin credenciales de acceso protegido (PAC).</span><span class="sxs-lookup"><span data-stu-id="80c4f-114">Use EAP-FAST without Protected Access Credential (PAC).</span></span>|
|<span data-ttu-id="80c4f-115">useProtectedAccessCredential</span><span class="sxs-lookup"><span data-stu-id="80c4f-115">useProtectedAccessCredential</span></span>|<span data-ttu-id="80c4f-116">1</span><span class="sxs-lookup"><span data-stu-id="80c4f-116">1</span></span>|<span data-ttu-id="80c4f-117">Uso protegida credenciales de acceso (PAC).</span><span class="sxs-lookup"><span data-stu-id="80c4f-117">Use Protected Access Credential (PAC).</span></span>|
|<span data-ttu-id="80c4f-118">useProtectedAccessCredentialAndProvision</span><span class="sxs-lookup"><span data-stu-id="80c4f-118">useProtectedAccessCredentialAndProvision</span></span>|<span data-ttu-id="80c4f-119">2</span><span class="sxs-lookup"><span data-stu-id="80c4f-119">2</span></span>|<span data-ttu-id="80c4f-120">Uso de acceso protegido (PAC) de credenciales y aprovisionamiento PAC.</span><span class="sxs-lookup"><span data-stu-id="80c4f-120">Use Protected Access Credential (PAC) and Provision PAC.</span></span>|
|<span data-ttu-id="80c4f-121">useProtectedAccessCredentialAndProvisionAnonymously</span><span class="sxs-lookup"><span data-stu-id="80c4f-121">useProtectedAccessCredentialAndProvisionAnonymously</span></span>|<span data-ttu-id="80c4f-122">3</span><span class="sxs-lookup"><span data-stu-id="80c4f-122">3</span></span>|<span data-ttu-id="80c4f-123">Use acceso credencial protegido (PAC), PAC de aprovisionamiento y hacerlo de forma anónima.</span><span class="sxs-lookup"><span data-stu-id="80c4f-123">Use Protected Access Credential (PAC), Provision PAC, and do so anonymously.</span></span>|





