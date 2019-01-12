---
title: tipo de enumeración firewallPreSharedKeyEncodingMethodType
description: Valores posibles para firewallPreSharedKeyEncodingMethod
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 513a6c545fedc73add4e710ed784ef223d1f8539
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976355"
---
# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="83e2a-103">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="83e2a-103">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="83e2a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="83e2a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="83e2a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="83e2a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="83e2a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="83e2a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="83e2a-107">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="83e2a-107">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="83e2a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="83e2a-108">Members</span></span>
|<span data-ttu-id="83e2a-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="83e2a-109">Member</span></span>|<span data-ttu-id="83e2a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="83e2a-110">Value</span></span>|<span data-ttu-id="83e2a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="83e2a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="83e2a-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="83e2a-112">deviceDefault</span></span>|<span data-ttu-id="83e2a-113">0</span><span class="sxs-lookup"><span data-stu-id="83e2a-113">0</span></span>|<span data-ttu-id="83e2a-114">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="83e2a-114">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="83e2a-115">none</span><span class="sxs-lookup"><span data-stu-id="83e2a-115">none</span></span>|<span data-ttu-id="83e2a-116">1</span><span class="sxs-lookup"><span data-stu-id="83e2a-116">1</span></span>|<span data-ttu-id="83e2a-117">No se ha codificado clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="83e2a-117">Preshared key is not encoded.</span></span> <span data-ttu-id="83e2a-118">En su lugar, se guarda en su formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="83e2a-118">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="83e2a-119">utF8</span><span class="sxs-lookup"><span data-stu-id="83e2a-119">utF8</span></span>|<span data-ttu-id="83e2a-120">2</span><span class="sxs-lookup"><span data-stu-id="83e2a-120">2</span></span>|<span data-ttu-id="83e2a-121">Codificar la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="83e2a-121">Encode the preshared key using UTF-8</span></span>|





