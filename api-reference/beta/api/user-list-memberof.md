---
title: Miembro de usuario de lista
description: Obtener grupos, roles de Active directory y unidades administrativas que el usuario es miembro directo. Esta operación no es transitiva.
ms.openlocfilehash: 0d22189f35e41798929c10d63219a5f5688c42c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087231"
---
# <a name="list-user-memberof"></a><span data-ttu-id="ffa90-104">Miembro de usuario de lista</span><span class="sxs-lookup"><span data-stu-id="ffa90-104">List user memberOf</span></span>

> <span data-ttu-id="ffa90-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffa90-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffa90-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffa90-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ffa90-107">Obtener grupos, roles de Active directory y unidades administrativas que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="ffa90-107">Get groups, directory roles and administrative units that the user is a direct member of.</span></span> <span data-ttu-id="ffa90-108">Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="ffa90-108">This operation is not transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="ffa90-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ffa90-109">Permissions</span></span>

<span data-ttu-id="ffa90-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ffa90-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ffa90-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ffa90-112">Permission type</span></span>      | <span data-ttu-id="ffa90-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ffa90-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ffa90-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ffa90-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ffa90-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ffa90-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ffa90-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ffa90-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ffa90-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffa90-117">Not supported.</span></span>    |
|<span data-ttu-id="ffa90-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ffa90-118">Application</span></span> | <span data-ttu-id="ffa90-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffa90-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ffa90-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ffa90-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/memberOf
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ffa90-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ffa90-121">Optional query parameters</span></span>

<span data-ttu-id="ffa90-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffa90-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ffa90-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ffa90-123">Request headers</span></span>
| <span data-ttu-id="ffa90-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffa90-124">Header</span></span>       | <span data-ttu-id="ffa90-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ffa90-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ffa90-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="ffa90-126">Authorization</span></span>  | <span data-ttu-id="ffa90-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffa90-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ffa90-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ffa90-129">Accept</span></span>  | <span data-ttu-id="ffa90-130">application/json</span><span class="sxs-lookup"><span data-stu-id="ffa90-130">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ffa90-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ffa90-131">Request body</span></span>

<span data-ttu-id="ffa90-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ffa90-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ffa90-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffa90-133">Response</span></span>

<span data-ttu-id="ffa90-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffa90-134">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ffa90-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffa90-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="ffa90-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ffa90-136">Request</span></span>

<span data-ttu-id="ffa90-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ffa90-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user_memberof"
}-->
```http
GET https://graph.microsoft.com/beta/me/memberOf
```

### <a name="response"></a><span data-ttu-id="ffa90-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffa90-138">Response</span></span>

<span data-ttu-id="ffa90-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ffa90-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "id-value",
      "createdDateTime": null,
      "description": "All users at the company",
      "displayName": "All Users",
      "groupTypes": [],
      "mailEnabled": false,
      "securityEnabled": true,
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->