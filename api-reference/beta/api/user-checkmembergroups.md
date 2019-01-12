---
title: checkMemberGroups
description: Comprueba la pertenencia a en la lista especificada de grupos. Devuelve desde la lista de los grupos de los cuales
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 18ae4e88eb9f80255ee8cda2ce0c353be9b28580
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923610"
---
# <a name="checkmembergroups"></a><span data-ttu-id="2f7cd-104">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="2f7cd-104">checkMemberGroups</span></span>

> <span data-ttu-id="2f7cd-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f7cd-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2f7cd-p103">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-p103">Check for membership in the specified list of groups. Returns from the list those groups of which the user has a direct or transitive membership.</span></span>

<span data-ttu-id="2f7cd-p104">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-p104">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="2f7cd-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="2f7cd-113">Permissions</span></span>

<span data-ttu-id="2f7cd-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2f7cd-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="2f7cd-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2f7cd-116">Permission type</span></span>                        | <span data-ttu-id="2f7cd-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2f7cd-117">Permissions (from least to most privileged)</span></span>                                                                        |
| :------------------------------------- | :----------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="2f7cd-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2f7cd-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="2f7cd-119">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2f7cd-119">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="2f7cd-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2f7cd-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2f7cd-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-121">Not supported.</span></span>                                                                                                     |
| <span data-ttu-id="2f7cd-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2f7cd-122">Application</span></span>                            | <span data-ttu-id="2f7cd-123">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2f7cd-123">~~User.Read.All~~, ~~User.ReadWrite.All~~, Directory.Read.All, Directory.ReadWrite.All</span></span>                             |

> <span data-ttu-id="2f7cd-124">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-124">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="2f7cd-125">Uso de la `User.Read.All` o `User.ReadWrite.All` permisos devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-125">Using the `User.Read.All` or `User.ReadWrite.All` permissions will return an error.</span></span> <span data-ttu-id="2f7cd-126">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-126">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="2f7cd-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f7cd-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="2f7cd-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f7cd-128">Request headers</span></span>

| <span data-ttu-id="2f7cd-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f7cd-129">Header</span></span>        | <span data-ttu-id="2f7cd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2f7cd-130">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="2f7cd-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="2f7cd-131">Authorization</span></span> | <span data-ttu-id="2f7cd-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2f7cd-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2f7cd-134">Content-Type</span></span>  | <span data-ttu-id="2f7cd-135">application/json</span><span class="sxs-lookup"><span data-stu-id="2f7cd-135">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="2f7cd-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2f7cd-136">Request body</span></span>

<span data-ttu-id="2f7cd-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2f7cd-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2f7cd-138">Parameter</span></span> | <span data-ttu-id="2f7cd-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f7cd-139">Type</span></span>   | <span data-ttu-id="2f7cd-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f7cd-140">Description</span></span>           |
| :-------- | :----- | :-------------------- |
| <span data-ttu-id="2f7cd-141">groupIds</span><span class="sxs-lookup"><span data-stu-id="2f7cd-141">groupIds</span></span>  | <span data-ttu-id="2f7cd-142">String</span><span class="sxs-lookup"><span data-stu-id="2f7cd-142">String</span></span> | <span data-ttu-id="2f7cd-143">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="2f7cd-143">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="2f7cd-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f7cd-144">Response</span></span>

<span data-ttu-id="2f7cd-145">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-145">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2f7cd-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f7cd-146">Example</span></span>

<span data-ttu-id="2f7cd-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-147">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="2f7cd-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f7cd-148">Request</span></span>

<span data-ttu-id="2f7cd-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-149">Here is an example of the request.</span></span>

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

##### <a name="response"></a><span data-ttu-id="2f7cd-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f7cd-150">Response</span></span>

<span data-ttu-id="2f7cd-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
