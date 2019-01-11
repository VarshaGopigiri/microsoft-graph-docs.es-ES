---
title: List directoryRoleTemplates
description: Recuperar una lista de objetos de directoryroletemplate.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: a61127b7fdd31ce55f44a42ac847c5ac50932cf6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848569"
---
# <a name="list-directoryroletemplates"></a><span data-ttu-id="eb3d4-103">List directoryRoleTemplates</span><span class="sxs-lookup"><span data-stu-id="eb3d4-103">List directoryRoleTemplates</span></span>

> <span data-ttu-id="eb3d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb3d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eb3d4-106">Recuperar una lista de objetos de directoryroletemplate.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-106">Retrieve a list of directoryroletemplate objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="eb3d4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eb3d4-107">Permissions</span></span>
<span data-ttu-id="eb3d4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb3d4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb3d4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb3d4-110">Permission type</span></span>      | <span data-ttu-id="eb3d4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb3d4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb3d4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb3d4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eb3d4-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eb3d4-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eb3d4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb3d4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb3d4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-115">Not supported.</span></span>    |
|<span data-ttu-id="eb3d4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb3d4-116">Application</span></span> | <span data-ttu-id="eb3d4-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb3d4-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb3d4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb3d4-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="eb3d4-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="eb3d4-119">Optional query parameters</span></span>
<span data-ttu-id="eb3d4-120">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="eb3d4-120">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="eb3d4-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb3d4-121">Request headers</span></span>
| <span data-ttu-id="eb3d4-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb3d4-122">Name</span></span>       | <span data-ttu-id="eb3d4-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb3d4-123">Type</span></span> | <span data-ttu-id="eb3d4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb3d4-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="eb3d4-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="eb3d4-125">Authorization</span></span>  | <span data-ttu-id="eb3d4-126">string</span><span class="sxs-lookup"><span data-stu-id="eb3d4-126">string</span></span>  | <span data-ttu-id="eb3d4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eb3d4-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb3d4-129">Request body</span></span>
<span data-ttu-id="eb3d4-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eb3d4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb3d4-131">Response</span></span>

<span data-ttu-id="eb3d4-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-132">If successful, this method returns a `200 OK` response code and collection of [directoryRoleTemplate](../resources/directoryroletemplate.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="eb3d4-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb3d4-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eb3d4-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb3d4-134">Request</span></span>
<span data-ttu-id="eb3d4-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplates"
}-->
```http
GET https://graph.microsoft.com/beta/directoryRoleTemplates
```
##### <a name="response"></a><span data-ttu-id="eb3d4-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb3d4-136">Response</span></span>
<span data-ttu-id="eb3d4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb3d4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
