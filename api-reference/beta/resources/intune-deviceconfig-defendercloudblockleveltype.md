---
title: tipo de enumeración defenderCloudBlockLevelType
description: Posibles valores de nivel de bloque en la nube
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 13f8828478eb063eaa25d8561d5a254c86f4b856
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924723"
---
# <a name="defendercloudblockleveltype-enum-type"></a><span data-ttu-id="3e19d-103">tipo de enumeración defenderCloudBlockLevelType</span><span class="sxs-lookup"><span data-stu-id="3e19d-103">defenderCloudBlockLevelType enum type</span></span>

> <span data-ttu-id="3e19d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3e19d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3e19d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3e19d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3e19d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3e19d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3e19d-107">Posibles valores de nivel de bloque en la nube</span><span class="sxs-lookup"><span data-stu-id="3e19d-107">Possible values of Cloud Block Level</span></span>
## <a name="members"></a><span data-ttu-id="3e19d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e19d-108">Members</span></span>
|<span data-ttu-id="3e19d-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="3e19d-109">Member</span></span>|<span data-ttu-id="3e19d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3e19d-110">Value</span></span>|<span data-ttu-id="3e19d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e19d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3e19d-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="3e19d-112">notConfigured</span></span>|<span data-ttu-id="3e19d-113">0</span><span class="sxs-lookup"><span data-stu-id="3e19d-113">0</span></span>|<span data-ttu-id="3e19d-114">Valor predeterminado, se utiliza el bloqueo de Windows Defender Antivirus predeterminado de nivel y se proporciona una detección de segura sin aumentar el riesgo de detectar legítimos archivos</span><span class="sxs-lookup"><span data-stu-id="3e19d-114">Default value, uses the default Windows Defender Antivirus blocking level and provides strong detection without increasing the risk of detecting legitimate files</span></span>|
|<span data-ttu-id="3e19d-115">alta</span><span class="sxs-lookup"><span data-stu-id="3e19d-115">high</span></span>|<span data-ttu-id="3e19d-116">1</span><span class="sxs-lookup"><span data-stu-id="3e19d-116">1</span></span>|<span data-ttu-id="3e19d-117">Alta aplica a un alto nivel de detección.</span><span class="sxs-lookup"><span data-stu-id="3e19d-117">High applies a strong level of detection.</span></span>|
|<span data-ttu-id="3e19d-118">highPlus</span><span class="sxs-lookup"><span data-stu-id="3e19d-118">highPlus</span></span>|<span data-ttu-id="3e19d-119">2</span><span class="sxs-lookup"><span data-stu-id="3e19d-119">2</span></span>|<span data-ttu-id="3e19d-120">Alta + utiliza el nivel alto y se aplica a las medidas de protección de adición</span><span class="sxs-lookup"><span data-stu-id="3e19d-120">High + uses the High level and applies addition protection measures</span></span>|
|<span data-ttu-id="3e19d-121">zeroTolerance</span><span class="sxs-lookup"><span data-stu-id="3e19d-121">zeroTolerance</span></span>|<span data-ttu-id="3e19d-122">3</span><span class="sxs-lookup"><span data-stu-id="3e19d-122">3</span></span>|<span data-ttu-id="3e19d-123">Cero tolerancia bloquea todos los archivos ejecutables desconocidos</span><span class="sxs-lookup"><span data-stu-id="3e19d-123">Zero tolerance blocks all unknown executables</span></span>|





