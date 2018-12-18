---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
ms.openlocfilehash: b8ab119c58aec6e62c0a32ccf310f43eab029573
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343592"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="10d5c-103">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="10d5c-103">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="10d5c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="10d5c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="10d5c-105">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="10d5c-105">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="10d5c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="10d5c-106">Members</span></span>
|<span data-ttu-id="10d5c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="10d5c-107">Member</span></span>|<span data-ttu-id="10d5c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="10d5c-108">Value</span></span>|<span data-ttu-id="10d5c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="10d5c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="10d5c-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="10d5c-110">deviceDefault</span></span>|<span data-ttu-id="10d5c-111">0</span><span class="sxs-lookup"><span data-stu-id="10d5c-111">0</span></span>|<span data-ttu-id="10d5c-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="10d5c-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="10d5c-113">ninguno</span><span class="sxs-lookup"><span data-stu-id="10d5c-113">none</span></span>|<span data-ttu-id="10d5c-114">1</span><span class="sxs-lookup"><span data-stu-id="10d5c-114">1</span></span>|<span data-ttu-id="10d5c-115">No se ha codificado clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="10d5c-115">Preshared key is not encoded.</span></span> <span data-ttu-id="10d5c-116">En su lugar, se guarda en su formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="10d5c-116">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="10d5c-117">utF8</span><span class="sxs-lookup"><span data-stu-id="10d5c-117">utF8</span></span>|<span data-ttu-id="10d5c-118">2</span><span class="sxs-lookup"><span data-stu-id="10d5c-118">2</span></span>|<span data-ttu-id="10d5c-119">Codificar la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="10d5c-119">Encode the preshared key using UTF-8</span></span>|



