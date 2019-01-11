---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 9ca34a44b1ea4e55199eb65283f839cb50e222da
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807808"
---
# <a name="applockerapplicationcontroltype-enum-type"></a><span data-ttu-id="535af-103">tipo de enumeración appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="535af-103">appLockerApplicationControlType enum type</span></span>

> <span data-ttu-id="535af-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="535af-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="535af-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="535af-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="535af-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="535af-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="535af-107">Posibles valores de tipos de Control de aplicación de AppLocker</span><span class="sxs-lookup"><span data-stu-id="535af-107">Possible values of AppLocker Application Control Types</span></span>
## <a name="members"></a><span data-ttu-id="535af-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="535af-108">Members</span></span>
|<span data-ttu-id="535af-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="535af-109">Member</span></span>|<span data-ttu-id="535af-110">Valor</span><span class="sxs-lookup"><span data-stu-id="535af-110">Value</span></span>|<span data-ttu-id="535af-111">Description</span><span class="sxs-lookup"><span data-stu-id="535af-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="535af-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="535af-112">notConfigured</span></span>|<span data-ttu-id="535af-113">0</span><span class="sxs-lookup"><span data-stu-id="535af-113">0</span></span>|<span data-ttu-id="535af-114">Valor predeterminado de dispositivo, no se ha seleccionado ningún tipo de Control de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="535af-114">Device default value, no Application Control type selected.</span></span>|
|<span data-ttu-id="535af-115">enforceComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="535af-115">enforceComponentsAndStoreApps</span></span>|<span data-ttu-id="535af-116">1</span><span class="sxs-lookup"><span data-stu-id="535af-116">1</span></span>|<span data-ttu-id="535af-117">Exigir la aplicación de las aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="535af-117">Enforce Windows component and store apps.</span></span>|
|<span data-ttu-id="535af-118">auditComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="535af-118">auditComponentsAndStoreApps</span></span>|<span data-ttu-id="535af-119">2</span><span class="sxs-lookup"><span data-stu-id="535af-119">2</span></span>|<span data-ttu-id="535af-120">Auditoría de aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="535af-120">Audit Windows component and store apps.</span></span>|
|<span data-ttu-id="535af-121">enforceComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="535af-121">enforceComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="535af-122">3</span><span class="sxs-lookup"><span data-stu-id="535af-122">3</span></span>|<span data-ttu-id="535af-123">Exigir la aplicación de componentes de Windows, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="535af-123">Enforce Windows components, store apps and smart locker.</span></span>|
|<span data-ttu-id="535af-124">auditComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="535af-124">auditComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="535af-125">4</span><span class="sxs-lookup"><span data-stu-id="535af-125">4</span></span>|<span data-ttu-id="535af-126">Componentes de Windows de auditoría, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="535af-126">Audit Windows components, store apps and smart locker.</span></span>|





