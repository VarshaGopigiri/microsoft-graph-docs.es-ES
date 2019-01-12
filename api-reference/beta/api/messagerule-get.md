---
title: Obtener regla
description: Obtener las propiedades y relaciones de un objeto messageRule.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 9828986680febc4b499163f2591a537c43a98cd1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916715"
---
# <a name="get-rule"></a><span data-ttu-id="b7ca7-103">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="b7ca7-103">Get rule</span></span>

> <span data-ttu-id="b7ca7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b7ca7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b7ca7-106">Obtener las propiedades y relaciones de un objeto [messageRule](../resources/messagerule.md).</span><span class="sxs-lookup"><span data-stu-id="b7ca7-106">Get the properties and relationships of a [messageRule](../resources/messagerule.md) object.</span></span>


## <a name="permissions"></a><span data-ttu-id="b7ca7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7ca7-107">Permissions</span></span>
<span data-ttu-id="b7ca7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7ca7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7ca7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7ca7-110">Permission type</span></span>      | <span data-ttu-id="b7ca7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7ca7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7ca7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7ca7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b7ca7-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="b7ca7-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="b7ca7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7ca7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7ca7-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="b7ca7-115">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="b7ca7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7ca7-116">Application</span></span> | <span data-ttu-id="b7ca7-117">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="b7ca7-117">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="b7ca7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7ca7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/inbox/messagerules/{id}
GET /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b7ca7-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b7ca7-119">Optional query parameters</span></span>
<span data-ttu-id="b7ca7-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b7ca7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ca7-121">Request headers</span></span>
| <span data-ttu-id="b7ca7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b7ca7-122">Name</span></span>      |<span data-ttu-id="b7ca7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ca7-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b7ca7-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b7ca7-124">Authorization</span></span>  | <span data-ttu-id="b7ca7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="b7ca7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ca7-127">Request body</span></span>
<span data-ttu-id="b7ca7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="b7ca7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7ca7-129">Response</span></span>
<span data-ttu-id="b7ca7-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-130">If successful, this method returns a `200 OK` response code and [messageRule](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b7ca7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7ca7-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b7ca7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ca7-132">Request</span></span>
<span data-ttu-id="b7ca7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messagerule"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')
```
##### <a name="response"></a><span data-ttu-id="b7ca7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7ca7-134">Response</span></span>
<span data-ttu-id="b7ca7-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-135">Here is an example of the response.</span></span> <span data-ttu-id="b7ca7-136">De forma predeterminada, las propiedades de fecha y hora de la respuesta están en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-136">By default, the date-time properties in the response are in UTC.</span></span> 

<span data-ttu-id="b7ca7-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b7ca7-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
