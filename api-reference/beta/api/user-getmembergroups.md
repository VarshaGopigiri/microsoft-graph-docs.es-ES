---
title: 'usuario: getMemberGroups'
description: Devolver todos los grupos que el usuario es un miembro de. La comprobación es transitiva, a diferencia de lectura de la
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 68c01242927a80e9a35625f6e0ad733b44d4c3fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959681"
---
# <a name="user-getmembergroups"></a><span data-ttu-id="7eeee-104">usuario: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="7eeee-104">user: getMemberGroups</span></span>

> <span data-ttu-id="7eeee-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7eeee-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7eeee-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7eeee-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7eeee-p103">Devuelva todos los grupos de los que el usuario es miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/user-list-memberof.md), que devuelve solo los grupos de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="7eeee-p103">Return all the groups that the user is a member of. The check is transitive, unlike reading the [memberOf](../api/user-list-memberof.md) navigation property, which returns only the groups that the user is a direct member of.</span></span>

<span data-ttu-id="7eeee-p104">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="7eeee-p104">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="7eeee-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="7eeee-113">Permissions</span></span>

<span data-ttu-id="7eeee-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7eeee-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7eeee-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7eeee-116">Permission type</span></span>                        | <span data-ttu-id="7eeee-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7eeee-117">Permissions (from least to most privileged)</span></span>                                                                                                          |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="7eeee-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7eeee-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="7eeee-119">~~User.Read y Group.Read.All~~, ~~User.ReadBasic.All y Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7eeee-119">~~User.Read and Group.Read.All~~, ~~User.ReadBasic.All and Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="7eeee-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7eeee-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7eeee-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7eeee-121">Not supported.</span></span>                                                                                                                                       |
| <span data-ttu-id="7eeee-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7eeee-122">Application</span></span>                            | <span data-ttu-id="7eeee-123">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7eeee-123">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span></span>                                                                                        |

> <span data-ttu-id="7eeee-124">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="7eeee-124">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="7eeee-125">Con el permiso Group.Read.All, solos o en combinación con un `User.` permiso, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="7eeee-125">Using the Group.Read.All permission, either alone or in combination with a `User.` permission, will return an error.</span></span> <span data-ttu-id="7eeee-126">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="7eeee-126">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="7eeee-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7eeee-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/getMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="7eeee-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7eeee-128">Request headers</span></span>

| <span data-ttu-id="7eeee-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7eeee-129">Header</span></span>        | <span data-ttu-id="7eeee-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7eeee-130">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="7eeee-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="7eeee-131">Authorization</span></span> | <span data-ttu-id="7eeee-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7eeee-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7eeee-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7eeee-134">Content-Type</span></span>  | <span data-ttu-id="7eeee-135">application/json</span><span class="sxs-lookup"><span data-stu-id="7eeee-135">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="7eeee-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7eeee-136">Request body</span></span>

<span data-ttu-id="7eeee-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7eeee-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7eeee-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7eeee-138">Parameter</span></span>           | <span data-ttu-id="7eeee-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="7eeee-139">Type</span></span>    | <span data-ttu-id="7eeee-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="7eeee-140">Description</span></span>                                                                                                                                                                                                                                                                         |
| :------------------ | :------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="7eeee-141">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="7eeee-141">securityEnabledOnly</span></span> | <span data-ttu-id="7eeee-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="7eeee-142">Boolean</span></span> | <span data-ttu-id="7eeee-p108">**true** para especificar que solo se deben devolver los grupos de seguridad de los que el usuario es miembro; **false** para especificar que se deben devolver todos los grupos de los que el usuario es miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="7eeee-p108">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span> |

## <a name="response"></a><span data-ttu-id="7eeee-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7eeee-145">Response</span></span>

<span data-ttu-id="7eeee-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="7eeee-146">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="7eeee-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7eeee-147">Example</span></span>

<span data-ttu-id="7eeee-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7eeee-148">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="7eeee-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7eeee-149">Request</span></span>

<span data-ttu-id="7eeee-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7eeee-150">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_getmembergroups"
}-->

```http
POST https://graph.microsoft.com/beta/me/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="7eeee-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7eeee-151">Response</span></span>

<span data-ttu-id="7eeee-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7eeee-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
