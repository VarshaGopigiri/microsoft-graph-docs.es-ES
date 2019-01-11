---
title: tipo de recurso implicitGrantSettings
description: Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita. Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes. Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.
localization_priority: Normal
ms.openlocfilehash: 93a54ac0c0e4c6c32ebb99c9747d44d75f98af07
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834268"
---
# <a name="implicitgrantsettings-resource-type"></a><span data-ttu-id="fb762-105">tipo de recurso implicitGrantSettings</span><span class="sxs-lookup"><span data-stu-id="fb762-105">implicitGrantSettings resource type</span></span>

> <span data-ttu-id="fb762-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb762-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb762-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb762-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fb762-108">Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="fb762-108">Specifies whether this web application can request tokens using the OAuth 2.0 implicit flow.</span></span> <span data-ttu-id="fb762-109">Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes.</span><span class="sxs-lookup"><span data-stu-id="fb762-109">Separate properties are available to request ID and access tokens as part of the implicit flow.</span></span> <span data-ttu-id="fb762-110">Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.</span><span class="sxs-lookup"><span data-stu-id="fb762-110">To enable implicit flow, at least one of the following properties must be set to true.</span></span>

## <a name="properties"></a><span data-ttu-id="fb762-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb762-111">Properties</span></span>

| <span data-ttu-id="fb762-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb762-112">Property</span></span> | <span data-ttu-id="fb762-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb762-113">Type</span></span> | <span data-ttu-id="fb762-114">Description</span><span class="sxs-lookup"><span data-stu-id="fb762-114">Description</span></span> |
|:---------|:-----|:------------|
|<span data-ttu-id="fb762-115">enableIdTokenIssuance</span><span class="sxs-lookup"><span data-stu-id="fb762-115">enableIdTokenIssuance</span></span>| <span data-ttu-id="fb762-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb762-116">Boolean</span></span> | <span data-ttu-id="fb762-117">Especifica si esta aplicación web puede solicitar un token de identificador con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="fb762-117">Specifies whether this web application can request an ID token using the OAuth 2.0 implicit flow.</span></span>|
|<span data-ttu-id="fb762-118">enableAccessTokenIssuance</span><span class="sxs-lookup"><span data-stu-id="fb762-118">enableAccessTokenIssuance</span></span>| <span data-ttu-id="fb762-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb762-119">Boolean</span></span> | <span data-ttu-id="fb762-120">Especifica si esta aplicación web puede solicitar un token de acceso con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="fb762-120">Specifies whether this web application can request an access token using the OAuth 2.0 implicit flow.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fb762-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb762-121">JSON representation</span></span>
<span data-ttu-id="fb762-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fb762-122">Here is a JSON representation of the resource.</span></span>

```json
{
  "enableIdTokenIssuance": "Boolean",
  "enableAccessTokenIssuance": "Boolean"
}

```
