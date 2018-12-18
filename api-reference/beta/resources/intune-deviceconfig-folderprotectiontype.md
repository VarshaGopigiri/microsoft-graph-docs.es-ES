---
title: tipo de enumeración folderProtectionType
description: Valores posibles de protección de carpeta
author: tfitzmac
ms.openlocfilehash: 93df62da9bb5d849cba86b52384f45bfe7bd760f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350606"
---
# <a name="folderprotectiontype-enum-type"></a><span data-ttu-id="547de-103">tipo de enumeración folderProtectionType</span><span class="sxs-lookup"><span data-stu-id="547de-103">folderProtectionType enum type</span></span>

> <span data-ttu-id="547de-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="547de-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="547de-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="547de-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="547de-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="547de-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="547de-107">Valores posibles de protección de carpeta</span><span class="sxs-lookup"><span data-stu-id="547de-107">Possible values of Folder Protection</span></span>
## <a name="members"></a><span data-ttu-id="547de-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="547de-108">Members</span></span>
|<span data-ttu-id="547de-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="547de-109">Member</span></span>|<span data-ttu-id="547de-110">Valor</span><span class="sxs-lookup"><span data-stu-id="547de-110">Value</span></span>|<span data-ttu-id="547de-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="547de-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="547de-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="547de-112">userDefined</span></span>|<span data-ttu-id="547de-113">0</span><span class="sxs-lookup"><span data-stu-id="547de-113">0</span></span>|<span data-ttu-id="547de-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="547de-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="547de-115">habilitar</span><span class="sxs-lookup"><span data-stu-id="547de-115">enable</span></span>|<span data-ttu-id="547de-116">1</span><span class="sxs-lookup"><span data-stu-id="547de-116">1</span></span>|<span data-ttu-id="547de-117">Funcionalidad de bloque.</span><span class="sxs-lookup"><span data-stu-id="547de-117">Block functionality.</span></span>|
|<span data-ttu-id="547de-118">auditMode</span><span class="sxs-lookup"><span data-stu-id="547de-118">auditMode</span></span>|<span data-ttu-id="547de-119">2</span><span class="sxs-lookup"><span data-stu-id="547de-119">2</span></span>|<span data-ttu-id="547de-120">Permitir la funcionalidad pero los registros que se genere.</span><span class="sxs-lookup"><span data-stu-id="547de-120">Allow functionality but generate logs.</span></span>|
|<span data-ttu-id="547de-121">blockDiskModification</span><span class="sxs-lookup"><span data-stu-id="547de-121">blockDiskModification</span></span>|<span data-ttu-id="547de-122">3</span><span class="sxs-lookup"><span data-stu-id="547de-122">3</span></span>|<span data-ttu-id="547de-123">Bloquear las aplicaciones que no se confía escribir en sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="547de-123">Block untrusted apps from writing to disk sectors.</span></span>|
|<span data-ttu-id="547de-124">auditDiskModification</span><span class="sxs-lookup"><span data-stu-id="547de-124">auditDiskModification</span></span>|<span data-ttu-id="547de-125">4</span><span class="sxs-lookup"><span data-stu-id="547de-125">4</span></span>|<span data-ttu-id="547de-126">Generar registros al escriben aplicaciones que no se confía a sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="547de-126">Generate logs when untrusted apps write to disk sectors.</span></span>|





