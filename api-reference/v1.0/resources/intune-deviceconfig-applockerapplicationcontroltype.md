---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 241387f34a64b4b58d974fc21e2aa5d3af696736
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871984"
---
# <a name="applockerapplicationcontroltype-enum-type"></a><span data-ttu-id="43ff5-103">tipo de enumeración appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="43ff5-103">appLockerApplicationControlType enum type</span></span>

> <span data-ttu-id="43ff5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="43ff5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="43ff5-105">Posibles valores de tipos de Control de aplicación de AppLocker</span><span class="sxs-lookup"><span data-stu-id="43ff5-105">Possible values of AppLocker Application Control Types</span></span>
## <a name="members"></a><span data-ttu-id="43ff5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="43ff5-106">Members</span></span>
|<span data-ttu-id="43ff5-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="43ff5-107">Member</span></span>|<span data-ttu-id="43ff5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="43ff5-108">Value</span></span>|<span data-ttu-id="43ff5-109">Description</span><span class="sxs-lookup"><span data-stu-id="43ff5-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="43ff5-110">No configurado</span><span class="sxs-lookup"><span data-stu-id="43ff5-110">notConfigured</span></span>|<span data-ttu-id="43ff5-111">0</span><span class="sxs-lookup"><span data-stu-id="43ff5-111">0</span></span>|<span data-ttu-id="43ff5-112">Valor predeterminado de dispositivo, no se ha seleccionado ningún tipo de Control de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="43ff5-112">Device default value, no Application Control type selected.</span></span>|
|<span data-ttu-id="43ff5-113">enforceComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="43ff5-113">enforceComponentsAndStoreApps</span></span>|<span data-ttu-id="43ff5-114">1</span><span class="sxs-lookup"><span data-stu-id="43ff5-114">1</span></span>|<span data-ttu-id="43ff5-115">Exigir la aplicación de las aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="43ff5-115">Enforce Windows component and store apps.</span></span>|
|<span data-ttu-id="43ff5-116">auditComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="43ff5-116">auditComponentsAndStoreApps</span></span>|<span data-ttu-id="43ff5-117">2</span><span class="sxs-lookup"><span data-stu-id="43ff5-117">2</span></span>|<span data-ttu-id="43ff5-118">Auditoría de aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="43ff5-118">Audit Windows component and store apps.</span></span>|
|<span data-ttu-id="43ff5-119">enforceComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="43ff5-119">enforceComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="43ff5-120">3</span><span class="sxs-lookup"><span data-stu-id="43ff5-120">3</span></span>|<span data-ttu-id="43ff5-121">Exigir la aplicación de componentes de Windows, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="43ff5-121">Enforce Windows components, store apps and smart locker.</span></span>|
|<span data-ttu-id="43ff5-122">auditComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="43ff5-122">auditComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="43ff5-123">4</span><span class="sxs-lookup"><span data-stu-id="43ff5-123">4</span></span>|<span data-ttu-id="43ff5-124">Componentes de Windows de auditoría, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="43ff5-124">Audit Windows components, store apps and smart locker.</span></span>|



