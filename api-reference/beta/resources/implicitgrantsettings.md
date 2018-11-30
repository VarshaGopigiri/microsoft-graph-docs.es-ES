---
title: tipo de recurso implicitGrantSettings
description: Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita. Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes. Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.
ms.openlocfilehash: 018cd422b56724811e1913ff0e94aea16d7c68f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085474"
---
# <a name="implicitgrantsettings-resource-type"></a><span data-ttu-id="a41fb-105">tipo de recurso implicitGrantSettings</span><span class="sxs-lookup"><span data-stu-id="a41fb-105">implicitGrantSettings resource type</span></span>

> <span data-ttu-id="a41fb-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a41fb-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a41fb-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a41fb-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a41fb-108">Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="a41fb-108">Specifies whether this web application can request tokens using the OAuth 2.0 implicit flow.</span></span> <span data-ttu-id="a41fb-109">Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes.</span><span class="sxs-lookup"><span data-stu-id="a41fb-109">Separate properties are available to request ID and access tokens as part of the implicit flow.</span></span> <span data-ttu-id="a41fb-110">Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.</span><span class="sxs-lookup"><span data-stu-id="a41fb-110">To enable implicit flow, at least one of the following properties must be set to true.</span></span>

## <a name="properties"></a><span data-ttu-id="a41fb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a41fb-111">Properties</span></span>

| <span data-ttu-id="a41fb-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a41fb-112">Property</span></span> | <span data-ttu-id="a41fb-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="a41fb-113">Type</span></span> | <span data-ttu-id="a41fb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a41fb-114">Description</span></span> |
|:---------|:-----|:------------|
|<span data-ttu-id="a41fb-115">enableIdTokenIssuance</span><span class="sxs-lookup"><span data-stu-id="a41fb-115">enableIdTokenIssuance</span></span>| <span data-ttu-id="a41fb-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="a41fb-116">Boolean</span></span> | <span data-ttu-id="a41fb-117">Especifica si esta aplicación web puede solicitar un token de identificador con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="a41fb-117">Specifies whether this web application can request an ID token using the OAuth 2.0 implicit flow.</span></span>|
|<span data-ttu-id="a41fb-118">enableAccessTokenIssuance</span><span class="sxs-lookup"><span data-stu-id="a41fb-118">enableAccessTokenIssuance</span></span>| <span data-ttu-id="a41fb-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="a41fb-119">Boolean</span></span> | <span data-ttu-id="a41fb-120">Especifica si esta aplicación web puede solicitar un token de acceso con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="a41fb-120">Specifies whether this web application can request an access token using the OAuth 2.0 implicit flow.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a41fb-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a41fb-121">JSON representation</span></span>
<span data-ttu-id="a41fb-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a41fb-122">Here is a JSON representation of the resource.</span></span>

```json
{
  "enableIdTokenIssuance": "Boolean",
  "enableAccessTokenIssuance": "Boolean"
}

```
