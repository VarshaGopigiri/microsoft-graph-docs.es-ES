---
title: tipo de recurso Web
description: Especifica la configuración para una aplicación web.
localization_priority: Normal
ms.openlocfilehash: 26efe59eda739597e7193fa1ff79443f3d64b5a7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890205"
---
# <a name="web-resource-type"></a><span data-ttu-id="c360d-103">tipo de recurso Web</span><span class="sxs-lookup"><span data-stu-id="c360d-103">web resource type</span></span>

> <span data-ttu-id="c360d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c360d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c360d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c360d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c360d-106">Especifica la configuración para una aplicación web.</span><span class="sxs-lookup"><span data-stu-id="c360d-106">Specifies settings for a web application.</span></span>

## <a name="properties"></a><span data-ttu-id="c360d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c360d-107">Properties</span></span>

| <span data-ttu-id="c360d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c360d-108">Property</span></span> | <span data-ttu-id="c360d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c360d-109">Type</span></span> | <span data-ttu-id="c360d-110">Description</span><span class="sxs-lookup"><span data-stu-id="c360d-110">Description</span></span> |
|:---------|:-----|:------------|
|<span data-ttu-id="c360d-111">implicitGrantSettings</span><span class="sxs-lookup"><span data-stu-id="c360d-111">implicitGrantSettings</span></span>|[<span data-ttu-id="c360d-112">implicitGrantSettings</span><span class="sxs-lookup"><span data-stu-id="c360d-112">implicitGrantSettings</span></span>](implicitgrantsettings.md)| <span data-ttu-id="c360d-113">Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita.</span><span class="sxs-lookup"><span data-stu-id="c360d-113">Specifies whether this web application can request tokens using the OAuth 2.0 implicit flow.</span></span>|
|<span data-ttu-id="c360d-114">logoutUrl</span><span class="sxs-lookup"><span data-stu-id="c360d-114">logoutUrl</span></span>|<span data-ttu-id="c360d-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="c360d-115">String</span></span>| <span data-ttu-id="c360d-116">Especifica la dirección URL que usará el servicio de autorización de Microsoft para cerrar sesión de un usuario mediante [canal de frente](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back canal](https://openid.net/specs/openid-connect-backchannel-1_0.html) o protocolos de cierre de sesión SAML.</span><span class="sxs-lookup"><span data-stu-id="c360d-116">Specifies the URL that will be used by Microsoft's authorization service to logout an user using [front-channel](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back-channel](https://openid.net/specs/openid-connect-backchannel-1_0.html) or SAML logout protocols.</span></span> |
|<span data-ttu-id="c360d-117">oauth2AllowImplicitFlow</span><span class="sxs-lookup"><span data-stu-id="c360d-117">oauth2AllowImplicitFlow</span></span>|<span data-ttu-id="c360d-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="c360d-118">Boolean</span></span>| <span data-ttu-id="c360d-119">En desuso.</span><span class="sxs-lookup"><span data-stu-id="c360d-119">Deprecated.</span></span> <span data-ttu-id="c360d-120">No la use.</span><span class="sxs-lookup"><span data-stu-id="c360d-120">Do not use.</span></span> | 
|<span data-ttu-id="c360d-121">redirectUris</span><span class="sxs-lookup"><span data-stu-id="c360d-121">redirectUris</span></span>|<span data-ttu-id="c360d-122">Colección String</span><span class="sxs-lookup"><span data-stu-id="c360d-122">String collection</span></span>| <span data-ttu-id="c360d-123">Especifica las direcciones URL que los tokens de usuario se envían a para el inicio de sesión o el redireccionamiento de los códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a.</span><span class="sxs-lookup"><span data-stu-id="c360d-123">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="c360d-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c360d-124">JSON representation</span></span>
<span data-ttu-id="c360d-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c360d-125">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.web"
}-->

```json
{
  "implicitGrantSettings": {"@odata.type": "microsoft.graph.implicitGrantSettings"},
  "logoutUrl": "String",
  "oauth2AllowImplicitFlow": false,
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "web resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
