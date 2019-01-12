---
title: Obtener grupo
description: Obtiene las propiedades y relaciones de un objeto de grupo.
author: dkershaw10
localization_priority: Priority
ms.prod: groups
ms.openlocfilehash: 99215af564be186edaf57563ae493f363c9cc2fa
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941054"
---
# <a name="get-group"></a><span data-ttu-id="68dc7-103">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="68dc7-103">Get group</span></span>

> <span data-ttu-id="68dc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="68dc7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="68dc7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="68dc7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="68dc7-106">Obtener las propiedades y relaciones de un objeto de [grupo](../resources/group.md) .</span><span class="sxs-lookup"><span data-stu-id="68dc7-106">Get the properties and relationships of a [group](../resources/group.md) object.</span></span>

##### <a name="default-properties"></a><span data-ttu-id="68dc7-107">Propiedades predeterminadas</span><span class="sxs-lookup"><span data-stu-id="68dc7-107">Default properties</span></span>

<span data-ttu-id="68dc7-p102">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener o enumerar grupos. Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="68dc7-p102">The following represent the default set of properties that are returned when getting or listing groups. These are a subset of all available properties.</span></span> 

* <span data-ttu-id="68dc7-110">classification</span><span class="sxs-lookup"><span data-stu-id="68dc7-110">classification</span></span>
* <span data-ttu-id="68dc7-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="68dc7-111">createdDateTime</span></span>
* <span data-ttu-id="68dc7-112">descripción</span><span class="sxs-lookup"><span data-stu-id="68dc7-112">description</span></span>
* <span data-ttu-id="68dc7-113">displayName</span><span class="sxs-lookup"><span data-stu-id="68dc7-113">displayName</span></span>
* <span data-ttu-id="68dc7-114">groupTypes</span><span class="sxs-lookup"><span data-stu-id="68dc7-114">groupTypes</span></span>
* <span data-ttu-id="68dc7-115">id</span><span class="sxs-lookup"><span data-stu-id="68dc7-115">id</span></span>
* <span data-ttu-id="68dc7-116">mail</span><span class="sxs-lookup"><span data-stu-id="68dc7-116">mail</span></span>
* <span data-ttu-id="68dc7-117">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="68dc7-117">mailEnabled</span></span>
* <span data-ttu-id="68dc7-118">mailNickname</span><span class="sxs-lookup"><span data-stu-id="68dc7-118">mailNickname</span></span>
* <span data-ttu-id="68dc7-119">membershipRule</span><span class="sxs-lookup"><span data-stu-id="68dc7-119">membershipRule</span></span>
* <span data-ttu-id="68dc7-120">membershipRuleProcessingState</span><span class="sxs-lookup"><span data-stu-id="68dc7-120">membershipRuleProcessingState</span></span>
* <span data-ttu-id="68dc7-121">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="68dc7-121">onPremisesLastSyncDateTime</span></span>
* <span data-ttu-id="68dc7-122">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="68dc7-122">onPremisesSecurityIdentifier</span></span>
* <span data-ttu-id="68dc7-123">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="68dc7-123">onPremisesSyncEnabled</span></span>
* <span data-ttu-id="68dc7-124">preferredLanguage - no se admite; no puede ser un valor para esta propiedad conjunto y devuelve `null` cuando llama.</span><span class="sxs-lookup"><span data-stu-id="68dc7-124">preferredLanguage - Not supported; a value for this property cannot be set and returns `null` when called.</span></span>
* <span data-ttu-id="68dc7-125">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="68dc7-125">proxyAddresses</span></span>
* <span data-ttu-id="68dc7-126">renewedDateTime</span><span class="sxs-lookup"><span data-stu-id="68dc7-126">renewedDateTime</span></span>
* <span data-ttu-id="68dc7-127">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="68dc7-127">securityEnabled</span></span>
* <span data-ttu-id="68dc7-128">tema</span><span class="sxs-lookup"><span data-stu-id="68dc7-128">theme</span></span>
* <span data-ttu-id="68dc7-129">visibility</span><span class="sxs-lookup"><span data-stu-id="68dc7-129">visibility</span></span>

<span data-ttu-id="68dc7-130">De forma predeterminada, no se devuelven las siguientes propiedades de grupo:</span><span class="sxs-lookup"><span data-stu-id="68dc7-130">The following group properties are not returned by default:</span></span>

* <span data-ttu-id="68dc7-131">accessType</span><span class="sxs-lookup"><span data-stu-id="68dc7-131">accessType</span></span>
* <span data-ttu-id="68dc7-132">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="68dc7-132">allowExternalSenders</span></span>
* <span data-ttu-id="68dc7-133">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="68dc7-133">autoSubscribeNewMembers</span></span>
* <span data-ttu-id="68dc7-134">hasMembersWithLicenseErrors</span><span class="sxs-lookup"><span data-stu-id="68dc7-134">hasMembersWithLicenseErrors</span></span>
* <span data-ttu-id="68dc7-135">isSubscribedByMail</span><span class="sxs-lookup"><span data-stu-id="68dc7-135">isSubscribedByMail</span></span>
* <span data-ttu-id="68dc7-136">isFavorite</span><span class="sxs-lookup"><span data-stu-id="68dc7-136">isFavorite</span></span>
* <span data-ttu-id="68dc7-137">unseenConversationsCount</span><span class="sxs-lookup"><span data-stu-id="68dc7-137">unseenConversationsCount</span></span>
* <span data-ttu-id="68dc7-138">unseenCount</span><span class="sxs-lookup"><span data-stu-id="68dc7-138">unseenCount</span></span>
* <span data-ttu-id="68dc7-139">unseenMessagesCount</span><span class="sxs-lookup"><span data-stu-id="68dc7-139">unseenMessagesCount</span></span>

<span data-ttu-id="68dc7-140">Para obtener estas propiedades (excepto **isFavorite** y **hasMembersWithLicenseErrors**), utilice la `$select` parámetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="68dc7-140">To get these properties (except **isFavorite** and **hasMembersWithLicenseErrors**), use the `$select` query parameter.</span></span> <span data-ttu-id="68dc7-141">Estos son algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="68dc7-141">The following are examples:</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount

GET https://graph.microsoft.com/beta/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=description,allowExternalSenders
```

<span data-ttu-id="68dc7-142">Para devolver los grupos que contienen a miembros con errores de licencia, use el parámetro de consulta **$filter** :</span><span class="sxs-lookup"><span data-stu-id="68dc7-142">To return groups containing members with license errors, use the **$filter** query parameter:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET GET https://graph.microsoft.com/beta/groups?$filter=hasMembersWithLicenseErrors+eq+true
```

<span data-ttu-id="68dc7-143">Puesto que el recurso de **grupo** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de **grupo** .</span><span class="sxs-lookup"><span data-stu-id="68dc7-143">Since the **group** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **group** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="68dc7-144">Permisos</span><span class="sxs-lookup"><span data-stu-id="68dc7-144">Permissions</span></span>
<span data-ttu-id="68dc7-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68dc7-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="68dc7-147">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68dc7-147">Permission type</span></span>      | <span data-ttu-id="68dc7-148">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68dc7-148">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="68dc7-149">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68dc7-149">Delegated (work or school account)</span></span> | <span data-ttu-id="68dc7-150">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68dc7-150">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="68dc7-151">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68dc7-151">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="68dc7-152">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68dc7-152">Not supported.</span></span>    |
|<span data-ttu-id="68dc7-153">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68dc7-153">Application</span></span> | <span data-ttu-id="68dc7-154">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68dc7-154">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="68dc7-155">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68dc7-155">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="68dc7-156">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="68dc7-156">Optional query parameters</span></span>
<span data-ttu-id="68dc7-157">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68dc7-157">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="68dc7-158">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68dc7-158">Request headers</span></span>
| <span data-ttu-id="68dc7-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="68dc7-159">Name</span></span>       | <span data-ttu-id="68dc7-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="68dc7-160">Type</span></span> | <span data-ttu-id="68dc7-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="68dc7-161">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="68dc7-162">Autorización</span><span class="sxs-lookup"><span data-stu-id="68dc7-162">Authorization</span></span>  | <span data-ttu-id="68dc7-163">string</span><span class="sxs-lookup"><span data-stu-id="68dc7-163">string</span></span>  | <span data-ttu-id="68dc7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68dc7-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="68dc7-166">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68dc7-166">Request body</span></span>
<span data-ttu-id="68dc7-167">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68dc7-167">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="68dc7-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68dc7-168">Response</span></span>
<span data-ttu-id="68dc7-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68dc7-169">If successful, this method returns a `200 OK` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68dc7-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68dc7-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="68dc7-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68dc7-171">Request</span></span>
<span data-ttu-id="68dc7-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68dc7-172">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}
```

### <a name="response"></a><span data-ttu-id="68dc7-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68dc7-173">Response</span></span>
<span data-ttu-id="68dc7-174">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68dc7-174">The following is an example of the response.</span></span> 
><span data-ttu-id="68dc7-175">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="68dc7-175">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="68dc7-176">Se devolverán todas las propiedades predeterminadas de una llamada real, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="68dc7-176">The default properties will be returned from an actual call, as described before.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="68dc7-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="68dc7-177">See also</span></span>

- [<span data-ttu-id="68dc7-178">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="68dc7-178">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="68dc7-179">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="68dc7-179">Add custom data to users using open extensions</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="68dc7-180">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="68dc7-180">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
