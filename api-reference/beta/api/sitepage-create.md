---
author: rahmit
ms.author: rahmit
ms.date: 05/07/2018
title: Crear una nueva página en un sitio de SharePoint
localization_priority: Normal
ms.openlocfilehash: 8b3c1f6cabbacd62e671a27c03658c68b237ef92
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885599"
---
# <a name="create-a-page-in-the-site-pages-list-of-a-site"></a><span data-ttu-id="c39f5-102">Crear una página en la lista de páginas de sitio de un sitio</span><span class="sxs-lookup"><span data-stu-id="c39f5-102">Create a page in the site pages list of a site</span></span>

> <span data-ttu-id="c39f5-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c39f5-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c39f5-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c39f5-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c39f5-105">Crear un nuevo [sitePage][] en el de las páginas de sitio [lista][] en un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="c39f5-105">Create a new [sitePage][] in the site pages [list][] in a [site][].</span></span>

## <a name="permissions"></a><span data-ttu-id="c39f5-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c39f5-106">Permissions</span></span>

<span data-ttu-id="c39f5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c39f5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c39f5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c39f5-109">Permission type</span></span>      | <span data-ttu-id="c39f5-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c39f5-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c39f5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c39f5-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c39f5-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c39f5-112">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="c39f5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c39f5-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c39f5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c39f5-114">Not supported.</span></span>    |
|<span data-ttu-id="c39f5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c39f5-115">Application</span></span> | <span data-ttu-id="c39f5-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c39f5-116">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c39f5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c39f5-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{site-id}/pages
```

## <a name="request-body"></a><span data-ttu-id="c39f5-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c39f5-118">Request body</span></span>

<span data-ttu-id="c39f5-119">En el cuerpo de la solicitud, proporcionar una representación JSON del recurso para crear [sitePage][] .</span><span class="sxs-lookup"><span data-stu-id="c39f5-119">In the request body, supply a JSON representation of the [sitePage][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="c39f5-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c39f5-120">Example</span></span>

<span data-ttu-id="c39f5-121">En el ejemplo siguiente se muestra cómo crear una nueva página.</span><span class="sxs-lookup"><span data-stu-id="c39f5-121">The following example shows how to create a new page.</span></span>

<!-- { "blockType": "request", "name": "create-page", "scopes": "sites.readwrite.all" } -->

```json
POST /sites/{site-id}/page
Content-Type: application/json

{
    "name": "Events.aspx",
    "title": "Team Events",
    "publishingState": {
        "level": "checkedOut",
        "versionId": "0.1"
    },
    "webParts": [
        {
            "type": "rte",
            "innerHTML": "<p>Here are the team's upcoming events:</p>"
        },
        {
            "type": "d1d91016-032f-456d-98a4-721247c305e8",
            "data": {
                "title": "Events",
                "description": "Display upcoming events",
                "serverProcessedContent": {
                    "htmlStrings": {},
                    "searchablePlainTexts": {
                        "title": ""
                    },
                    "imageSources": {},
                    "links": {
                        "baseUrl": "https://www.contoso.com/sites/Engineering"
                    },
                    "componentDependencies": {
                        "layoutComponentId": "8ac0c53c-e8d0-4e3e-87d0-7449eb0d4027"
                    }
                },
                "dataVersion": "1.0",
                "properties": {
                    "selectedListId": "032e08ab-89b0-4d8f-bc10-73094233615c",
                    "selectedCategory": "",
                    "dateRangeOption": 0,
                    "startDate": "",
                    "endDate": "",
                    "isOnSeeAllPage": false,
                    "layoutId": "FilmStrip",
                    "dataProviderId": "Event",
                    "webId": "0764c419-1ecc-4126-ba32-0c25ae0fffe8",
                    "siteId": "6b4ffc7a-cfc2-4a76-903a-1cc3686dee23"
                }
            }
        }
    ]
}
```

## <a name="response"></a><span data-ttu-id="c39f5-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c39f5-122">Response</span></span>

<span data-ttu-id="c39f5-123">Si se realiza correctamente, este método devuelve una [sitePage][] en el cuerpo de la respuesta de la página creada.</span><span class="sxs-lookup"><span data-stu-id="c39f5-123">If successful, this method returns a [sitePage][] in the response body for the created page.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.sitePage", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": 2,
    "eTag": "75bc70e2-6587-45be-8493-c99a956b2e05,7",
    "createdDateTime": "2016-12-06T20:04:40Z",
    "lastModifiedDateTime": "2016-12-06T20:05:09Z",
    "webUrl": "https://www.contoso.com/sites/Engineering/SitePages/Events.aspx",
    "createdBy": {
        "user": {
            "email": "rahmit",
            "id": "1b37d2e1-5000-4648-b431-7dfa509b5660",
            "displayName": "Rahul Mittal"
        }
    },
    "lastModifiedBy": {
        "user": {
            "email": "rahmit",
            "id": "1b37d2e1-5000-4648-b431-7dfa509b5660",
            "displayName": "Rahul Mittal"
        }
    },
    "parentReference": {
        "id": "eb3bfd48-56f8-4c1e-8312-e58588b22e7c"
    },
    "contentType": {
        "id": "0x0101009D1CB255DA76424F860D91F20E6C411800C9E7033636784C4B88A284B1823C45FD",
        "name": "Site Page"
    },
    "description": "",
    "title": "Team Events",
    "webParts": [
        {
            "type": "rte",
            "data": {
                "innerHTML": "<p>Here are the team's upcoming events:</p>"
            }
        },
        {
            "type": "d1d91016-032f-456d-98a4-721247c305e8",
            "data": {
                "title": "Events",
                "description": "Display upcoming events",
                "serverProcessedContent": {
                    "htmlStrings": {},
                    "searchablePlainTexts": {
                        "title": ""
                    },
                    "imageSources": {},
                    "links": {
                        "baseUrl": "https://www.contoso.com/teams/Engineering"
                    },
                    "componentDependencies": {
                        "layoutComponentId": "8ac0c53c-e8d0-4e3e-87d0-7449eb0d4027"
                    }
                },
                "dataVersion": "1.0",
                "properties": {
                    "selectedListId": "032e08ab-89b0-4d8f-bc10-73094233615c",
                    "selectedCategory": "",
                    "dateRangeOption": 0,
                    "startDate": "",
                    "endDate": "",
                    "isOnSeeAllPage": false,
                    "layoutId": "FilmStrip",
                    "dataProviderId": "Event",
                    "webId": "0764c419-1ecc-4126-ba32-0c25ae0fffe8",
                    "siteId": "6b4ffc7a-cfc2-4a76-903a-1cc3686dee23"
                }
            }
        }
    ]
}
```

<span data-ttu-id="c39f5-124">**Nota:** El objeto Response se trunca para obtener una mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="c39f5-124">**Note:** The response object is truncated for clarity.</span></span> <span data-ttu-id="c39f5-125">Se devolverán las propiedades predeterminadas de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="c39f5-125">Default properties will be returned from the actual call.</span></span>

[list]: ../resources/list.md
[listItem]: ../resources/listitem.md
[site]: ../resources/site.md
[sitePage]: ../resources/sitepage.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a sitePage in the SitePages list in a site.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Pages/Create"
} -->
