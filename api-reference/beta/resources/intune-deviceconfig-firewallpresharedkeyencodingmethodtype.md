---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2dd5eb58c4fe2e8729ab1adc4aa55ad0c701157f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862156"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="939d6-103">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="939d6-103">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="939d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="939d6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="939d6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="939d6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="939d6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="939d6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="939d6-107">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="939d6-107">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="939d6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="939d6-108">Members</span></span>
|<span data-ttu-id="939d6-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="939d6-109">Member</span></span>|<span data-ttu-id="939d6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="939d6-110">Value</span></span>|<span data-ttu-id="939d6-111">Description</span><span class="sxs-lookup"><span data-stu-id="939d6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="939d6-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="939d6-112">deviceDefault</span></span>|<span data-ttu-id="939d6-113">0</span><span class="sxs-lookup"><span data-stu-id="939d6-113">0</span></span>|<span data-ttu-id="939d6-114">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="939d6-114">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="939d6-115">none</span><span class="sxs-lookup"><span data-stu-id="939d6-115">none</span></span>|<span data-ttu-id="939d6-116">1</span><span class="sxs-lookup"><span data-stu-id="939d6-116">1</span></span>|<span data-ttu-id="939d6-117">No se ha codificado clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="939d6-117">Preshared key is not encoded.</span></span> <span data-ttu-id="939d6-118">En su lugar, se guarda en su formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="939d6-118">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="939d6-119">utF8</span><span class="sxs-lookup"><span data-stu-id="939d6-119">utF8</span></span>|<span data-ttu-id="939d6-120">2</span><span class="sxs-lookup"><span data-stu-id="939d6-120">2</span></span>|<span data-ttu-id="939d6-121">Codificar la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="939d6-121">Encode the preshared key using UTF-8</span></span>|





