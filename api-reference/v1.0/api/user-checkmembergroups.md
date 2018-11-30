---
title: checkMemberGroups
description: Comprueba la pertenencia a en la lista especificada de grupos. Devuelve desde la lista de los grupos de los cuales
ms.openlocfilehash: 78e34be05c1abd5962b1077a2a4c646867cdf5f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029349"
---
# <a name="checkmembergroups"></a><span data-ttu-id="cf5b6-104">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="cf5b6-104">checkMemberGroups</span></span>

<span data-ttu-id="cf5b6-p102">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-p102">Check for membership in the specified list of groups. Returns from the list those groups of which the user has a direct or transitive membership.</span></span>

<span data-ttu-id="cf5b6-p103">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-p103">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="cf5b6-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="cf5b6-111">Permissions</span></span>

<span data-ttu-id="cf5b6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf5b6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="cf5b6-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf5b6-114">Permission type</span></span>                        | <span data-ttu-id="cf5b6-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf5b6-115">Permissions (from least to most privileged)</span></span>                                                                        |
| :------------------------------------- | :----------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="cf5b6-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf5b6-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="cf5b6-117">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cf5b6-117">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="cf5b6-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf5b6-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cf5b6-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-119">Not supported.</span></span>                                                                                                     |
| <span data-ttu-id="cf5b6-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf5b6-120">Application</span></span>                            | <span data-ttu-id="cf5b6-121">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf5b6-121">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All</span></span>                             |

> <span data-ttu-id="cf5b6-122">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-122">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="cf5b6-123">Uso de la `User.Read.All` o `User.ReadWrite.All` permisos devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-123">Using the `User.Read.All` or `User.ReadWrite.All` permissions will return an error.</span></span> <span data-ttu-id="cf5b6-124">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-124">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="cf5b6-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf5b6-125">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="cf5b6-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf5b6-126">Request headers</span></span>

| <span data-ttu-id="cf5b6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf5b6-127">Header</span></span>        | <span data-ttu-id="cf5b6-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cf5b6-128">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="cf5b6-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf5b6-129">Authorization</span></span> | <span data-ttu-id="cf5b6-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cf5b6-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cf5b6-132">Content-Type</span></span>  | <span data-ttu-id="cf5b6-133">application/json</span><span class="sxs-lookup"><span data-stu-id="cf5b6-133">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="cf5b6-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf5b6-134">Request body</span></span>

<span data-ttu-id="cf5b6-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="cf5b6-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cf5b6-136">Parameter</span></span> | <span data-ttu-id="cf5b6-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf5b6-137">Type</span></span>              | <span data-ttu-id="cf5b6-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf5b6-138">Description</span></span>           |
| :-------- | :---------------- | :-------------------- |
| <span data-ttu-id="cf5b6-139">groupIds</span><span class="sxs-lookup"><span data-stu-id="cf5b6-139">groupIds</span></span>  | <span data-ttu-id="cf5b6-140">Colección String</span><span class="sxs-lookup"><span data-stu-id="cf5b6-140">String collection</span></span> | <span data-ttu-id="cf5b6-141">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="cf5b6-141">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="cf5b6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf5b6-142">Response</span></span>

<span data-ttu-id="cf5b6-143">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-143">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf5b6-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf5b6-144">Example</span></span>

<span data-ttu-id="cf5b6-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-145">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="cf5b6-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf5b6-146">Request</span></span>

<span data-ttu-id="cf5b6-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-147">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_checkmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="cf5b6-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf5b6-148">Response</span></span>

<span data-ttu-id="cf5b6-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf5b6-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
  "description": "user: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->