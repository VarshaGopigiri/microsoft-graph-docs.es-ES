---
title: 'usuario: getMemberGroups'
description: Devolver todos los grupos que el usuario es un miembro de. La comprobación es transitiva, a diferencia de lectura de la
localization_priority: Normal
ms.openlocfilehash: 097d6d6eafa031bf86460e97ced58d0063eee4ed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879789"
---
# <a name="user-getmembergroups"></a><span data-ttu-id="b195a-104">usuario: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="b195a-104">user: getMemberGroups</span></span>

> <span data-ttu-id="b195a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b195a-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b195a-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b195a-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b195a-p103">Devuelva todos los grupos de los que el usuario es miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/user-list-memberof.md), que devuelve solo los grupos de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="b195a-p103">Return all the groups that the user is a member of. The check is transitive, unlike reading the [memberOf](../api/user-list-memberof.md) navigation property, which returns only the groups that the user is a direct member of.</span></span>

<span data-ttu-id="b195a-p104">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="b195a-p104">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="b195a-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="b195a-113">Permissions</span></span>

<span data-ttu-id="b195a-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b195a-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b195a-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b195a-116">Permission type</span></span>                        | <span data-ttu-id="b195a-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b195a-117">Permissions (from least to most privileged)</span></span>                                                                                                          |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="b195a-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b195a-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="b195a-119">~~User.Read y Group.Read.All~~, ~~User.ReadBasic.All y Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b195a-119">~~User.Read and Group.Read.All~~, ~~User.ReadBasic.All and Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="b195a-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b195a-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b195a-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b195a-121">Not supported.</span></span>                                                                                                                                       |
| <span data-ttu-id="b195a-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b195a-122">Application</span></span>                            | <span data-ttu-id="b195a-123">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b195a-123">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span></span>                                                                                        |

> <span data-ttu-id="b195a-124">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="b195a-124">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="b195a-125">Con el permiso Group.Read.All, solos o en combinación con un `User.` permiso, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="b195a-125">Using the Group.Read.All permission, either alone or in combination with a `User.` permission, will return an error.</span></span> <span data-ttu-id="b195a-126">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="b195a-126">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="b195a-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b195a-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/getMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="b195a-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b195a-128">Request headers</span></span>

| <span data-ttu-id="b195a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b195a-129">Header</span></span>        | <span data-ttu-id="b195a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b195a-130">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="b195a-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="b195a-131">Authorization</span></span> | <span data-ttu-id="b195a-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b195a-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b195a-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b195a-134">Content-Type</span></span>  | <span data-ttu-id="b195a-135">application/json</span><span class="sxs-lookup"><span data-stu-id="b195a-135">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="b195a-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b195a-136">Request body</span></span>

<span data-ttu-id="b195a-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b195a-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b195a-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b195a-138">Parameter</span></span>           | <span data-ttu-id="b195a-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="b195a-139">Type</span></span>    | <span data-ttu-id="b195a-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="b195a-140">Description</span></span>                                                                                                                                                                                                                                                                         |
| :------------------ | :------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="b195a-141">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="b195a-141">securityEnabledOnly</span></span> | <span data-ttu-id="b195a-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="b195a-142">Boolean</span></span> | <span data-ttu-id="b195a-p108">**true** para especificar que solo se deben devolver los grupos de seguridad de los que el usuario es miembro; **false** para especificar que se deben devolver todos los grupos de los que el usuario es miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="b195a-p108">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span> |

## <a name="response"></a><span data-ttu-id="b195a-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b195a-145">Response</span></span>

<span data-ttu-id="b195a-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="b195a-146">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="b195a-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b195a-147">Example</span></span>

<span data-ttu-id="b195a-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b195a-148">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="b195a-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b195a-149">Request</span></span>

<span data-ttu-id="b195a-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b195a-150">Here is an example of the request.</span></span>

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

##### <a name="response"></a><span data-ttu-id="b195a-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b195a-151">Response</span></span>

<span data-ttu-id="b195a-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b195a-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
