---
title: List contactFolders
description: Obtiene la colección de la carpeta de contactos predeterminada del usuario que inició sesión.
author: dkershaw10
ms.openlocfilehash: b1f467fa74fa2962efbfc5e02c0de0a45c28ddde
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310531"
---
# <a name="list-contactfolders"></a><span data-ttu-id="93a95-103">List contactFolders</span><span class="sxs-lookup"><span data-stu-id="93a95-103">List contactFolders</span></span>

<span data-ttu-id="93a95-104">Obtiene la colección de la carpeta de contactos predeterminada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="93a95-104">Get the contact folder collection in the default Contacts folder of the signed-in user.</span></span>
## <a name="permissions"></a><span data-ttu-id="93a95-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="93a95-105">Permissions</span></span>
<span data-ttu-id="93a95-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="93a95-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="93a95-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="93a95-108">Permission type</span></span>      | <span data-ttu-id="93a95-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="93a95-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="93a95-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="93a95-110">Delegated (work or school account)</span></span> | <span data-ttu-id="93a95-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="93a95-111">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="93a95-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="93a95-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="93a95-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="93a95-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="93a95-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="93a95-114">Application</span></span> | <span data-ttu-id="93a95-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="93a95-115">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="93a95-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93a95-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/contactFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="93a95-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="93a95-117">Optional query parameters</span></span>
<span data-ttu-id="93a95-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93a95-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="93a95-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="93a95-119">Request headers</span></span>
| <span data-ttu-id="93a95-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93a95-120">Header</span></span>       | <span data-ttu-id="93a95-121">Valor</span><span class="sxs-lookup"><span data-stu-id="93a95-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="93a95-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="93a95-122">Authorization</span></span>  | <span data-ttu-id="93a95-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="93a95-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="93a95-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="93a95-125">Content-Type</span></span>   | <span data-ttu-id="93a95-126">application/json</span><span class="sxs-lookup"><span data-stu-id="93a95-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="93a95-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="93a95-127">Request body</span></span>
<span data-ttu-id="93a95-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="93a95-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="93a95-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93a95-129">Response</span></span>

<span data-ttu-id="93a95-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93a95-130">If successful, this method returns a `200 OK` response code and collection of [ContactFolder](../resources/contactfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="93a95-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93a95-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="93a95-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93a95-132">Request</span></span>
<span data-ttu-id="93a95-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="93a95-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders
```
##### <a name="response"></a><span data-ttu-id="93a95-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93a95-134">Response</span></span>
<span data-ttu-id="93a95-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="93a95-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
