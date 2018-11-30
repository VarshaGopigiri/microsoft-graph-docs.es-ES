---
title: 'usuario: getMemberGroups'
description: Devolver todos los grupos que el usuario es un miembro de. La comprobación es transitiva, a diferencia de lectura de la
ms.openlocfilehash: 875228e2c40be7928024e8507416d81e9b80a805
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031771"
---
# <a name="user-getmembergroups"></a><span data-ttu-id="bd056-104">usuario: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="bd056-104">user: getMemberGroups</span></span>

<span data-ttu-id="bd056-p102">Devuelva todos los grupos de los que el usuario es miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/user-list-memberof.md), que devuelve solo los grupos de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="bd056-p102">Return all the groups that the user is a member of. The check is transitive, unlike reading the [memberOf](../api/user-list-memberof.md) navigation property, which returns only the groups that the user is a direct member of.</span></span>

<span data-ttu-id="bd056-p103">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="bd056-p103">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="bd056-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd056-111">Permissions</span></span>

<span data-ttu-id="bd056-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd056-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bd056-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd056-114">Permission type</span></span>                        | <span data-ttu-id="bd056-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd056-115">Permissions (from least to most privileged)</span></span>                                                                                                          |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="bd056-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd056-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="bd056-117">~~User.Read y Group.Read.All~~, ~~User.ReadBasic.All y Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bd056-117">~~User.Read and Group.Read.All~~, ~~User.ReadBasic.All and Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="bd056-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd056-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd056-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd056-119">Not supported.</span></span>                                                                                                                                       |
| <span data-ttu-id="bd056-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd056-120">Application</span></span>                            | <span data-ttu-id="bd056-121">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bd056-121">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span></span>                                                                                        |

> <span data-ttu-id="bd056-122">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="bd056-122">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="bd056-123">Con el permiso Group.Read.All, solos o en combinación con un `User.` permiso, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="bd056-123">Using the Group.Read.All permission, either alone or in combination with a `User.` permission, will return an error.</span></span> <span data-ttu-id="bd056-124">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="bd056-124">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="bd056-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd056-125">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/getMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="bd056-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd056-126">Request headers</span></span>

| <span data-ttu-id="bd056-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd056-127">Header</span></span>        | <span data-ttu-id="bd056-128">Valor</span><span class="sxs-lookup"><span data-stu-id="bd056-128">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="bd056-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="bd056-129">Authorization</span></span> | <span data-ttu-id="bd056-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd056-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bd056-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bd056-132">Content-Type</span></span>  | <span data-ttu-id="bd056-133">application/json</span><span class="sxs-lookup"><span data-stu-id="bd056-133">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="bd056-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd056-134">Request body</span></span>

<span data-ttu-id="bd056-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="bd056-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bd056-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bd056-136">Parameter</span></span>           | <span data-ttu-id="bd056-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd056-137">Type</span></span>    | <span data-ttu-id="bd056-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd056-138">Description</span></span>                                                                                                                                                                                                                                                                         |
| :------------------ | :------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="bd056-139">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="bd056-139">securityEnabledOnly</span></span> | <span data-ttu-id="bd056-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="bd056-140">Boolean</span></span> | <span data-ttu-id="bd056-p107">**true** para especificar que solo se deben devolver los grupos de seguridad de los que el usuario es miembro; **false** para especificar que se deben devolver todos los grupos de los que el usuario es miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="bd056-p107">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span> |

## <a name="response"></a><span data-ttu-id="bd056-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd056-143">Response</span></span>

<span data-ttu-id="bd056-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="bd056-144">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="bd056-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd056-145">Example</span></span>

<span data-ttu-id="bd056-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bd056-146">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="bd056-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd056-147">Request</span></span>

<span data-ttu-id="bd056-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd056-148">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_getmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="bd056-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd056-149">Response</span></span>

<span data-ttu-id="bd056-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd056-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "user: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
