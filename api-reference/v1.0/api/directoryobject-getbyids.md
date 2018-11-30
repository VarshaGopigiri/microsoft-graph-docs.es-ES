---
title: Obtener objetos de directorio a partir de una lista de identificadores
description: Seleccione ' opción de consulta no está disponible para esta operación.
ms.openlocfilehash: 4a2b765d71fe799195a4afcd404ba21718fa87c8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028781"
---
# <a name="get-directory-objects-from-a-list-of-ids"></a><span data-ttu-id="77321-103">Obtener objetos de directorio a partir de una lista de identificadores</span><span class="sxs-lookup"><span data-stu-id="77321-103">Get directory objects from a list of ids</span></span>

<span data-ttu-id="77321-p101">Devuelve los objetos de directorio especificados en una lista de identificadores.  NOTA: Los objetos de directorio devueltos son los objetos completos que contienen **todas** sus propiedades. La opción de consulta `$select` no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="77321-p101">Returns the directory objects specified in a list of ids.  NOTE: The directory objects returned are the full objects containing **all** their properties. The `$select` query option is not available for this operation.</span></span>

<span data-ttu-id="77321-107">Algunos usos comunes de esta función son:</span><span class="sxs-lookup"><span data-stu-id="77321-107">Some common uses for this function are to:</span></span>

* <span data-ttu-id="77321-108">Resolver identificadores devueltos por funciones (que devuelven colecciones de identificadores) como [getMemberObjects](directoryobject-getmemberobjects.md) o [getMemberGroups](directoryobject-getmembergroups.md) a sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77321-108">Resolve ids returned by functions (that return collections of ids) such as [getMemberObjects](directoryobject-getmemberobjects.md) or [getMemberGroups](directoryobject-getmembergroups.md)  to their backing directory objects.</span></span>
* <span data-ttu-id="77321-109">Resolver identificadores que conserva la aplicación en un almacén externo para sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77321-109">Resolve ids persisted in an external store by the application to their backing directory objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="77321-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="77321-110">Permissions</span></span>

<span data-ttu-id="77321-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77321-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="77321-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77321-113">Permission type</span></span>      | <span data-ttu-id="77321-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77321-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="77321-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77321-115">Delegated (work or school account)</span></span> | <span data-ttu-id="77321-116">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="77321-116">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="77321-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77321-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77321-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77321-118">Not supported.</span></span>    |
|<span data-ttu-id="77321-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77321-119">Application</span></span> | <span data-ttu-id="77321-120">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="77321-120">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="77321-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77321-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /directoryObjects/getByIds
```

## <a name="request-headers"></a><span data-ttu-id="77321-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77321-122">Request headers</span></span>

| <span data-ttu-id="77321-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="77321-123">Name</span></span>       | <span data-ttu-id="77321-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="77321-124">Type</span></span> | <span data-ttu-id="77321-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="77321-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="77321-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="77321-126">Authorization</span></span>  | <span data-ttu-id="77321-127">string</span><span class="sxs-lookup"><span data-stu-id="77321-127">string</span></span>  | <span data-ttu-id="77321-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77321-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="77321-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="77321-130">Content-Type</span></span>  | <span data-ttu-id="77321-131">string</span><span class="sxs-lookup"><span data-stu-id="77321-131">string</span></span> | <span data-ttu-id="77321-132">application/json</span><span class="sxs-lookup"><span data-stu-id="77321-132">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="77321-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77321-133">Request body</span></span>

<span data-ttu-id="77321-134">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="77321-134">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="77321-135">Parámetro</span><span class="sxs-lookup"><span data-stu-id="77321-135">Parameter</span></span>   | <span data-ttu-id="77321-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="77321-136">Type</span></span> |<span data-ttu-id="77321-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="77321-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="77321-138">ids</span><span class="sxs-lookup"><span data-stu-id="77321-138">ids</span></span>|<span data-ttu-id="77321-139">Colección string</span><span class="sxs-lookup"><span data-stu-id="77321-139">String collection</span></span>| <span data-ttu-id="77321-p104">Una colección de identificadores para devolverles objetos. Se pueden especificar hasta 1000 identificadores.</span><span class="sxs-lookup"><span data-stu-id="77321-p104">A collection of ids for which to return objects. You can specify up to 1000 ids.</span></span> |
|<span data-ttu-id="77321-142">types</span><span class="sxs-lookup"><span data-stu-id="77321-142">types</span></span>|<span data-ttu-id="77321-143">Colección string</span><span class="sxs-lookup"><span data-stu-id="77321-143">String collection</span></span>| <span data-ttu-id="77321-144">Una colección de tipos de recursos que especifica el conjunto de colecciones de recursos para buscar.</span><span class="sxs-lookup"><span data-stu-id="77321-144">A collection of resource types that specifies the set of resource collections to search.</span></span> <span data-ttu-id="77321-145">Si no se especifica, el valor predeterminado es [directoryObject](../resources/directoryobject.md), que contiene todos los tipos de recursos definidos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="77321-145">If not specified, the default is [directoryObject](../resources/directoryobject.md), which contains all of the resource types defined in the directory.</span></span> <span data-ttu-id="77321-146">Cualquier objeto que se deriva de `directoryObject` pueden especificarse en la colección; Por ejemplo: [usuario](../resources/user.md), [grupo](../resources/group.md), [dispositivo](../resources/device.md)y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="77321-146">Any object that derives from `directoryObject` may be specified in the collection; for example: [user](../resources/user.md), [group](../resources/group.md), [device](../resources/device.md), and so on.</span></span> <span data-ttu-id="77321-147">Los valores no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="77321-147">The values are not case-sensitive.</span></span>|

## <a name="response"></a><span data-ttu-id="77321-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77321-148">Response</span></span>

<span data-ttu-id="77321-149">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77321-149">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77321-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77321-150">Example</span></span>

##### <a name="request"></a><span data-ttu-id="77321-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77321-151">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_getById"
}-->

```http
POST https://graph.microsoft.com/v1.0/directoryObjects/getByIds
Content-type: application/json

{
    "ids":["84b80893874940a3-97b7-68513b600544","5d6059b6368d-45f8-91e18e07d485f1d0"],
    "types":["user"]
}
```

##### <a name="response"></a><span data-ttu-id="77321-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77321-152">Response</span></span>

<span data-ttu-id="77321-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77321-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directoryObjects",
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
