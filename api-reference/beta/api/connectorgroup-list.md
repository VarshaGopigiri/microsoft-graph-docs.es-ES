---
title: Lista connectorGroups
description: Recuperar una lista de objetos de connectorgroup.
localization_priority: Normal
ms.openlocfilehash: a9629e045487e7f29c84f3f24be0abedbe846ea8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808364"
---
# <a name="list-connectorgroups"></a><span data-ttu-id="65e56-103">Lista connectorGroups</span><span class="sxs-lookup"><span data-stu-id="65e56-103">List connectorGroups</span></span>

> <span data-ttu-id="65e56-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65e56-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65e56-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65e56-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="65e56-106">Recuperar una lista de objetos de connectorgroup.</span><span class="sxs-lookup"><span data-stu-id="65e56-106">Retrieve a list of connectorgroup objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="65e56-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="65e56-107">Permissions</span></span>
<span data-ttu-id="65e56-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65e56-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65e56-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65e56-110">Permission type</span></span>      | <span data-ttu-id="65e56-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65e56-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="65e56-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65e56-112">Delegated (work or school account)</span></span> | <span data-ttu-id="65e56-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="65e56-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="65e56-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65e56-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="65e56-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65e56-115">Not supported.</span></span>    |
|<span data-ttu-id="65e56-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65e56-116">Application</span></span> | <span data-ttu-id="65e56-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="65e56-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="65e56-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65e56-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /connectorGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="65e56-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="65e56-119">Optional query parameters</span></span>
<span data-ttu-id="65e56-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65e56-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="65e56-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65e56-121">Request headers</span></span>
| <span data-ttu-id="65e56-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="65e56-122">Name</span></span>      |<span data-ttu-id="65e56-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="65e56-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="65e56-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="65e56-124">Authorization</span></span>  | <span data-ttu-id="65e56-125">Bearer.</span><span class="sxs-lookup"><span data-stu-id="65e56-125">Bearer.</span></span> <span data-ttu-id="65e56-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="65e56-126">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="65e56-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65e56-127">Request body</span></span>
<span data-ttu-id="65e56-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="65e56-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="65e56-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65e56-129">Response</span></span>

<span data-ttu-id="65e56-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [connectorGroup](../resources/connectorgroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65e56-130">If successful, this method returns a `200 OK` response code and collection of [connectorGroup](../resources/connectorgroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="65e56-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65e56-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="65e56-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65e56-132">Request</span></span>
<span data-ttu-id="65e56-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65e56-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_connectorgroups"
}-->
```http
GET https://graph.microsoft.com/{ver}/connectorGroups
```
##### <a name="response"></a><span data-ttu-id="65e56-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65e56-134">Response</span></span>
<span data-ttu-id="65e56-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65e56-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.connectorGroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 164

{
  "value": [
    {
      "id": "id-value",
      "name": "name-value",
      "connectorGroupType": "connectorGroupType-value",
      "isDefault": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List connectorGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
