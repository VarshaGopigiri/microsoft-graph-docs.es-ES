---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
ms.openlocfilehash: 238d2b0845b0d79ea109cea5b326914815d600de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030798"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="ddf4a-103">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="ddf4a-103">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="ddf4a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ddf4a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ddf4a-105">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="ddf4a-105">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="ddf4a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddf4a-106">Members</span></span>
|<span data-ttu-id="ddf4a-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ddf4a-107">Member</span></span>|<span data-ttu-id="ddf4a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf4a-108">Value</span></span>|<span data-ttu-id="ddf4a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddf4a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ddf4a-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="ddf4a-110">deviceDefault</span></span>|<span data-ttu-id="ddf4a-111">0</span><span class="sxs-lookup"><span data-stu-id="ddf4a-111">0</span></span>|<span data-ttu-id="ddf4a-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="ddf4a-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="ddf4a-113">ninguno</span><span class="sxs-lookup"><span data-stu-id="ddf4a-113">none</span></span>|<span data-ttu-id="ddf4a-114">1</span><span class="sxs-lookup"><span data-stu-id="ddf4a-114">1</span></span>|<span data-ttu-id="ddf4a-115">No se ha codificado clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="ddf4a-115">Preshared key is not encoded.</span></span> <span data-ttu-id="ddf4a-116">En su lugar, se guarda en su formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="ddf4a-116">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="ddf4a-117">utF8</span><span class="sxs-lookup"><span data-stu-id="ddf4a-117">utF8</span></span>|<span data-ttu-id="ddf4a-118">2</span><span class="sxs-lookup"><span data-stu-id="ddf4a-118">2</span></span>|<span data-ttu-id="ddf4a-119">Codificar la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="ddf4a-119">Encode the preshared key using UTF-8</span></span>|



