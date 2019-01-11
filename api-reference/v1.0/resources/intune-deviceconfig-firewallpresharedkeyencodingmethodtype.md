---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bba6033985f2b960a272134614d98acc7203a9d8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871753"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="933ad-103">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="933ad-103">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="933ad-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="933ad-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="933ad-105">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="933ad-105">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="933ad-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="933ad-106">Members</span></span>
|<span data-ttu-id="933ad-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="933ad-107">Member</span></span>|<span data-ttu-id="933ad-108">Valor</span><span class="sxs-lookup"><span data-stu-id="933ad-108">Value</span></span>|<span data-ttu-id="933ad-109">Description</span><span class="sxs-lookup"><span data-stu-id="933ad-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="933ad-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="933ad-110">deviceDefault</span></span>|<span data-ttu-id="933ad-111">0</span><span class="sxs-lookup"><span data-stu-id="933ad-111">0</span></span>|<span data-ttu-id="933ad-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="933ad-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="933ad-113">none</span><span class="sxs-lookup"><span data-stu-id="933ad-113">none</span></span>|<span data-ttu-id="933ad-114">1</span><span class="sxs-lookup"><span data-stu-id="933ad-114">1</span></span>|<span data-ttu-id="933ad-115">No se ha codificado clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="933ad-115">Preshared key is not encoded.</span></span> <span data-ttu-id="933ad-116">En su lugar, se guarda en su formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="933ad-116">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="933ad-117">utF8</span><span class="sxs-lookup"><span data-stu-id="933ad-117">utF8</span></span>|<span data-ttu-id="933ad-118">2</span><span class="sxs-lookup"><span data-stu-id="933ad-118">2</span></span>|<span data-ttu-id="933ad-119">Codificar la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="933ad-119">Encode the preshared key using UTF-8</span></span>|



