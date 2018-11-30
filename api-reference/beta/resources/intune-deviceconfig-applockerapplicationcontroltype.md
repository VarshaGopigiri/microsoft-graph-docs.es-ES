---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
ms.openlocfilehash: 150e3daa6b8deb2d1e17c3ea7caf345ba39446f3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085561"
---
# <a name="applockerapplicationcontroltype-enum-type"></a><span data-ttu-id="b67a8-103">tipo de enumeración appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="b67a8-103">appLockerApplicationControlType enum type</span></span>

> <span data-ttu-id="b67a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b67a8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b67a8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b67a8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b67a8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b67a8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b67a8-107">Posibles valores de tipos de Control de aplicación de AppLocker</span><span class="sxs-lookup"><span data-stu-id="b67a8-107">Possible values of AppLocker Application Control Types</span></span>
## <a name="members"></a><span data-ttu-id="b67a8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b67a8-108">Members</span></span>
|<span data-ttu-id="b67a8-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b67a8-109">Member</span></span>|<span data-ttu-id="b67a8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b67a8-110">Value</span></span>|<span data-ttu-id="b67a8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b67a8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b67a8-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="b67a8-112">notConfigured</span></span>|<span data-ttu-id="b67a8-113">0</span><span class="sxs-lookup"><span data-stu-id="b67a8-113">0</span></span>|<span data-ttu-id="b67a8-114">Valor predeterminado de dispositivo, no se ha seleccionado ningún tipo de Control de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b67a8-114">Device default value, no Application Control type selected.</span></span>|
|<span data-ttu-id="b67a8-115">enforceComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="b67a8-115">enforceComponentsAndStoreApps</span></span>|<span data-ttu-id="b67a8-116">1</span><span class="sxs-lookup"><span data-stu-id="b67a8-116">1</span></span>|<span data-ttu-id="b67a8-117">Exigir la aplicación de las aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="b67a8-117">Enforce Windows component and store apps.</span></span>|
|<span data-ttu-id="b67a8-118">auditComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="b67a8-118">auditComponentsAndStoreApps</span></span>|<span data-ttu-id="b67a8-119">2</span><span class="sxs-lookup"><span data-stu-id="b67a8-119">2</span></span>|<span data-ttu-id="b67a8-120">Auditoría de aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="b67a8-120">Audit Windows component and store apps.</span></span>|
|<span data-ttu-id="b67a8-121">enforceComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="b67a8-121">enforceComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="b67a8-122">3</span><span class="sxs-lookup"><span data-stu-id="b67a8-122">3</span></span>|<span data-ttu-id="b67a8-123">Exigir la aplicación de componentes de Windows, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="b67a8-123">Enforce Windows components, store apps and smart locker.</span></span>|
|<span data-ttu-id="b67a8-124">auditComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="b67a8-124">auditComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="b67a8-125">4</span><span class="sxs-lookup"><span data-stu-id="b67a8-125">4</span></span>|<span data-ttu-id="b67a8-126">Componentes de Windows de auditoría, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="b67a8-126">Audit Windows components, store apps and smart locker.</span></span>|





