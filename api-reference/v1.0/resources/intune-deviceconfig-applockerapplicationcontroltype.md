---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
ms.openlocfilehash: 703cc18dfee49a01adb3cd4f61c5d7e99e30fb00
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029140"
---
# <a name="applockerapplicationcontroltype-enum-type"></a><span data-ttu-id="ace5d-103">tipo de enumeración appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="ace5d-103">appLockerApplicationControlType enum type</span></span>

> <span data-ttu-id="ace5d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ace5d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ace5d-105">Posibles valores de tipos de Control de aplicación de AppLocker</span><span class="sxs-lookup"><span data-stu-id="ace5d-105">Possible values of AppLocker Application Control Types</span></span>
## <a name="members"></a><span data-ttu-id="ace5d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ace5d-106">Members</span></span>
|<span data-ttu-id="ace5d-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ace5d-107">Member</span></span>|<span data-ttu-id="ace5d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ace5d-108">Value</span></span>|<span data-ttu-id="ace5d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ace5d-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ace5d-110">No configurado</span><span class="sxs-lookup"><span data-stu-id="ace5d-110">notConfigured</span></span>|<span data-ttu-id="ace5d-111">0</span><span class="sxs-lookup"><span data-stu-id="ace5d-111">0</span></span>|<span data-ttu-id="ace5d-112">Valor predeterminado de dispositivo, no se ha seleccionado ningún tipo de Control de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ace5d-112">Device default value, no Application Control type selected.</span></span>|
|<span data-ttu-id="ace5d-113">enforceComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="ace5d-113">enforceComponentsAndStoreApps</span></span>|<span data-ttu-id="ace5d-114">1</span><span class="sxs-lookup"><span data-stu-id="ace5d-114">1</span></span>|<span data-ttu-id="ace5d-115">Exigir la aplicación de las aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="ace5d-115">Enforce Windows component and store apps.</span></span>|
|<span data-ttu-id="ace5d-116">auditComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="ace5d-116">auditComponentsAndStoreApps</span></span>|<span data-ttu-id="ace5d-117">2</span><span class="sxs-lookup"><span data-stu-id="ace5d-117">2</span></span>|<span data-ttu-id="ace5d-118">Auditoría de aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="ace5d-118">Audit Windows component and store apps.</span></span>|
|<span data-ttu-id="ace5d-119">enforceComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="ace5d-119">enforceComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="ace5d-120">3</span><span class="sxs-lookup"><span data-stu-id="ace5d-120">3</span></span>|<span data-ttu-id="ace5d-121">Exigir la aplicación de componentes de Windows, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="ace5d-121">Enforce Windows components, store apps and smart locker.</span></span>|
|<span data-ttu-id="ace5d-122">auditComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="ace5d-122">auditComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="ace5d-123">4</span><span class="sxs-lookup"><span data-stu-id="ace5d-123">4</span></span>|<span data-ttu-id="ace5d-124">Componentes de Windows de auditoría, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="ace5d-124">Audit Windows components, store apps and smart locker.</span></span>|



