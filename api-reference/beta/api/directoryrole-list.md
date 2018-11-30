---
title: List directoryRoles
description: Enumera los roles de directorio que están activados en el inquilino.
ms.openlocfilehash: b7753fc62a7d3412e4f017eb644644561d1faf05
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087774"
---
# <a name="list-directoryroles"></a><span data-ttu-id="71810-103">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="71810-103">List directoryRoles</span></span>

> <span data-ttu-id="71810-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71810-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71810-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71810-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="71810-106">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="71810-106">List the directory roles that are activated in the tenant.</span></span>
## <a name="permissions"></a><span data-ttu-id="71810-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="71810-107">Permissions</span></span>
<span data-ttu-id="71810-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71810-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71810-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71810-110">Permission type</span></span>      | <span data-ttu-id="71810-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71810-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71810-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71810-112">Delegated (work or school account)</span></span> | <span data-ttu-id="71810-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="71810-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="71810-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71810-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71810-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71810-115">Not supported.</span></span>    |
|<span data-ttu-id="71810-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71810-116">Application</span></span> | <span data-ttu-id="71810-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71810-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="71810-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71810-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles
```
## <a name="optional-query-parameters"></a><span data-ttu-id="71810-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="71810-119">Optional query parameters</span></span>
<span data-ttu-id="71810-120">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="71810-120">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="71810-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71810-121">Request headers</span></span>
| <span data-ttu-id="71810-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="71810-122">Name</span></span>       | <span data-ttu-id="71810-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="71810-123">Type</span></span> | <span data-ttu-id="71810-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="71810-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="71810-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="71810-125">Authorization</span></span>  | <span data-ttu-id="71810-126">string</span><span class="sxs-lookup"><span data-stu-id="71810-126">string</span></span>  | <span data-ttu-id="71810-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71810-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="71810-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71810-129">Request body</span></span>
<span data-ttu-id="71810-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71810-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71810-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71810-131">Response</span></span>

<span data-ttu-id="71810-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71810-132">If successful, this method returns a `200 OK` response code and collection of [directoryRole](../resources/directoryrole.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="71810-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71810-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="71810-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71810-134">Request</span></span>
<span data-ttu-id="71810-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71810-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroles"
}-->
```http
GET https://graph.microsoft.com/beta/directoryRoles
```
##### <a name="response"></a><span data-ttu-id="71810-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71810-136">Response</span></span>
<span data-ttu-id="71810-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71810-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 187

{
  "value": [
    {
      "description": "description-value",
      "displayName": "displayName-value",
      "roleTemplateId": "roleTemplateId-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directoryRoles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
