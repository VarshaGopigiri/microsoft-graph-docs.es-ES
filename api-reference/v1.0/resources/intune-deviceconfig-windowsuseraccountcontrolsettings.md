---
title: tipo de enumeración windowsUserAccountControlSettings
description: Valores posibles para la configuración de control de cuenta de usuario de Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0475d8fb013cbb07f8d69a659f8ecde2eb580e43
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972477"
---
# <a name="windowsuseraccountcontrolsettings-enum-type"></a><span data-ttu-id="40c32-103">tipo de enumeración windowsUserAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="40c32-103">windowsUserAccountControlSettings enum type</span></span>

> <span data-ttu-id="40c32-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40c32-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40c32-105">Valores posibles para la configuración de control de cuenta de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="40c32-105">Possible values for Windows user account control settings.</span></span>
## <a name="members"></a><span data-ttu-id="40c32-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="40c32-106">Members</span></span>
|<span data-ttu-id="40c32-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="40c32-107">Member</span></span>|<span data-ttu-id="40c32-108">Valor</span><span class="sxs-lookup"><span data-stu-id="40c32-108">Value</span></span>|<span data-ttu-id="40c32-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="40c32-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40c32-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="40c32-110">userDefined</span></span>|<span data-ttu-id="40c32-111">0</span><span class="sxs-lookup"><span data-stu-id="40c32-111">0</span></span>|<span data-ttu-id="40c32-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="40c32-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="40c32-113">alwaysNotify</span><span class="sxs-lookup"><span data-stu-id="40c32-113">alwaysNotify</span></span>|<span data-ttu-id="40c32-114">1</span><span class="sxs-lookup"><span data-stu-id="40c32-114">1</span></span>|<span data-ttu-id="40c32-115">Notificarme siempre.</span><span class="sxs-lookup"><span data-stu-id="40c32-115">Always notify.</span></span>|
|<span data-ttu-id="40c32-116">notifyOnAppChanges</span><span class="sxs-lookup"><span data-stu-id="40c32-116">notifyOnAppChanges</span></span>|<span data-ttu-id="40c32-117">2</span><span class="sxs-lookup"><span data-stu-id="40c32-117">2</span></span>|<span data-ttu-id="40c32-118">Notificar en los cambios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40c32-118">Notify on app changes.</span></span>|
|<span data-ttu-id="40c32-119">notifyOnAppChangesWithoutDimming</span><span class="sxs-lookup"><span data-stu-id="40c32-119">notifyOnAppChangesWithoutDimming</span></span>|<span data-ttu-id="40c32-120">3</span><span class="sxs-lookup"><span data-stu-id="40c32-120">3</span></span>|<span data-ttu-id="40c32-121">Notificar en los cambios de la aplicación sin atenuar el escritorio.</span><span class="sxs-lookup"><span data-stu-id="40c32-121">Notify on app changes without dimming desktop.</span></span>|
|<span data-ttu-id="40c32-122">neverNotify</span><span class="sxs-lookup"><span data-stu-id="40c32-122">neverNotify</span></span>|<span data-ttu-id="40c32-123">4</span><span class="sxs-lookup"><span data-stu-id="40c32-123">4</span></span>|<span data-ttu-id="40c32-124">No notificar nunca.</span><span class="sxs-lookup"><span data-stu-id="40c32-124">Never notify.</span></span>|



