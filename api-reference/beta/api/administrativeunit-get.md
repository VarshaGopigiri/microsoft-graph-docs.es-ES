---
title: Obtener administrativeUnit
description: Recuperar las propiedades y relaciones de un objeto administrativeUnit.
ms.openlocfilehash: d6e19762a74883da3dcff1d8ea423dc06192dd46
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084656"
---
# <a name="get-administrativeunit"></a><span data-ttu-id="299e6-103">Obtener administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="299e6-103">Get administrativeUnit</span></span>

> <span data-ttu-id="299e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="299e6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="299e6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="299e6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="299e6-106">Recuperar las propiedades y relaciones de un objeto [administrativeUnit](../resources/administrativeunit.md) .</span><span class="sxs-lookup"><span data-stu-id="299e6-106">Retrieve the properties and relationships of an [administrativeUnit](../resources/administrativeunit.md) object.</span></span>

<span data-ttu-id="299e6-107">Puesto que el recurso **administrativeUnit** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de **administrativeUnit** .</span><span class="sxs-lookup"><span data-stu-id="299e6-107">Since the **administrativeUnit** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in an **administrativeUnit** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="299e6-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="299e6-108">Permissions</span></span>
<span data-ttu-id="299e6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="299e6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="299e6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="299e6-111">Permission type</span></span>      | <span data-ttu-id="299e6-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="299e6-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="299e6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="299e6-113">Delegated (work or school account)</span></span> | <span data-ttu-id="299e6-114">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="299e6-114">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="299e6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="299e6-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="299e6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="299e6-116">Not supported.</span></span>    |
|<span data-ttu-id="299e6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="299e6-117">Application</span></span> | <span data-ttu-id="299e6-118">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="299e6-118">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="299e6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="299e6-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /administrativeUnits/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="299e6-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="299e6-120">Optional query parameters</span></span>
<span data-ttu-id="299e6-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="299e6-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="299e6-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="299e6-122">Request headers</span></span>
| <span data-ttu-id="299e6-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="299e6-123">Name</span></span>      |<span data-ttu-id="299e6-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="299e6-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="299e6-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="299e6-125">Authorization</span></span>  | <span data-ttu-id="299e6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="299e6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="299e6-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="299e6-128">Request body</span></span>
<span data-ttu-id="299e6-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="299e6-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="299e6-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="299e6-130">Response</span></span>

<span data-ttu-id="299e6-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [administrativeUnit](../resources/administrativeunit.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="299e6-131">If successful, this method returns a `200 OK` response code and [administrativeUnit](../resources/administrativeunit.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="299e6-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="299e6-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="299e6-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="299e6-133">Request</span></span>
<span data-ttu-id="299e6-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="299e6-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_administrativeunit"
}-->
```http
GET https://graph.microsoft.com/beta/administrativeUnits/{id}
```
##### <a name="response"></a><span data-ttu-id="299e6-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="299e6-135">Response</span></span>
<span data-ttu-id="299e6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="299e6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.administrativeUnit"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "displayName": "displayName-value",
  "description": "description-value",
  "visibility": "visibility-value",
  "id": "id-value"
}
```

## <a name="see-also"></a><span data-ttu-id="299e6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="299e6-139">See also</span></span>

- [<span data-ttu-id="299e6-140">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="299e6-140">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="299e6-141">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="299e6-141">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get administrativeUnit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->