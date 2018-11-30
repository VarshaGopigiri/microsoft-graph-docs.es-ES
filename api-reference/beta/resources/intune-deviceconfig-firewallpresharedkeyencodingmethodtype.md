---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
ms.openlocfilehash: 3f6d4a88ec4f0296bfd0d35f30695ddae14d4c95
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083203"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="ebdfc-103">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="ebdfc-103">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="ebdfc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ebdfc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ebdfc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ebdfc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ebdfc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebdfc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebdfc-107">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="ebdfc-107">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="ebdfc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ebdfc-108">Members</span></span>
|<span data-ttu-id="ebdfc-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ebdfc-109">Member</span></span>|<span data-ttu-id="ebdfc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ebdfc-110">Value</span></span>|<span data-ttu-id="ebdfc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebdfc-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ebdfc-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="ebdfc-112">deviceDefault</span></span>|<span data-ttu-id="ebdfc-113">0</span><span class="sxs-lookup"><span data-stu-id="ebdfc-113">0</span></span>|<span data-ttu-id="ebdfc-114">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="ebdfc-114">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="ebdfc-115">ninguno</span><span class="sxs-lookup"><span data-stu-id="ebdfc-115">none</span></span>|<span data-ttu-id="ebdfc-116">1</span><span class="sxs-lookup"><span data-stu-id="ebdfc-116">1</span></span>|<span data-ttu-id="ebdfc-117">No se ha codificado clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="ebdfc-117">Preshared key is not encoded.</span></span> <span data-ttu-id="ebdfc-118">En su lugar, se guarda en su formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="ebdfc-118">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="ebdfc-119">utF8</span><span class="sxs-lookup"><span data-stu-id="ebdfc-119">utF8</span></span>|<span data-ttu-id="ebdfc-120">2</span><span class="sxs-lookup"><span data-stu-id="ebdfc-120">2</span></span>|<span data-ttu-id="ebdfc-121">Codificar la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="ebdfc-121">Encode the preshared key using UTF-8</span></span>|





