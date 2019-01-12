---
title: tipo de enumeración mobileAppPublishingState
description: Indica el estado de publicación de una aplicación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6b2ae893a0c971bfa0a80a09bb8e7c80b6146555
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932822"
---
# <a name="mobileapppublishingstate-enum-type"></a><span data-ttu-id="5bcf3-103">tipo de enumeración mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="5bcf3-103">mobileAppPublishingState enum type</span></span>

> <span data-ttu-id="5bcf3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5bcf3-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5bcf3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5bcf3-107">Indica el estado de publicación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-107">Indicates the publishing state of an app.</span></span>
## <a name="members"></a><span data-ttu-id="5bcf3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5bcf3-108">Members</span></span>
|<span data-ttu-id="5bcf3-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5bcf3-109">Member</span></span>|<span data-ttu-id="5bcf3-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcf3-110">Value</span></span>|<span data-ttu-id="5bcf3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bcf3-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5bcf3-112">notPublished</span><span class="sxs-lookup"><span data-stu-id="5bcf3-112">notPublished</span></span>|<span data-ttu-id="5bcf3-113">0</span><span class="sxs-lookup"><span data-stu-id="5bcf3-113">0</span></span>|<span data-ttu-id="5bcf3-114">La aplicación no se ha publicado aún.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-114">The app is not yet published.</span></span>|
|<span data-ttu-id="5bcf3-115">procesamiento</span><span class="sxs-lookup"><span data-stu-id="5bcf3-115">processing</span></span>|<span data-ttu-id="5bcf3-116">1</span><span class="sxs-lookup"><span data-stu-id="5bcf3-116">1</span></span>|<span data-ttu-id="5bcf3-117">La aplicación está pendiente de procesamiento del servicio.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-117">The app is pending service-side processing.</span></span>|
|<span data-ttu-id="5bcf3-118">publicado</span><span class="sxs-lookup"><span data-stu-id="5bcf3-118">published</span></span>|<span data-ttu-id="5bcf3-119">2</span><span class="sxs-lookup"><span data-stu-id="5bcf3-119">2</span></span>|<span data-ttu-id="5bcf3-120">Se publica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5bcf3-120">The app is published.</span></span>|





