---
author: rahmit
ms.author: rahmit
ms.date: 03/15/2018
title: Lista de las páginas de un sitio
ms.openlocfilehash: 51177558d938400a5e559e83d6e1d2333de318cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089152"
---
# <a name="list-the-pages-in-the-site-pages-list-of-a-site"></a><span data-ttu-id="49e83-102">Lista de las páginas en la lista de páginas de sitio de un sitio</span><span class="sxs-lookup"><span data-stu-id="49e83-102">List the pages in the site pages list of a site</span></span>

> <span data-ttu-id="49e83-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49e83-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49e83-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49e83-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="49e83-105">Obtener la colección de [] [sitePages] de la de las páginas de sitio [lista][] en un sitio del [sitio][].</span><span class="sxs-lookup"><span data-stu-id="49e83-105">Get the collection of [sitePages][] from the site pages [list][] in a site [site][].</span></span> <span data-ttu-id="49e83-106">Se devuelven todas las páginas del sitio (con paginación).</span><span class="sxs-lookup"><span data-stu-id="49e83-106">All pages in the site are returned (with pagination).</span></span>

[sitePage]: ../resources/sitepage.md
[list]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="49e83-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="49e83-109">Permissions</span></span>

<span data-ttu-id="49e83-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49e83-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49e83-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49e83-112">Permission type</span></span>      | <span data-ttu-id="49e83-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49e83-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="49e83-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49e83-114">Delegated (work or school account)</span></span> | <span data-ttu-id="49e83-115">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49e83-115">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="49e83-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49e83-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="49e83-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49e83-117">Not supported.</span></span>    |
|<span data-ttu-id="49e83-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49e83-118">Application</span></span> | <span data-ttu-id="49e83-119">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49e83-119">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="49e83-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49e83-120">HTTP request</span></span>

```http
GET /sites/{site-id}/pages

```

## <a name="example"></a><span data-ttu-id="49e83-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49e83-121">Example</span></span>

#### <a name="request"></a><span data-ttu-id="49e83-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49e83-122">Request</span></span>

<!-- { "blockType": "request", "name": "get-pages", "scopes": "sites.read.all", "tags": "service.sharepoint" } -->

```http
GET /sites/{site-id}/pages
```

#### <a name="response"></a><span data-ttu-id="49e83-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49e83-123">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.sitePage)", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "5",
            "eTag": "{8BEE5ABE-49B9-431B-AEBA-C96D6DEF44E3},4",
            "lastModifiedDateTime": "2018-08-15T19:20:20Z",
            "name": "EventInstructions.aspx",
            "webUrl": "SitePages/EventInstructions.aspx",
            "uniqueId": "8bee5abe-49b9-431b-aeba-c96d6def44e3",
            "description": "",
            "title": "Event Instructions",
            "pageLayoutType": "Article",
            "createdBy": {
                "user": {
                    "displayName": "Jimmy Felts",
                    "email": "jimmy@contoso.com"
                }
            },
            "lastModifiedBy": {
                "user": {
                    "displayName": "Jimmy Felts",
                    "email": "jimmy@contoso.com"
                }
            },
            "parentReference": {
                "listId": "334e40f2-1614-4fdc-87ad-d7b91407c5a9",
                "siteId": "66bed137-bf1f-41c8-a0e9-2bc01097a797"
            },
            "contentType": {
                "id": "0x0101009D1CB255DA76424F860D91F20E6C4118",
                "name": "Site Page"
            },
            "publishingState": {
                "level": "published",
                "versionId": "1.0"
            },
            "webParts": [
                {
                    "type": "daf0b71c-6de8-4ef7-b511-faae7c388708",
                    "data": {
                        "id": "daf0b71c-6de8-4ef7-b511-faae7c388708",
                        "instanceId": "b646d2e4-2b9c-41c7-a567-0c05c2909d5a",
                        "title": "Registration",
                        "description": "...",
                        "serverProcessedContent": {
                            "htmlStrings": {},
                            "searchablePlainTexts": {
                                "title": ""
                            },
                            "imageSources": {},
                            "links": {
                                "baseUrl": "/teams/SPClientTest"
                            },
                            "componentDependencies": {
                                "layoutComponentId": "62680648-d047-46ec-81e0-475ee78e482d"
                            }
                        },
                        "dataVersion": "2.1",
                        "properties": {
                            "webId": "4a15f359-257c-4f31-8350-5025104e30d5",
                            "siteId": "00c6b6c6-c466-4e64-a370-2b6ddb7cdfe3",
                            "query": { ... },
                            "templateId": 1,
                            "maxItemsPerPage": 10,
                            "hideWebPartWhenEmpty": false,
                            "kqlQueryTemplate": "...",
                            "displayMaps": { ... },
                            "sites": [],
                            "layoutId": "Card",
                            "dataProviderId": "Search"
                        }
                    }
                }
            ]
        },
        {
            "id": 2,
            "eTag": "75bc70e2-6587-45be-8493-c99a956b2e05,7",
            "createdDateTime": "2016-12-06T20:04:40Z",
            "lastModifiedDateTime": "2016-12-06T20:05:09Z",
            "webUrl": "https://www.contoso.com/sites/Engineering/SitePages/Events.aspx",
            "createdBy": {
                "user": {
                    "email": "jimmy@contoso.com",
                    "id": "1b37d2e1-5000-4648-b431-7dfa509b5660",
                    "displayName": "Jimmy Felts"
                }
            },
            "lastModifiedBy": {
                "user": {
                    "email": "jimmy@contoso.com",
                    "id": "1b37d2e1-5000-4648-b431-7dfa509b5660",
                    "displayName": "Jimmy Felts"
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
            "title": "Upcoming Events",
            "publishingState": {
                "level": "checkout",
                "versionId": "1.1",
                "checkedOutBy": {
                    "user": {
                        "displayName": "Jimmy Felts",
                        "email": "jimmy@contoso.com"
                    }
                }
            },
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
    ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Enumerate the list of pages in a site",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Pages/Enumerate"
} -->