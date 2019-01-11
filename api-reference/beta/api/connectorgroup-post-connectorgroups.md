---
title: Crear connectorGroup
description: Utilice esta API para crear un nuevo connectorGroup.
localization_priority: Normal
ms.openlocfilehash: 65fe6dd901de6238c450b4896b37d56fa8ea602f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824300"
---
# <a name="create-connectorgroup"></a><span data-ttu-id="c64c9-103">Crear connectorGroup</span><span class="sxs-lookup"><span data-stu-id="c64c9-103">Create connectorGroup</span></span>

> <span data-ttu-id="c64c9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c64c9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c64c9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c64c9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c64c9-106">Utilice esta API para crear un nuevo connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="c64c9-106">Use this API to create a new connectorGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="c64c9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c64c9-107">Permissions</span></span>
<span data-ttu-id="c64c9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c64c9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c64c9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c64c9-110">Permission type</span></span>      | <span data-ttu-id="c64c9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c64c9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c64c9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c64c9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c64c9-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c64c9-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c64c9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c64c9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c64c9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c64c9-115">Not supported.</span></span>    |
|<span data-ttu-id="c64c9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c64c9-116">Application</span></span> | <span data-ttu-id="c64c9-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c64c9-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c64c9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c64c9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /connectorGroups

```
## <a name="request-headers"></a><span data-ttu-id="c64c9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c64c9-119">Request headers</span></span>
| <span data-ttu-id="c64c9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c64c9-120">Name</span></span>       | <span data-ttu-id="c64c9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c64c9-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c64c9-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="c64c9-122">Authorization</span></span>  | <span data-ttu-id="c64c9-123">Bearer.</span><span class="sxs-lookup"><span data-stu-id="c64c9-123">Bearer.</span></span> <span data-ttu-id="c64c9-124">Necesario</span><span class="sxs-lookup"><span data-stu-id="c64c9-124">Requried</span></span>|

## <a name="request-body"></a><span data-ttu-id="c64c9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c64c9-125">Request body</span></span>
<span data-ttu-id="c64c9-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [connectorGroup](../resources/connectorgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c64c9-126">In the request body, supply a JSON representation of [connectorGroup](../resources/connectorgroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c64c9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c64c9-127">Response</span></span>

<span data-ttu-id="c64c9-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y [connectorGroup](../resources/connectorgroup.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c64c9-128">If successful, this method returns `201 Created` response code and [connectorGroup](../resources/connectorgroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c64c9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c64c9-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c64c9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c64c9-130">Request</span></span>
<span data-ttu-id="c64c9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c64c9-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_connectorgroup_from_connectorgroups"
}-->
```http
POST https://graph.microsoft.com/{ver}/connectorGroups
Content-type: application/json
Content-length: 99

{
  "name": "name-value",
  "connectorGroupType": "connectorGroupType-value",
  "isDefault": false
}
```
<span data-ttu-id="c64c9-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [connectorGroup](../resources/connectorgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c64c9-132">In the request body, supply a JSON representation of [connectorGroup](../resources/connectorgroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="c64c9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c64c9-133">Response</span></span>
<span data-ttu-id="c64c9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c64c9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.connectorGroup"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 119

{
  "id": "id-value",
  "name": "name-value",
  "connectorGroupType": "connectorGroupType-value",
  "isDefault": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create connectorGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
