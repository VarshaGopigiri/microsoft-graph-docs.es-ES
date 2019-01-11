---
title: 'usuario: getMailTips'
description: Obtenga las sugerencias de correo electrónico de uno o más destinatarios como disponible para el usuario ha iniciado sesión.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 2577b37f6cbfa3bd6dc5eff712c07562ecdadbf2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855968"
---
# <a name="user-getmailtips"></a><span data-ttu-id="ee6a7-103">usuario: getMailTips</span><span class="sxs-lookup"><span data-stu-id="ee6a7-103">user: getMailTips</span></span>

> <span data-ttu-id="ee6a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee6a7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee6a7-106">Obtenga las sugerencias de correo electrónico de uno o más destinatarios como disponibles para el [usuario](../resources/user.md)de ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-106">Get the MailTips of one or more recipients as available to the signed-in [user](../resources/user.md).</span></span>

<span data-ttu-id="ee6a7-107">Tenga en cuenta que al hacer que un `POST` llamar a la `getMailTips` acción, puede solicitar tipos específicos de sugerencias de correo electrónico que se devolverá para más de un destinatario a la vez.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-107">Note that by making a `POST` call to the `getMailTips` action, you can request specific types of MailTips to be returned for more than one recipient at one time.</span></span> <span data-ttu-id="ee6a7-108">Las sugerencias de correo electrónico solicitados se devuelven en una colección de [sugerencias de correo electrónico](../resources/mailtips.md) .</span><span class="sxs-lookup"><span data-stu-id="ee6a7-108">The requested MailTips are returned in a [mailTips](../resources/mailtips.md) collection.</span></span>

## <a name="permissions"></a><span data-ttu-id="ee6a7-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee6a7-109">Permissions</span></span>
<span data-ttu-id="ee6a7-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee6a7-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ee6a7-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee6a7-112">Permission type</span></span>      | <span data-ttu-id="ee6a7-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee6a7-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ee6a7-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee6a7-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ee6a7-115">Mail.Read, Mail.Read.Shared</span><span class="sxs-lookup"><span data-stu-id="ee6a7-115">Mail.Read, Mail.Read.Shared</span></span>    |
|<span data-ttu-id="ee6a7-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee6a7-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee6a7-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="ee6a7-117">Mail.Read</span></span>    |
|<span data-ttu-id="ee6a7-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee6a7-118">Application</span></span> | <span data-ttu-id="ee6a7-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="ee6a7-119">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="ee6a7-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee6a7-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMailTips
POST /users/{id|userPrincipalName}/getMailTips
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ee6a7-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ee6a7-121">Optional query parameters</span></span>
<span data-ttu-id="ee6a7-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ee6a7-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee6a7-123">Request headers</span></span>
| <span data-ttu-id="ee6a7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee6a7-124">Header</span></span>       | <span data-ttu-id="ee6a7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ee6a7-125">Value</span></span>|
|:-----------  |:------|
| <span data-ttu-id="ee6a7-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee6a7-126">Authorization</span></span> | <span data-ttu-id="ee6a7-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ee6a7-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ee6a7-129">Content-Type</span></span>  | <span data-ttu-id="ee6a7-130">application/json</span><span class="sxs-lookup"><span data-stu-id="ee6a7-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ee6a7-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee6a7-131">Request body</span></span>
<span data-ttu-id="ee6a7-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ee6a7-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee6a7-133">Property</span></span>     | <span data-ttu-id="ee6a7-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee6a7-134">Type</span></span>   |<span data-ttu-id="ee6a7-135">Description</span><span class="sxs-lookup"><span data-stu-id="ee6a7-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee6a7-136">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="ee6a7-136">EmailAddresses</span></span>|<span data-ttu-id="ee6a7-137">Colección String</span><span class="sxs-lookup"><span data-stu-id="ee6a7-137">String collection</span></span>|<span data-ttu-id="ee6a7-138">Una colección de direcciones SMTP de los destinatarios para obtener sugerencias de correo electrónico para.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-138">A collection of SMTP addresses of recipients to get MailTips for.</span></span>|
|<span data-ttu-id="ee6a7-139">MailTipsOptions</span><span class="sxs-lookup"><span data-stu-id="ee6a7-139">MailTipsOptions</span></span>|<span data-ttu-id="ee6a7-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee6a7-140">String</span></span>|<span data-ttu-id="ee6a7-141">Una enumeración de indicadores que representa las sugerencias de correo electrónico solicitado.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-141">A enumeration of flags that represents the requested mailtips.</span></span> <span data-ttu-id="ee6a7-142">Los valores posibles son: `automaticReplies`, `customMailTip`, `deliveryRestriction`, `externalMemberCount`, `mailboxFullStatus`, `maxMessageSize`, `moderationStatus`, `recipientScope`, `recipientSuggestions`, y `totalMemberCount`.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-142">Possible values are: `automaticReplies`, `customMailTip`, `deliveryRestriction`, `externalMemberCount`, `mailboxFullStatus`, `maxMessageSize`, `moderationStatus`, `recipientScope`, `recipientSuggestions`, and `totalMemberCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="ee6a7-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee6a7-143">Response</span></span>

<span data-ttu-id="ee6a7-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [sugerencias de correo electrónico](../resources/mailtips.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-144">If successful, this method returns a `200 OK` response code and a collection of [mailTips](../resources/mailtips.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ee6a7-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee6a7-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ee6a7-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee6a7-146">Request</span></span>
<span data-ttu-id="ee6a7-147">En el ejemplo siguiente se obtiene sugerencias de correo electrónico para los destinatarios especificados, para cualquier configuración de respuestas automáticas y el estado completo del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-147">The following example gets MailTips for the specified recipients, for any automatic reply settings and the mailbox full status.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_getmailtips"
}-->
```http
POST https://graph.microsoft.com/beta/me/getMailTips
Content-Type: application/json

{
    "EmailAddresses": [
        "danas@contoso.onmicrosoft.com", 
        "fannyd@contoso.onmicrosoft.com"
    ],
    "MailTipsOptions": "automaticReplies, mailboxFullStatus"
}
```

##### <a name="response"></a><span data-ttu-id="ee6a7-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee6a7-148">Response</span></span>
<span data-ttu-id="ee6a7-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.mailTips)",
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
