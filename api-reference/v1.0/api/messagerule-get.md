---
title: Obtener regla
description: Obtener las propiedades y relaciones de un objeto messageRule.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: cfc934ffccb5dd4462f7cf51c318bef198d952dd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814108"
---
# <a name="get-rule"></a><span data-ttu-id="742cd-103">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="742cd-103">Get rule</span></span>


<span data-ttu-id="742cd-104">Obtener las propiedades y relaciones de un objeto [messageRule](../resources/messagerule.md).</span><span class="sxs-lookup"><span data-stu-id="742cd-104">Get the properties and relationships of a [messageRule](../resources/messagerule.md) object.</span></span>


## <a name="permissions"></a><span data-ttu-id="742cd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="742cd-105">Permissions</span></span>
<span data-ttu-id="742cd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="742cd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="742cd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="742cd-108">Permission type</span></span>      | <span data-ttu-id="742cd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="742cd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="742cd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="742cd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="742cd-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="742cd-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="742cd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="742cd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="742cd-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="742cd-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="742cd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="742cd-114">Application</span></span> | <span data-ttu-id="742cd-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="742cd-115">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="742cd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="742cd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/inbox/messageRules/{id}
GET /users/{id | userPrincipalName}/mailFolders/inbox/messageRules/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="742cd-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="742cd-117">Optional query parameters</span></span>
<span data-ttu-id="742cd-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="742cd-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="742cd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="742cd-119">Request headers</span></span>
| <span data-ttu-id="742cd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="742cd-120">Name</span></span>      |<span data-ttu-id="742cd-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="742cd-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="742cd-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="742cd-122">Authorization</span></span>  | <span data-ttu-id="742cd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="742cd-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="742cd-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="742cd-125">Request body</span></span>
<span data-ttu-id="742cd-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="742cd-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="742cd-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="742cd-127">Response</span></span>
<span data-ttu-id="742cd-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="742cd-128">If successful, this method returns a `200 OK` response code and [messageRule](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="742cd-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="742cd-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="742cd-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="742cd-130">Request</span></span>
<span data-ttu-id="742cd-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="742cd-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox", "AQAAAJ5dZqA="],
  "name": "get_messagerule"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules/AQAAAJ5dZqA=
```
##### <a name="response"></a><span data-ttu-id="742cd-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="742cd-132">Response</span></span>
<span data-ttu-id="742cd-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="742cd-133">Here is an example of the response.</span></span> <span data-ttu-id="742cd-134">De forma predeterminada, las propiedades de fecha y hora de la respuesta están en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="742cd-134">By default, the date-time properties in the response are in UTC.</span></span> 

<span data-ttu-id="742cd-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="742cd-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
  "id":"AQAAAJ5dZqA=",
  "displayName":"From partner",
  "sequence":2,
  "isEnabled":true,
  "hasError":false,
  "isReadOnly":false,
  "conditions":{
    "senderContains":[
      "ADELE"
    ]
  },
  "actions":{
    "stopProcessingRules":true,
    "forwardTo":[
      {
        "emailAddress":{
          "name":"Alex Wilbur",
          "address":"AlexW@contoso.onmicrosoft.com"
        }
      }
    ]
  }
}
```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
