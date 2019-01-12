---
title: 'usuario: getMailTips'
description: Obtenga las sugerencias de correo electrónico de uno o más destinatarios como disponible para el usuario ha iniciado sesión.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 4c931d6e7f3b7762534d773b647f7db68461a230
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978140"
---
# <a name="user-getmailtips"></a><span data-ttu-id="30e69-103">usuario: getMailTips</span><span class="sxs-lookup"><span data-stu-id="30e69-103">user: getMailTips</span></span>

<span data-ttu-id="30e69-104">Obtenga las sugerencias de correo electrónico de uno o más destinatarios como disponibles para el [usuario](../resources/user.md)de ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="30e69-104">Get the MailTips of one or more recipients as available to the signed-in [user](../resources/user.md).</span></span>

<span data-ttu-id="30e69-105">Tenga en cuenta que al hacer que un `POST` llamar a la `getMailTips` acción, puede solicitar tipos específicos de sugerencias de correo electrónico que se devolverá para más de un destinatario a la vez.</span><span class="sxs-lookup"><span data-stu-id="30e69-105">Note that by making a `POST` call to the `getMailTips` action, you can request specific types of MailTips to be returned for more than one recipient at one time.</span></span> <span data-ttu-id="30e69-106">Las sugerencias de correo electrónico solicitados se devuelven en una colección de [sugerencias de correo electrónico](../resources/mailtips.md) .</span><span class="sxs-lookup"><span data-stu-id="30e69-106">The requested MailTips are returned in a [mailTips](../resources/mailtips.md) collection.</span></span>

## <a name="permissions"></a><span data-ttu-id="30e69-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="30e69-107">Permissions</span></span>
<span data-ttu-id="30e69-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30e69-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30e69-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30e69-110">Permission type</span></span>      | <span data-ttu-id="30e69-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30e69-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="30e69-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30e69-112">Delegated (work or school account)</span></span> | <span data-ttu-id="30e69-113">Mail.Read, Mail.Read.Shared</span><span class="sxs-lookup"><span data-stu-id="30e69-113">Mail.Read, Mail.Read.Shared</span></span>    |
|<span data-ttu-id="30e69-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30e69-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="30e69-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="30e69-115">Mail.Read</span></span>    |
|<span data-ttu-id="30e69-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30e69-116">Application</span></span> | <span data-ttu-id="30e69-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="30e69-117">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="30e69-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30e69-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMailTips
POST /users/{id|userPrincipalName}/getMailTips
```
## <a name="optional-query-parameters"></a><span data-ttu-id="30e69-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="30e69-119">Optional query parameters</span></span>
<span data-ttu-id="30e69-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30e69-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="30e69-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30e69-121">Request headers</span></span>
| <span data-ttu-id="30e69-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30e69-122">Header</span></span>       | <span data-ttu-id="30e69-123">Valor</span><span class="sxs-lookup"><span data-stu-id="30e69-123">Value</span></span>|
|:-----------  |:------|
| <span data-ttu-id="30e69-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="30e69-124">Authorization</span></span> | <span data-ttu-id="30e69-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30e69-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="30e69-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="30e69-127">Content-Type</span></span>  | <span data-ttu-id="30e69-128">application/json</span><span class="sxs-lookup"><span data-stu-id="30e69-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="30e69-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30e69-129">Request body</span></span>
<span data-ttu-id="30e69-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="30e69-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="30e69-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30e69-131">Property</span></span>     | <span data-ttu-id="30e69-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="30e69-132">Type</span></span>   |<span data-ttu-id="30e69-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="30e69-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="30e69-134">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="30e69-134">EmailAddresses</span></span>|<span data-ttu-id="30e69-135">Colección String</span><span class="sxs-lookup"><span data-stu-id="30e69-135">String collection</span></span>|<span data-ttu-id="30e69-136">Una colección de direcciones SMTP de los destinatarios para obtener sugerencias de correo electrónico para.</span><span class="sxs-lookup"><span data-stu-id="30e69-136">A collection of SMTP addresses of recipients to get MailTips for.</span></span>|
|<span data-ttu-id="30e69-137">MailTipsOptions</span><span class="sxs-lookup"><span data-stu-id="30e69-137">MailTipsOptions</span></span>|<span data-ttu-id="30e69-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="30e69-138">String</span></span>|<span data-ttu-id="30e69-139">Una enumeración de indicadores que representa las sugerencias de correo electrónico solicitado.</span><span class="sxs-lookup"><span data-stu-id="30e69-139">A enumeration of flags that represents the requested mailtips.</span></span> <span data-ttu-id="30e69-140">Los valores posibles son: `automaticReplies`, `customMailTip`, `deliveryRestriction`, `externalMemberCount`, `mailboxFullStatus`, `maxMessageSize`, `moderationStatus`, `recipientScope`, `recipientSuggestions`, y `totalMemberCount`.</span><span class="sxs-lookup"><span data-stu-id="30e69-140">Possible values are: `automaticReplies`, `customMailTip`, `deliveryRestriction`, `externalMemberCount`, `mailboxFullStatus`, `maxMessageSize`, `moderationStatus`, `recipientScope`, `recipientSuggestions`, and `totalMemberCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="30e69-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30e69-141">Response</span></span>

<span data-ttu-id="30e69-142">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [sugerencias de correo electrónico](../resources/mailtips.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30e69-142">If successful, this method returns a `200 OK` response code and a collection of [mailTips](../resources/mailtips.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="30e69-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e69-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="30e69-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30e69-144">Request</span></span>
<span data-ttu-id="30e69-145">En el ejemplo siguiente se obtiene sugerencias de correo electrónico para los destinatarios especificados, para cualquier configuración de respuestas automáticas y el estado completo del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="30e69-145">The following example gets MailTips for the specified recipients, for any automatic reply settings and the mailbox full status.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_getmailtips"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMailTips
Content-Type: application/json

{
    "EmailAddresses": [
        "danas@contoso.onmicrosoft.com", 
        "fannyd@contoso.onmicrosoft.com"
    ],
    "MailTipsOptions": "automaticReplies, mailboxFullStatus"
}
```

##### <a name="response"></a><span data-ttu-id="30e69-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30e69-146">Response</span></span>
<span data-ttu-id="30e69-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30e69-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailTips",
  isCollection: true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.mailTips)",
    "value":[
        {
            "emailAddress":{
                "name":"",
                "address":"danas@contoso.onmicrosoft.com"
            },
            "automaticReplies":{
                "message":"<style type=\"text/css\" style=\"\">\r\n<!--\r\np\r\n\t{margin-top:0;\r\n\tmargin-bottom:0}\r\n-->\r\n</style>\r\n<div dir=\"ltr\">\r\n<div id=\"x_divtagdefaultwrapper\" style=\"font-size:12pt; color:#000000; background-color:#FFFFFF; font-family:Calibri,Arial,Helvetica,sans-serif\">\r\n<p>Hi, I am on vacation right now. I'll get back to you after I return.<br>\r\n</p>\r\n</div>\r\n</div>",
                "messageLanguage":{
                    "locale":"en-US",
                    "displayName":"English (United States)"
                },
                "scheduledStartTime": {
                    "dateTime": "2018-08-07T02:00:00.0000000",
                    "timeZone": "UTC"
                },
                "scheduledEndTime": {
                    "dateTime": "2018-08-09T02:00:00.0000000",
                    "timeZone": "UTC"
                }
            },
            "mailboxFull":false
        },
        {
            "emailAddress":{
                "name":"",
                "address":"fannyd@contoso.onmicrosoft.com"
            },
            "automaticReplies":{
                "message":""
            },
            "mailboxFull":false
        }
    ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: getMailTips",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
