---
title: 'group: checkMemberGroups'
description: Comprueba la pertenencia a en la lista especificada de grupos. Devuelve desde la lista de los grupos de los cuales
author: dkershaw10
localization_priority: Priority
ms.prod: groups
ms.openlocfilehash: 8abac44bf6c97e0ebbd8235ec246f19f0c73e920
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932122"
---
# <a name="group-checkmembergroups"></a><span data-ttu-id="a2e4d-104">group: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="a2e4d-104">group: checkMemberGroups</span></span>

<span data-ttu-id="a2e4d-p102">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-p102">Check for membership in the specified list of groups. Returns from the list those groups of which the specified group has a direct or transitive membership.</span></span>

<span data-ttu-id="a2e4d-p103">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-p103">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="a2e4d-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2e4d-111">Permissions</span></span>

<span data-ttu-id="a2e4d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2e4d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a2e4d-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2e4d-114">Permission type</span></span>                        | <span data-ttu-id="a2e4d-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2e4d-115">Permissions (from least to most privileged)</span></span>                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| <span data-ttu-id="a2e4d-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2e4d-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="a2e4d-117">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a2e4d-117">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="a2e4d-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2e4d-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2e4d-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-119">Not supported.</span></span>                                                                              |
| <span data-ttu-id="a2e4d-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2e4d-120">Application</span></span>                            | <span data-ttu-id="a2e4d-121">_Group.Read.All_, Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-121">_Group.Read.All_, Directory.Read.All.</span></span> <span data-ttu-id="a2e4d-122">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2e4d-122">Directory.ReadWrite.All</span></span>                               |

> <span data-ttu-id="a2e4d-123">**Nota:** Esta API requiere actualmente el `Directory.Read.All` permiso o superior.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-123">**Note:** This API currently requires the `Directory.Read.All` permission or higher.</span></span> <span data-ttu-id="a2e4d-124">Uso de la `Group.Read.All` permiso devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-124">Using the `Group.Read.All` permission will return an error.</span></span> <span data-ttu-id="a2e4d-125">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-125">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="a2e4d-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2e4d-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="a2e4d-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2e4d-127">Request headers</span></span>

| <span data-ttu-id="a2e4d-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2e4d-128">Name</span></span>          | <span data-ttu-id="a2e4d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2e4d-129">Type</span></span>   | <span data-ttu-id="a2e4d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2e4d-130">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="a2e4d-131">Autorización</span><span class="sxs-lookup"><span data-stu-id="a2e4d-131">Authorization</span></span> | <span data-ttu-id="a2e4d-132">string</span><span class="sxs-lookup"><span data-stu-id="a2e4d-132">string</span></span> | <span data-ttu-id="a2e4d-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-p107">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a2e4d-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2e4d-135">Request body</span></span>

<span data-ttu-id="a2e4d-136">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-136">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a2e4d-137">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a2e4d-137">Parameter</span></span> | <span data-ttu-id="a2e4d-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2e4d-138">Type</span></span>              | <span data-ttu-id="a2e4d-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2e4d-139">Description</span></span>           |
| :-------- | :---------------- | :-------------------- |
| <span data-ttu-id="a2e4d-140">groupIds</span><span class="sxs-lookup"><span data-stu-id="a2e4d-140">groupIds</span></span>  | <span data-ttu-id="a2e4d-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="a2e4d-141">String collection</span></span> | <span data-ttu-id="a2e4d-142">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="a2e4d-142">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="a2e4d-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2e4d-143">Response</span></span>

<span data-ttu-id="a2e4d-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-144">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2e4d-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2e4d-145">Example</span></span>

<span data-ttu-id="a2e4d-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-146">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="a2e4d-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2e4d-147">Request</span></span>

<span data-ttu-id="a2e4d-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-148">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "group_checkmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/groups/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="a2e4d-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2e4d-149">Response</span></span>

<span data-ttu-id="a2e4d-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2e4d-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
