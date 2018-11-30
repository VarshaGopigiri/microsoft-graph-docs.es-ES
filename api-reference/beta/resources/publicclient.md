---
title: tipo de recurso publicClient
description: Especifica la configuración para que no sean Web App o la Api de Web. (por ejemplo, Mobile u otro pública cliente como una aplicación instalada que se ejecutan en un dispositivo de escritorio)
ms.openlocfilehash: ba921fecb554a8749a9020508c538c68a7ff342e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083784"
---
# <a name="publicclient-resource-type"></a><span data-ttu-id="5b168-104">tipo de recurso publicClient</span><span class="sxs-lookup"><span data-stu-id="5b168-104">publicClient resource type</span></span>

> <span data-ttu-id="5b168-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5b168-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5b168-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5b168-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5b168-107">Especifica la configuración para que no sean Web App o la Api de Web.</span><span class="sxs-lookup"><span data-stu-id="5b168-107">Specifies settings for non Web App or Web Api.</span></span> <span data-ttu-id="5b168-108">(por ejemplo, Mobile u otro pública cliente como una aplicación instalada que se ejecutan en un dispositivo de escritorio)</span><span class="sxs-lookup"><span data-stu-id="5b168-108">(e.g. Mobile or other public client such as an installed application running on a desktop device)</span></span>

## <a name="properties"></a><span data-ttu-id="5b168-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5b168-109">Properties</span></span>

| <span data-ttu-id="5b168-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5b168-110">Property</span></span> | <span data-ttu-id="5b168-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b168-111">Type</span></span> | <span data-ttu-id="5b168-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b168-112">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="5b168-113">redirectUris</span><span class="sxs-lookup"><span data-stu-id="5b168-113">redirectUris</span></span>|<span data-ttu-id="5b168-114">Colección String</span><span class="sxs-lookup"><span data-stu-id="5b168-114">String collection</span></span>| <span data-ttu-id="5b168-115">Especifica las direcciones URL que los tokens de usuario se envían a para el inicio de sesión o el redireccionamiento de los códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a.</span><span class="sxs-lookup"><span data-stu-id="5b168-115">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="5b168-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5b168-116">JSON representation</span></span>
<span data-ttu-id="5b168-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5b168-117">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.installedClient"
}-->

```json
{
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "installedClient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->