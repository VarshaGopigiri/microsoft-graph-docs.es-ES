---
title: tipo de recurso onPremisesPublishing
description: Aquí tiene una representación JSON del recurso.
ms.openlocfilehash: 8dba505347fc12d3c4a8521ebe32551d738dc4a2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087026"
---
# <a name="onpremisespublishing-resource-type"></a><span data-ttu-id="8cdf6-103">tipo de recurso onPremisesPublishing</span><span class="sxs-lookup"><span data-stu-id="8cdf6-103">onPremisesPublishing resource type</span></span>

> <span data-ttu-id="8cdf6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8cdf6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="8cdf6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8cdf6-106">Properties</span></span>
| <span data-ttu-id="8cdf6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8cdf6-107">Property</span></span>     | <span data-ttu-id="8cdf6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8cdf6-108">Type</span></span>   |<span data-ttu-id="8cdf6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cdf6-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8cdf6-110">customDomainCertificate</span><span class="sxs-lookup"><span data-stu-id="8cdf6-110">customDomainCertificate</span></span>|<span data-ttu-id="8cdf6-111">String</span><span class="sxs-lookup"><span data-stu-id="8cdf6-111">String</span></span>|<span data-ttu-id="8cdf6-112">Detalles del certificado asociado a la aplicación cuando un dominio personalizado está en uso.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-112">Details of the certificate associated with the applicaiton when a custom domain is in use.</span></span> <span data-ttu-id="8cdf6-113">NULL cuando se usa el dominio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-113">Null when using the default domain.</span></span>|
|<span data-ttu-id="8cdf6-114">externalAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8cdf6-114">externalAuthenticationType</span></span>|<span data-ttu-id="8cdf6-115">String</span><span class="sxs-lookup"><span data-stu-id="8cdf6-115">String</span></span>|<span data-ttu-id="8cdf6-116">Se explica la configuración de la autenticación previa para la aplicación de los valores posibles es: `passthru`, `aadPreAuthentication`.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-116">Details the pre-authentication setting for the application Possible values are: `passthru`, `aadPreAuthentication`.</span></span>|
|<span data-ttu-id="8cdf6-117">externalUrl</span><span class="sxs-lookup"><span data-stu-id="8cdf6-117">externalUrl</span></span>|<span data-ttu-id="8cdf6-118">String</span><span class="sxs-lookup"><span data-stu-id="8cdf6-118">String</span></span>|<span data-ttu-id="8cdf6-119">La dirección de url externa publicado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-119">The published external url for the application.</span></span> <span data-ttu-id="8cdf6-120">Por ejemplohttps://intranet-contoso.msappproxy.net/</span><span class="sxs-lookup"><span data-stu-id="8cdf6-120">For example https://intranet-contoso.msappproxy.net/</span></span>  |
|<span data-ttu-id="8cdf6-121">internalUrl</span><span class="sxs-lookup"><span data-stu-id="8cdf6-121">internalUrl</span></span>|<span data-ttu-id="8cdf6-122">String</span><span class="sxs-lookup"><span data-stu-id="8cdf6-122">String</span></span>|<span data-ttu-id="8cdf6-123">La dirección url interna de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-123">The internal url of the application.</span></span> <span data-ttu-id="8cdf6-124">Por ejemplohttps://intranet/</span><span class="sxs-lookup"><span data-stu-id="8cdf6-124">For example https://intranet/</span></span> |
|<span data-ttu-id="8cdf6-125">isOnPremPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="8cdf6-125">isOnPremPublishingEnabled</span></span>|<span data-ttu-id="8cdf6-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="8cdf6-126">Boolean</span></span>|<span data-ttu-id="8cdf6-127">Indica si la aplicación se publica actualmente o no.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-127">Indicates if the application is currently being published or not.</span></span>|
|<span data-ttu-id="8cdf6-128">applicationServerTimeout</span><span class="sxs-lookup"><span data-stu-id="8cdf6-128">applicationServerTimeout</span></span>|<span data-ttu-id="8cdf6-129">String</span><span class="sxs-lookup"><span data-stu-id="8cdf6-129">String</span></span>|<span data-ttu-id="8cdf6-130">La duración el conector esperará una respuesta de la aplicación back-end antes de cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-130">The duration the connector will wait for a response from the backend application before closing the connection.</span></span> <span data-ttu-id="8cdf6-131">Los valores posibles son `default`, `long`.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-131">Possible values are `default`, `long`.</span></span> <span data-ttu-id="8cdf6-132">Uso `long` si su servidor tarda más de 75 de 60 segundos para responder a las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-132">Use `long` if your server takes more than 60-75 seconds to respond to requests.</span></span> <span data-ttu-id="8cdf6-133">Intente también `long` si no puede tener acceso a la aplicación y el estado de error es "Backend Timeout".</span><span class="sxs-lookup"><span data-stu-id="8cdf6-133">Also try `long` if you are unable to access the application and the error status is "Backend Timeout".</span></span>|
|<span data-ttu-id="8cdf6-134">isTranslateHostHeaderEnabled</span><span class="sxs-lookup"><span data-stu-id="8cdf6-134">isTranslateHostHeaderEnabled</span></span>|<span data-ttu-id="8cdf6-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="8cdf6-135">Boolean</span></span>|<span data-ttu-id="8cdf6-136">Indica si la aplicación debe traducir las direcciones URL en los encabezados de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-136">Indicates if the application should translate urls in the reponse headers.</span></span> <span data-ttu-id="8cdf6-137">Esto incluye la configuración del sitio correcto para las cookies.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-137">This includes setting the correct site for cookies.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8cdf6-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8cdf6-138">JSON representation</span></span>

<span data-ttu-id="8cdf6-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8cdf6-139">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesPublishing"
}-->

```json
{
  "customDomainCertificate": "String",
  "externalAuthenticationType": "String",
  "externalUrl": "String",
  "internalUrl": "String",
  "isOnPremPublishingEnabled": true,
  "applicationServerTimeout": "String",
  "isTranslateHostHeaderEnabled": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesPublishing resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
