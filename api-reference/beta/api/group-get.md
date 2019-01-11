---
title: Obtener grupo
description: Obtiene las propiedades y relaciones de un objeto de grupo.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: 48bc4322326087895542ac24e23c7a57f5ddf07e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838678"
---
# <a name="get-group"></a><span data-ttu-id="a1860-103">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="a1860-103">Get group</span></span>

> <span data-ttu-id="a1860-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a1860-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a1860-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a1860-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a1860-106">Obtener las propiedades y relaciones de un objeto de [grupo](../resources/group.md) .</span><span class="sxs-lookup"><span data-stu-id="a1860-106">Get the properties and relationships of a [group](../resources/group.md) object.</span></span>

##### <a name="default-properties"></a><span data-ttu-id="a1860-107">Propiedades predeterminadas</span><span class="sxs-lookup"><span data-stu-id="a1860-107">Default properties</span></span>

<span data-ttu-id="a1860-p102">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener o enumerar grupos. Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="a1860-p102">The following represent the default set of properties that are returned when getting or listing groups. These are a subset of all available properties.</span></span> 

* <span data-ttu-id="a1860-110">classification</span><span class="sxs-lookup"><span data-stu-id="a1860-110">classification</span></span>
* <span data-ttu-id="a1860-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a1860-111">createdDateTime</span></span>
* <span data-ttu-id="a1860-112">descripción</span><span class="sxs-lookup"><span data-stu-id="a1860-112">description</span></span>
* <span data-ttu-id="a1860-113">displayName</span><span class="sxs-lookup"><span data-stu-id="a1860-113">displayName</span></span>
* <span data-ttu-id="a1860-114">groupTypes</span><span class="sxs-lookup"><span data-stu-id="a1860-114">groupTypes</span></span>
* <span data-ttu-id="a1860-115">id</span><span class="sxs-lookup"><span data-stu-id="a1860-115">id</span></span>
* <span data-ttu-id="a1860-116">mail</span><span class="sxs-lookup"><span data-stu-id="a1860-116">mail</span></span>
* <span data-ttu-id="a1860-117">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="a1860-117">mailEnabled</span></span>
* <span data-ttu-id="a1860-118">mailNickname</span><span class="sxs-lookup"><span data-stu-id="a1860-118">mailNickname</span></span>
* <span data-ttu-id="a1860-119">membershipRule</span><span class="sxs-lookup"><span data-stu-id="a1860-119">membershipRule</span></span>
* <span data-ttu-id="a1860-120">membershipRuleProcessingState</span><span class="sxs-lookup"><span data-stu-id="a1860-120">membershipRuleProcessingState</span></span>
* <span data-ttu-id="a1860-121">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="a1860-121">onPremisesLastSyncDateTime</span></span>
* <span data-ttu-id="a1860-122">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="a1860-122">onPremisesSecurityIdentifier</span></span>
* <span data-ttu-id="a1860-123">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="a1860-123">onPremisesSyncEnabled</span></span>
* <span data-ttu-id="a1860-124">preferredLanguage - no se admite; no puede ser un valor para esta propiedad conjunto y devuelve `null` cuando llama.</span><span class="sxs-lookup"><span data-stu-id="a1860-124">preferredLanguage - Not supported; a value for this property cannot be set and returns `null` when called.</span></span>
* <span data-ttu-id="a1860-125">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a1860-125">proxyAddresses</span></span>
* <span data-ttu-id="a1860-126">renewedDateTime</span><span class="sxs-lookup"><span data-stu-id="a1860-126">renewedDateTime</span></span>
* <span data-ttu-id="a1860-127">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="a1860-127">securityEnabled</span></span>
* <span data-ttu-id="a1860-128">tema</span><span class="sxs-lookup"><span data-stu-id="a1860-128">theme</span></span>
* <span data-ttu-id="a1860-129">visibility</span><span class="sxs-lookup"><span data-stu-id="a1860-129">visibility</span></span>

<span data-ttu-id="a1860-130">De forma predeterminada, no se devuelven las siguientes propiedades de grupo:</span><span class="sxs-lookup"><span data-stu-id="a1860-130">The following group properties are not returned by default:</span></span>

* <span data-ttu-id="a1860-131">accessType</span><span class="sxs-lookup"><span data-stu-id="a1860-131">accessType</span></span>
* <span data-ttu-id="a1860-132">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="a1860-132">allowExternalSenders</span></span>
* <span data-ttu-id="a1860-133">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="a1860-133">autoSubscribeNewMembers</span></span>
* <span data-ttu-id="a1860-134">hasMembersWithLicenseErrors</span><span class="sxs-lookup"><span data-stu-id="a1860-134">hasMembersWithLicenseErrors</span></span>
* <span data-ttu-id="a1860-135">isSubscribedByMail</span><span class="sxs-lookup"><span data-stu-id="a1860-135">isSubscribedByMail</span></span>
* <span data-ttu-id="a1860-136">isFavorite</span><span class="sxs-lookup"><span data-stu-id="a1860-136">isFavorite</span></span>
* <span data-ttu-id="a1860-137">unseenConversationsCount</span><span class="sxs-lookup"><span data-stu-id="a1860-137">unseenConversationsCount</span></span>
* <span data-ttu-id="a1860-138">unseenCount</span><span class="sxs-lookup"><span data-stu-id="a1860-138">unseenCount</span></span>
* <span data-ttu-id="a1860-139">unseenMessagesCount</span><span class="sxs-lookup"><span data-stu-id="a1860-139">unseenMessagesCount</span></span>

<span data-ttu-id="a1860-140">Para obtener estas propiedades (excepto **isFavorite** y **hasMembersWithLicenseErrors**), utilice la `$select` parámetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="a1860-140">To get these properties (except **isFavorite** and **hasMembersWithLicenseErrors**), use the `$select` query parameter.</span></span> <span data-ttu-id="a1860-141">Estos son algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="a1860-141">The following are examples:</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount

GET https://graph.microsoft.com/beta/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=description,allowExternalSenders
```

<span data-ttu-id="a1860-142">Para devolver los grupos que contienen a miembros con errores de licencia, use el parámetro de consulta **$filter** :</span><span class="sxs-lookup"><span data-stu-id="a1860-142">To return groups containing members with license errors, use the **$filter** query parameter:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET GET https://graph.microsoft.com/beta/groups?$filter=hasMembersWithLicenseErrors+eq+true
```

<span data-ttu-id="a1860-143">Puesto que el recurso de **grupo** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de **grupo** .</span><span class="sxs-lookup"><span data-stu-id="a1860-143">Since the **group** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **group** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="a1860-144">Permisos</span><span class="sxs-lookup"><span data-stu-id="a1860-144">Permissions</span></span>
<span data-ttu-id="a1860-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a1860-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a1860-147">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1860-147">Permission type</span></span>      | <span data-ttu-id="a1860-148">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1860-148">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1860-149">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1860-149">Delegated (work or school account)</span></span> | <span data-ttu-id="a1860-150">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1860-150">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a1860-151">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1860-151">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a1860-152">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1860-152">Not supported.</span></span>    |
|<span data-ttu-id="a1860-153">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1860-153">Application</span></span> | <span data-ttu-id="a1860-154">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1860-154">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a1860-155">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1860-155">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a1860-156">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a1860-156">Optional query parameters</span></span>
<span data-ttu-id="a1860-157">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1860-157">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a1860-158">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1860-158">Request headers</span></span>
| <span data-ttu-id="a1860-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="a1860-159">Name</span></span>       | <span data-ttu-id="a1860-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1860-160">Type</span></span> | <span data-ttu-id="a1860-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1860-161">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a1860-162">Autorización</span><span class="sxs-lookup"><span data-stu-id="a1860-162">Authorization</span></span>  | <span data-ttu-id="a1860-163">string</span><span class="sxs-lookup"><span data-stu-id="a1860-163">string</span></span>  | <span data-ttu-id="a1860-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a1860-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a1860-166">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1860-166">Request body</span></span>
<span data-ttu-id="a1860-167">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a1860-167">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a1860-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1860-168">Response</span></span>
<span data-ttu-id="a1860-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1860-169">If successful, this method returns a `200 OK` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1860-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1860-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="a1860-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1860-171">Request</span></span>
<span data-ttu-id="a1860-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1860-172">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}
```

### <a name="response"></a><span data-ttu-id="a1860-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1860-173">Response</span></span>
<span data-ttu-id="a1860-174">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1860-174">The following is an example of the response.</span></span> 
><span data-ttu-id="a1860-175">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a1860-175">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="a1860-176">Se devolverán todas las propiedades predeterminadas de una llamada real, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a1860-176">The default properties will be returned from an actual call, as described before.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="a1860-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1860-177">See also</span></span>

- [<span data-ttu-id="a1860-178">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="a1860-178">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="a1860-179">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="a1860-179">Add custom data to users using open extensions</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="a1860-180">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="a1860-180">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
