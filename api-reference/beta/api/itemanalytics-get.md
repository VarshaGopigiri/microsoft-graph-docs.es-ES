---
author: daspek
ms.author: dspektor
ms.date: 10/06/2017
title: Obtener análisis
ms.openlocfilehash: 57f009e0d2a07a5bf8c9a0f3b3617083bc279545
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087401"
---
# <a name="get-analytics"></a><span data-ttu-id="51e99-102">Obtener análisis</span><span class="sxs-lookup"><span data-stu-id="51e99-102">Get analytics</span></span>

> <span data-ttu-id="51e99-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51e99-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51e99-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51e99-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="51e99-105">Obtener [itemAnalytics][] acerca de las vistas que tuvieron lugar en este recurso.</span><span class="sxs-lookup"><span data-stu-id="51e99-105">Get [itemAnalytics][] about the views that took place under this resource.</span></span>
<span data-ttu-id="51e99-106">El recurso **itemAnalytics** es una forma cómoda para obtener estadísticas de actividad de `allTime` y el `lastSevenDays`.</span><span class="sxs-lookup"><span data-stu-id="51e99-106">The **itemAnalytics** resource is a convenient way to get activity stats for `allTime` and the `lastSevenDays`.</span></span>
<span data-ttu-id="51e99-107">Para un intervalo de tiempo personalizado o el intervalo, utilice la API [getActivitiesByInterval][] .</span><span class="sxs-lookup"><span data-stu-id="51e99-107">For a custom time range or interval, use the [getActivitiesByInterval][] API.</span></span>

><span data-ttu-id="51e99-108">**Nota:** El recurso **itemAnalytics** aún no está disponible en todas las [implementaciones nacionales](/graph/deployments).</span><span class="sxs-lookup"><span data-stu-id="51e99-108">**Note:** The **itemAnalytics** resource is not yet available in all [national deployments](/graph/deployments).</span></span>

[itemAnalytics]: ../resources/itemanalytics.md
[getActivitiesByInterval]: ../api/itemactivity-getbyinterval.md

## <a name="permissions"></a><span data-ttu-id="51e99-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="51e99-111">Permissions</span></span>

<span data-ttu-id="51e99-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51e99-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51e99-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51e99-114">Permission type</span></span>                        | <span data-ttu-id="51e99-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51e99-115">Permissions (from least to most privileged)</span></span>
|:--------------------------------------|:-------------------------------------
|<span data-ttu-id="51e99-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51e99-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="51e99-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51e99-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>
|<span data-ttu-id="51e99-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51e99-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="51e99-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51e99-119">Not supported.</span></span>
|<span data-ttu-id="51e99-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51e99-120">Application</span></span>                            | <span data-ttu-id="51e99-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51e99-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="51e99-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51e99-122">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/analytics
GET /sites/{site-id}/analytics
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/analytics
```

## <a name="example"></a><span data-ttu-id="51e99-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51e99-123">Example</span></span>

#### <a name="request"></a><span data-ttu-id="51e99-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51e99-124">Request</span></span>

<!-- { "blockType": "request", "name": "get-analytics" } -->

```http
GET /drives/{drive-id}/items/{item-id}/analytics
```

#### <a name="response"></a><span data-ttu-id="51e99-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51e99-125">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.itemAnalytics", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
    "allTime": {
        "access": {
            "actionCount": 123,
            "actorCount": 89
        }
    },
    "lastSevenDays": {
        "access": {
            "actionCount": 52,
            "actorCount": 41
        }
    }
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "BaseItem/Get analytics"
} -->
