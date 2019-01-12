---
title: tipo de enumeración androidDeviceOwnerSystemUpdateInstallType
description: Tipos de actualización del sistema para dispositivos Android propietario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9a46d60972bab46fa0e2cda8d03a090bd8b810a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980975"
---
# <a name="androiddeviceownersystemupdateinstalltype-enum-type"></a><span data-ttu-id="b74ec-103">tipo de enumeración androidDeviceOwnerSystemUpdateInstallType</span><span class="sxs-lookup"><span data-stu-id="b74ec-103">androidDeviceOwnerSystemUpdateInstallType enum type</span></span>

> <span data-ttu-id="b74ec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b74ec-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b74ec-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b74ec-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b74ec-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b74ec-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b74ec-107">Tipos de actualización del sistema para dispositivos Android propietario.</span><span class="sxs-lookup"><span data-stu-id="b74ec-107">System Update Types for Android Device Owner.</span></span>
## <a name="members"></a><span data-ttu-id="b74ec-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b74ec-108">Members</span></span>
|<span data-ttu-id="b74ec-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b74ec-109">Member</span></span>|<span data-ttu-id="b74ec-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b74ec-110">Value</span></span>|<span data-ttu-id="b74ec-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b74ec-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b74ec-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="b74ec-112">deviceDefault</span></span>|<span data-ttu-id="b74ec-113">0</span><span class="sxs-lookup"><span data-stu-id="b74ec-113">0</span></span>|<span data-ttu-id="b74ec-114">Comportamiento predeterminado de dispositivo, que normalmente se solicita al usuario que acepte actualizaciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="b74ec-114">Device default behavior, which typically prompts the user to accept system updates.</span></span>|
|<span data-ttu-id="b74ec-115">Posponer</span><span class="sxs-lookup"><span data-stu-id="b74ec-115">postpone</span></span>|<span data-ttu-id="b74ec-116">1</span><span class="sxs-lookup"><span data-stu-id="b74ec-116">1</span></span>|<span data-ttu-id="b74ec-117">Posponer la instalación automática de actualizaciones de seguridad en 30 días.</span><span class="sxs-lookup"><span data-stu-id="b74ec-117">Postpone automatic install of updates up to 30 days.</span></span>|
|<span data-ttu-id="b74ec-118">ventana</span><span class="sxs-lookup"><span data-stu-id="b74ec-118">windowed</span></span>|<span data-ttu-id="b74ec-119">2</span><span class="sxs-lookup"><span data-stu-id="b74ec-119">2</span></span>|<span data-ttu-id="b74ec-120">Instalar automáticamente dentro de un período de mantenimiento diario.</span><span class="sxs-lookup"><span data-stu-id="b74ec-120">Install automatically inside a daily maintenance window.</span></span>|
|<span data-ttu-id="b74ec-121">Automático</span><span class="sxs-lookup"><span data-stu-id="b74ec-121">automatic</span></span>|<span data-ttu-id="b74ec-122">3</span><span class="sxs-lookup"><span data-stu-id="b74ec-122">3</span></span>|<span data-ttu-id="b74ec-123">Instalar automáticamente las actualizaciones tan pronto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="b74ec-123">Automatically install updates as soon as possible.</span></span>|





