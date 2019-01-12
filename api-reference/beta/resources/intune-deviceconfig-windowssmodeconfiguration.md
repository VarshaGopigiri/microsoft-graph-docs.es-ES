---
title: tipo de enumeración windowsSModeConfiguration
description: Las posibles opciones para configurar el modo de S desbloquear
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 28106a073a6bb213fe17e80193cb32d1e6b3b9ce
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947382"
---
# <a name="windowssmodeconfiguration-enum-type"></a><span data-ttu-id="d0447-103">tipo de enumeración windowsSModeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0447-103">windowsSModeConfiguration enum type</span></span>

> <span data-ttu-id="d0447-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0447-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0447-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0447-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d0447-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0447-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0447-107">Las posibles opciones para configurar el modo de S desbloquear</span><span class="sxs-lookup"><span data-stu-id="d0447-107">The possible options to configure S mode unlock</span></span>
## <a name="members"></a><span data-ttu-id="d0447-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0447-108">Members</span></span>
|<span data-ttu-id="d0447-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d0447-109">Member</span></span>|<span data-ttu-id="d0447-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d0447-110">Value</span></span>|<span data-ttu-id="d0447-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0447-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0447-112">noRestriction</span><span class="sxs-lookup"><span data-stu-id="d0447-112">noRestriction</span></span>|<span data-ttu-id="d0447-113">0</span><span class="sxs-lookup"><span data-stu-id="d0447-113">0</span></span>|<span data-ttu-id="d0447-114">Esta opción quitará todas las restricciones para desbloquear el modo S - predeterminada</span><span class="sxs-lookup"><span data-stu-id="d0447-114">This option will remove all restrictions to unlock S mode - default</span></span>|
|<span data-ttu-id="d0447-115">bloque</span><span class="sxs-lookup"><span data-stu-id="d0447-115">block</span></span>|<span data-ttu-id="d0447-116">1</span><span class="sxs-lookup"><span data-stu-id="d0447-116">1</span></span>|<span data-ttu-id="d0447-117">Esta opción bloqueará el usuario para desbloquear el dispositivo desde el modo de S</span><span class="sxs-lookup"><span data-stu-id="d0447-117">This option will block the user to unlock the device from S mode</span></span>|
|<span data-ttu-id="d0447-118">desbloquear</span><span class="sxs-lookup"><span data-stu-id="d0447-118">unlock</span></span>|<span data-ttu-id="d0447-119">2</span><span class="sxs-lookup"><span data-stu-id="d0447-119">2</span></span>|<span data-ttu-id="d0447-120">Esta opción desbloquear el dispositivo desde el modo de S</span><span class="sxs-lookup"><span data-stu-id="d0447-120">This option will unlock the device from S mode</span></span>|





