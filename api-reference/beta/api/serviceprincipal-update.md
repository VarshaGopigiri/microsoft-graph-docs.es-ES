---
title: Actualizar serviceprincipal
description: Actualizar las propiedades del objeto serviceprincipal.
ms.openlocfilehash: a24a8c949d48f577a3d7fe6208a1422819772801
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090670"
---
# <a name="update-serviceprincipal"></a><span data-ttu-id="9a6d2-103">Actualizar serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="9a6d2-103">Update serviceprincipal</span></span>

> <span data-ttu-id="9a6d2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9a6d2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9a6d2-106">Actualizar las propiedades del objeto serviceprincipal.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-106">Update the properties of serviceprincipal object.</span></span>
## <a name="permissions"></a><span data-ttu-id="9a6d2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a6d2-107">Permissions</span></span>
<span data-ttu-id="9a6d2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9a6d2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9a6d2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a6d2-110">Permission type</span></span>      | <span data-ttu-id="9a6d2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a6d2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a6d2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a6d2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9a6d2-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9a6d2-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9a6d2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a6d2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a6d2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-115">Not supported.</span></span>    |
|<span data-ttu-id="9a6d2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a6d2-116">Application</span></span> | <span data-ttu-id="9a6d2-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9a6d2-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a6d2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a6d2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /servicePrincipals/{id}
```
## <a name="request-headers"></a><span data-ttu-id="9a6d2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a6d2-119">Request headers</span></span>
| <span data-ttu-id="9a6d2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a6d2-120">Name</span></span>       | <span data-ttu-id="9a6d2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a6d2-121">Type</span></span> | <span data-ttu-id="9a6d2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a6d2-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9a6d2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a6d2-123">Authorization</span></span>  | <span data-ttu-id="9a6d2-124">string</span><span class="sxs-lookup"><span data-stu-id="9a6d2-124">string</span></span>  | <span data-ttu-id="9a6d2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9a6d2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a6d2-127">Request body</span></span>
<span data-ttu-id="9a6d2-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9a6d2-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a6d2-131">Property</span></span>     | <span data-ttu-id="9a6d2-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a6d2-132">Type</span></span>   |<span data-ttu-id="9a6d2-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a6d2-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a6d2-134">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="9a6d2-134">accountEnabled</span></span>|<span data-ttu-id="9a6d2-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="9a6d2-135">Boolean</span></span>|                <span data-ttu-id="9a6d2-136">**true** si la cuenta de servicio de entidad de seguridad está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-136">**true** if the service principal account is enabled; otherwise, **false**.</span></span>            |
|<span data-ttu-id="9a6d2-137">appDisplayName</span><span class="sxs-lookup"><span data-stu-id="9a6d2-137">appDisplayName</span></span>|<span data-ttu-id="9a6d2-138">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-138">String</span></span>|<span data-ttu-id="9a6d2-139">El nombre para mostrar expuesto por la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-139">The display name exposed by the associated application.</span></span>|
|<span data-ttu-id="9a6d2-140">appId</span><span class="sxs-lookup"><span data-stu-id="9a6d2-140">appId</span></span>|<span data-ttu-id="9a6d2-141">cadena</span><span class="sxs-lookup"><span data-stu-id="9a6d2-141">String</span></span>|<span data-ttu-id="9a6d2-142">El identificador único para la aplicación asociada (su propiedad **appId** ).</span><span class="sxs-lookup"><span data-stu-id="9a6d2-142">The unique identifier for the associated application (its **appId** property).</span></span>|
|<span data-ttu-id="9a6d2-143">appRoleAssignmentRequired</span><span class="sxs-lookup"><span data-stu-id="9a6d2-143">appRoleAssignmentRequired</span></span>|<span data-ttu-id="9a6d2-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="9a6d2-144">Boolean</span></span>|<span data-ttu-id="9a6d2-145">Especifica si un **appRoleAssignment** a un usuario o grupo es necesaria antes de Azure AD emitirá un usuario o un token de acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-145">Specifies whether an **appRoleAssignment** to a user or group is required before Azure AD will issue a user or access token to the application.</span></span>                            <span data-ttu-id="9a6d2-146">**Notas**: requiere la versión 1.5 o versiones posteriores, no acepta valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-146">**Notes**: Requires version 1.5 or newer, not nullable.</span></span>            |
|<span data-ttu-id="9a6d2-147">appRoles</span><span class="sxs-lookup"><span data-stu-id="9a6d2-147">appRoles</span></span>|<span data-ttu-id="9a6d2-148">función de aplicación</span><span class="sxs-lookup"><span data-stu-id="9a6d2-148">appRole</span></span>|<span data-ttu-id="9a6d2-149">Las funciones de aplicación expuestas por la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-149">The application roles exposed by the associated application.</span></span> <span data-ttu-id="9a6d2-150">Para obtener más información, vea la definición de la propiedad **appRoles** en la entidad de aplicación **notas**: requiere la versión 1.5 o versiones posteriores, no acepta valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-150">For more information see the **appRoles** property definition on the application entity                            **Notes**: Requires version 1.5 or newer, not nullable.</span></span>            |
|<span data-ttu-id="9a6d2-151">displayName</span><span class="sxs-lookup"><span data-stu-id="9a6d2-151">displayName</span></span>|<span data-ttu-id="9a6d2-152">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-152">String</span></span>|<span data-ttu-id="9a6d2-153">El nombre para mostrar para la entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-153">The display name for the service principal.</span></span>|
|<span data-ttu-id="9a6d2-154">errorUrl</span><span class="sxs-lookup"><span data-stu-id="9a6d2-154">errorUrl</span></span>|<span data-ttu-id="9a6d2-155">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-155">String</span></span>|            |
|<span data-ttu-id="9a6d2-156">página principal</span><span class="sxs-lookup"><span data-stu-id="9a6d2-156">homepage</span></span>|<span data-ttu-id="9a6d2-157">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-157">String</span></span>|<span data-ttu-id="9a6d2-158">La dirección URL a la página principal de la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-158">The URL to the homepage of the associated application.</span></span>|
|<span data-ttu-id="9a6d2-159">keyCredentials</span><span class="sxs-lookup"><span data-stu-id="9a6d2-159">keyCredentials</span></span>|<span data-ttu-id="9a6d2-160">keyCredential</span><span class="sxs-lookup"><span data-stu-id="9a6d2-160">keyCredential</span></span>|<span data-ttu-id="9a6d2-161">La colección de credenciales claves asociado con el servicio de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-161">The collection of key credentials associated with the service principal.</span></span>                            <span data-ttu-id="9a6d2-162">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-162">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9a6d2-163">logoutUrl</span><span class="sxs-lookup"><span data-stu-id="9a6d2-163">logoutUrl</span></span>|<span data-ttu-id="9a6d2-164">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-164">String</span></span>| <span data-ttu-id="9a6d2-165">Especifica la dirección URL que usará el servicio de autorización de Microsoft para cerrar sesión de un usuario mediante [canal de frente](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back canal](https://openid.net/specs/openid-connect-backchannel-1_0.html) o protocolos de cierre de sesión SAML.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-165">Specifies the URL that will be used by Microsoft's authorization service to logout an user using [front-channel](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back-channel](https://openid.net/specs/openid-connect-backchannel-1_0.html) or SAML logout protocols.</span></span> |
|<span data-ttu-id="9a6d2-166">oauth2Permissions</span><span class="sxs-lookup"><span data-stu-id="9a6d2-166">oauth2Permissions</span></span>|<span data-ttu-id="9a6d2-167">oAuth2Permission</span><span class="sxs-lookup"><span data-stu-id="9a6d2-167">oAuth2Permission</span></span>|<span data-ttu-id="9a6d2-168">Los permisos de OAuth 2.0 expuestos por la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-168">The OAuth 2.0 permissions exposed by the associated application.</span></span> <span data-ttu-id="9a6d2-169">Para obtener más información, vea la definición de la propiedad **oauth2Permissions** en la entidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-169">For more information see the **oauth2Permissions** property definition on the application entity.</span></span>                            <span data-ttu-id="9a6d2-170">**Notas**: requiere la versión 1.5 o versiones posteriores, no acepta valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-170">**Notes**: Requires version 1.5 or newer, not nullable.</span></span>            |
|<span data-ttu-id="9a6d2-171">passwordCredentials</span><span class="sxs-lookup"><span data-stu-id="9a6d2-171">passwordCredentials</span></span>|<span data-ttu-id="9a6d2-172">passwordCredential</span><span class="sxs-lookup"><span data-stu-id="9a6d2-172">passwordCredential</span></span>|<span data-ttu-id="9a6d2-173">La colección de credenciales de contraseña asociada con la entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-173">The collection of password credentials associated with the service principal.</span></span>                            <span data-ttu-id="9a6d2-174">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-174">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9a6d2-175">preferredTokenSigningKeyThumbprint</span><span class="sxs-lookup"><span data-stu-id="9a6d2-175">preferredTokenSigningKeyThumbprint</span></span>|<span data-ttu-id="9a6d2-176">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-176">String</span></span>|<span data-ttu-id="9a6d2-177">Reservado sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-177">Reserved for internal use only.</span></span> <span data-ttu-id="9a6d2-178">No escribir ni en caso contrario, se basan en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-178">Do not write or otherwise rely on this property.</span></span> <span data-ttu-id="9a6d2-179">Puede quitarse en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-179">May be removed in future versions.</span></span>                            <span data-ttu-id="9a6d2-180">**Notas**: requiere la versión 1.5 o más reciente.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-180">**Notes**: Requires version 1.5 or newer.</span></span>            |
|<span data-ttu-id="9a6d2-181">publisherName</span><span class="sxs-lookup"><span data-stu-id="9a6d2-181">publisherName</span></span>|<span data-ttu-id="9a6d2-182">cadena</span><span class="sxs-lookup"><span data-stu-id="9a6d2-182">String</span></span>|<span data-ttu-id="9a6d2-183">El nombre para mostrar del inquilino en el que se especifica la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-183">The display name of the tenant in which the associated application is specified.</span></span>|
|<span data-ttu-id="9a6d2-184">replyUrls</span><span class="sxs-lookup"><span data-stu-id="9a6d2-184">replyUrls</span></span>|<span data-ttu-id="9a6d2-185">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-185">String</span></span>|<span data-ttu-id="9a6d2-186">Las direcciones URL que los tokens de usuario se envían a para el inicio de sesión con la aplicación asociada o el redireccionamiento de códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a para la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-186">The URLs that user tokens are sent to for sign in with the associated application, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to for the associated application.</span></span>                            <span data-ttu-id="9a6d2-187">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-187">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9a6d2-188">samlMetadataUrl</span><span class="sxs-lookup"><span data-stu-id="9a6d2-188">samlMetadataUrl</span></span>|<span data-ttu-id="9a6d2-189">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-189">String</span></span>|            |
|<span data-ttu-id="9a6d2-190">servicePrincipalNames</span><span class="sxs-lookup"><span data-stu-id="9a6d2-190">servicePrincipalNames</span></span>|<span data-ttu-id="9a6d2-191">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-191">String</span></span>|<span data-ttu-id="9a6d2-192">El URI que identifica la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-192">The URIs that identify the associated application.</span></span> <span data-ttu-id="9a6d2-193">Para obtener más información, vea [objetos de la aplicación y los objetos a principales de servicio](https://msdn.microsoft.com/library/azure/dn132633.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a6d2-193">For more information see, [Application Objects and Service Principal Objects](https://msdn.microsoft.com/library/azure/dn132633.aspx).</span></span>                            <span data-ttu-id="9a6d2-194">**Notas**: no acepta valores NULL, el operador **any** es necesario para las expresiones de filtro en las propiedades multivalor; Para obtener más información, vea [admiten consultas, filtros y las opciones de paginación](https://msdn.microsoft.com/library/azure/dn727074.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a6d2-194">**Notes**: not nullable, the **any** operator is required for filter expressions on multi-valued properties; for more information, see [Supported Queries, Filters, and Paging Options](https://msdn.microsoft.com/library/azure/dn727074.aspx).</span></span>            |
|<span data-ttu-id="9a6d2-195">de cierre</span><span class="sxs-lookup"><span data-stu-id="9a6d2-195">tags</span></span>|<span data-ttu-id="9a6d2-196">String</span><span class="sxs-lookup"><span data-stu-id="9a6d2-196">String</span></span>|                                        <span data-ttu-id="9a6d2-197">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-197">**Notes**: not nullable.</span></span>            |

## <a name="response"></a><span data-ttu-id="9a6d2-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a6d2-198">Response</span></span>

<span data-ttu-id="9a6d2-199">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [servicePrincipal](../resources/serviceprincipal.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-199">If successful, this method returns a `200 OK` response code and updated [servicePrincipal](../resources/serviceprincipal.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9a6d2-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a6d2-200">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9a6d2-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a6d2-201">Request</span></span>
<span data-ttu-id="9a6d2-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-202">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_serviceprincipal"
}-->
```http
PATCH https://graph.microsoft.com/beta/servicePrincipals/{id}
Content-type: application/json
Content-length: 391

{
  "accountEnabled": true,
  "addIns": [
    {
      "id": "id-value",
      "type": "type-value",
      "properties": [
        {
          "key": "key-value",
          "value": "value-value"
        }
      ]
    }
  ],
  "appDisplayName": "appDisplayName-value",
  "appId": "appId-value",
  "appOwnerOrganizationId": "appOwnerOrganizationId-value",
  "appRoleAssignmentRequired": true
}
```
##### <a name="response"></a><span data-ttu-id="9a6d2-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a6d2-203">Response</span></span>
<span data-ttu-id="9a6d2-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a6d2-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.serviceprincipal"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 391

{
  "accountEnabled": true,
  "addIns": [
    {
      "id": "id-value",
      "type": "type-value",
      "properties": [
        {
          "key": "key-value",
          "value": "value-value"
        }
      ]
    }
  ],
  "appDisplayName": "appDisplayName-value",
  "appId": "appId-value",
  "appOwnerOrganizationId": "appOwnerOrganizationId-value",
  "appRoleAssignmentRequired": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update serviceprincipal",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->