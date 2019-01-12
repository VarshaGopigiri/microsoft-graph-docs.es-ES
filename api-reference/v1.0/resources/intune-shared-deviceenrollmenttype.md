---
title: tipo de enumeración deviceEnrollmentType
description: Posibles maneras de agregar un dispositivo móvil a la administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 72acbdf412ebb91269fcdc3f851ffbc204e0274b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987758"
---
# <a name="deviceenrollmenttype-enum-type"></a><span data-ttu-id="03b8e-103">tipo de enumeración deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="03b8e-103">deviceEnrollmentType enum type</span></span>

> <span data-ttu-id="03b8e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03b8e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03b8e-105">Posibles maneras de agregar un dispositivo móvil a la administración.</span><span class="sxs-lookup"><span data-stu-id="03b8e-105">Possible ways of adding a mobile device to management.</span></span>

## <a name="members"></a><span data-ttu-id="03b8e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="03b8e-106">Members</span></span>
|<span data-ttu-id="03b8e-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="03b8e-107">Member</span></span>|<span data-ttu-id="03b8e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="03b8e-108">Value</span></span>|<span data-ttu-id="03b8e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="03b8e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="03b8e-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="03b8e-110">unknown</span></span>|<span data-ttu-id="03b8e-111">0</span><span class="sxs-lookup"><span data-stu-id="03b8e-111">0</span></span>|<span data-ttu-id="03b8e-112">No se recopiló el valor predeterminado, el tipo de inscripción.</span><span class="sxs-lookup"><span data-stu-id="03b8e-112">Default value, enrollment type was not collected.</span></span>|
|<span data-ttu-id="03b8e-113">userEnrollment</span><span class="sxs-lookup"><span data-stu-id="03b8e-113">userEnrollment</span></span>|<span data-ttu-id="03b8e-114">1</span><span class="sxs-lookup"><span data-stu-id="03b8e-114">1</span></span>|<span data-ttu-id="03b8e-115">Inscripción impulsada de usuario a través del canal BYOD.</span><span class="sxs-lookup"><span data-stu-id="03b8e-115">User driven enrollment through BYOD channel.</span></span>|
|<span data-ttu-id="03b8e-116">deviceEnrollmentManager</span><span class="sxs-lookup"><span data-stu-id="03b8e-116">deviceEnrollmentManager</span></span>|<span data-ttu-id="03b8e-117">2</span><span class="sxs-lookup"><span data-stu-id="03b8e-117">2</span></span>|<span data-ttu-id="03b8e-118">Inscripción de usuario con una cuenta de administrador de inscripción de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03b8e-118">User enrollment with a device enrollment manager account.</span></span>|
|<span data-ttu-id="03b8e-119">appleBulkWithUser</span><span class="sxs-lookup"><span data-stu-id="03b8e-119">appleBulkWithUser</span></span>|<span data-ttu-id="03b8e-120">3</span><span class="sxs-lookup"><span data-stu-id="03b8e-120">3</span></span>|<span data-ttu-id="03b8e-121">Inscripción masiva de Apple con desafío de usuario (DEP, Configurador de Apple).</span><span class="sxs-lookup"><span data-stu-id="03b8e-121">Apple bulk enrollment with user challenge (DEP, Apple Configurator).</span></span>|
|<span data-ttu-id="03b8e-122">appleBulkWithoutUser</span><span class="sxs-lookup"><span data-stu-id="03b8e-122">appleBulkWithoutUser</span></span>|<span data-ttu-id="03b8e-123">4</span><span class="sxs-lookup"><span data-stu-id="03b8e-123">4</span></span>|<span data-ttu-id="03b8e-124">Inscripción masiva de Apple sin desafío de usuario (configuración DEP, Configurador de Apple, Mobile).</span><span class="sxs-lookup"><span data-stu-id="03b8e-124">Apple bulk enrollment without user challenge (DEP, Apple Configurator, Mobile Config).</span></span>|
|<span data-ttu-id="03b8e-125">windowsAzureADJoin</span><span class="sxs-lookup"><span data-stu-id="03b8e-125">windowsAzureADJoin</span></span>|<span data-ttu-id="03b8e-126">5</span><span class="sxs-lookup"><span data-stu-id="03b8e-126">5</span></span>|<span data-ttu-id="03b8e-127">Unirse Windows Azure AD de 10.</span><span class="sxs-lookup"><span data-stu-id="03b8e-127">Windows 10 Azure AD Join.</span></span>|
|<span data-ttu-id="03b8e-128">windowsBulkUserless</span><span class="sxs-lookup"><span data-stu-id="03b8e-128">windowsBulkUserless</span></span>|<span data-ttu-id="03b8e-129">6</span><span class="sxs-lookup"><span data-stu-id="03b8e-129">6</span></span>|<span data-ttu-id="03b8e-130">Inscripción de Windows 10 masiva a través de ICD con certificado.</span><span class="sxs-lookup"><span data-stu-id="03b8e-130">Windows 10 Bulk enrollment through ICD with certificate.</span></span>|
|<span data-ttu-id="03b8e-131">windowsAutoEnrollment</span><span class="sxs-lookup"><span data-stu-id="03b8e-131">windowsAutoEnrollment</span></span>|<span data-ttu-id="03b8e-132">7</span><span class="sxs-lookup"><span data-stu-id="03b8e-132">7</span></span>|<span data-ttu-id="03b8e-133">10 de Windows la inscripción automática.</span><span class="sxs-lookup"><span data-stu-id="03b8e-133">Windows 10 automatic enrollment.</span></span> <span data-ttu-id="03b8e-134">(Agregar la cuenta de trabajo)</span><span class="sxs-lookup"><span data-stu-id="03b8e-134">(Add work account)</span></span>|
|<span data-ttu-id="03b8e-135">windowsBulkAzureDomainJoin</span><span class="sxs-lookup"><span data-stu-id="03b8e-135">windowsBulkAzureDomainJoin</span></span>|<span data-ttu-id="03b8e-136">8</span><span class="sxs-lookup"><span data-stu-id="03b8e-136">8</span></span>|<span data-ttu-id="03b8e-137">Windows 10 masivo participar en Azure AD.</span><span class="sxs-lookup"><span data-stu-id="03b8e-137">Windows 10 bulk Azure AD Join.</span></span>|
|<span data-ttu-id="03b8e-138">windowsCoManagement</span><span class="sxs-lookup"><span data-stu-id="03b8e-138">windowsCoManagement</span></span>|<span data-ttu-id="03b8e-139">9</span><span class="sxs-lookup"><span data-stu-id="03b8e-139">9</span></span>|<span data-ttu-id="03b8e-140">CO-administración de 10 Windows desencadenada por piloto automático o directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="03b8e-140">Windows 10 co-management triggered by AutoPilot or Group Policy.</span></span>|



