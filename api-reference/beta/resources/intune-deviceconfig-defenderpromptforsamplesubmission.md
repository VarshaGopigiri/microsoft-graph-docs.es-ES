---
title: tipo de enumeración defenderPromptForSampleSubmission
description: Valores posibles para solicitar información de usuario para el envío de ejemplos.
author: tfitzmac
ms.openlocfilehash: 19498f587759df56ae671b119b59abe7e7acd62c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314934"
---
# <a name="defenderpromptforsamplesubmission-enum-type"></a><span data-ttu-id="f6cd9-103">tipo de enumeración defenderPromptForSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="f6cd9-103">defenderPromptForSampleSubmission enum type</span></span>

> <span data-ttu-id="f6cd9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6cd9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f6cd9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6cd9-107">Valores posibles para solicitar información de usuario para el envío de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-107">Possible values for prompting user for samples submission.</span></span>
## <a name="members"></a><span data-ttu-id="f6cd9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6cd9-108">Members</span></span>
|<span data-ttu-id="f6cd9-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="f6cd9-109">Member</span></span>|<span data-ttu-id="f6cd9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f6cd9-110">Value</span></span>|<span data-ttu-id="f6cd9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6cd9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6cd9-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="f6cd9-112">userDefined</span></span>|<span data-ttu-id="f6cd9-113">0</span><span class="sxs-lookup"><span data-stu-id="f6cd9-113">0</span></span>|<span data-ttu-id="f6cd9-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="f6cd9-115">alwaysPrompt</span><span class="sxs-lookup"><span data-stu-id="f6cd9-115">alwaysPrompt</span></span>|<span data-ttu-id="f6cd9-116">1</span><span class="sxs-lookup"><span data-stu-id="f6cd9-116">1</span></span>|<span data-ttu-id="f6cd9-117">Preguntar siempre.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-117">Always prompt.</span></span>|
|<span data-ttu-id="f6cd9-118">promptBeforeSendingPersonalData</span><span class="sxs-lookup"><span data-stu-id="f6cd9-118">promptBeforeSendingPersonalData</span></span>|<span data-ttu-id="f6cd9-119">2</span><span class="sxs-lookup"><span data-stu-id="f6cd9-119">2</span></span>|<span data-ttu-id="f6cd9-120">Preguntar antes de enviar datos personales.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-120">Prompt before sending personal data.</span></span>|
|<span data-ttu-id="f6cd9-121">neverSendData</span><span class="sxs-lookup"><span data-stu-id="f6cd9-121">neverSendData</span></span>|<span data-ttu-id="f6cd9-122">3</span><span class="sxs-lookup"><span data-stu-id="f6cd9-122">3</span></span>|<span data-ttu-id="f6cd9-123">No enviar nunca datos.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-123">Never send data.</span></span>|
|<span data-ttu-id="f6cd9-124">sendAllDataWithoutPrompting</span><span class="sxs-lookup"><span data-stu-id="f6cd9-124">sendAllDataWithoutPrompting</span></span>|<span data-ttu-id="f6cd9-125">4</span><span class="sxs-lookup"><span data-stu-id="f6cd9-125">4</span></span>|<span data-ttu-id="f6cd9-126">Enviar todos los datos sin preguntar.</span><span class="sxs-lookup"><span data-stu-id="f6cd9-126">Send all data without prompting.</span></span>|





