---
title: List directoryRoleTemplates
description: Recuperar una lista de objetos de directoryroletemplate.
ms.openlocfilehash: 58d88187c7b7791ca0b4308fdd6224c6bebc4a8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083604"
---
# <a name="list-directoryroletemplates"></a><span data-ttu-id="3d7f0-103">List directoryRoleTemplates</span><span class="sxs-lookup"><span data-stu-id="3d7f0-103">List directoryRoleTemplates</span></span>

> <span data-ttu-id="3d7f0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3d7f0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3d7f0-106">Recuperar una lista de objetos de directoryroletemplate.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-106">Retrieve a list of directoryroletemplate objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="3d7f0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d7f0-107">Permissions</span></span>
<span data-ttu-id="3d7f0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d7f0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3d7f0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d7f0-110">Permission type</span></span>      | <span data-ttu-id="3d7f0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d7f0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3d7f0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d7f0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3d7f0-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3d7f0-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3d7f0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d7f0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d7f0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-115">Not supported.</span></span>    |
|<span data-ttu-id="3d7f0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d7f0-116">Application</span></span> | <span data-ttu-id="3d7f0-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3d7f0-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3d7f0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d7f0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3d7f0-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3d7f0-119">Optional query parameters</span></span>
<span data-ttu-id="3d7f0-120">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="3d7f0-120">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="3d7f0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d7f0-121">Request headers</span></span>
| <span data-ttu-id="3d7f0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d7f0-122">Name</span></span>       | <span data-ttu-id="3d7f0-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d7f0-123">Type</span></span> | <span data-ttu-id="3d7f0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d7f0-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3d7f0-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d7f0-125">Authorization</span></span>  | <span data-ttu-id="3d7f0-126">string</span><span class="sxs-lookup"><span data-stu-id="3d7f0-126">string</span></span>  | <span data-ttu-id="3d7f0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3d7f0-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3d7f0-129">Request body</span></span>
<span data-ttu-id="3d7f0-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3d7f0-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d7f0-131">Response</span></span>

<span data-ttu-id="3d7f0-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-132">If successful, this method returns a `200 OK` response code and collection of [directoryRoleTemplate](../resources/directoryroletemplate.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3d7f0-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d7f0-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3d7f0-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d7f0-134">Request</span></span>
<span data-ttu-id="3d7f0-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplates"
}-->
```http
GET https://graph.microsoft.com/beta/directoryRoleTemplates
```
##### <a name="response"></a><span data-ttu-id="3d7f0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d7f0-136">Response</span></span>
<span data-ttu-id="3d7f0-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3d7f0-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRoleTemplate",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 139

{
  "value": [
    {
      "description": "description-value",
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
  "description": "List directoryRoleTemplates",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
