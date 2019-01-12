---
title: tipo de enumeración windowsPrivacyDataAccessLevel
description: Determinar el nivel de acceso a la categoría de datos de privacidad de Windows específica.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 64db5eb78708a0cfa835bd695ba01b2c267fc4fd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959320"
---
# <a name="windowsprivacydataaccesslevel-enum-type"></a><span data-ttu-id="2db0f-103">tipo de enumeración windowsPrivacyDataAccessLevel</span><span class="sxs-lookup"><span data-stu-id="2db0f-103">windowsPrivacyDataAccessLevel enum type</span></span>

> <span data-ttu-id="2db0f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2db0f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2db0f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2db0f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2db0f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2db0f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2db0f-107">Determinar el nivel de acceso a la categoría de datos de privacidad de Windows específica.</span><span class="sxs-lookup"><span data-stu-id="2db0f-107">Determine the access level to specific Windows privacy data category.</span></span>
## <a name="members"></a><span data-ttu-id="2db0f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2db0f-108">Members</span></span>
|<span data-ttu-id="2db0f-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="2db0f-109">Member</span></span>|<span data-ttu-id="2db0f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2db0f-110">Value</span></span>|<span data-ttu-id="2db0f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2db0f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2db0f-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="2db0f-112">notConfigured</span></span>|<span data-ttu-id="2db0f-113">0</span><span class="sxs-lookup"><span data-stu-id="2db0f-113">0</span></span>|<span data-ttu-id="2db0f-114">Ningún nivel de acceso no especificado, del color.</span><span class="sxs-lookup"><span data-stu-id="2db0f-114">No access level specified, no intents.</span></span> <span data-ttu-id="2db0f-115">Es posible que se comportan de dispositivo ya sea como en UserInControl o ForceAllow.</span><span class="sxs-lookup"><span data-stu-id="2db0f-115">Device may behave either as in UserInControl or ForceAllow.</span></span> <span data-ttu-id="2db0f-116">Es posible que dependen de los datos de privacidad sido tener acceso a las versiones de Windows y otros factores.</span><span class="sxs-lookup"><span data-stu-id="2db0f-116">It may depend on the privacy data been accessed, Windows versions and other factors.</span></span>|
|<span data-ttu-id="2db0f-117">forceAllow</span><span class="sxs-lookup"><span data-stu-id="2db0f-117">forceAllow</span></span>|<span data-ttu-id="2db0f-118">1</span><span class="sxs-lookup"><span data-stu-id="2db0f-118">1</span></span>|<span data-ttu-id="2db0f-119">Aplicaciones podrán tener acceso a los datos de privacidad especificado.</span><span class="sxs-lookup"><span data-stu-id="2db0f-119">Apps will be allowed to access the specified privacy data.</span></span>|
|<span data-ttu-id="2db0f-120">forceDeny</span><span class="sxs-lookup"><span data-stu-id="2db0f-120">forceDeny</span></span>|<span data-ttu-id="2db0f-121">2</span><span class="sxs-lookup"><span data-stu-id="2db0f-121">2</span></span>|<span data-ttu-id="2db0f-122">Se denegarán aplicaciones para tener acceso a datos de privacidad especificado.</span><span class="sxs-lookup"><span data-stu-id="2db0f-122">Apps will be denied to access specified privacy data.</span></span>|
|<span data-ttu-id="2db0f-123">userInControl</span><span class="sxs-lookup"><span data-stu-id="2db0f-123">userInControl</span></span>|<span data-ttu-id="2db0f-124">3</span><span class="sxs-lookup"><span data-stu-id="2db0f-124">3</span></span>|<span data-ttu-id="2db0f-125">Se pedirá a los usuarios cuando aplicaciones intenta obtener acceso a datos de privacidad especificado.</span><span class="sxs-lookup"><span data-stu-id="2db0f-125">Users will be prompted when apps try to access specified privacy data.</span></span>|





