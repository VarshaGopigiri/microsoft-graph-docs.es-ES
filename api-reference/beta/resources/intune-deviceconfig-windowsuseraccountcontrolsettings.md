---
title: tipo de enumeración windowsUserAccountControlSettings
description: Valores posibles para la configuración de control de cuenta de usuario de Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cd16db4236096687ddcc9f169dd657c938fd6815
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911815"
---
# <a name="windowsuseraccountcontrolsettings-enum-type"></a><span data-ttu-id="26ecd-103">tipo de enumeración windowsUserAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="26ecd-103">windowsUserAccountControlSettings enum type</span></span>

> <span data-ttu-id="26ecd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26ecd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26ecd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26ecd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="26ecd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26ecd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26ecd-107">Valores posibles para la configuración de control de cuenta de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="26ecd-107">Possible values for Windows user account control settings.</span></span>
## <a name="members"></a><span data-ttu-id="26ecd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="26ecd-108">Members</span></span>
|<span data-ttu-id="26ecd-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="26ecd-109">Member</span></span>|<span data-ttu-id="26ecd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="26ecd-110">Value</span></span>|<span data-ttu-id="26ecd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="26ecd-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="26ecd-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="26ecd-112">userDefined</span></span>|<span data-ttu-id="26ecd-113">0</span><span class="sxs-lookup"><span data-stu-id="26ecd-113">0</span></span>|<span data-ttu-id="26ecd-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="26ecd-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="26ecd-115">alwaysNotify</span><span class="sxs-lookup"><span data-stu-id="26ecd-115">alwaysNotify</span></span>|<span data-ttu-id="26ecd-116">1</span><span class="sxs-lookup"><span data-stu-id="26ecd-116">1</span></span>|<span data-ttu-id="26ecd-117">Notificarme siempre.</span><span class="sxs-lookup"><span data-stu-id="26ecd-117">Always notify.</span></span>|
|<span data-ttu-id="26ecd-118">notifyOnAppChanges</span><span class="sxs-lookup"><span data-stu-id="26ecd-118">notifyOnAppChanges</span></span>|<span data-ttu-id="26ecd-119">2</span><span class="sxs-lookup"><span data-stu-id="26ecd-119">2</span></span>|<span data-ttu-id="26ecd-120">Notificar en los cambios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="26ecd-120">Notify on app changes.</span></span>|
|<span data-ttu-id="26ecd-121">notifyOnAppChangesWithoutDimming</span><span class="sxs-lookup"><span data-stu-id="26ecd-121">notifyOnAppChangesWithoutDimming</span></span>|<span data-ttu-id="26ecd-122">3</span><span class="sxs-lookup"><span data-stu-id="26ecd-122">3</span></span>|<span data-ttu-id="26ecd-123">Notificar en los cambios de la aplicación sin atenuar el escritorio.</span><span class="sxs-lookup"><span data-stu-id="26ecd-123">Notify on app changes without dimming desktop.</span></span>|
|<span data-ttu-id="26ecd-124">neverNotify</span><span class="sxs-lookup"><span data-stu-id="26ecd-124">neverNotify</span></span>|<span data-ttu-id="26ecd-125">4</span><span class="sxs-lookup"><span data-stu-id="26ecd-125">4</span></span>|<span data-ttu-id="26ecd-126">No notificar nunca.</span><span class="sxs-lookup"><span data-stu-id="26ecd-126">Never notify.</span></span>|





