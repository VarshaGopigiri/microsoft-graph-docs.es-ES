---
title: Enumerar reglas
description: Obtener todos los objetos messageRule definidos para la Bandeja de entrada del usuario.
localization_priority: Normal
ms.openlocfilehash: 3145c1f2b2900971021b6799917996e23cf36866
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863367"
---
# <a name="list-rules"></a><span data-ttu-id="efe63-103">Enumerar reglas</span><span class="sxs-lookup"><span data-stu-id="efe63-103">List rules</span></span>

> <span data-ttu-id="efe63-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="efe63-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="efe63-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="efe63-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="efe63-106">Obtener todos los objetos [messageRule](../resources/messagerule.md) definidos para la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="efe63-106">Get all the [messageRule](../resources/messagerule.md) objects defined for the user's Inbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="efe63-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="efe63-107">Permissions</span></span>
<span data-ttu-id="efe63-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="efe63-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="efe63-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="efe63-110">Permission type</span></span>      | <span data-ttu-id="efe63-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="efe63-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="efe63-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="efe63-112">Delegated (work or school account)</span></span> | <span data-ttu-id="efe63-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="efe63-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="efe63-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="efe63-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="efe63-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="efe63-115">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="efe63-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="efe63-116">Application</span></span> | <span data-ttu-id="efe63-117">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="efe63-117">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="efe63-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="efe63-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/inbox/messagerules
GET /users/{id | userPrincipalName}/mailFolders/inbox/messagerules
```
## <a name="optional-query-parameters"></a><span data-ttu-id="efe63-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="efe63-119">Optional query parameters</span></span>
<span data-ttu-id="efe63-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="efe63-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="efe63-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="efe63-121">Request headers</span></span>
| <span data-ttu-id="efe63-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="efe63-122">Name</span></span>       | <span data-ttu-id="efe63-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="efe63-123">Type</span></span> | <span data-ttu-id="efe63-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="efe63-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="efe63-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="efe63-125">Authorization</span></span>  | <span data-ttu-id="efe63-126">string</span><span class="sxs-lookup"><span data-stu-id="efe63-126">string</span></span>  | <span data-ttu-id="efe63-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="efe63-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="efe63-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="efe63-129">Request body</span></span>
<span data-ttu-id="efe63-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="efe63-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="efe63-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="efe63-131">Response</span></span>
<span data-ttu-id="efe63-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [messageRule](../resources/messagerule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="efe63-132">If successful, this method returns a `200 OK` response code and collection of [messageRule](../resources/messagerule.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="efe63-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="efe63-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="efe63-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="efe63-134">Request</span></span>
<span data-ttu-id="efe63-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="efe63-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messagerules"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/inbox/messagerules
```
##### <a name="response"></a><span data-ttu-id="efe63-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="efe63-136">Response</span></span>
<span data-ttu-id="efe63-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="efe63-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Me/mailFolders('inbox')/messageRules",
  "value":[
    {
      "id":"AQAAAJ5dZp8=",
      "displayName":"Remove spam",
      "sequence":1,
      "isEnabled":true,
      "hasError":false,
      "isReadOnly":false,
      "conditions":{
        "subjectContains":[
          "enter to win"
        ]
      },
      "actions":{
        "delete":true,
        "stopProcessingRules":true
      }
    },
    {
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
  ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List rules",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
