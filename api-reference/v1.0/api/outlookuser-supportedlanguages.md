---
title: 'outlookUser: supportedLanguages'
description: Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.
localization_priority: Normal
ms.openlocfilehash: 78093c61e73dd4248e881596bf8a18004acc48ca
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839837"
---
# <a name="outlookuser-supportedlanguages"></a><span data-ttu-id="21f71-103">outlookUser: supportedLanguages</span><span class="sxs-lookup"><span data-stu-id="21f71-103">outlookUser: supportedLanguages</span></span>

<span data-ttu-id="21f71-104">Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="21f71-104">Get the list of locales and languages that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="21f71-105">Al configurar un cliente de Outlook, el usuario selecciona el idioma preferido de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="21f71-105">When setting up an Outlook client, the user selects the preferred language from this supported list.</span></span> <span data-ttu-id="21f71-106">Posteriormente, puede obtener el idioma preferido [obteniendo la configuración del buzón del usuario](user-get-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="21f71-106">You can subsequently get the preferred language by [getting the user's mailbox settings](user-get-mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="21f71-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="21f71-107">Permissions</span></span>
<span data-ttu-id="21f71-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21f71-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21f71-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21f71-110">Permission type</span></span>      | <span data-ttu-id="21f71-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21f71-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="21f71-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21f71-112">Delegated (work or school account)</span></span> | <span data-ttu-id="21f71-113">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="21f71-113">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="21f71-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21f71-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="21f71-115">User.Read</span><span class="sxs-lookup"><span data-stu-id="21f71-115">User.Read</span></span>    |
|<span data-ttu-id="21f71-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21f71-116">Application</span></span> | <span data-ttu-id="21f71-117">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="21f71-117">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="21f71-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21f71-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedLanguages
GET /users/{id|userPrincipalName}/outlook/supportedLanguages
```
## <a name="request-headers"></a><span data-ttu-id="21f71-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21f71-119">Request headers</span></span>
| <span data-ttu-id="21f71-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="21f71-120">Name</span></span>       | <span data-ttu-id="21f71-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="21f71-121">Type</span></span> | <span data-ttu-id="21f71-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="21f71-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="21f71-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="21f71-123">Authorization</span></span>  | <span data-ttu-id="21f71-124">string</span><span class="sxs-lookup"><span data-stu-id="21f71-124">string</span></span>  | <span data-ttu-id="21f71-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21f71-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="21f71-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21f71-127">Request body</span></span>
<span data-ttu-id="21f71-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21f71-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="21f71-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21f71-129">Response</span></span>
<span data-ttu-id="21f71-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [localeInfo](../resources/localeinfo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21f71-130">If successful, this method returns `200 OK` response code and a collection of [localeInfo](../resources/localeinfo.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="21f71-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21f71-131">Example</span></span>
<span data-ttu-id="21f71-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="21f71-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="21f71-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21f71-133">Request</span></span>
<span data-ttu-id="21f71-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21f71-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_supportedlanguages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedLanguages
```

##### <a name="response"></a><span data-ttu-id="21f71-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21f71-135">Response</span></span>
<span data-ttu-id="21f71-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21f71-136">Here is an example of the response.</span></span> 
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
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.localeInfo)",
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
