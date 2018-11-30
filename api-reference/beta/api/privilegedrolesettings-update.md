---
title: Actualizar privilegedRoleSettings
description: Actualizar la configuración de las funciones para la configuración de rol determinado. Se devuelve un objeto privilegedRoleSettings.
ms.openlocfilehash: 0e0f6b7253a1c1d8570c0b91fac4b08bbd39dfff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090378"
---
# <a name="update-privilegedrolesettings"></a><span data-ttu-id="d12dd-104">Actualizar privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="d12dd-104">Update privilegedRoleSettings</span></span>

> <span data-ttu-id="d12dd-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d12dd-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d12dd-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d12dd-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d12dd-107">Actualizar la configuración de las funciones para la configuración de rol determinado.</span><span class="sxs-lookup"><span data-stu-id="d12dd-107">Update the role settings for the given role setting.</span></span> <span data-ttu-id="d12dd-108">Se devuelve un objeto [privilegedRoleSettings](../resources/privilegedrolesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="d12dd-108">A [privilegedRoleSettings](../resources/privilegedrolesettings.md) object will be returned.</span></span>
## <a name="permissions"></a><span data-ttu-id="d12dd-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="d12dd-109">Permissions</span></span>

<span data-ttu-id="d12dd-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d12dd-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

><span data-ttu-id="d12dd-112">**Nota:** El solicitante debe tener uno de los siguientes roles: Administrador de roles con privilegios, administrador Global, Administrador de seguridad o lector de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d12dd-112">**Note:** The requester must have one of the following roles: Privileged Role Administrator, Global Administrator, Security Administrator, or Security Reader.</span></span> 

|<span data-ttu-id="d12dd-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d12dd-113">Permission type</span></span>      | <span data-ttu-id="d12dd-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d12dd-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d12dd-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d12dd-115">Delegated (work or school account)</span></span> | <span data-ttu-id="d12dd-116">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d12dd-116">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d12dd-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d12dd-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d12dd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d12dd-118">Not supported.</span></span>    |
|<span data-ttu-id="d12dd-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d12dd-119">Application</span></span> | <span data-ttu-id="d12dd-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d12dd-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d12dd-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d12dd-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /privilegedRoles/{id}/settings
```

## <a name="request-headers"></a><span data-ttu-id="d12dd-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d12dd-122">Request headers</span></span>
| <span data-ttu-id="d12dd-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d12dd-123">Name</span></span>      |<span data-ttu-id="d12dd-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d12dd-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d12dd-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d12dd-125">Authorization</span></span>  | <span data-ttu-id="d12dd-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d12dd-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d12dd-128">Request body</span></span>
<span data-ttu-id="d12dd-129">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [privilegedRoleSettings](../resources/privilegedrolesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="d12dd-129">In the request body, supply a JSON representation of a [privilegedRoleSettings](../resources/privilegedrolesettings.md) object.</span></span>

<span data-ttu-id="d12dd-130">En la siguiente tabla se enumera las propiedades que puede proporcionar al actualizar una configuración de rol.</span><span class="sxs-lookup"><span data-stu-id="d12dd-130">The following table lists the properties that you can supply when you update a role setting.</span></span>

|<span data-ttu-id="d12dd-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d12dd-131">Property</span></span>|<span data-ttu-id="d12dd-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="d12dd-132">Type</span></span>|<span data-ttu-id="d12dd-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d12dd-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d12dd-134">elevationDuration</span><span class="sxs-lookup"><span data-stu-id="d12dd-134">elevationDuration</span></span>|<span data-ttu-id="d12dd-135">duration</span><span class="sxs-lookup"><span data-stu-id="d12dd-135">duration</span></span>|<span data-ttu-id="d12dd-136">La duración cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-136">The duration when the role is activated.</span></span> <span data-ttu-id="d12dd-137">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-137">Required.</span></span>|
|<span data-ttu-id="d12dd-138">id</span><span class="sxs-lookup"><span data-stu-id="d12dd-138">id</span></span>|<span data-ttu-id="d12dd-139">string</span><span class="sxs-lookup"><span data-stu-id="d12dd-139">string</span></span>|<span data-ttu-id="d12dd-140">El identificador único para la configuración de las funciones.</span><span class="sxs-lookup"><span data-stu-id="d12dd-140">The unique identifier for the role settings.</span></span> <span data-ttu-id="d12dd-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d12dd-141">Read-only.</span></span> <span data-ttu-id="d12dd-142">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-142">Required.</span></span>|
|<span data-ttu-id="d12dd-143">isMfaOnElevationConfigurable</span><span class="sxs-lookup"><span data-stu-id="d12dd-143">isMfaOnElevationConfigurable</span></span>|<span data-ttu-id="d12dd-144">boolean</span><span class="sxs-lookup"><span data-stu-id="d12dd-144">boolean</span></span>|<span data-ttu-id="d12dd-145">**true** si mfaOnElevation es configurable.</span><span class="sxs-lookup"><span data-stu-id="d12dd-145">**true** if mfaOnElevation is configurable.</span></span> <span data-ttu-id="d12dd-146">**false** si no se puede configurar mfaOnElevation.</span><span class="sxs-lookup"><span data-stu-id="d12dd-146">**false** if mfaOnElevation is not configurable.</span></span> <span data-ttu-id="d12dd-147">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-147">Required.</span></span>|
|<span data-ttu-id="d12dd-148">lastGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="d12dd-148">lastGlobalAdmin</span></span>|<span data-ttu-id="d12dd-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="d12dd-149">Boolean</span></span>|<span data-ttu-id="d12dd-150">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="d12dd-150">For internal use only.</span></span>|
|<span data-ttu-id="d12dd-151">maxElavationDuration</span><span class="sxs-lookup"><span data-stu-id="d12dd-151">maxElavationDuration</span></span>|<span data-ttu-id="d12dd-152">duration</span><span class="sxs-lookup"><span data-stu-id="d12dd-152">duration</span></span>|<span data-ttu-id="d12dd-153">Duración máxima de la función activada.</span><span class="sxs-lookup"><span data-stu-id="d12dd-153">Maximum duration for the activated role.</span></span> <span data-ttu-id="d12dd-154">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-154">Required.</span></span>|
|<span data-ttu-id="d12dd-155">mfaOnElevation</span><span class="sxs-lookup"><span data-stu-id="d12dd-155">mfaOnElevation</span></span>|<span data-ttu-id="d12dd-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="d12dd-156">Boolean</span></span>|<span data-ttu-id="d12dd-157">**true** si MFA se requiere para activar la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-157">**true** if MFA is required to activate the role.</span></span> <span data-ttu-id="d12dd-158">**false** si no es necesario MFA para activar la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-158">**false** if MFA is not required to activate the role.</span></span> <span data-ttu-id="d12dd-159">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-159">Required.</span></span>|
|<span data-ttu-id="d12dd-160">minElevationDuration</span><span class="sxs-lookup"><span data-stu-id="d12dd-160">minElevationDuration</span></span>|<span data-ttu-id="d12dd-161">duration</span><span class="sxs-lookup"><span data-stu-id="d12dd-161">duration</span></span>|<span data-ttu-id="d12dd-162">Duración mínima para la función activada.</span><span class="sxs-lookup"><span data-stu-id="d12dd-162">Minimum duration for the activated role.</span></span> <span data-ttu-id="d12dd-163">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-163">Required.</span></span>|
|<span data-ttu-id="d12dd-164">notificationToUserOnElevation</span><span class="sxs-lookup"><span data-stu-id="d12dd-164">notificationToUserOnElevation</span></span>|<span data-ttu-id="d12dd-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="d12dd-165">Boolean</span></span>|<span data-ttu-id="d12dd-166">**true** si enviar notificación para el usuario final cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-166">**true** if send notification to the end user when the role is activated.</span></span> <span data-ttu-id="d12dd-167">**false** si no enviar notificación cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-167">**false** if do not send notification when the role is activated.</span></span> <span data-ttu-id="d12dd-168">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-168">Required.</span></span>|
|<span data-ttu-id="d12dd-169">ticketingInfoOnElevation</span><span class="sxs-lookup"><span data-stu-id="d12dd-169">ticketingInfoOnElevation</span></span>|<span data-ttu-id="d12dd-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="d12dd-170">Boolean</span></span>|<span data-ttu-id="d12dd-171">**true** si se requiere la información mediante vales cuándo activar la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-171">**true** if the ticketing information is required when activate the role.</span></span> <span data-ttu-id="d12dd-172">**false** si la información mediante vales no se requiere cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-172">**false** if the ticketing information is not required when activate the role.</span></span> <span data-ttu-id="d12dd-173">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-173">Required.</span></span>|
|<span data-ttu-id="d12dd-174">approvalOnElevation</span><span class="sxs-lookup"><span data-stu-id="d12dd-174">approvalOnElevation</span></span>|<span data-ttu-id="d12dd-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="d12dd-175">Boolean</span></span>|<span data-ttu-id="d12dd-176">**true** si se requiere la aprobación cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-176">**true** if the approval is required when activate the role.</span></span> <span data-ttu-id="d12dd-177">**false** si la aprobación no se requiere cuando se activa la función.</span><span class="sxs-lookup"><span data-stu-id="d12dd-177">**false** if the approval is not required when activate the role.</span></span> <span data-ttu-id="d12dd-178">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12dd-178">Required.</span></span>|
|<span data-ttu-id="d12dd-179">approverIds</span><span class="sxs-lookup"><span data-stu-id="d12dd-179">approverIds</span></span>|<span data-ttu-id="d12dd-180">matriz</span><span class="sxs-lookup"><span data-stu-id="d12dd-180">array</span></span>|<span data-ttu-id="d12dd-181">Lista de identificadores de aprobación, si se necesita aprobación para la activación.</span><span class="sxs-lookup"><span data-stu-id="d12dd-181">List of Approval IDs, if approval is required for activation.</span></span>|

## <a name="response"></a><span data-ttu-id="d12dd-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d12dd-182">Response</span></span>

<span data-ttu-id="d12dd-183">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d12dd-183">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="d12dd-184">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="d12dd-184">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="d12dd-185">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="d12dd-185">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="d12dd-186">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d12dd-186">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d12dd-187">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d12dd-187">Request</span></span>
<span data-ttu-id="d12dd-188">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d12dd-188">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "put_privilegedrolesettings"
}-->
```http
PUT https://graph.microsoft.com/beta/privilegedRoles/{id}/settings
Content-type: application/json

{
    "id": "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3",
    "elevationDuration": "PT8H",
    "notificationToUserOnElevation": false,
    "ticketingInfoOnElevation": true,
    "mfaOnElevation": false,
    "maxElavationDuration": "PT0S",
    "minElevationDuration": "PT0S",
    "lastGlobalAdmin": false,
    "isMfaOnElevationConfigurable": true,
    "approvalOnElevation": false,
    "approverIds": ["e2b2a2fb-13d7-495c-adc9-941fe966793f", "22770e3f-b9b4-418e-9dea-d0e3d2f275dd"]
}
```
##### <a name="response"></a><span data-ttu-id="d12dd-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d12dd-189">Response</span></span>
<span data-ttu-id="d12dd-190">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d12dd-190">Here is an example of the response.</span></span>

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update privilegedRoleSettings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
