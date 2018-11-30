---
title: Obtener objetos de directorio a partir de una lista de identificadores
description: Seleccione ' opción de consulta no está disponible para esta operación.
ms.openlocfilehash: 87fa774910c1ea6795b6df65ee0f5538d12296bb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084070"
---
# <a name="get-directory-objects-from-a-list-of-ids"></a><span data-ttu-id="ee181-103">Obtener objetos de directorio a partir de una lista de identificadores</span><span class="sxs-lookup"><span data-stu-id="ee181-103">Get directory objects from a list of ids</span></span>

> <span data-ttu-id="ee181-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee181-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee181-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee181-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee181-p102">Devuelve los objetos de directorio especificados en una lista de identificadores.  NOTA: Los objetos de directorio devueltos son los objetos completos que contienen **todas** sus propiedades. La opción de consulta `$select` no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="ee181-p102">Returns the directory objects specified in a list of ids.  NOTE: The directory objects returned are the full objects containing **all** their properties. The `$select` query option is not available for this operation.</span></span>

<span data-ttu-id="ee181-109">Algunos usos comunes de esta función son:</span><span class="sxs-lookup"><span data-stu-id="ee181-109">Some common uses for this function are to:</span></span>

* <span data-ttu-id="ee181-110">Resolver identificadores devueltos por funciones (que devuelven colecciones de identificadores) como [getMemberObjects](directoryobject-getmemberobjects.md) o [getMemberGroups](directoryobject-getmembergroups.md) a sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ee181-110">Resolve ids returned by functions (that return collections of ids) such as [getMemberObjects](directoryobject-getmemberobjects.md) or [getMemberGroups](directoryobject-getmembergroups.md)  to their backing directory objects.</span></span>
* <span data-ttu-id="ee181-111">Resolver identificadores que conserva la aplicación en un almacén externo para sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ee181-111">Resolve ids persisted in an external store by the application to their backing directory objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="ee181-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee181-112">Permissions</span></span>

<span data-ttu-id="ee181-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee181-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ee181-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee181-115">Permission type</span></span>      | <span data-ttu-id="ee181-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee181-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ee181-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee181-117">Delegated (work or school account)</span></span> | <span data-ttu-id="ee181-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="ee181-118">Directory.Read.All</span></span>    |
|<span data-ttu-id="ee181-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee181-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee181-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee181-120">Not supported.</span></span>    |
|<span data-ttu-id="ee181-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee181-121">Application</span></span> | <span data-ttu-id="ee181-122">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="ee181-122">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ee181-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee181-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /directoryObjects/getById
```

## <a name="request-headers"></a><span data-ttu-id="ee181-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee181-124">Request headers</span></span>

| <span data-ttu-id="ee181-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ee181-125">Name</span></span>       | <span data-ttu-id="ee181-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee181-126">Type</span></span> | <span data-ttu-id="ee181-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee181-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ee181-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee181-128">Authorization</span></span>  | <span data-ttu-id="ee181-129">string</span><span class="sxs-lookup"><span data-stu-id="ee181-129">string</span></span>  | <span data-ttu-id="ee181-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee181-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ee181-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ee181-132">Content-Type</span></span>  | <span data-ttu-id="ee181-133">application/json</span><span class="sxs-lookup"><span data-stu-id="ee181-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ee181-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee181-134">Request body</span></span>

<span data-ttu-id="ee181-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee181-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ee181-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ee181-136">Parameter</span></span>   | <span data-ttu-id="ee181-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee181-137">Type</span></span> |<span data-ttu-id="ee181-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee181-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee181-139">ids</span><span class="sxs-lookup"><span data-stu-id="ee181-139">ids</span></span>|<span data-ttu-id="ee181-140">Colección string</span><span class="sxs-lookup"><span data-stu-id="ee181-140">String collection</span></span>| <span data-ttu-id="ee181-p105">Una colección de identificadores para devolverles objetos. Se pueden especificar hasta 1000 identificadores.</span><span class="sxs-lookup"><span data-stu-id="ee181-p105">A collection of ids for which to return objects. You can specify up to 1000 ids.</span></span> |
|<span data-ttu-id="ee181-143">types</span><span class="sxs-lookup"><span data-stu-id="ee181-143">types</span></span>|<span data-ttu-id="ee181-144">Colección string</span><span class="sxs-lookup"><span data-stu-id="ee181-144">String collection</span></span>| <span data-ttu-id="ee181-145">Una colección de tipos de recursos que especifica el conjunto de colecciones de recursos para buscar.</span><span class="sxs-lookup"><span data-stu-id="ee181-145">A collection of resource types that specifies the set of resource collections to search.</span></span> <span data-ttu-id="ee181-146">Si no se especifica, el valor predeterminado es [directoryObject](../resources/directoryobject.md), que contiene todos los tipos de recursos definidos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="ee181-146">If not specified, the default is [directoryObject](../resources/directoryobject.md), which contains all of the resource types defined in the directory.</span></span> <span data-ttu-id="ee181-147">Cualquier objeto que se deriva de `directoryObject` pueden especificarse en la colección; Por ejemplo: [usuario](../resources/user.md), [grupo](../resources/group.md), [dispositivo](../resources/device.md)y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ee181-147">Any object that derives from `directoryObject` may be specified in the collection; for example: [user](../resources/user.md), [group](../resources/group.md), [device](../resources/device.md), and so on.</span></span> <span data-ttu-id="ee181-148">Los valores no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ee181-148">The values are not case-sensitive.</span></span>|

## <a name="response"></a><span data-ttu-id="ee181-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee181-149">Response</span></span>

<span data-ttu-id="ee181-150">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee181-150">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee181-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee181-151">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ee181-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee181-152">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_getById"
}-->

```http
POST https://graph.microsoft.com/beta/directoryObjects/getByIds
Content-type: application/json

{
    "ids":["84b80893-8749-40a3-97b7-68513b600544","5d6059b6-368d-45f8-91e1-8e07d485f1d0"],
    "types":["user"]
}
```

##### <a name="response"></a><span data-ttu-id="ee181-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee181-153">Response</span></span>

<span data-ttu-id="ee181-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee181-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#directoryObjects",
    "value": [
      {
        "@odata.type": "#microsoft.graph.user",
        "id": "84b80893-8749-40a3-97b7-68513b600544",
        "accountEnabled": true,
        "displayName": "Trevor Jones"
      },
      {
        "@odata.type": "#microsoft.graph.user",
        "id": "84b80893-8749-40a3-97b7-68513b600544",
        "accountEnabled": true,
        "displayName": "Billy Smith"
      }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: getById",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
