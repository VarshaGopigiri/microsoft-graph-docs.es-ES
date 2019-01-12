---
title: tipo de enumeración configurationManagerClientState
description: Estado de cliente del Administrador de configuración
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fc6f3f2db68273097d70ba9dccc6844b86afa3f6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923890"
---
# <a name="configurationmanagerclientstate-enum-type"></a><span data-ttu-id="76566-103">tipo de enumeración configurationManagerClientState</span><span class="sxs-lookup"><span data-stu-id="76566-103">configurationManagerClientState enum type</span></span>

> <span data-ttu-id="76566-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="76566-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="76566-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="76566-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="76566-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="76566-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="76566-107">Estado de cliente del Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="76566-107">Configuration manager client state</span></span>
## <a name="members"></a><span data-ttu-id="76566-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="76566-108">Members</span></span>
|<span data-ttu-id="76566-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="76566-109">Member</span></span>|<span data-ttu-id="76566-110">Valor</span><span class="sxs-lookup"><span data-stu-id="76566-110">Value</span></span>|<span data-ttu-id="76566-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="76566-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="76566-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="76566-112">unknown</span></span>|<span data-ttu-id="76566-113">0</span><span class="sxs-lookup"><span data-stu-id="76566-113">0</span></span>|<span data-ttu-id="76566-114">Agente de configuración del administrador es más antiguo que 1806 o no está instalado o este dispositivo no ha desprotegido en Intune durante más de 30 días.</span><span class="sxs-lookup"><span data-stu-id="76566-114">Configuration manager agent is older than 1806 or not installed or this device has not checked into Intune for over 30 days.</span></span>|
|<span data-ttu-id="76566-115">instalado</span><span class="sxs-lookup"><span data-stu-id="76566-115">installed</span></span>|<span data-ttu-id="76566-116">1</span><span class="sxs-lookup"><span data-stu-id="76566-116">1</span></span>|<span data-ttu-id="76566-117">El agente de configuración del administrador está instalado pero es posible que no se aparece en la consola de administrador de configuración todavía.</span><span class="sxs-lookup"><span data-stu-id="76566-117">The configuration manager agent is installed but may not be showing up in the configuration manager console yet.</span></span> <span data-ttu-id="76566-118">Espere unas cuantas horas para que pueda actualizar.</span><span class="sxs-lookup"><span data-stu-id="76566-118">Wait a few hours for it to refresh.</span></span>|
|<span data-ttu-id="76566-119">buen estado</span><span class="sxs-lookup"><span data-stu-id="76566-119">healthy</span></span>|<span data-ttu-id="76566-120">7</span><span class="sxs-lookup"><span data-stu-id="76566-120">7</span></span>|<span data-ttu-id="76566-121">Este dispositivo pudo comprobar correctamente con el servicio de administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="76566-121">This device was able to check in with the configuration manager service successfully.</span></span>|
|<span data-ttu-id="76566-122">installFailed</span><span class="sxs-lookup"><span data-stu-id="76566-122">installFailed</span></span>|<span data-ttu-id="76566-123">8</span><span class="sxs-lookup"><span data-stu-id="76566-123">8</span></span>|<span data-ttu-id="76566-124">No se pudo instalar el agente de configuración del administrador.</span><span class="sxs-lookup"><span data-stu-id="76566-124">The configuration manager agent failed to install.</span></span>|
|<span data-ttu-id="76566-125">updateFailed</span><span class="sxs-lookup"><span data-stu-id="76566-125">updateFailed</span></span>|<span data-ttu-id="76566-126">11</span><span class="sxs-lookup"><span data-stu-id="76566-126">11</span></span>|<span data-ttu-id="76566-127">Error al actualizar desde la versión x a y de la versión del agente de administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="76566-127">The update from version x to version y of the configuration manager agent failed.</span></span> |
|<span data-ttu-id="76566-128">communicationError</span><span class="sxs-lookup"><span data-stu-id="76566-128">communicationError</span></span>|<span data-ttu-id="76566-129">19</span><span class="sxs-lookup"><span data-stu-id="76566-129">19</span></span>|<span data-ttu-id="76566-130">El agente de configuración del administrador puede ponerse en contacto con el servicio de administrador de configuración en el pasado, pero ahora ya no es capaz de.</span><span class="sxs-lookup"><span data-stu-id="76566-130">The configuration manager agent was able to reach the configuration manager service in the past but is now no longer able to.</span></span> |





