---
title: List memberOf
description: Recuperar el connectorgroup de que el conector es un miembro.
localization_priority: Normal
ms.openlocfilehash: 4eb56931aa134375370167f989d6348760010647
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864725"
---
# <a name="list-memberof"></a><span data-ttu-id="927e1-103">List memberOf</span><span class="sxs-lookup"><span data-stu-id="927e1-103">List memberOf</span></span>

> <span data-ttu-id="927e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="927e1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="927e1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="927e1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="927e1-106">Recuperar el connectorgroup de que el conector es un miembro.</span><span class="sxs-lookup"><span data-stu-id="927e1-106">Retrieve the connectorgroup the connector is a member of.</span></span>
## <a name="permissions"></a><span data-ttu-id="927e1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="927e1-107">Permissions</span></span>
<span data-ttu-id="927e1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="927e1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="927e1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="927e1-110">Permission type</span></span>      | <span data-ttu-id="927e1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="927e1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="927e1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="927e1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="927e1-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="927e1-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="927e1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="927e1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="927e1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="927e1-115">Not supported.</span></span>    |
|<span data-ttu-id="927e1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="927e1-116">Application</span></span> | <span data-ttu-id="927e1-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="927e1-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="927e1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="927e1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /connectors/{id}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="927e1-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="927e1-119">Optional query parameters</span></span>
<span data-ttu-id="927e1-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="927e1-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="927e1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="927e1-121">Request headers</span></span>
| <span data-ttu-id="927e1-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="927e1-122">Name</span></span>      |<span data-ttu-id="927e1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="927e1-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="927e1-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="927e1-124">Authorization</span></span>  | <span data-ttu-id="927e1-125">Bearer.</span><span class="sxs-lookup"><span data-stu-id="927e1-125">Bearer.</span></span> <span data-ttu-id="927e1-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="927e1-126">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="927e1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="927e1-127">Request body</span></span>
<span data-ttu-id="927e1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="927e1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="927e1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="927e1-129">Response</span></span>

<span data-ttu-id="927e1-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [connectorGroup](../resources/connectorgroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="927e1-130">If successful, this method returns a `200 OK` response code and collection of [connectorGroup](../resources/connectorgroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="927e1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="927e1-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="927e1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="927e1-132">Request</span></span>
<span data-ttu-id="927e1-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="927e1-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/{ver}/connectors/{id}/memberOf
```
##### <a name="response"></a><span data-ttu-id="927e1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="927e1-134">Response</span></span>
<span data-ttu-id="927e1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="927e1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
