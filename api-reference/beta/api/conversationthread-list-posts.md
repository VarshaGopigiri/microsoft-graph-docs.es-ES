---
title: Enumerar publicaciones
description: 'Obtenga las publicaciones del hilo especificado. Puede especificar la conversación primario y el subproceso, o bien, '
ms.openlocfilehash: 9253076a0232954acfdd1effad3fdb8084bba3fd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086626"
---
# <a name="list-posts"></a><span data-ttu-id="9223d-104">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="9223d-104">List posts</span></span>

> <span data-ttu-id="9223d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9223d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9223d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9223d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9223d-p103">Obtiene las publicaciones del hilo especificado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="9223d-p103">Get the posts of the specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="9223d-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9223d-109">Permissions</span></span>
<span data-ttu-id="9223d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9223d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9223d-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9223d-112">Permission type</span></span>      | <span data-ttu-id="9223d-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9223d-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9223d-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9223d-114">Delegated (work or school account)</span></span> | <span data-ttu-id="9223d-115">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="9223d-115">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="9223d-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9223d-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9223d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9223d-117">Not supported.</span></span>    |
|<span data-ttu-id="9223d-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9223d-118">Application</span></span> | <span data-ttu-id="9223d-119">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="9223d-119">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9223d-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9223d-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts
GET /groups/{id}/conversations/{id}/threads/{id}/posts

```
## <a name="optional-query-parameters"></a><span data-ttu-id="9223d-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9223d-121">Optional query parameters</span></span>
<span data-ttu-id="9223d-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9223d-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9223d-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9223d-123">Request headers</span></span>
| <span data-ttu-id="9223d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9223d-124">Header</span></span>       | <span data-ttu-id="9223d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9223d-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9223d-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="9223d-126">Authorization</span></span>  | <span data-ttu-id="9223d-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9223d-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9223d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9223d-129">Request body</span></span>
<span data-ttu-id="9223d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9223d-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9223d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9223d-131">Response</span></span>

<span data-ttu-id="9223d-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9223d-132">If successful, this method returns a `200 OK` response code and collection of [Post](../resources/post.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9223d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9223d-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9223d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9223d-134">Request</span></span>
<span data-ttu-id="9223d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9223d-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_posts"
}-->
```http
GET https://graph.microsoft.com/beta/groups/0d75b8dc-c42d-44dd-890a-751a99c0589f/threads/AAQkAD8EJUmcWwTJi06Cew==/posts
```
##### <a name="response"></a><span data-ttu-id="9223d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9223d-136">Response</span></span>
<span data-ttu-id="9223d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9223d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('0d75b8dc-c42d-44dd-890a-751a99c0589f')/threads('AAQkAD8EJUmcWwTJi06Cew%3D%3D')/posts",
    "value":[
        {
            "@odata.etag":"W/\"CQAAABYAAAC/3QURwysWS6IJYYw5exv4AAAAAAlK\"",
            "id":"AQMkADgAAAIJbQAAAA==",
            "createdDateTime":"2018-01-11T17:36:17Z",
            "lastModifiedDateTime":"2018-01-11T17:36:17Z",
            "importance": "normal",
            "changeKey":"CQAAABYAAAC/3QURwysWS6IJYYw5exv4AAAAAAlK",
            "categories":[

            ],
            "receivedDateTime":"2018-01-11T17:36:17Z",
            "hasAttachments":false,
            "body":{
                "contentType":"html",
                "content":"<html><body></body></html>"
            },
            "from":{
                "emailAddress":{
                    "name":"Marketing",
                    "address":"Marketing@M365B489948.onmicrosoft.com"
                }
            },
            "sender":{
                "emailAddress":{
                    "name":"Marketing",
                    "address":"Marketing@M365B489948.onmicrosoft.com"
                }
            }
        }
    ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List posts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
