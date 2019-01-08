---
title: Lista grupo transitivas (miembros de)
description: Obtener una lista de los miembros del grupo. Un grupo puede tener los usuarios, contactos, dispositivos, entidades de seguridad de servicio y otros grupos como miembros. Esta operación es transitiva y también devolverá una lista plana de todos los miembros anidados.
ms.openlocfilehash: 703515f4549e409d3711699c79671ed0b1a93cb3
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748559"
---
# <a name="list-group-transitive-members"></a><span data-ttu-id="6e9f2-105">Lista grupo transitivas (miembros de)</span><span class="sxs-lookup"><span data-stu-id="6e9f2-105">List group transitive members</span></span>

> <span data-ttu-id="6e9f2-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e9f2-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6e9f2-108">Obtener una lista de los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-108">Get a list of the group's members.</span></span> <span data-ttu-id="6e9f2-109">Un grupo puede tener los usuarios, contactos, dispositivos, entidades de seguridad de servicio y otros grupos como miembros.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-109">A group can have users, contacts, devices, service principals and other groups as members.</span></span> <span data-ttu-id="6e9f2-110">Esta operación es transitiva y también devolverá una lista plana de todos los miembros anidados.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-110">This operation is transitive and will also return a flat list of all nested members.</span></span>

## <a name="permissions"></a><span data-ttu-id="6e9f2-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="6e9f2-111">Permissions</span></span>

<span data-ttu-id="6e9f2-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e9f2-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e9f2-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e9f2-114">Permission type</span></span>      | <span data-ttu-id="6e9f2-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e9f2-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6e9f2-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e9f2-116">Delegated (work or school account)</span></span> | <span data-ttu-id="6e9f2-117">Directory.Read.All, Directory.AccessAsUser.All, User.ReadBasic.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="6e9f2-117">Directory.Read.All, Directory.AccessAsUser.All, User.ReadBasic.All, User.Read.All</span></span>    |
|<span data-ttu-id="6e9f2-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e9f2-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6e9f2-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-119">Not supported.</span></span>    |
|<span data-ttu-id="6e9f2-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e9f2-120">Application</span></span> | <span data-ttu-id="6e9f2-121">Directory.Read.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="6e9f2-121">Directory.Read.All, User.Read.All</span></span> |

> <span data-ttu-id="6e9f2-122">Nota: Para obtener una lista de los miembros de un grupo de pertenencia oculta, se requiere el permiso Member.Read.Hidden.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-122">Note: To list the members of a hidden membership group, the Member.Read.Hidden permission is required.</span></span>

## <a name="http-request"></a><span data-ttu-id="6e9f2-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e9f2-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /groups/{id}/transitiveMembers
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6e9f2-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6e9f2-124">Optional query parameters</span></span>

<span data-ttu-id="6e9f2-125">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-125">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6e9f2-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e9f2-126">Request headers</span></span>

| <span data-ttu-id="6e9f2-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="6e9f2-127">Name</span></span>       | <span data-ttu-id="6e9f2-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e9f2-128">Type</span></span> | <span data-ttu-id="6e9f2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e9f2-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6e9f2-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e9f2-130">Authorization</span></span>  | <span data-ttu-id="6e9f2-131">string</span><span class="sxs-lookup"><span data-stu-id="6e9f2-131">string</span></span>  | <span data-ttu-id="6e9f2-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6e9f2-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e9f2-134">Request body</span></span>

<span data-ttu-id="6e9f2-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6e9f2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e9f2-136">Response</span></span>

<span data-ttu-id="6e9f2-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-137">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6e9f2-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e9f2-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="6e9f2-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e9f2-139">Request</span></span>

<span data-ttu-id="6e9f2-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-140">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_transitivemembers"
}-->

```http
GET https://graph.microsoft.com/beta/groups/{id}/transitiveMembers
```

### <a name="response"></a><span data-ttu-id="6e9f2-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e9f2-141">Response</span></span>

<span data-ttu-id="6e9f2-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-142">The following is an example of the response.</span></span>
><span data-ttu-id="6e9f2-143">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="6e9f2-144">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e9f2-144">All the properties will be returned from an actual call.</span></span>
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
  "description": "List transitive group members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
