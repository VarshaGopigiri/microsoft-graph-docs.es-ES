---
title: tipo de enumeración defenderCloudBlockLevelType
description: Posibles valores de nivel de bloque en la nube
author: tfitzmac
ms.openlocfilehash: 19c101cc82673009a39d6545f7340fabf65b287a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326617"
---
# <a name="defendercloudblockleveltype-enum-type"></a><span data-ttu-id="ffd92-103">tipo de enumeración defenderCloudBlockLevelType</span><span class="sxs-lookup"><span data-stu-id="ffd92-103">defenderCloudBlockLevelType enum type</span></span>

> <span data-ttu-id="ffd92-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffd92-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffd92-105">Posibles valores de nivel de bloque en la nube</span><span class="sxs-lookup"><span data-stu-id="ffd92-105">Possible values of Cloud Block Level</span></span>
## <a name="members"></a><span data-ttu-id="ffd92-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ffd92-106">Members</span></span>
|<span data-ttu-id="ffd92-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ffd92-107">Member</span></span>|<span data-ttu-id="ffd92-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ffd92-108">Value</span></span>|<span data-ttu-id="ffd92-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffd92-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ffd92-110">No configurado</span><span class="sxs-lookup"><span data-stu-id="ffd92-110">notConfigured</span></span>|<span data-ttu-id="ffd92-111">0</span><span class="sxs-lookup"><span data-stu-id="ffd92-111">0</span></span>|<span data-ttu-id="ffd92-112">Valor predeterminado, se utiliza el bloqueo de Windows Defender Antivirus predeterminado de nivel y se proporciona una detección de segura sin aumentar el riesgo de detectar legítimos archivos</span><span class="sxs-lookup"><span data-stu-id="ffd92-112">Default value, uses the default Windows Defender Antivirus blocking level and provides strong detection without increasing the risk of detecting legitimate files</span></span>|
|<span data-ttu-id="ffd92-113">alta</span><span class="sxs-lookup"><span data-stu-id="ffd92-113">high</span></span>|<span data-ttu-id="ffd92-114">1</span><span class="sxs-lookup"><span data-stu-id="ffd92-114">1</span></span>|<span data-ttu-id="ffd92-115">Alta aplica a un alto nivel de detección.</span><span class="sxs-lookup"><span data-stu-id="ffd92-115">High applies a strong level of detection.</span></span>|
|<span data-ttu-id="ffd92-116">highPlus</span><span class="sxs-lookup"><span data-stu-id="ffd92-116">highPlus</span></span>|<span data-ttu-id="ffd92-117">2</span><span class="sxs-lookup"><span data-stu-id="ffd92-117">2</span></span>|<span data-ttu-id="ffd92-118">Alta + utiliza el nivel alto y se aplica a las medidas de protección de adición</span><span class="sxs-lookup"><span data-stu-id="ffd92-118">High + uses the High level and applies addition protection measures</span></span>|
|<span data-ttu-id="ffd92-119">zeroTolerance</span><span class="sxs-lookup"><span data-stu-id="ffd92-119">zeroTolerance</span></span>|<span data-ttu-id="ffd92-120">3</span><span class="sxs-lookup"><span data-stu-id="ffd92-120">3</span></span>|<span data-ttu-id="ffd92-121">Cero tolerancia bloquea todos los archivos ejecutables desconocidos</span><span class="sxs-lookup"><span data-stu-id="ffd92-121">Zero tolerance blocks all unknown executables</span></span>|



