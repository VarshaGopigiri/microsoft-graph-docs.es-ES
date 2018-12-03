---
title: Obtener regla
description: Obtener las propiedades y relaciones de un objeto messageRule.
ms.openlocfilehash: fa71a8447656fbf89fffe60bccec27d46d17c92a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031304"
---
# <a name="get-rule"></a><span data-ttu-id="cef3e-103">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="cef3e-103">Get rule</span></span>


<span data-ttu-id="cef3e-104">Obtener las propiedades y relaciones de un objeto [messageRule](../resources/messagerule.md).</span><span class="sxs-lookup"><span data-stu-id="cef3e-104">Get the properties and relationships of a [messageRule](../resources/messagerule.md) object.</span></span>


## <a name="permissions"></a><span data-ttu-id="cef3e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="cef3e-105">Permissions</span></span>
<span data-ttu-id="cef3e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cef3e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cef3e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cef3e-108">Permission type</span></span>      | <span data-ttu-id="cef3e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cef3e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cef3e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cef3e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="cef3e-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="cef3e-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="cef3e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cef3e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cef3e-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="cef3e-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="cef3e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cef3e-114">Application</span></span> | <span data-ttu-id="cef3e-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="cef3e-115">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="cef3e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cef3e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/inbox/messageRules/{id}
GET /users/{id | userPrincipalName}/mailFolders/inbox/messageRules/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="cef3e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cef3e-117">Optional query parameters</span></span>
<span data-ttu-id="cef3e-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cef3e-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cef3e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cef3e-119">Request headers</span></span>
| <span data-ttu-id="cef3e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cef3e-120">Name</span></span>      |<span data-ttu-id="cef3e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cef3e-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="cef3e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="cef3e-122">Authorization</span></span>  | <span data-ttu-id="cef3e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cef3e-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="cef3e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cef3e-125">Request body</span></span>
<span data-ttu-id="cef3e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cef3e-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="cef3e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cef3e-127">Response</span></span>
<span data-ttu-id="cef3e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cef3e-128">If successful, this method returns a `200 OK` response code and [messageRule](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cef3e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cef3e-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cef3e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cef3e-130">Request</span></span>
<span data-ttu-id="cef3e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cef3e-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox", "AQAAAJ5dZqA="],
  "name": "get_messagerule"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules/AQAAAJ5dZqA=
```
##### <a name="response"></a><span data-ttu-id="cef3e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cef3e-132">Response</span></span>
<span data-ttu-id="cef3e-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cef3e-133">Here is an example of the response.</span></span> <span data-ttu-id="cef3e-134">De forma predeterminada, las propiedades de fecha y hora de la respuesta están en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="cef3e-134">By default, the date-time properties in the response are in UTC.</span></span> 

<span data-ttu-id="cef3e-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cef3e-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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