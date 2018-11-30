---
title: Participantes de la lista
description: Recuperar una lista de objetos de participantes en la llamada.
ms.openlocfilehash: a18dc609204712f1b7c7b31150975543277ffa67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084964"
---
# <a name="list-participants"></a><span data-ttu-id="a8e91-103">Participantes de la lista</span><span class="sxs-lookup"><span data-stu-id="a8e91-103">List participants</span></span>

> <span data-ttu-id="a8e91-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a8e91-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8e91-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a8e91-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a8e91-106">Recuperar una lista de objetos de participantes en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a8e91-106">Retrieve a list of participant objects in the call.</span></span>

## <a name="permissions"></a><span data-ttu-id="a8e91-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a8e91-107">Permissions</span></span>
<span data-ttu-id="a8e91-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a8e91-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a8e91-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8e91-110">Permission type</span></span> | <span data-ttu-id="a8e91-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8e91-111">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="a8e91-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8e91-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="a8e91-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="a8e91-113">Not Supported</span></span>        |
| <span data-ttu-id="a8e91-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8e91-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a8e91-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="a8e91-115">Not Supported</span></span>        |
| <span data-ttu-id="a8e91-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8e91-116">Application</span></span>     | <span data-ttu-id="a8e91-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a8e91-117">None</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="a8e91-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8e91-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}/participants
GET /applications/{id}/calls/{id}/participants
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a8e91-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a8e91-119">Optional query parameters</span></span>
<span data-ttu-id="a8e91-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8e91-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a8e91-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8e91-121">Request headers</span></span>
| <span data-ttu-id="a8e91-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8e91-122">Name</span></span>          | <span data-ttu-id="a8e91-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8e91-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="a8e91-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a8e91-124">Authorization</span></span> | <span data-ttu-id="a8e91-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a8e91-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a8e91-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a8e91-127">Request body</span></span>
<span data-ttu-id="a8e91-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a8e91-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a8e91-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8e91-129">Response</span></span>
<span data-ttu-id="a8e91-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [participante](../resources/participant.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8e91-130">If successful, this method returns a `200 OK` response code and collection of [participant](../resources/participant.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="a8e91-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8e91-131">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="a8e91-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8e91-132">Example 1</span></span>

##### <a name="request"></a><span data-ttu-id="a8e91-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8e91-133">Request</span></span>
<span data-ttu-id="a8e91-134">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8e91-134">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_participants"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}/participants
```

##### <a name="response"></a><span data-ttu-id="a8e91-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8e91-135">Response</span></span>

> <span data-ttu-id="a8e91-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a8e91-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.participant",
  "isCollection": true,
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1152

{
  "value": [
    {
      "id": "id-value",
      "info": {
        "identity": {
          "user": {
            "id": "550fae72-d251-43ec-868c-373732c2704f",
            "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
            "displayName": "Heidi Steen"
          }
        },
        "languageId": "languageId-value",
        "region": "region-value"
      },
      "isInLobby": false,
      "isMuted": true,
      "mediaStreams": [
        {
          "sourceId": "1",
          "direction": "sendReceive",
          "label": "main-audio",
          "mediaType": "audio",
          "serverMuted": false
        }
      ],
      "metadata": "metadata-value"
    }
  ]
}
```

### <a name="example-2"></a><span data-ttu-id="a8e91-138">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a8e91-138">Example 2</span></span>

##### <a name="request"></a><span data-ttu-id="a8e91-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8e91-139">Request</span></span>

```http
GET /app/calls/57DAB8B1894C409AB240BD8BEAE78896/participants
Authorization: Bearer <TOKEN>
```

##### <a name="response"></a><span data-ttu-id="a8e91-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8e91-140">Response</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.participant",
  "isCollection": true,
  "truncated": true
}-->
```json
{
  "value": [
    {
      "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
      "info": {
        "identity" : {
          "user" : {
            "displayName": "Test User",
            "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
          }
        },
        "region": "westus",
        "languageId": "en-US"
      },
      "mediaStreams": [
        {
          "sourceId": "1",
          "mediaType": "audio",
          "label": "main-audio",
          "direction": "sendReceive",
          "serverMuted": false
        }
      ]
    },
    {
      "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
      "info": {
        "identity" : {
          "phone": {
            "displayName": "+12345678890",
            "id": "+12345678890"
          }
        }
      },
      "mediaStreams": [
        {
          "sourceId": "2",
          "mediaType": "audio",
          "label": "main-audio",
          "direction": "sendReceive",
          "serverMuted": false
        }
      ],
      "isMuted": true
    },
    {
      "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
      "info": {
        "identity" : {
          "application" : {
            "displayName": "Test BOT",
            "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
          }
        },
        "region": "westus",
        "languageId": "en-US"
      },
      "mediaStreams": [
        {
          "sourceId": "3",
          "mediaType": "audio",
          "label": "main-audio",
          "direction": "sendReceive",
          "serverMuted": false
        }
      ],
      "isMuted": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List participants",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->