---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 258a98b9ec4945c807a6aae2b34a178628952ac4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937960"
---
# <a name="applockerapplicationcontroltype-enum-type"></a><span data-ttu-id="d35e1-103">tipo de enumeración appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="d35e1-103">appLockerApplicationControlType enum type</span></span>

> <span data-ttu-id="d35e1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d35e1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d35e1-105">Posibles valores de tipos de Control de aplicación de AppLocker</span><span class="sxs-lookup"><span data-stu-id="d35e1-105">Possible values of AppLocker Application Control Types</span></span>
## <a name="members"></a><span data-ttu-id="d35e1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d35e1-106">Members</span></span>
|<span data-ttu-id="d35e1-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d35e1-107">Member</span></span>|<span data-ttu-id="d35e1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d35e1-108">Value</span></span>|<span data-ttu-id="d35e1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d35e1-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d35e1-110">No configurado</span><span class="sxs-lookup"><span data-stu-id="d35e1-110">notConfigured</span></span>|<span data-ttu-id="d35e1-111">0</span><span class="sxs-lookup"><span data-stu-id="d35e1-111">0</span></span>|<span data-ttu-id="d35e1-112">Valor predeterminado de dispositivo, no se ha seleccionado ningún tipo de Control de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d35e1-112">Device default value, no Application Control type selected.</span></span>|
|<span data-ttu-id="d35e1-113">enforceComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="d35e1-113">enforceComponentsAndStoreApps</span></span>|<span data-ttu-id="d35e1-114">1</span><span class="sxs-lookup"><span data-stu-id="d35e1-114">1</span></span>|<span data-ttu-id="d35e1-115">Exigir la aplicación de las aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="d35e1-115">Enforce Windows component and store apps.</span></span>|
|<span data-ttu-id="d35e1-116">auditComponentsAndStoreApps</span><span class="sxs-lookup"><span data-stu-id="d35e1-116">auditComponentsAndStoreApps</span></span>|<span data-ttu-id="d35e1-117">2</span><span class="sxs-lookup"><span data-stu-id="d35e1-117">2</span></span>|<span data-ttu-id="d35e1-118">Auditoría de aplicaciones de componente y almacenamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="d35e1-118">Audit Windows component and store apps.</span></span>|
|<span data-ttu-id="d35e1-119">enforceComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="d35e1-119">enforceComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="d35e1-120">3</span><span class="sxs-lookup"><span data-stu-id="d35e1-120">3</span></span>|<span data-ttu-id="d35e1-121">Exigir la aplicación de componentes de Windows, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="d35e1-121">Enforce Windows components, store apps and smart locker.</span></span>|
|<span data-ttu-id="d35e1-122">auditComponentsStoreAppsAndSmartlocker</span><span class="sxs-lookup"><span data-stu-id="d35e1-122">auditComponentsStoreAppsAndSmartlocker</span></span>|<span data-ttu-id="d35e1-123">4</span><span class="sxs-lookup"><span data-stu-id="d35e1-123">4</span></span>|<span data-ttu-id="d35e1-124">Componentes de Windows de auditoría, almacenar aplicaciones y almacén inteligente.</span><span class="sxs-lookup"><span data-stu-id="d35e1-124">Audit Windows components, store apps and smart locker.</span></span>|



