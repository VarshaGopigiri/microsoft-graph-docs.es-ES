---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
ms.openlocfilehash: 59bc1aa080f84fdd25a2da26ec9e7ff9aba20641
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084792"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="06212-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="06212-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="06212-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06212-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06212-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06212-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="06212-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="06212-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06212-107">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="06212-107">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="06212-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="06212-108">Members</span></span>
|<span data-ttu-id="06212-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="06212-109">Member</span></span>|<span data-ttu-id="06212-110">Valor</span><span class="sxs-lookup"><span data-stu-id="06212-110">Value</span></span>|<span data-ttu-id="06212-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="06212-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="06212-112">Local</span><span class="sxs-lookup"><span data-stu-id="06212-112">onPremises</span></span>|<span data-ttu-id="06212-113">0</span><span class="sxs-lookup"><span data-stu-id="06212-113">0</span></span>|<span data-ttu-id="06212-114">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="06212-114">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="06212-115">hospedado</span><span class="sxs-lookup"><span data-stu-id="06212-115">hosted</span></span>|<span data-ttu-id="06212-116">1</span><span class="sxs-lookup"><span data-stu-id="06212-116">1</span></span>|<span data-ttu-id="06212-117">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="06212-117">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="06212-118">serviceToService</span><span class="sxs-lookup"><span data-stu-id="06212-118">serviceToService</span></span>|<span data-ttu-id="06212-119">2</span><span class="sxs-lookup"><span data-stu-id="06212-119">2</span></span>|<span data-ttu-id="06212-120">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="06212-120">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="06212-121">dedicada</span><span class="sxs-lookup"><span data-stu-id="06212-121">dedicated</span></span>|<span data-ttu-id="06212-122">3</span><span class="sxs-lookup"><span data-stu-id="06212-122">3</span></span>|<span data-ttu-id="06212-123">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="06212-123">Connects to O365 Dedicated Exchange environment.</span></span>|





