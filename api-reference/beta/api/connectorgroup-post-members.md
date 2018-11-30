---
title: Agregar conector a connectorGroup
description: Utilice esta API para agregar un conector a un connectorGroup.
ms.openlocfilehash: f5e7330dd5476daacda47a78400181ad3ebc0e2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085609"
---
# <a name="add-connector-to-connectorgroup"></a><span data-ttu-id="7fb02-103">Agregar conector a connectorGroup</span><span class="sxs-lookup"><span data-stu-id="7fb02-103">Add connector to connectorGroup</span></span>

> <span data-ttu-id="7fb02-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7fb02-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7fb02-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7fb02-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7fb02-106">Utilice esta API para agregar un conector a un connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="7fb02-106">Use this API to add a connector to a connectorGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="7fb02-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7fb02-107">Permissions</span></span>
<span data-ttu-id="7fb02-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7fb02-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7fb02-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7fb02-110">Permission type</span></span>      | <span data-ttu-id="7fb02-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7fb02-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7fb02-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7fb02-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7fb02-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7fb02-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7fb02-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7fb02-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7fb02-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fb02-115">Not supported.</span></span>    |
|<span data-ttu-id="7fb02-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7fb02-116">Application</span></span> | <span data-ttu-id="7fb02-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7fb02-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7fb02-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7fb02-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /connectorGroups/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="7fb02-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7fb02-119">Request headers</span></span>
| <span data-ttu-id="7fb02-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7fb02-120">Name</span></span>       | <span data-ttu-id="7fb02-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fb02-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7fb02-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="7fb02-122">Authorization</span></span>  | <span data-ttu-id="7fb02-123">Bearer.</span><span class="sxs-lookup"><span data-stu-id="7fb02-123">Bearer.</span></span> <span data-ttu-id="7fb02-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7fb02-124">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="7fb02-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7fb02-125">Request body</span></span>
<span data-ttu-id="7fb02-126">En el cuerpo de la solicitud, proporcionar una representación JSON de un vínculo a un objeto de [conector](../resources/connector.md) .</span><span class="sxs-lookup"><span data-stu-id="7fb02-126">In the request body, supply a JSON representation of a link to a   [connector](../resources/connector.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="7fb02-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fb02-127">Response</span></span>

<span data-ttu-id="7fb02-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y el [conector](../resources/connector.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fb02-128">If successful, this method returns `201 Created` response code and [connector](../resources/connector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7fb02-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fb02-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7fb02-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7fb02-130">Request</span></span>
<span data-ttu-id="7fb02-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7fb02-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_connector_from_connectorgroup"
}-->
```http
POST https://graph.microsoft.com/{ver}/connectorGroups/{id}/members/$ref
Content-type: application/json
Content-length: 104

{
  "@odata.id": "https://graph.microsoft.com/{ver}/connector/{id}"
}
```
<span data-ttu-id="7fb02-132">En el cuerpo de la solicitud, proporcionar una representación JSON de un vínculo a un objeto de [conector](../resources/connector.md) .</span><span class="sxs-lookup"><span data-stu-id="7fb02-132">In the request body, supply a JSON representation of a link to a  [connector](../resources/connector.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="7fb02-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fb02-133">Response</span></span>
<span data-ttu-id="7fb02-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7fb02-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.connector"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 124

{
  "id": "id-value",
  "machineName": "machineName-value",
  "externalIp": "externalIp-value",
  "status": "status-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create connector",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->