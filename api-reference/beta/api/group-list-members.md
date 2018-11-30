---
title: Lista de miembros de grupo
description: Obtener una lista de los miembros del grupo directa. Un grupo puede tener los usuarios, contactos, dispositivos, entidades de seguridad de servicio y otros grupos como miembros. Esta operación no es transitiva.
ms.openlocfilehash: 788939d2b81e7e5667b3a6164c7e44b83ce63a3e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083927"
---
# <a name="list-group-members"></a><span data-ttu-id="68a19-105">Lista de miembros de grupo</span><span class="sxs-lookup"><span data-stu-id="68a19-105">List group members</span></span>

> <span data-ttu-id="68a19-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="68a19-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="68a19-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="68a19-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="68a19-108">Obtener una lista de los miembros del grupo directa.</span><span class="sxs-lookup"><span data-stu-id="68a19-108">Get a list of the group's direct members.</span></span> <span data-ttu-id="68a19-109">Un grupo puede tener los usuarios, contactos, dispositivos, entidades de seguridad de servicio y otros grupos como miembros.</span><span class="sxs-lookup"><span data-stu-id="68a19-109">A group can have users, contacts, devices, service principals, and other groups as members.</span></span> <span data-ttu-id="68a19-110">Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="68a19-110">This operation is not transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="68a19-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="68a19-111">Permissions</span></span>

<span data-ttu-id="68a19-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68a19-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="68a19-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68a19-114">Permission type</span></span>      | <span data-ttu-id="68a19-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68a19-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="68a19-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68a19-116">Delegated (work or school account)</span></span> | <span data-ttu-id="68a19-117">Directory.Read.All, Directory.AccessAsUser.All, User.ReadBasic.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="68a19-117">Directory.Read.All, Directory.AccessAsUser.All, User.ReadBasic.All, User.Read.All</span></span>    |
|<span data-ttu-id="68a19-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68a19-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="68a19-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68a19-119">Not supported.</span></span>    |
|<span data-ttu-id="68a19-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68a19-120">Application</span></span> | <span data-ttu-id="68a19-121">Directory.Read.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="68a19-121">Directory.Read.All, User.Read.All</span></span> |

> <span data-ttu-id="68a19-122">Nota: Para obtener una lista de los miembros de un grupo de pertenencia oculta, se requiere el permiso Member.Read.Hidden.</span><span class="sxs-lookup"><span data-stu-id="68a19-122">Note: To list the members of a hidden membership group, the Member.Read.Hidden permission is required.</span></span>
 
## <a name="http-request"></a><span data-ttu-id="68a19-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68a19-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/members
```

## <a name="optional-query-parameters"></a><span data-ttu-id="68a19-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="68a19-124">Optional query parameters</span></span>
<span data-ttu-id="68a19-125">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68a19-125">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="68a19-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68a19-126">Request headers</span></span>
| <span data-ttu-id="68a19-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="68a19-127">Name</span></span>       | <span data-ttu-id="68a19-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="68a19-128">Type</span></span> | <span data-ttu-id="68a19-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="68a19-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="68a19-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="68a19-130">Authorization</span></span>  | <span data-ttu-id="68a19-131">string</span><span class="sxs-lookup"><span data-stu-id="68a19-131">string</span></span>  | <span data-ttu-id="68a19-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68a19-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="68a19-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68a19-134">Request body</span></span>
<span data-ttu-id="68a19-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68a19-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="68a19-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68a19-136">Response</span></span>
<span data-ttu-id="68a19-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68a19-137">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68a19-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68a19-138">Example</span></span>
#### <a name="request"></a><span data-ttu-id="68a19-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68a19-139">Request</span></span>
<span data-ttu-id="68a19-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68a19-140">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_members"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/members
```

#### <a name="response"></a><span data-ttu-id="68a19-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68a19-141">Response</span></span>
<span data-ttu-id="68a19-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68a19-142">The following is an example of the response.</span></span>
><span data-ttu-id="68a19-143">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="68a19-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="68a19-144">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68a19-144">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    "@odata.type": "#microsoft.graph.user",
    {
      "businessPhones": [
        "businessPhones-value"
      ],
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "jobTitle": "jobTitle-value",
      "mail": "mail-value",
      "mobilePhone": "mobilePhone-value",
      "officeLocation": "officeLocation-value",
      "preferredLanguage": "preferredLanguage-value",
      "surname": "surname-value",
      "userPrincipalName": "userPrincipalName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List group members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->