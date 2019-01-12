---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c05410c3b3b7c889840d0b47aca05f6457564eb4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934957"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="58384-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="58384-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="58384-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58384-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58384-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58384-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="58384-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="58384-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="58384-107">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="58384-107">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="58384-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="58384-108">Members</span></span>
|<span data-ttu-id="58384-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="58384-109">Member</span></span>|<span data-ttu-id="58384-110">Valor</span><span class="sxs-lookup"><span data-stu-id="58384-110">Value</span></span>|<span data-ttu-id="58384-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="58384-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="58384-112">Local</span><span class="sxs-lookup"><span data-stu-id="58384-112">onPremises</span></span>|<span data-ttu-id="58384-113">0</span><span class="sxs-lookup"><span data-stu-id="58384-113">0</span></span>|<span data-ttu-id="58384-114">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="58384-114">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="58384-115">hospedado</span><span class="sxs-lookup"><span data-stu-id="58384-115">hosted</span></span>|<span data-ttu-id="58384-116">1</span><span class="sxs-lookup"><span data-stu-id="58384-116">1</span></span>|<span data-ttu-id="58384-117">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="58384-117">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="58384-118">serviceToService</span><span class="sxs-lookup"><span data-stu-id="58384-118">serviceToService</span></span>|<span data-ttu-id="58384-119">2</span><span class="sxs-lookup"><span data-stu-id="58384-119">2</span></span>|<span data-ttu-id="58384-120">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="58384-120">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="58384-121">dedicada</span><span class="sxs-lookup"><span data-stu-id="58384-121">dedicated</span></span>|<span data-ttu-id="58384-122">3</span><span class="sxs-lookup"><span data-stu-id="58384-122">3</span></span>|<span data-ttu-id="58384-123">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="58384-123">Connects to O365 Dedicated Exchange environment.</span></span>|





