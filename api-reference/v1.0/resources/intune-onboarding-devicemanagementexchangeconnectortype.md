---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8e9e50a4475ca2d57b3f38567703046588d4fb3c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986435"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="fb17b-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="fb17b-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="fb17b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb17b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb17b-105">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fb17b-105">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="fb17b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb17b-106">Members</span></span>
|<span data-ttu-id="fb17b-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="fb17b-107">Member</span></span>|<span data-ttu-id="fb17b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fb17b-108">Value</span></span>|<span data-ttu-id="fb17b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb17b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb17b-110">Local</span><span class="sxs-lookup"><span data-stu-id="fb17b-110">onPremises</span></span>|<span data-ttu-id="fb17b-111">0</span><span class="sxs-lookup"><span data-stu-id="fb17b-111">0</span></span>|<span data-ttu-id="fb17b-112">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="fb17b-112">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="fb17b-113">hospedado</span><span class="sxs-lookup"><span data-stu-id="fb17b-113">hosted</span></span>|<span data-ttu-id="fb17b-114">1</span><span class="sxs-lookup"><span data-stu-id="fb17b-114">1</span></span>|<span data-ttu-id="fb17b-115">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="fb17b-115">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="fb17b-116">serviceToService</span><span class="sxs-lookup"><span data-stu-id="fb17b-116">serviceToService</span></span>|<span data-ttu-id="fb17b-117">2</span><span class="sxs-lookup"><span data-stu-id="fb17b-117">2</span></span>|<span data-ttu-id="fb17b-118">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="fb17b-118">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="fb17b-119">dedicada</span><span class="sxs-lookup"><span data-stu-id="fb17b-119">dedicated</span></span>|<span data-ttu-id="fb17b-120">3</span><span class="sxs-lookup"><span data-stu-id="fb17b-120">3</span></span>|<span data-ttu-id="fb17b-121">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="fb17b-121">Connects to O365 Dedicated Exchange environment.</span></span>|



