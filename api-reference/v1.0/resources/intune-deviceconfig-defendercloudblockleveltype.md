---
title: tipo de enumeración defenderCloudBlockLevelType
description: Posibles valores de nivel de bloque en la nube
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 283bb12c775b1215a1bcfecf4f248882a56573aa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839504"
---
# <a name="defendercloudblockleveltype-enum-type"></a><span data-ttu-id="1b93c-103">tipo de enumeración defenderCloudBlockLevelType</span><span class="sxs-lookup"><span data-stu-id="1b93c-103">defenderCloudBlockLevelType enum type</span></span>

> <span data-ttu-id="1b93c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1b93c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1b93c-105">Posibles valores de nivel de bloque en la nube</span><span class="sxs-lookup"><span data-stu-id="1b93c-105">Possible values of Cloud Block Level</span></span>
## <a name="members"></a><span data-ttu-id="1b93c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b93c-106">Members</span></span>
|<span data-ttu-id="1b93c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="1b93c-107">Member</span></span>|<span data-ttu-id="1b93c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1b93c-108">Value</span></span>|<span data-ttu-id="1b93c-109">Description</span><span class="sxs-lookup"><span data-stu-id="1b93c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1b93c-110">No configurado</span><span class="sxs-lookup"><span data-stu-id="1b93c-110">notConfigured</span></span>|<span data-ttu-id="1b93c-111">0</span><span class="sxs-lookup"><span data-stu-id="1b93c-111">0</span></span>|<span data-ttu-id="1b93c-112">Valor predeterminado, se utiliza el bloqueo de Windows Defender Antivirus predeterminado de nivel y se proporciona una detección de segura sin aumentar el riesgo de detectar legítimos archivos</span><span class="sxs-lookup"><span data-stu-id="1b93c-112">Default value, uses the default Windows Defender Antivirus blocking level and provides strong detection without increasing the risk of detecting legitimate files</span></span>|
|<span data-ttu-id="1b93c-113">alta</span><span class="sxs-lookup"><span data-stu-id="1b93c-113">high</span></span>|<span data-ttu-id="1b93c-114">1</span><span class="sxs-lookup"><span data-stu-id="1b93c-114">1</span></span>|<span data-ttu-id="1b93c-115">Alta aplica a un alto nivel de detección.</span><span class="sxs-lookup"><span data-stu-id="1b93c-115">High applies a strong level of detection.</span></span>|
|<span data-ttu-id="1b93c-116">highPlus</span><span class="sxs-lookup"><span data-stu-id="1b93c-116">highPlus</span></span>|<span data-ttu-id="1b93c-117">2</span><span class="sxs-lookup"><span data-stu-id="1b93c-117">2</span></span>|<span data-ttu-id="1b93c-118">Alta + utiliza el nivel alto y se aplica a las medidas de protección de adición</span><span class="sxs-lookup"><span data-stu-id="1b93c-118">High + uses the High level and applies addition protection measures</span></span>|
|<span data-ttu-id="1b93c-119">zeroTolerance</span><span class="sxs-lookup"><span data-stu-id="1b93c-119">zeroTolerance</span></span>|<span data-ttu-id="1b93c-120">3</span><span class="sxs-lookup"><span data-stu-id="1b93c-120">3</span></span>|<span data-ttu-id="1b93c-121">Cero tolerancia bloquea todos los archivos ejecutables desconocidos</span><span class="sxs-lookup"><span data-stu-id="1b93c-121">Zero tolerance blocks all unknown executables</span></span>|



