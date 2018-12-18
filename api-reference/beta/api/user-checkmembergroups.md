---
title: checkMemberGroups
description: Comprueba la pertenencia a en la lista especificada de grupos. Devuelve desde la lista de los grupos de los cuales
author: dkershaw10
ms.openlocfilehash: 613faacdbd2651700f264cdf89ec396b54752b76
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310601"
---
# <a name="checkmembergroups"></a><span data-ttu-id="bfacb-104">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="bfacb-104">checkMemberGroups</span></span>

> <span data-ttu-id="bfacb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bfacb-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bfacb-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bfacb-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bfacb-p103">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="bfacb-p103">Check for membership in the specified list of groups. Returns from the list those groups of which the user has a direct or transitive membership.</span></span>

<span data-ttu-id="bfacb-p104">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="bfacb-p104">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="bfacb-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="bfacb-113">Permissions</span></span>

<span data-ttu-id="bfacb-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bfacb-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bfacb-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bfacb-116">Permission type</span></span>                        | <span data-ttu-id="bfacb-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bfacb-117">Permissions (from least to most privileged)</span></span>                                                                        |
| :------------------------------------- | :----------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="bfacb-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bfacb-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="bfacb-119">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bfacb-119">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="bfacb-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bfacb-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bfacb-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfacb-121">Not supported.</span></span>                                                                                                     |
| <span data-ttu-id="bfacb-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bfacb-122">Application</span></span>                            | <span data-ttu-id="bfacb-123">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bfacb-123">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All</span></span>                             |

> <span data-ttu-id="bfacb-124">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="bfacb-124">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="bfacb-125">Uso de la `User.Read.All` o `User.ReadWrite.All` permisos devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="bfacb-125">Using the `User.Read.All` or `User.ReadWrite.All` permissions will return an error.</span></span> <span data-ttu-id="bfacb-126">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="bfacb-126">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="bfacb-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfacb-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="bfacb-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfacb-128">Request headers</span></span>

| <span data-ttu-id="bfacb-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfacb-129">Header</span></span>        | <span data-ttu-id="bfacb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="bfacb-130">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="bfacb-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="bfacb-131">Authorization</span></span> | <span data-ttu-id="bfacb-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfacb-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bfacb-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bfacb-134">Content-Type</span></span>  | <span data-ttu-id="bfacb-135">application/json</span><span class="sxs-lookup"><span data-stu-id="bfacb-135">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="bfacb-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfacb-136">Request body</span></span>

<span data-ttu-id="bfacb-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="bfacb-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bfacb-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bfacb-138">Parameter</span></span> | <span data-ttu-id="bfacb-139">Type</span><span class="sxs-lookup"><span data-stu-id="bfacb-139">Type</span></span>   | <span data-ttu-id="bfacb-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfacb-140">Description</span></span>           |
| :-------- | :----- | :-------------------- |
| <span data-ttu-id="bfacb-141">groupIds</span><span class="sxs-lookup"><span data-stu-id="bfacb-141">groupIds</span></span>  | <span data-ttu-id="bfacb-142">String</span><span class="sxs-lookup"><span data-stu-id="bfacb-142">String</span></span> | <span data-ttu-id="bfacb-143">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="bfacb-143">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="bfacb-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfacb-144">Response</span></span>

<span data-ttu-id="bfacb-145">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfacb-145">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bfacb-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfacb-146">Example</span></span>

<span data-ttu-id="bfacb-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bfacb-147">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="bfacb-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfacb-148">Request</span></span>

<span data-ttu-id="bfacb-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfacb-149">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_checkmembergroups"
}-->

```http
POST https://graph.microsoft.com/beta/me/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="bfacb-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfacb-150">Response</span></span>

<span data-ttu-id="bfacb-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bfacb-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
