---
title: Obtener objetos de directorio a partir de una lista de identificadores
description: Seleccione ' opción de consulta no está disponible para esta operación.
author: lleonard-msft
ms.openlocfilehash: 335a6ba915e714ebbd95ba818d14043037f38050
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336291"
---
# <a name="get-directory-objects-from-a-list-of-ids"></a><span data-ttu-id="ec940-103">Obtener objetos de directorio a partir de una lista de identificadores</span><span class="sxs-lookup"><span data-stu-id="ec940-103">Get directory objects from a list of ids</span></span>

> <span data-ttu-id="ec940-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec940-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec940-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec940-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ec940-p102">Devuelve los objetos de directorio especificados en una lista de identificadores.  NOTA: Los objetos de directorio devueltos son los objetos completos que contienen **todas** sus propiedades. La opción de consulta `$select` no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="ec940-p102">Returns the directory objects specified in a list of ids.  NOTE: The directory objects returned are the full objects containing **all** their properties. The `$select` query option is not available for this operation.</span></span>

<span data-ttu-id="ec940-109">Algunos usos comunes de esta función son:</span><span class="sxs-lookup"><span data-stu-id="ec940-109">Some common uses for this function are to:</span></span>

* <span data-ttu-id="ec940-110">Resolver identificadores devueltos por funciones (que devuelven colecciones de identificadores) como [getMemberObjects](/graph/api/directoryobject-getmemberobjects.md?view=graph-rest-beta) o [getMemberGroups](/graph/api/directoryobject-getmembergroups.md?view=graph-rest-beta) a sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ec940-110">Resolve ids returned by functions (that return collections of ids) such as [getMemberObjects](/graph/api/directoryobject-getmemberobjects.md?view=graph-rest-beta) or [getMemberGroups](/graph/api/directoryobject-getmembergroups.md?view=graph-rest-beta)  to their backing directory objects.</span></span>
* <span data-ttu-id="ec940-111">Resolver identificadores que conserva la aplicación en un almacén externo para sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ec940-111">Resolve ids persisted in an external store by the application to their backing directory objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="ec940-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="ec940-112">Permissions</span></span>

<span data-ttu-id="ec940-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ec940-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ec940-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec940-115">Permission type</span></span>      | <span data-ttu-id="ec940-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec940-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ec940-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec940-117">Delegated (work or school account)</span></span> | <span data-ttu-id="ec940-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="ec940-118">Directory.Read.All</span></span>    |
|<span data-ttu-id="ec940-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec940-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ec940-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec940-120">Not supported.</span></span>    |
|<span data-ttu-id="ec940-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec940-121">Application</span></span> | <span data-ttu-id="ec940-122">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="ec940-122">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ec940-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec940-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /directoryObjects/getByIds
```

## <a name="request-headers"></a><span data-ttu-id="ec940-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec940-124">Request headers</span></span>

| <span data-ttu-id="ec940-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec940-125">Name</span></span>       | <span data-ttu-id="ec940-126">Type</span><span class="sxs-lookup"><span data-stu-id="ec940-126">Type</span></span> | <span data-ttu-id="ec940-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec940-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ec940-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="ec940-128">Authorization</span></span>  | <span data-ttu-id="ec940-129">string</span><span class="sxs-lookup"><span data-stu-id="ec940-129">string</span></span>  | <span data-ttu-id="ec940-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec940-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ec940-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ec940-132">Content-Type</span></span>  | <span data-ttu-id="ec940-133">application/json</span><span class="sxs-lookup"><span data-stu-id="ec940-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ec940-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec940-134">Request body</span></span>

<span data-ttu-id="ec940-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ec940-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ec940-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ec940-136">Parameter</span></span>   | <span data-ttu-id="ec940-137">Type</span><span class="sxs-lookup"><span data-stu-id="ec940-137">Type</span></span> |<span data-ttu-id="ec940-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec940-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ec940-139">ids</span><span class="sxs-lookup"><span data-stu-id="ec940-139">ids</span></span>|<span data-ttu-id="ec940-140">Colección string</span><span class="sxs-lookup"><span data-stu-id="ec940-140">String collection</span></span>| <span data-ttu-id="ec940-p105">Una colección de identificadores para devolverles objetos. Se pueden especificar hasta 1000 identificadores.</span><span class="sxs-lookup"><span data-stu-id="ec940-p105">A collection of ids for which to return objects. You can specify up to 1000 ids.</span></span> |
|<span data-ttu-id="ec940-143">types</span><span class="sxs-lookup"><span data-stu-id="ec940-143">types</span></span>|<span data-ttu-id="ec940-144">Colección string</span><span class="sxs-lookup"><span data-stu-id="ec940-144">String collection</span></span>| <span data-ttu-id="ec940-145">Una colección de tipos de recursos que especifica el conjunto de colecciones de recursos para buscar.</span><span class="sxs-lookup"><span data-stu-id="ec940-145">A collection of resource types that specifies the set of resource collections to search.</span></span> <span data-ttu-id="ec940-146">Si no se especifica, el valor predeterminado es [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta), que contiene todos los tipos de recursos definidos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="ec940-146">If not specified, the default is [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta), which contains all of the resource types defined in the directory.</span></span> <span data-ttu-id="ec940-147">Cualquier objeto que se deriva de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta) puede especificarse en la colección; Por ejemplo: [usuario](/graph/api/resources/user?view=graph-rest-beta), [grupo](/graph/api/resources/group?view=graph-rest-beta), [dispositivo](/graph/api/resources/device?view=graph-rest-beta)y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ec940-147">Any object that derives from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta) may be specified in the collection; for example: [user](/graph/api/resources/user?view=graph-rest-beta), [group](/graph/api/resources/group?view=graph-rest-beta), [device](/graph/api/resources/device?view=graph-rest-beta), and so on.</span></span> <span data-ttu-id="ec940-148">Para buscar referencias a un socio de [Proveedor de soluciones de nube](https://partner.microsoft.com/en-us/cloud-solution-provider) organización especificar [directoryObjectPartnerReference](/graph/api/resources/directoryobjectpartnerreference?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="ec940-148">To search for references to a [Cloud Solution Provider](https://partner.microsoft.com/en-us/cloud-solution-provider) partner organization specify [directoryObjectPartnerReference](/graph/api/resources/directoryobjectpartnerreference?view=graph-rest-beta).</span></span> <span data-ttu-id="ec940-149">Si no se especifica, el valor predeterminado es [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta), que contiene todos los tipos de recursos definidos en el directorio, excepto para las referencias a una organización asociada de [Proveedor de soluciones de nube](https://partner.microsoft.com/en-us/cloud-solution-provider) .</span><span class="sxs-lookup"><span data-stu-id="ec940-149">If not specified, the default is [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-beta), which contains all of the resource types defined in the directory, except for references to a [Cloud Solution Provider](https://partner.microsoft.com/en-us/cloud-solution-provider) partner organization.</span></span> <span data-ttu-id="ec940-150">Los valores no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ec940-150">The values are not case-sensitive.</span></span>|

## <a name="response"></a><span data-ttu-id="ec940-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec940-151">Response</span></span>

<span data-ttu-id="ec940-152">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec940-152">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ec940-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec940-153">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ec940-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec940-154">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_getByIds"
}-->

```http
POST https://graph.microsoft.com/beta/directoryObjects/getByIds
Content-type: application/json

{
    "ids":["84b80893-8749-40a3-97b7-68513b600544","5d6059b6-368d-45f8-91e1-8e07d485f1d0"],
    "types":["user"]
}
```

##### <a name="response"></a><span data-ttu-id="ec940-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec940-155">Response</span></span>

<span data-ttu-id="ec940-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ec940-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
