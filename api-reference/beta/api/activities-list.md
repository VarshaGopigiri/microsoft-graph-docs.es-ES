---
author: daspek
ms.author: dspektor
ms.date: 09/10/2017
title: Actividades de archivo
ms.openlocfilehash: f228f96083d899c4d9a43f6a4d41f2b90ce2eaf7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084346"
---
# <a name="enumerate-activities-preview"></a><span data-ttu-id="c5d0b-102">Enumerar actividades (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="c5d0b-102">Enumerate activities (preview)</span></span>

> <span data-ttu-id="c5d0b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5d0b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5d0b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5d0b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c5d0b-105">Enumere las [actividades][] más recientes que tuvieron lugar en una jerarquía o un elemento.</span><span class="sxs-lookup"><span data-stu-id="c5d0b-105">List the recent [activities][] that took place on an item or under a hierarchy.</span></span>

<span data-ttu-id="c5d0b-106">**Nota**: Actividades está en versión preliminar limitada, por lo que aún no está disponible para todos los inquilinos.</span><span class="sxs-lookup"><span data-stu-id="c5d0b-106">**Note:** Activities is in a limited Preview and not yet available to all tenants.</span></span>

[actividades]: ../resources/itemactivity.md
[activities]: ../resources/itemactivity.md

## <a name="permissions"></a><span data-ttu-id="c5d0b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c5d0b-108">Permissions</span></span>

<span data-ttu-id="c5d0b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5d0b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c5d0b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c5d0b-111">Permission type</span></span>                        | <span data-ttu-id="c5d0b-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c5d0b-112">Permissions (from least to most privileged)</span></span>
|:--------------------------------------|:-------------------------------------
|<span data-ttu-id="c5d0b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c5d0b-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="c5d0b-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c5d0b-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>
|<span data-ttu-id="c5d0b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c5d0b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c5d0b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5d0b-116">Not supported.</span></span>
|<span data-ttu-id="c5d0b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c5d0b-117">Application</span></span>                            | <span data-ttu-id="c5d0b-118">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c5d0b-118">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="c5d0b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5d0b-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/activities
GET /drives/{drive-id}/items/{item-id}/activities
GET /sites/{site-id}/lists/{list-id}/activities
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/activities
```

## <a name="example"></a><span data-ttu-id="c5d0b-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5d0b-120">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c5d0b-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5d0b-121">Request</span></span>

<!-- { "blockType": "request", "name": "list-activities" } -->

```http
GET https://graph.microsoft.com/beta/me/drive/activities
```

#### <a name="response"></a><span data-ttu-id="c5d0b-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5d0b-122">Response</span></span>

<!-- { "blockType": "response", "@type": "Collection(microsoft.graph.itemActivity)", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "action": {
                "comment": {}
            },
            "actor": {
                "user": {
                    "displayName": "Xavier Wilke"
                }
            },
            "id": "EJalEvjV1EgIYFQAAAAAAA==",
            "times": {
                "recordedTime": "2017-07-29T18:34:40Z"
            }
        },
        {
            "action": {
                "edit": {},
                "version": {
                    "newVersion": "2.0"
                }
            },
            "actor": {
                "user": {
                    "displayName": "Judith Clemons"
                }
            },
            "id": "cInT6/fV1EgFYFQAAAAAAA==",
            "times": {
                "recordedTime": "2017-07-29T16:23:35Z"
            }
        },
        {
            "action": {
                "mention": {
                    "mentionees": [
                        {
                            "user": {
                                "displayName": "Judith Clemons"
                            }
                        }
                    ]
                }
            },
            "actor": {
                "user": {
                    "displayName": "Misty Suarez"
                }
            },
            "id": "EBJa0vPV1EjFX1QAAAAAAA==",
            "times": {
                "recordedTime": "2017-07-28T20:14:14Z"
            }
        },
        {
            "action": {
                "rename": {
                    "oldName": "Document2.docx"
                }
            },
            "actor": {
                "user": {
                    "displayName": "Misty Suarez"
                }
            },
            "id": "QFJFlfPV1Ei/X1QAAAAAAA==",
            "times": {
                "recordedTime": "2017-07-28T20:12:32Z"
            }
        },
        {
            "action": {
                "create": {}
            },
            "actor": {
                "user": {
                    "displayName": "Misty Suarez"
                }
            },
            "id": "IJydkPPV1Ei9X1QAAAAAAA==",
            "times": {
                "recordedTime": "2017-07-28T20:02:24Z"
            }
        }
    ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Site/List sites"
} -->
