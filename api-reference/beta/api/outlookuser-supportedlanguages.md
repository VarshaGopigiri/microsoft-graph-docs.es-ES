---
title: 'outlookUser: supportedLanguages'
description: Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.
ms.openlocfilehash: ac1b9693121f3ba3f180b53532bb6a6c917e2108
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083373"
---
# <a name="outlookuser-supportedlanguages"></a><span data-ttu-id="b1d8b-103">outlookUser: supportedLanguages</span><span class="sxs-lookup"><span data-stu-id="b1d8b-103">outlookUser: supportedLanguages</span></span>

> <span data-ttu-id="b1d8b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1d8b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b1d8b-106">Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-106">Get the list of locales and languages that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="b1d8b-107">Al configurar un cliente de Outlook, el usuario selecciona el idioma preferido de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-107">When setting up an Outlook client, the user selects the preferred language from this supported list.</span></span> <span data-ttu-id="b1d8b-108">Posteriormente, puede obtener el idioma preferido [obteniendo la configuración del buzón del usuario](user-get-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="b1d8b-108">You can subsequently get the preferred language by [getting the user's mailbox settings](user-get-mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="b1d8b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b1d8b-109">Permissions</span></span>
<span data-ttu-id="b1d8b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1d8b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1d8b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1d8b-112">Permission type</span></span>      | <span data-ttu-id="b1d8b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1d8b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b1d8b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1d8b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="b1d8b-115">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="b1d8b-115">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="b1d8b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1d8b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b1d8b-117">User.Read</span><span class="sxs-lookup"><span data-stu-id="b1d8b-117">User.Read</span></span>    |
|<span data-ttu-id="b1d8b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1d8b-118">Application</span></span> | <span data-ttu-id="b1d8b-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="b1d8b-119">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b1d8b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1d8b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedLanguages
GET /users/{id|userPrincipalName}/outlook/supportedLanguages
```
## <a name="request-headers"></a><span data-ttu-id="b1d8b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1d8b-121">Request headers</span></span>
| <span data-ttu-id="b1d8b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1d8b-122">Name</span></span>       | <span data-ttu-id="b1d8b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1d8b-123">Type</span></span> | <span data-ttu-id="b1d8b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1d8b-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b1d8b-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1d8b-125">Authorization</span></span>  | <span data-ttu-id="b1d8b-126">string</span><span class="sxs-lookup"><span data-stu-id="b1d8b-126">string</span></span>  | <span data-ttu-id="b1d8b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-p104">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="b1d8b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1d8b-129">Request body</span></span>
<span data-ttu-id="b1d8b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b1d8b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1d8b-131">Response</span></span>
<span data-ttu-id="b1d8b-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [localeInfo](../resources/localeinfo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-132">If successful, this method returns `200 OK` response code and a collection of [localeInfo](../resources/localeinfo.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b1d8b-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1d8b-133">Example</span></span>
<span data-ttu-id="b1d8b-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b1d8b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1d8b-135">Request</span></span>
<span data-ttu-id="b1d8b-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_supportedlanguages"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/supportedLanguages
```

##### <a name="response"></a><span data-ttu-id="b1d8b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1d8b-137">Response</span></span>
<span data-ttu-id="b1d8b-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1d8b-138">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.localeInfo",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.localeInfo)",
  "value":[
    {
      "locale":"af-ZA",
      "displayName":"Afrikaans (Suid-Afrika)"
    },
    {
      "locale":"en-US",
      "displayName":"English (United States)"
    },
    {
       "locale":"en-CA",
       "displayName":"English (Canada)"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: supportedLanguages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->