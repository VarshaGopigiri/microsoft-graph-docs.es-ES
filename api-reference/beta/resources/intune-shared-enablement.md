---
title: tipo enum de habilitación
description: 'Valores utilizados para indicar el estado de un dispositivo. '
author: tfitzmac
ms.openlocfilehash: 5b1d494fd116eab437b4654d396b029e1384a817
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356892"
---
# <a name="enablement-enum-type"></a><span data-ttu-id="fd3a7-103">tipo enum de habilitación</span><span class="sxs-lookup"><span data-stu-id="fd3a7-103">enablement enum type</span></span>

> <span data-ttu-id="fd3a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd3a7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fd3a7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fd3a7-107">Valores utilizados para indicar el estado de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-107">Values used to indicate the status of a device.</span></span> 

<span data-ttu-id="fd3a7-108">Tenga en cuenta que hay una diferencia entre deshabilitado y no está definida.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-108">Note that there is a difference between disabled and not configured.</span></span>

## <a name="members"></a><span data-ttu-id="fd3a7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd3a7-109">Members</span></span>
|<span data-ttu-id="fd3a7-110">Miembro	</span><span class="sxs-lookup"><span data-stu-id="fd3a7-110">Member</span></span>|<span data-ttu-id="fd3a7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="fd3a7-111">Value</span></span>|<span data-ttu-id="fd3a7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd3a7-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fd3a7-113">No configurado</span><span class="sxs-lookup"><span data-stu-id="fd3a7-113">notConfigured</span></span>|<span data-ttu-id="fd3a7-114">0</span><span class="sxs-lookup"><span data-stu-id="fd3a7-114">0</span></span>|<span data-ttu-id="fd3a7-115">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-115">Device default value, no intent.</span></span>|
|<span data-ttu-id="fd3a7-116">enabled</span><span class="sxs-lookup"><span data-stu-id="fd3a7-116">enabled</span></span>|<span data-ttu-id="fd3a7-117">1</span><span class="sxs-lookup"><span data-stu-id="fd3a7-117">1</span></span>|<span data-ttu-id="fd3a7-118">Habilita a la configuración en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-118">Enables the setting on the device.</span></span>|
|<span data-ttu-id="fd3a7-119">deshabilitado</span><span class="sxs-lookup"><span data-stu-id="fd3a7-119">disabled</span></span>|<span data-ttu-id="fd3a7-120">2</span><span class="sxs-lookup"><span data-stu-id="fd3a7-120">2</span></span>|<span data-ttu-id="fd3a7-121">Deshabilita a la configuración en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3a7-121">Disables the setting on the device.</span></span>|
