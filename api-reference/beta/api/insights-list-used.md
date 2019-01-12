---
title: Lista usada
description: Insight calculado que devuelve la lista de archivos que se utiliza con un usuario.
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 107e9429228bbedf131ae4ca4adde79e280cedb9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990638"
---
# <a name="list-used"></a><span data-ttu-id="b6299-103">Lista usada</span><span class="sxs-lookup"><span data-stu-id="b6299-103">List used</span></span>

> <span data-ttu-id="b6299-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6299-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6299-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6299-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b6299-106">Insight calculado que devuelve la lista de archivos que se utiliza con un usuario.</span><span class="sxs-lookup"><span data-stu-id="b6299-106">Calculated insight that returns the list of files used with a user.</span></span>

## <a name="permissions"></a><span data-ttu-id="b6299-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6299-107">Permissions</span></span>
<span data-ttu-id="b6299-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6299-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6299-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6299-110">Permission type</span></span>      | <span data-ttu-id="b6299-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6299-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b6299-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6299-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b6299-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6299-113">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b6299-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6299-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b6299-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6299-115">Not supported.</span></span>    |
|<span data-ttu-id="b6299-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6299-116">Application</span></span> | <span data-ttu-id="b6299-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6299-117">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b6299-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6299-118">HTTP request</span></span>
```http
GET /me/insights/used
```
<span data-ttu-id="b6299-119">Solicitar devuelve resultados de otro usuario documentos utilizados ordenados por 'lastModifiedDateTime' y 'lastAccessedDateTime' está establecida en 'lastModifiedDateTime'.</span><span class="sxs-lookup"><span data-stu-id="b6299-119">Requesting other user's used documents returns results sorted by 'lastModifiedDateTime' and 'lastAccessedDateTime' is set to 'lastModifiedDateTime'.</span></span>
```http
GET /users/<id | userPrincipalName>/insights/used
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b6299-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b6299-120">Optional query parameters</span></span>
<span data-ttu-id="b6299-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6299-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="b6299-122">Puede usar el `$filter` parámetro a los elementos de filtro usado de consulta.</span><span class="sxs-lookup"><span data-stu-id="b6299-122">You can use the `$filter` query parameter to filter used items.</span></span> <span data-ttu-id="b6299-123">Por ejemplo, se basa en el tipo de:</span><span class="sxs-lookup"><span data-stu-id="b6299-123">For example, based on Type:</span></span>

`https://graph.microsoft.com/beta/me/insights/used?$filter=ResourceVisualization/Type eq 'PowerPoint'`

<span data-ttu-id="b6299-124">O en función de tipo de contenedor:</span><span class="sxs-lookup"><span data-stu-id="b6299-124">Or based on Container Type:</span></span>

`https://graph.microsoft.com/beta/me/insights/used?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`

<span data-ttu-id="b6299-125">Vea los tipos de contenedor y disponibles que puede filtrar los datos en [resourceVisualization](../resources/insights-resourcevisualization.md).</span><span class="sxs-lookup"><span data-stu-id="b6299-125">See the available Container Types and Types you can filter by in [resourceVisualization](../resources/insights-resourcevisualization.md).</span></span>


## <a name="request-headers"></a><span data-ttu-id="b6299-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6299-126">Request headers</span></span>
| <span data-ttu-id="b6299-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6299-127">Header</span></span>       |  <span data-ttu-id="b6299-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b6299-128">Value</span></span>|
|:-------------|:------|
| <span data-ttu-id="b6299-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6299-129">Authorization</span></span>  | <span data-ttu-id="b6299-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6299-p104">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="b6299-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b6299-132">Accept</span></span>  | <span data-ttu-id="b6299-133">application/json</span><span class="sxs-lookup"><span data-stu-id="b6299-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6299-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6299-134">Request body</span></span>
<span data-ttu-id="b6299-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6299-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6299-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6299-136">Response</span></span>

<span data-ttu-id="b6299-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de elementos [utilizados](../resources/insights-used.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6299-137">If successful, this method returns a `200 OK` response code and a list of [used](../resources/insights-used.md) items in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b6299-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6299-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="b6299-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6299-139">Request</span></span>

<span data-ttu-id="b6299-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6299-140">Here is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/me/insights/used
```

##### <a name="response"></a><span data-ttu-id="b6299-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6299-141">Response</span></span>

<span data-ttu-id="b6299-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6299-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span> 
```http
{
    "value": [
        {   
            "id": "id-value",
            "lastused" : { 
                "lastAccessedDateTime" : "lastAccessedDateTime-value", 
                "lastModifiedDateTime": "lastModifiedDateTime-value" 
            },
            "resourceVisualization": { 
                "title" : "title-value, 
                "type"  : "type-value",
                "mediaType" : "mediaType-value",
                "previewImageUrl" : previewImageUrl-value, 
                "previewText" : "previewText-value", 
                "containerWebUrl" : "containerWebUrl-value", 
                "containerDisplayName" : "containerDisplayName-value", 
                "containerType" : "containerType-value" 
            }, 
            "resourceReference" : { 
                "webUrl" : "webUrl-value", 
                "id": "id-value", 
                "type: "type-value" 
            }
        }
    ]
}
```

### <a name="expanding-resource"></a><span data-ttu-id="b6299-145">Expansión de recursos</span><span class="sxs-lookup"><span data-stu-id="b6299-145">Expanding resource</span></span>
<span data-ttu-id="b6299-146">Se puede expandir el recurso al que hace referencia un entendimiento usado.</span><span class="sxs-lookup"><span data-stu-id="b6299-146">The resource referenced by a used insight can be expanded.</span></span>
```http
GET https://graph.microsoft.com/beta/me/insights/used/{id}/resource
```
