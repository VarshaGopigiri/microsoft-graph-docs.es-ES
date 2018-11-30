---
title: Tendencias de lista
description: Insight calculado que devuelve la lista de elementos tendencias alrededor del usuario.
ms.openlocfilehash: 94433d094c2ab527e33ac04730cdbb72a1b94c1f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086997"
---
# <a name="list-trending"></a><span data-ttu-id="00e82-103">Tendencias de lista</span><span class="sxs-lookup"><span data-stu-id="00e82-103">List trending</span></span>

> <span data-ttu-id="00e82-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00e82-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00e82-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00e82-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="00e82-106">Insight calculado que devuelve la lista de elementos tendencias alrededor del usuario.</span><span class="sxs-lookup"><span data-stu-id="00e82-106">Calculated insight that returns the list of items trending around the user.</span></span>

## <a name="permissions"></a><span data-ttu-id="00e82-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="00e82-107">Permissions</span></span>
<span data-ttu-id="00e82-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00e82-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="00e82-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00e82-110">Permission type</span></span>      | <span data-ttu-id="00e82-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00e82-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="00e82-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00e82-112">Delegated (work or school account)</span></span> | <span data-ttu-id="00e82-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00e82-113">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="00e82-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00e82-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00e82-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00e82-115">Not supported.</span></span>    |
|<span data-ttu-id="00e82-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00e82-116">Application</span></span> | <span data-ttu-id="00e82-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00e82-117">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="00e82-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00e82-118">HTTP request</span></span>
```http
GET /me/insights/trending
GET /users/{id | userPrincipalName}/insights/trending
```

## <a name="optional-query-parameters"></a><span data-ttu-id="00e82-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="00e82-119">Optional query parameters</span></span>
<span data-ttu-id="00e82-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00e82-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="00e82-121">Puede usar el `$filter` parámetro para filtrar los elementos de tendencias de consulta.</span><span class="sxs-lookup"><span data-stu-id="00e82-121">You can use the `$filter` query parameter to filter trending items.</span></span> <span data-ttu-id="00e82-122">Por ejemplo, se basa en el tipo de:</span><span class="sxs-lookup"><span data-stu-id="00e82-122">For example, based on Type:</span></span>

`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/Type eq 'PowerPoint'`

<span data-ttu-id="00e82-123">O en función de tipo de contenedor:</span><span class="sxs-lookup"><span data-stu-id="00e82-123">Or based on Container Type:</span></span>

`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`

<span data-ttu-id="00e82-124">Vea los tipos de contenedor y disponibles que puede filtrar los datos en [resourceVisualization](../resources/insights-resourcevisualization.md).</span><span class="sxs-lookup"><span data-stu-id="00e82-124">See the available Container Types and Types you can filter by in [resourceVisualization](../resources/insights-resourcevisualization.md).</span></span>


## <a name="request-headers"></a><span data-ttu-id="00e82-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00e82-125">Request headers</span></span>
| <span data-ttu-id="00e82-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00e82-126">Header</span></span>       |  <span data-ttu-id="00e82-127">Valor</span><span class="sxs-lookup"><span data-stu-id="00e82-127">Value</span></span>|
|:-------------|:------|
| <span data-ttu-id="00e82-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="00e82-128">Authorization</span></span>  | <span data-ttu-id="00e82-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00e82-p104">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="00e82-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="00e82-131">Accept</span></span>  | <span data-ttu-id="00e82-132">application/json</span><span class="sxs-lookup"><span data-stu-id="00e82-132">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="00e82-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00e82-133">Request body</span></span>
<span data-ttu-id="00e82-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="00e82-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="00e82-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00e82-135">Response</span></span>

<span data-ttu-id="00e82-136">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de elementos de [tendencias](../resources/insights-trending.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00e82-136">If successful, this method returns a `200 OK` response code and a list of [trending](../resources/insights-trending.md) items in the response body.</span></span> <span data-ttu-id="00e82-137">Cada elemento contiene propiedades de la visualización para mostrar el elemento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="00e82-137">Each item contains visualization properties for displaying the item in your experience.</span></span>

## <a name="example"></a><span data-ttu-id="00e82-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00e82-138">Example</span></span>
#### <a name="request"></a><span data-ttu-id="00e82-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00e82-139">Request</span></span>
<span data-ttu-id="00e82-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00e82-140">Here is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/me/insights/trending
```
#### <a name="response"></a><span data-ttu-id="00e82-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00e82-141">Response</span></span>
<span data-ttu-id="00e82-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00e82-142">Here is an example of the response.</span></span> <span data-ttu-id="00e82-143">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="00e82-143">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="00e82-144">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="00e82-144">All of the properties will be returned from an actual call.</span></span> <span data-ttu-id="00e82-145">Vea una respuesta reactivar truncado de ejemplo en la parte inferior de la página.</span><span class="sxs-lookup"><span data-stu-id="00e82-145">See an example un-truncated response at the bottom of the page.</span></span>
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 801

{
    "value": [
        {
            "id": "id-value",
            "weight": "weight-value",
            "resourceVisualization": {
                "title": "title-value",
                "type": "type-value",
                "mediaType": "mediaType-value",
                "previewImageUrl": "previewImageUrl-value",
                "previewText": "previewText-value",
                "containerWebUrl": "containerWebUrl-value",
                "containerDisplayName": "containerDisplayName-value",
                "containerType": "containerType-value"
            },
            "resourceReference": {
                "webUrl": "webUrl-value",
                "id": "id-value",
                "type": "type-value"
            }
        }
    ]
}
```

### <a name="expanding-resource"></a><span data-ttu-id="00e82-146">Expansión de recursos</span><span class="sxs-lookup"><span data-stu-id="00e82-146">Expanding resource</span></span>
<span data-ttu-id="00e82-147">Se puede expandir el recurso al que hace referencia un entendimiento tendencia.</span><span class="sxs-lookup"><span data-stu-id="00e82-147">The resource referenced by a trending insight can be expanded.</span></span>
```http
GET https://graph.microsoft.com/beta/me/insights/trending/{id}/resource
```