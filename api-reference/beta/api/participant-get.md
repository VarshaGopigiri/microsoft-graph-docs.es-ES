---
title: Obtener participante
description: Recuperar las propiedades y relaciones de un objeto **participante** .
ms.openlocfilehash: 4e97278b7ac93d784884c789f4da089e63e195ad
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083756"
---
# <a name="get-participant"></a><span data-ttu-id="e3844-103">Obtener participante</span><span class="sxs-lookup"><span data-stu-id="e3844-103">Get participant</span></span>

> <span data-ttu-id="e3844-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e3844-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e3844-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e3844-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e3844-106">Recuperar las propiedades y relaciones de un objeto **participante** .</span><span class="sxs-lookup"><span data-stu-id="e3844-106">Retrieve the properties and relationships of a **participant** object.</span></span>

## <a name="permissions"></a><span data-ttu-id="e3844-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e3844-107">Permissions</span></span>
<span data-ttu-id="e3844-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3844-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e3844-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3844-110">Permission type</span></span> | <span data-ttu-id="e3844-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3844-111">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="e3844-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3844-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="e3844-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="e3844-113">Not Supported</span></span>        |
| <span data-ttu-id="e3844-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3844-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e3844-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="e3844-115">Not Supported</span></span>        |
| <span data-ttu-id="e3844-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3844-116">Application</span></span>     | <span data-ttu-id="e3844-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3844-117">None</span></span>                                        |

## <a name="http-request"></a><span data-ttu-id="e3844-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3844-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /app/calls/{id}/participants/{id}
GET /applications/{id}/calls/{id}/participants/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e3844-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e3844-119">Optional query parameters</span></span>
<span data-ttu-id="e3844-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3844-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e3844-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3844-121">Request headers</span></span>
| <span data-ttu-id="e3844-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3844-122">Name</span></span>          | <span data-ttu-id="e3844-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3844-123">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="e3844-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3844-124">Authorization</span></span> | <span data-ttu-id="e3844-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e3844-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e3844-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3844-127">Request body</span></span>
<span data-ttu-id="e3844-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e3844-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e3844-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3844-129">Response</span></span>
<span data-ttu-id="e3844-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [participante](../resources/participant.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3844-130">If successful, this method returns a `200 OK` response code and a [participant](../resources/participant.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3844-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3844-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="e3844-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3844-132">Request</span></span>
<span data-ttu-id="e3844-133">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3844-133">The following example shows the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_participant"
}-->
```http
GET https://graph.microsoft.com/beta/app/calls/{id}/participants/{id}
```

##### <a name="response"></a><span data-ttu-id="e3844-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3844-134">Response</span></span>

> <span data-ttu-id="e3844-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3844-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.participant"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 977

{
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
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
  "isInLobby": true,
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
  "metadata": "metadata-value",
  "recordingInfo": {
    "initiatedBy": {
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
    "status": "recordingCapable"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get participant",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->