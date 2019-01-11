---
title: List mailFolders
description: Obtenga todas las carpetas de correo en el buzón del usuario que ha iniciado sesión.
localization_priority: Normal
ms.openlocfilehash: dca8b39b9685a0744a4b1ba0c1de148ed8987436
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866748"
---
# <a name="list-mailfolders"></a><span data-ttu-id="1fbc7-103">List mailFolders</span><span class="sxs-lookup"><span data-stu-id="1fbc7-103">List mailFolders</span></span>

> <span data-ttu-id="1fbc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1fbc7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1fbc7-106">Obtenga todas las carpetas de correo en el buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-106">Get all the mail folders in the signed-in user's mailbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="1fbc7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1fbc7-107">Permissions</span></span>
<span data-ttu-id="1fbc7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1fbc7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1fbc7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1fbc7-110">Permission type</span></span>      | <span data-ttu-id="1fbc7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1fbc7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1fbc7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1fbc7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1fbc7-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1fbc7-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="1fbc7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1fbc7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1fbc7-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1fbc7-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="1fbc7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1fbc7-116">Application</span></span> | <span data-ttu-id="1fbc7-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1fbc7-117">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1fbc7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1fbc7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/mailFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1fbc7-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1fbc7-119">Optional query parameters</span></span>
<span data-ttu-id="1fbc7-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1fbc7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1fbc7-121">Request headers</span></span>
| <span data-ttu-id="1fbc7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fbc7-122">Header</span></span>       | <span data-ttu-id="1fbc7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1fbc7-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1fbc7-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="1fbc7-124">Authorization</span></span>  | <span data-ttu-id="1fbc7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="1fbc7-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1fbc7-127">Content-Type</span></span>   | <span data-ttu-id="1fbc7-128">application/json</span><span class="sxs-lookup"><span data-stu-id="1fbc7-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1fbc7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1fbc7-129">Request body</span></span>
<span data-ttu-id="1fbc7-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1fbc7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fbc7-131">Response</span></span>

<span data-ttu-id="1fbc7-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-132">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1fbc7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fbc7-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1fbc7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1fbc7-134">Request</span></span>
<span data-ttu-id="1fbc7-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders
```
##### <a name="response"></a><span data-ttu-id="1fbc7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fbc7-136">Response</span></span>
<span data-ttu-id="1fbc7-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 232

{
  "value": [
    {
      "displayName": "displayName-value",
      "parentFolderId": "parentFolderId-value",
      "childFolderCount": 99,
      "unreadItemCount": 99,
      "totalItemCount": 99,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List mailFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
