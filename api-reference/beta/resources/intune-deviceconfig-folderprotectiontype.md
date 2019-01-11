---
title: tipo de enumeración folderProtectionType
description: Valores posibles de protección de carpeta
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 435f3ea01f5a8ffc3c4cb54034d415d54732db5d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826134"
---
# <a name="folderprotectiontype-enum-type"></a><span data-ttu-id="3b817-103">tipo de enumeración folderProtectionType</span><span class="sxs-lookup"><span data-stu-id="3b817-103">folderProtectionType enum type</span></span>

> <span data-ttu-id="3b817-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b817-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b817-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b817-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3b817-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3b817-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3b817-107">Valores posibles de protección de carpeta</span><span class="sxs-lookup"><span data-stu-id="3b817-107">Possible values of Folder Protection</span></span>
## <a name="members"></a><span data-ttu-id="3b817-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b817-108">Members</span></span>
|<span data-ttu-id="3b817-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="3b817-109">Member</span></span>|<span data-ttu-id="3b817-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3b817-110">Value</span></span>|<span data-ttu-id="3b817-111">Description</span><span class="sxs-lookup"><span data-stu-id="3b817-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3b817-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="3b817-112">userDefined</span></span>|<span data-ttu-id="3b817-113">0</span><span class="sxs-lookup"><span data-stu-id="3b817-113">0</span></span>|<span data-ttu-id="3b817-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="3b817-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="3b817-115">habilitar</span><span class="sxs-lookup"><span data-stu-id="3b817-115">enable</span></span>|<span data-ttu-id="3b817-116">1</span><span class="sxs-lookup"><span data-stu-id="3b817-116">1</span></span>|<span data-ttu-id="3b817-117">Funcionalidad de bloque.</span><span class="sxs-lookup"><span data-stu-id="3b817-117">Block functionality.</span></span>|
|<span data-ttu-id="3b817-118">auditMode</span><span class="sxs-lookup"><span data-stu-id="3b817-118">auditMode</span></span>|<span data-ttu-id="3b817-119">2</span><span class="sxs-lookup"><span data-stu-id="3b817-119">2</span></span>|<span data-ttu-id="3b817-120">Permitir la funcionalidad pero los registros que se genere.</span><span class="sxs-lookup"><span data-stu-id="3b817-120">Allow functionality but generate logs.</span></span>|
|<span data-ttu-id="3b817-121">blockDiskModification</span><span class="sxs-lookup"><span data-stu-id="3b817-121">blockDiskModification</span></span>|<span data-ttu-id="3b817-122">3</span><span class="sxs-lookup"><span data-stu-id="3b817-122">3</span></span>|<span data-ttu-id="3b817-123">Bloquear las aplicaciones que no se confía escribir en sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="3b817-123">Block untrusted apps from writing to disk sectors.</span></span>|
|<span data-ttu-id="3b817-124">auditDiskModification</span><span class="sxs-lookup"><span data-stu-id="3b817-124">auditDiskModification</span></span>|<span data-ttu-id="3b817-125">4</span><span class="sxs-lookup"><span data-stu-id="3b817-125">4</span></span>|<span data-ttu-id="3b817-126">Generar registros al escriben aplicaciones que no se confía a sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="3b817-126">Generate logs when untrusted apps write to disk sectors.</span></span>|





