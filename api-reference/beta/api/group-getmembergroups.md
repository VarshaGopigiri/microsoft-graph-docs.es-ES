---
title: 'grupo: getMemberGroups'
description: Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación memberOf, que devuelve solo los grupos de los que el grupo es miembro directo.
localization_priority: Normal
ms.openlocfilehash: 0c5162e79921e6069d22861060e6c652d1a7de3f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887210"
---
# <a name="group-getmembergroups"></a><span data-ttu-id="e7bbf-104">grupo: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="e7bbf-104">group: getMemberGroups</span></span>

> <span data-ttu-id="e7bbf-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7bbf-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e7bbf-p103">Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/group-list-memberof.md), que devuelve solo los grupos de los que el grupo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-p103">Return all the groups that the specified group is a member of. The check is transitive, unlike reading the [memberOf](../api/group-list-memberof.md) navigation property, which returns only the groups that the group is a direct member of.</span></span>

<span data-ttu-id="e7bbf-p104">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-p104">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="e7bbf-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="e7bbf-113">Permissions</span></span>

<span data-ttu-id="e7bbf-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7bbf-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e7bbf-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7bbf-116">Permission type</span></span>                        | <span data-ttu-id="e7bbf-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7bbf-117">Permissions (from least to most privileged)</span></span>                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| <span data-ttu-id="e7bbf-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7bbf-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="e7bbf-119">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e7bbf-119">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="e7bbf-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7bbf-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e7bbf-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-121">Not supported.</span></span>                                                                              |
| <span data-ttu-id="e7bbf-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7bbf-122">Application</span></span>                            | <span data-ttu-id="e7bbf-123">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7bbf-123">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All</span></span>                             |

> <span data-ttu-id="e7bbf-124">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-124">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="e7bbf-125">Uso de la `Group.Read.All` permiso devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-125">Using the `Group.Read.All` permission will return an error.</span></span> <span data-ttu-id="e7bbf-126">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-126">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="e7bbf-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7bbf-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/getMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="e7bbf-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7bbf-128">Request headers</span></span>

| <span data-ttu-id="e7bbf-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="e7bbf-129">Name</span></span>          | <span data-ttu-id="e7bbf-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7bbf-130">Type</span></span>   | <span data-ttu-id="e7bbf-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7bbf-131">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="e7bbf-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="e7bbf-132">Authorization</span></span> | <span data-ttu-id="e7bbf-133">string</span><span class="sxs-lookup"><span data-stu-id="e7bbf-133">string</span></span> | <span data-ttu-id="e7bbf-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-p107">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e7bbf-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7bbf-136">Request body</span></span>

<span data-ttu-id="e7bbf-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e7bbf-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e7bbf-138">Parameter</span></span>           | <span data-ttu-id="e7bbf-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7bbf-139">Type</span></span>    | <span data-ttu-id="e7bbf-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7bbf-140">Description</span></span>                                                                           |
| :------------------ | :------ | :------------------------------------------------------------------------------------ |
| <span data-ttu-id="e7bbf-141">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="e7bbf-141">securityEnabledOnly</span></span> | <span data-ttu-id="e7bbf-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="e7bbf-142">Boolean</span></span> | <span data-ttu-id="e7bbf-p108">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-p108">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span> |

## <a name="response"></a><span data-ttu-id="e7bbf-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7bbf-145">Response</span></span>

<span data-ttu-id="e7bbf-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-146">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="e7bbf-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7bbf-147">Example</span></span>

#### <a name="request"></a><span data-ttu-id="e7bbf-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7bbf-148">Request</span></span>

<span data-ttu-id="e7bbf-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-149">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "group_getmembergroups"
}-->

```http
POST https://graph.microsoft.com/beta/groups/{id}/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a><span data-ttu-id="e7bbf-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7bbf-150">Response</span></span>

<span data-ttu-id="e7bbf-151">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-151">The following is an example of the response.</span></span>

> <span data-ttu-id="e7bbf-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7bbf-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
