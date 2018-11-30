---
title: Obtener directoryObject
description: Recupera las propiedades y relaciones del objeto directoryObject.
ms.openlocfilehash: 21086b7d30b1e4480450b0bb63f4be27f7e7bd5d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032121"
---
# <a name="get-directoryobject"></a><span data-ttu-id="13421-103">Obtener directoryObject</span><span class="sxs-lookup"><span data-stu-id="13421-103">Get directoryObject</span></span>

<span data-ttu-id="13421-104">Recupera las propiedades y relaciones del objeto directoryObject.</span><span class="sxs-lookup"><span data-stu-id="13421-104">Retrieve the properties and relationships of directoryObject object.</span></span>
## <a name="permissions"></a><span data-ttu-id="13421-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="13421-105">Permissions</span></span>
<span data-ttu-id="13421-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13421-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13421-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13421-108">Permission type</span></span>      | <span data-ttu-id="13421-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13421-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="13421-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13421-110">Delegated (work or school account)</span></span> | <span data-ttu-id="13421-111">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="13421-111">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="13421-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13421-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="13421-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13421-113">Not supported.</span></span>    |
|<span data-ttu-id="13421-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13421-114">Application</span></span> | <span data-ttu-id="13421-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="13421-115">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="13421-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13421-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryObjects/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="13421-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="13421-117">Optional query parameters</span></span>
<span data-ttu-id="13421-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13421-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="13421-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13421-119">Request headers</span></span>
| <span data-ttu-id="13421-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="13421-120">Name</span></span>       | <span data-ttu-id="13421-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="13421-121">Type</span></span> | <span data-ttu-id="13421-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="13421-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="13421-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="13421-123">Authorization</span></span>  | <span data-ttu-id="13421-124">string</span><span class="sxs-lookup"><span data-stu-id="13421-124">string</span></span>  | <span data-ttu-id="13421-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13421-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="13421-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13421-127">Request body</span></span>
<span data-ttu-id="13421-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="13421-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="13421-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13421-129">Response</span></span>

<span data-ttu-id="13421-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13421-130">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="13421-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13421-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="13421-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13421-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryobject"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryObjects/{id}
```
##### <a name="response"></a><span data-ttu-id="13421-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13421-133">Response</span></span>
<span data-ttu-id="13421-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13421-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

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