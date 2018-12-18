---
title: Obtener directoryObject
description: Recuperar las propiedades y relaciones del objeto directoryobject.
author: lleonard-msft
ms.openlocfilehash: 52862d10c8361ea8ba365d06dcbaf0ce06b2779f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316376"
---
# <a name="get-directoryobject"></a><span data-ttu-id="bf14b-103">Obtener directoryObject</span><span class="sxs-lookup"><span data-stu-id="bf14b-103">Get directoryObject</span></span>

> <span data-ttu-id="bf14b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf14b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf14b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf14b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bf14b-106">Recuperar las propiedades y relaciones del objeto directoryobject.</span><span class="sxs-lookup"><span data-stu-id="bf14b-106">Retrieve the properties and relationships of directoryobject object.</span></span>
## <a name="permissions"></a><span data-ttu-id="bf14b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf14b-107">Permissions</span></span>
<span data-ttu-id="bf14b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf14b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf14b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf14b-110">Permission type</span></span>      | <span data-ttu-id="bf14b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf14b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf14b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf14b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bf14b-113">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bf14b-113">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="bf14b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf14b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf14b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf14b-115">Not supported.</span></span>    |
|<span data-ttu-id="bf14b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf14b-116">Application</span></span> | <span data-ttu-id="bf14b-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="bf14b-117">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bf14b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf14b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryObjects/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bf14b-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bf14b-119">Optional query parameters</span></span>
<span data-ttu-id="bf14b-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf14b-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bf14b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf14b-121">Request headers</span></span>
| <span data-ttu-id="bf14b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf14b-122">Name</span></span>       | <span data-ttu-id="bf14b-123">Type</span><span class="sxs-lookup"><span data-stu-id="bf14b-123">Type</span></span> | <span data-ttu-id="bf14b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf14b-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bf14b-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="bf14b-125">Authorization</span></span>  | <span data-ttu-id="bf14b-126">string</span><span class="sxs-lookup"><span data-stu-id="bf14b-126">string</span></span>  | <span data-ttu-id="bf14b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf14b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bf14b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf14b-129">Request body</span></span>
<span data-ttu-id="bf14b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf14b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bf14b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf14b-131">Response</span></span>

<span data-ttu-id="bf14b-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf14b-132">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bf14b-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf14b-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bf14b-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf14b-134">Request</span></span>
<span data-ttu-id="bf14b-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf14b-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryobject"
}-->
```http
GET https://graph.microsoft.com/beta/directoryObjects/{id}
```
##### <a name="response"></a><span data-ttu-id="bf14b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf14b-136">Response</span></span>
<span data-ttu-id="bf14b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf14b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 22

{
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directoryObject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
