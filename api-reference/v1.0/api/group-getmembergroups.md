---
title: 'grupo: getMemberGroups'
description: Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación memberOf, que devuelve solo los grupos de los que el grupo es miembro directo.
localization_priority: Priority
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 578caa1660ee86f24483cff9143a9153ca448526
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934285"
---
# <a name="group-getmembergroups"></a><span data-ttu-id="b943c-104">grupo: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="b943c-104">group: getMemberGroups</span></span>

<span data-ttu-id="b943c-p102">Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/group-list-memberof.md), que devuelve solo los grupos de los que el grupo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="b943c-p102">Return all the groups that the specified group is a member of. The check is transitive, unlike reading the [memberOf](../api/group-list-memberof.md) navigation property, which returns only the groups that the group is a direct member of.</span></span>

<span data-ttu-id="b943c-p103">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="b943c-p103">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="b943c-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="b943c-111">Permissions</span></span>

<span data-ttu-id="b943c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b943c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b943c-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b943c-114">Permission type</span></span>                        | <span data-ttu-id="b943c-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b943c-115">Permissions (from least to most privileged)</span></span>                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| <span data-ttu-id="b943c-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b943c-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="b943c-117">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b943c-117">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="b943c-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b943c-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b943c-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b943c-119">Not supported.</span></span>                                                                              |
| <span data-ttu-id="b943c-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b943c-120">Application</span></span>                            | <span data-ttu-id="b943c-121">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b943c-121">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All</span></span>                             |

> <span data-ttu-id="b943c-122">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="b943c-122">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="b943c-123">Uso de la `Group.Read.All` permiso devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="b943c-123">Using the `Group.Read.All` permission will return an error.</span></span> <span data-ttu-id="b943c-124">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="b943c-124">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="b943c-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b943c-125">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/getMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="b943c-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b943c-126">Request headers</span></span>

| <span data-ttu-id="b943c-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="b943c-127">Name</span></span>          | <span data-ttu-id="b943c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="b943c-128">Type</span></span>   | <span data-ttu-id="b943c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="b943c-129">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="b943c-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="b943c-130">Authorization</span></span> | <span data-ttu-id="b943c-131">string</span><span class="sxs-lookup"><span data-stu-id="b943c-131">string</span></span> | <span data-ttu-id="b943c-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b943c-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b943c-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b943c-134">Request body</span></span>

<span data-ttu-id="b943c-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b943c-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b943c-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b943c-136">Parameter</span></span>           | <span data-ttu-id="b943c-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="b943c-137">Type</span></span>    | <span data-ttu-id="b943c-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="b943c-138">Description</span></span>                                                                           |
| :------------------ | :------ | :------------------------------------------------------------------------------------ |
| <span data-ttu-id="b943c-139">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="b943c-139">securityEnabledOnly</span></span> | <span data-ttu-id="b943c-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="b943c-140">Boolean</span></span> | <span data-ttu-id="b943c-p107">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="b943c-p107">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span> |

## <a name="response"></a><span data-ttu-id="b943c-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b943c-143">Response</span></span>

<span data-ttu-id="b943c-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="b943c-144">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="b943c-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b943c-145">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b943c-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b943c-146">Request</span></span>

<span data-ttu-id="b943c-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b943c-147">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "group_getmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/groups/{id}/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a><span data-ttu-id="b943c-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b943c-148">Response</span></span>

<span data-ttu-id="b943c-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b943c-149">The following is an example of the response.</span></span>

> <span data-ttu-id="b943c-150">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b943c-150">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="b943c-151">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b943c-151">All the properties will be returned from an actual call.</span></span>

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
  "description": "group: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
