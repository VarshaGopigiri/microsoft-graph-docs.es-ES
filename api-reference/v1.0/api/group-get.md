---
title: Obtener grupo
description: Obtiene las propiedades y relaciones de un objeto de grupo.
ms.openlocfilehash: fbae878043580a9c5495b0462290e1da7af3bdd5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030556"
---
# <a name="get-group"></a><span data-ttu-id="3ca90-103">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="3ca90-103">Get group</span></span>
<span data-ttu-id="3ca90-104">Obtiene las propiedades y relaciones de un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="3ca90-104">Get the properties and relationships of a group object.</span></span>

##### <a name="default-properties"></a><span data-ttu-id="3ca90-105">Propiedades predeterminadas</span><span class="sxs-lookup"><span data-stu-id="3ca90-105">Default properties</span></span>

<span data-ttu-id="3ca90-p101">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener o enumerar grupos. Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="3ca90-p101">The following represent the default set of properties that are returned when getting or listing groups. These are a subset of all available properties.</span></span>

* <span data-ttu-id="3ca90-108">descripción</span><span class="sxs-lookup"><span data-stu-id="3ca90-108">description</span></span>
* <span data-ttu-id="3ca90-109">displayName</span><span class="sxs-lookup"><span data-stu-id="3ca90-109">displayName</span></span>
* <span data-ttu-id="3ca90-110">groupTypes</span><span class="sxs-lookup"><span data-stu-id="3ca90-110">groupTypes</span></span>
* <span data-ttu-id="3ca90-111">id</span><span class="sxs-lookup"><span data-stu-id="3ca90-111">id</span></span>
* <span data-ttu-id="3ca90-112">mail</span><span class="sxs-lookup"><span data-stu-id="3ca90-112">mail</span></span>
* <span data-ttu-id="3ca90-113">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="3ca90-113">mailEnabled</span></span>
* <span data-ttu-id="3ca90-114">mailNickname</span><span class="sxs-lookup"><span data-stu-id="3ca90-114">mailNickname</span></span>
* <span data-ttu-id="3ca90-115">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="3ca90-115">onPremisesLastSyncDateTime</span></span>
* <span data-ttu-id="3ca90-116">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="3ca90-116">onPremisesSecurityIdentifier</span></span>
* <span data-ttu-id="3ca90-117">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="3ca90-117">onPremisesSyncEnabled</span></span>
* <span data-ttu-id="3ca90-118">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="3ca90-118">proxyAddresses</span></span>
* <span data-ttu-id="3ca90-119">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="3ca90-119">securityEnabled</span></span>
* <span data-ttu-id="3ca90-120">visibility</span><span class="sxs-lookup"><span data-stu-id="3ca90-120">visibility</span></span>

<span data-ttu-id="3ca90-121">De forma predeterminada, no se devuelven las siguientes propiedades de grupo:</span><span class="sxs-lookup"><span data-stu-id="3ca90-121">The following group properties are not returned by default:</span></span>

* <span data-ttu-id="3ca90-122">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="3ca90-122">allowExternalSenders</span></span>
* <span data-ttu-id="3ca90-123">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="3ca90-123">autoSubscribeNewMembers</span></span>
* <span data-ttu-id="3ca90-124">isSubscribedByMail</span><span class="sxs-lookup"><span data-stu-id="3ca90-124">isSubscribedByMail</span></span>
* <span data-ttu-id="3ca90-125">unseenCount</span><span class="sxs-lookup"><span data-stu-id="3ca90-125">unseenCount</span></span>

<span data-ttu-id="3ca90-p102">Para obtener estas propiedades, use el parámetro de consulta **$select**. A continuación puede ver algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="3ca90-p102">To get these properties, use the **$select** query parameter. The following are examples:</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount

GET https://graph.microsoft.com/v1.0/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=description,allowExternalSenders
```


## <a name="permissions"></a><span data-ttu-id="3ca90-128">Permisos</span><span class="sxs-lookup"><span data-stu-id="3ca90-128">Permissions</span></span>
<span data-ttu-id="3ca90-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3ca90-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3ca90-131">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ca90-131">Permission type</span></span>      | <span data-ttu-id="3ca90-132">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ca90-132">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3ca90-133">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ca90-133">Delegated (work or school account)</span></span> | <span data-ttu-id="3ca90-134">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3ca90-134">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3ca90-135">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ca90-135">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3ca90-136">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ca90-136">Not supported.</span></span>    |
|<span data-ttu-id="3ca90-137">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ca90-137">Application</span></span> | <span data-ttu-id="3ca90-138">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3ca90-138">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3ca90-139">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ca90-139">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3ca90-140">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3ca90-140">Optional query parameters</span></span>
<span data-ttu-id="3ca90-141">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ca90-141">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3ca90-142">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ca90-142">Request headers</span></span>
| <span data-ttu-id="3ca90-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ca90-143">Name</span></span>       | <span data-ttu-id="3ca90-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ca90-144">Type</span></span> | <span data-ttu-id="3ca90-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ca90-145">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3ca90-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="3ca90-146">Authorization</span></span>  | <span data-ttu-id="3ca90-147">string</span><span class="sxs-lookup"><span data-stu-id="3ca90-147">string</span></span>  | <span data-ttu-id="3ca90-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3ca90-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3ca90-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3ca90-150">Request body</span></span>
<span data-ttu-id="3ca90-151">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3ca90-151">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3ca90-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ca90-152">Response</span></span>
<span data-ttu-id="3ca90-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ca90-153">If successful, this method returns a `200 OK` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3ca90-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ca90-154">Example</span></span>
#### <a name="request"></a><span data-ttu-id="3ca90-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ca90-155">Request</span></span>
<span data-ttu-id="3ca90-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ca90-156">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="3ca90-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ca90-157">Response</span></span>
<span data-ttu-id="3ca90-158">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ca90-158">The following is an example of the response.</span></span>

><span data-ttu-id="3ca90-159">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3ca90-159">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="3ca90-160">Se devolverán todas las propiedades predeterminadas de una llamada real, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3ca90-160">The default properties will be returned from an actual call, as described before.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
  "id": "id-value",
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value",
  "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
  "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
  "onPremisesSyncEnabled": true,
  "proxyAddresses": [
    "proxyAddresses-value"
   ],
   "securityEnabled": true,
   "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
