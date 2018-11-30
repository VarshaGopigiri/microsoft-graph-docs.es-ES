---
title: Lista compartida
description: Insight calculado que devuelve la lista de archivos compartidos con un usuario.
ms.openlocfilehash: 589cb8da4ecb82149d11e0ad518d5a37749cc3da
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090427"
---
# <a name="list-shared"></a><span data-ttu-id="e855e-103">Lista compartida</span><span class="sxs-lookup"><span data-stu-id="e855e-103">List shared</span></span>

> <span data-ttu-id="e855e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e855e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e855e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e855e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e855e-106">Insight calculado que devuelve la lista de archivos compartidos con un usuario.</span><span class="sxs-lookup"><span data-stu-id="e855e-106">Calculated insight that returns the list of files shared with a user.</span></span>

## <a name="permissions"></a><span data-ttu-id="e855e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e855e-107">Permissions</span></span>
<span data-ttu-id="e855e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e855e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e855e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e855e-110">Permission type</span></span>      | <span data-ttu-id="e855e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e855e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e855e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e855e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e855e-113">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e855e-113">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="e855e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e855e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e855e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e855e-115">Not supported.</span></span>    |
|<span data-ttu-id="e855e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e855e-116">Application</span></span> | <span data-ttu-id="e855e-117">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e855e-117">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e855e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e855e-118">HTTP request</span></span>
```http
GET /me/insights/shared
```
<span data-ttu-id="e855e-119">Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario, no por otra persona:</span><span class="sxs-lookup"><span data-stu-id="e855e-119">Request with a 'user id' or 'userPrincipalName' is only accessible by the user, not by anyone else:</span></span>
```http
GET /users/<id | userPrincipalName>/insights/shared
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e855e-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e855e-120">Optional query parameters</span></span>
<span data-ttu-id="e855e-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e855e-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e855e-122">Puede usar el `$filter` parámetro para filtrar los elementos compartidos de consulta.</span><span class="sxs-lookup"><span data-stu-id="e855e-122">You can use the `$filter` query parameter to filter shared items.</span></span> <span data-ttu-id="e855e-123">Por ejemplo, se basa en el tipo de:</span><span class="sxs-lookup"><span data-stu-id="e855e-123">For example, based on Type:</span></span>

`https://graph.microsoft.com/beta/me/insights/shared?$filter=ResourceVisualization/Type eq 'PowerPoint'`

<span data-ttu-id="e855e-124">Vea los tipos de contenedor y disponibles que puede filtrar los datos en [resourceVisualization](../resources/insights-resourcevisualization.md).</span><span class="sxs-lookup"><span data-stu-id="e855e-124">See the available Container Types and Types you can filter by in [resourceVisualization](../resources/insights-resourcevisualization.md).</span></span>

<span data-ttu-id="e855e-125">También puede recuperar los archivos compartidos por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="e855e-125">You can also retrieve files shared by a specific user.</span></span> <span data-ttu-id="e855e-126">Por ejemplo, mediante la especificación de la `lastshared/sharedby/address` (propiedad):</span><span class="sxs-lookup"><span data-stu-id="e855e-126">For example, by specifying the `lastshared/sharedby/address` property:</span></span>

`https://graph.microsoft.com/beta/me/insights/shared?$filter=lastshared/sharedby/address eq 'kellygraham@contoso.com'`

<span data-ttu-id="e855e-127">Vea el tipo complejo [sharingDetail](../resources/insights-sharingdetail.md) .</span><span class="sxs-lookup"><span data-stu-id="e855e-127">See the [sharingDetail](../resources/insights-sharingdetail.md) complex type.</span></span>


## <a name="request-headers"></a><span data-ttu-id="e855e-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e855e-128">Request headers</span></span>
| <span data-ttu-id="e855e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e855e-129">Header</span></span>       |  <span data-ttu-id="e855e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e855e-130">Value</span></span>|
|:-------------|:------|
| <span data-ttu-id="e855e-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="e855e-131">Authorization</span></span>  | <span data-ttu-id="e855e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e855e-p105">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="e855e-134">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e855e-134">Accept</span></span>  | <span data-ttu-id="e855e-135">application/json</span><span class="sxs-lookup"><span data-stu-id="e855e-135">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e855e-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e855e-136">Request body</span></span>
<span data-ttu-id="e855e-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e855e-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e855e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e855e-138">Response</span></span>

<span data-ttu-id="e855e-139">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de los elementos [compartidos](../resources/insights-shared.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e855e-139">If successful, this method returns a `200 OK` response code and a list of [shared](../resources/insights-shared.md) items in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e855e-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e855e-140">Example</span></span>

##### <a name="request"></a><span data-ttu-id="e855e-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e855e-141">Request</span></span>

<span data-ttu-id="e855e-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e855e-142">Here is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/me/insights/shared
```

##### <a name="response"></a><span data-ttu-id="e855e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e855e-143">Response</span></span>

<span data-ttu-id="e855e-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e855e-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
```http
{
    "value": [
        {   
            "id": "id-value",
            "lastShared" : { 
                "sharedDateTime" : "sharedDateTime-value",  
                "sharingSubject" : "sharingSubject-value",
                "sharingType" : "sharingType-value", 
                "sharedBy" : { 
                    "displayName" : "displayName-value", 
                    "id": "id-value" 
                }
                "sharingReference" : { 
                    "webUrl" : "webUrl-value",
                    "type: "type-value", 
                    "id": "id-value"
                } 
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
```

### <a name="expanding-resource"></a><span data-ttu-id="e855e-147">Expansión de recursos</span><span class="sxs-lookup"><span data-stu-id="e855e-147">Expanding resource</span></span>
<span data-ttu-id="e855e-148">Se puede expandir el recurso al que hace referencia un entendimiento compartida.</span><span class="sxs-lookup"><span data-stu-id="e855e-148">The resource referenced by a shared insight can be expanded.</span></span>
```http
GET https://graph.microsoft.com/beta/me/insights/shared/{id}/resource
```