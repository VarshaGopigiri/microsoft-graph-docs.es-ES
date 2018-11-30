---
title: List contactFolders
description: Obtenga todas las carpetas de contactos en el buzón del usuario que ha iniciado sesión.
ms.openlocfilehash: 08f763d8bc1e9a05c047f194e2847d76c385e587
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087222"
---
# <a name="list-contactfolders"></a><span data-ttu-id="7d994-103">List contactFolders</span><span class="sxs-lookup"><span data-stu-id="7d994-103">List contactFolders</span></span>

> <span data-ttu-id="7d994-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d994-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d994-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d994-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7d994-106">Obtenga todas las carpetas de contactos en el buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="7d994-106">Get all the contact folders in the signed-in user's mailbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="7d994-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d994-107">Permissions</span></span>
<span data-ttu-id="7d994-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d994-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d994-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d994-110">Permission type</span></span>      | <span data-ttu-id="7d994-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d994-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d994-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d994-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7d994-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7d994-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="7d994-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d994-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d994-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7d994-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="7d994-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d994-116">Application</span></span> | <span data-ttu-id="7d994-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7d994-117">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d994-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d994-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/contactFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7d994-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7d994-119">Optional query parameters</span></span>
<span data-ttu-id="7d994-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d994-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7d994-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d994-121">Request headers</span></span>
| <span data-ttu-id="7d994-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d994-122">Header</span></span>       | <span data-ttu-id="7d994-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7d994-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7d994-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="7d994-124">Authorization</span></span>  | <span data-ttu-id="7d994-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d994-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7d994-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7d994-127">Content-Type</span></span>   | <span data-ttu-id="7d994-128">application/json</span><span class="sxs-lookup"><span data-stu-id="7d994-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7d994-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d994-129">Request body</span></span>
<span data-ttu-id="7d994-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7d994-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7d994-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d994-131">Response</span></span>

<span data-ttu-id="7d994-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d994-132">If successful, this method returns a `200 OK` response code and collection of [ContactFolder](../resources/contactfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7d994-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d994-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7d994-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d994-134">Request</span></span>
<span data-ttu-id="7d994-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d994-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/contactFolders
```
##### <a name="response"></a><span data-ttu-id="7d994-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d994-136">Response</span></span>
<span data-ttu-id="7d994-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d994-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 145

{
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "displayName": "displayName-value",
      "wellKnownName": "wellKnownName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List contactFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
