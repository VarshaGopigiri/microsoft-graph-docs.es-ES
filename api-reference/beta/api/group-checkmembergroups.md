---
title: 'group: checkMemberGroups'
description: Comprueba la pertenencia a en la lista especificada de grupos. Devuelve desde la lista de los grupos de los cuales
ms.openlocfilehash: d591c4383971155a835d5d6456cdcd3a63803c92
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086526"
---
# <a name="group-checkmembergroups"></a><span data-ttu-id="fd5ce-104">group: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="fd5ce-104">group: checkMemberGroups</span></span>

> <span data-ttu-id="fd5ce-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd5ce-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fd5ce-p103">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-p103">Check for membership in the specified list of groups. Returns from the list those groups of which the specified group has a direct or transitive membership.</span></span>

<span data-ttu-id="fd5ce-p104">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-p104">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="fd5ce-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="fd5ce-113">Permissions</span></span>

<span data-ttu-id="fd5ce-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fd5ce-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="fd5ce-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd5ce-116">Permission type</span></span>                        | <span data-ttu-id="fd5ce-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd5ce-117">Permissions (from least to most privileged)</span></span>                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| <span data-ttu-id="fd5ce-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd5ce-118">Delegated (work or school account)</span></span>     | <span data-ttu-id="fd5ce-119">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="fd5ce-119">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="fd5ce-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd5ce-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fd5ce-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-121">Not supported.</span></span>                                                                              |
| <span data-ttu-id="fd5ce-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd5ce-122">Application</span></span>                            | <span data-ttu-id="fd5ce-123">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fd5ce-123">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All</span></span>                             |

> <span data-ttu-id="fd5ce-124">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-124">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="fd5ce-125">Uso de la `Group.Read.All` permiso devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-125">Using the `Group.Read.All` permission will return an error.</span></span> <span data-ttu-id="fd5ce-126">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-126">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="fd5ce-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd5ce-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="fd5ce-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fd5ce-128">Request headers</span></span>

| <span data-ttu-id="fd5ce-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="fd5ce-129">Name</span></span>          | <span data-ttu-id="fd5ce-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd5ce-130">Type</span></span>   | <span data-ttu-id="fd5ce-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd5ce-131">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="fd5ce-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="fd5ce-132">Authorization</span></span> | <span data-ttu-id="fd5ce-133">string</span><span class="sxs-lookup"><span data-stu-id="fd5ce-133">string</span></span> | <span data-ttu-id="fd5ce-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-p107">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fd5ce-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd5ce-136">Request body</span></span>

<span data-ttu-id="fd5ce-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="fd5ce-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fd5ce-138">Parameter</span></span> | <span data-ttu-id="fd5ce-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd5ce-139">Type</span></span>   | <span data-ttu-id="fd5ce-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd5ce-140">Description</span></span>           |
| :-------- | :----- | :-------------------- |
| <span data-ttu-id="fd5ce-141">groupIds</span><span class="sxs-lookup"><span data-stu-id="fd5ce-141">groupIds</span></span>  | <span data-ttu-id="fd5ce-142">String</span><span class="sxs-lookup"><span data-stu-id="fd5ce-142">String</span></span> | <span data-ttu-id="fd5ce-143">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="fd5ce-143">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="fd5ce-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd5ce-144">Response</span></span>

<span data-ttu-id="fd5ce-145">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-145">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fd5ce-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd5ce-146">Example</span></span>

<span data-ttu-id="fd5ce-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-147">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="fd5ce-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd5ce-148">Request</span></span>

<span data-ttu-id="fd5ce-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-149">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "group_checkmembergroups"
}-->

```http
POST https://graph.microsoft.com/beta/groups/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="fd5ce-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd5ce-150">Response</span></span>

<span data-ttu-id="fd5ce-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
  "description": "group: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->