---
title: Crear administrativeUnit
description: Utilice esta API para crear un nuevo administrativeUnit.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 9ec6d1579e1a27317bd7d4e126a73a1b4175ec86
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859874"
---
# <a name="create-administrativeunit"></a><span data-ttu-id="a332a-103">Crear administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="a332a-103">Create administrativeUnit</span></span>

> <span data-ttu-id="a332a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a332a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a332a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a332a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a332a-106">Utilice esta API para crear un nuevo [administrativeUnit](../resources/administrativeunit.md).</span><span class="sxs-lookup"><span data-stu-id="a332a-106">Use this API to create a new [administrativeUnit](../resources/administrativeunit.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="a332a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a332a-107">Permissions</span></span>
<span data-ttu-id="a332a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a332a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a332a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a332a-110">Permission type</span></span>      | <span data-ttu-id="a332a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a332a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a332a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a332a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a332a-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a332a-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a332a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a332a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a332a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a332a-115">Not supported.</span></span>    |
|<span data-ttu-id="a332a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a332a-116">Application</span></span> | <span data-ttu-id="a332a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a332a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a332a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a332a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /administrativeUnits

```
## <a name="request-headers"></a><span data-ttu-id="a332a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a332a-119">Request headers</span></span>
| <span data-ttu-id="a332a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a332a-120">Name</span></span>      |<span data-ttu-id="a332a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a332a-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a332a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a332a-122">Authorization</span></span>  | <span data-ttu-id="a332a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a332a-p103">Bearer {token}. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="a332a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a332a-125">Request body</span></span>
<span data-ttu-id="a332a-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [administrativeUnit](../resources/administrativeunit.md) .</span><span class="sxs-lookup"><span data-stu-id="a332a-126">In the request body, supply a JSON representation of [administrativeUnit](../resources/administrativeunit.md) object.</span></span>

<span data-ttu-id="a332a-127">Puesto que el recurso **administrativeUnit** admite [extensiones](/graph/extensibility-overview), puede usar el `POST` operación y agregar propiedades personalizadas con sus propios datos a la unidad administrativa al crearla.</span><span class="sxs-lookup"><span data-stu-id="a332a-127">Since the **administrativeUnit** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the administrative unit while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="a332a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a332a-128">Response</span></span>

<span data-ttu-id="a332a-129">Si tiene éxito, este método devuelve `201 Created` objeto de código y [administrativeUnit](../resources/administrativeunit.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a332a-129">If successful, this method returns `201 Created` response code and [administrativeUnit](../resources/administrativeunit.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a332a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a332a-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a332a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a332a-131">Request</span></span>
<span data-ttu-id="a332a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a332a-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_administrativeunit_from_administrativeunits"
}-->
```http
POST https://graph.microsoft.com/beta/administrativeUnits
Content-type: application/json
Content-length: 150

{
    "displayName": "Seattle District Technical Schools",
    "description": "Seattle district technical schools administration",
    "visibility": "true"
}
```
<span data-ttu-id="a332a-133">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [administrativeUnit](../resources/administrativeunit.md) .</span><span class="sxs-lookup"><span data-stu-id="a332a-133">In the request body, supply a JSON representation of [administrativeUnit](../resources/administrativeunit.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="a332a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a332a-134">Response</span></span>
<span data-ttu-id="a332a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a332a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.administrativeUnit"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 172

{
  "administrativeUnit": {
    "displayName": "Seattle District Technical Schools",
    "description": "Seattle district technical schools administration",
    "visibility": "true",
    "id": "7a3dc8f3-b3a0-4164-9a99-ed36f3af039f"
  }
}
```

## <a name="see-also"></a><span data-ttu-id="a332a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a332a-138">See also</span></span>

- [<span data-ttu-id="a332a-139">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="a332a-139">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="a332a-140">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="a332a-140">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create administrativeUnit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
