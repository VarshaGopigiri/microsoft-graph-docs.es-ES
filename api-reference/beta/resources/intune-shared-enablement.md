---
title: tipo enum de habilitación
description: 'Valores utilizados para indicar el estado de un dispositivo. '
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c77da7026640e9ad0a6f6f08f077d509cb411f22
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888259"
---
# <a name="enablement-enum-type"></a><span data-ttu-id="af5bf-103">tipo enum de habilitación</span><span class="sxs-lookup"><span data-stu-id="af5bf-103">enablement enum type</span></span>

> <span data-ttu-id="af5bf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af5bf-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af5bf-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af5bf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="af5bf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="af5bf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="af5bf-107">Valores utilizados para indicar el estado de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af5bf-107">Values used to indicate the status of a device.</span></span> 

<span data-ttu-id="af5bf-108">Tenga en cuenta que hay una diferencia entre deshabilitado y no está definida.</span><span class="sxs-lookup"><span data-stu-id="af5bf-108">Note that there is a difference between disabled and not configured.</span></span>

## <a name="members"></a><span data-ttu-id="af5bf-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="af5bf-109">Members</span></span>
|<span data-ttu-id="af5bf-110">Miembro	</span><span class="sxs-lookup"><span data-stu-id="af5bf-110">Member</span></span>|<span data-ttu-id="af5bf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="af5bf-111">Value</span></span>|<span data-ttu-id="af5bf-112">Description</span><span class="sxs-lookup"><span data-stu-id="af5bf-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="af5bf-113">No configurado</span><span class="sxs-lookup"><span data-stu-id="af5bf-113">notConfigured</span></span>|<span data-ttu-id="af5bf-114">0</span><span class="sxs-lookup"><span data-stu-id="af5bf-114">0</span></span>|<span data-ttu-id="af5bf-115">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="af5bf-115">Device default value, no intent.</span></span>|
|<span data-ttu-id="af5bf-116">enabled</span><span class="sxs-lookup"><span data-stu-id="af5bf-116">enabled</span></span>|<span data-ttu-id="af5bf-117">1</span><span class="sxs-lookup"><span data-stu-id="af5bf-117">1</span></span>|<span data-ttu-id="af5bf-118">Habilita a la configuración en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af5bf-118">Enables the setting on the device.</span></span>|
|<span data-ttu-id="af5bf-119">deshabilitado</span><span class="sxs-lookup"><span data-stu-id="af5bf-119">disabled</span></span>|<span data-ttu-id="af5bf-120">2</span><span class="sxs-lookup"><span data-stu-id="af5bf-120">2</span></span>|<span data-ttu-id="af5bf-121">Deshabilita a la configuración en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af5bf-121">Disables the setting on the device.</span></span>|
