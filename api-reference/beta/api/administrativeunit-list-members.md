---
title: Enumerar miembros
description: Utilice esta API para obtener los miembros de lista (de usuario y de grupo) en una unidad administrativa.
ms.openlocfilehash: c2d86992ccffd9d0ec4df90f5209ed5d6881ed16
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085964"
---
# <a name="list-members"></a><span data-ttu-id="62973-103">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="62973-103">List members</span></span>

> <span data-ttu-id="62973-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="62973-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="62973-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="62973-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="62973-106">Utilice esta API para obtener los miembros de lista (de usuario y de grupo) en una unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="62973-106">Use this API to get the members list (user and group) in an administrative unit.</span></span>

## <a name="permissions"></a><span data-ttu-id="62973-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="62973-107">Permissions</span></span>
<span data-ttu-id="62973-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62973-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="62973-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62973-110">Permission type</span></span>      | <span data-ttu-id="62973-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62973-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="62973-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62973-112">Delegated (work or school account)</span></span> | <span data-ttu-id="62973-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="62973-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="62973-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62973-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="62973-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62973-115">Not supported.</span></span>    |
|<span data-ttu-id="62973-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62973-116">Application</span></span> | <span data-ttu-id="62973-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="62973-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="62973-118">Nota: Para obtener una lista de los miembros de una pertenencia oculta en una unidad administrativa, es necesario el permiso Member.Read.Hidden.</span><span class="sxs-lookup"><span data-stu-id="62973-118">Note: To list the members of a hidden membership in an administrative unit, the Member.Read.Hidden permission is required.</span></span>

## <a name="http-request"></a><span data-ttu-id="62973-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62973-119">HTTP request</span></span>

```http
GET /administrativeUnits/{id}/members
GET /administrativeUnits/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="62973-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62973-120">Request headers</span></span>
| <span data-ttu-id="62973-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="62973-121">Name</span></span>      |<span data-ttu-id="62973-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="62973-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="62973-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="62973-123">Authorization</span></span>  | <span data-ttu-id="62973-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="62973-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="62973-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62973-126">Request body</span></span>
<span data-ttu-id="62973-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="62973-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="62973-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62973-128">Response</span></span>

<span data-ttu-id="62973-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [usuario](../resources/user.md) o [grupo](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62973-129">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/user.md) and/or [group](../resources/group.md) objects in the response body.</span></span>  <span data-ttu-id="62973-130">En su lugar, si coloca `$ref` al final de la solicitud, la respuesta contendrá una colección de `@odata.id` vínculos y direcciones URL a los miembros.</span><span class="sxs-lookup"><span data-stu-id="62973-130">Instead, if you put `$ref` at the end of the request, the response will contain a collection of `@odata.id` links/URLs to the members.</span></span>

## <a name="examples"></a><span data-ttu-id="62973-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="62973-131">Examples</span></span>
##### <a name="list-member-objects"></a><span data-ttu-id="62973-132">Objetos de lista de miembros</span><span class="sxs-lookup"><span data-stu-id="62973-132">List member objects</span></span>
<span data-ttu-id="62973-133">La solicitud siguiente enumeran a los miembros de la unidad administrativa, devuelve una colección de usuarios o grupos.</span><span class="sxs-lookup"><span data-stu-id="62973-133">The following request will list the members of the administrative unit, returning a collection of users and/or groups.</span></span>

```http
GET https://graph.microsoft.com/beta/administrativeUnits/{id}/members
```

<span data-ttu-id="62973-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62973-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
 
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "value":[
    {
      "@odata.type":"#microsoft.graph.user",
      "id":"492c5308-59fd-4740-9c83-4b3db07a6d70"
      "accountEnabled":true,
      "businessPhones":[],
      "companyName":null,
      "displayName":"Demo User"
    },
    {
      "@odata.type":"#microsoft.graph.group",
      "id":"07eaa5c7-c9b6-45cf-8ff7-3147d5122caa",
      "description":"This group is the best ever",
      "displayName":"Awesome group"
    }
  ]
}
```

##### <a name="list-member-references"></a><span data-ttu-id="62973-137">Referencias de miembro de lista</span><span class="sxs-lookup"><span data-stu-id="62973-137">List member references</span></span>
<span data-ttu-id="62973-138">La siguiente solicitud mostrará una lista de las referencias de miembro de la unidad administrativa, devuelve una colección de `@odata.id` referencias a los miembros.</span><span class="sxs-lookup"><span data-stu-id="62973-138">The following request will list the member references of the administrative unit, returning a collection of `@odata.id` references to the members.</span></span>
```
GET https://graph.microsoft.com/beta/administrativeUnits/{id}/members/$ref
```
<span data-ttu-id="62973-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62973-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
 
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "value":[
    {
      "@odata.id": "https://graph.microsoft.com/beta/directoryObjects/492c5308-59fd-4740-9c83-4b3db07a6d70"
    },
    {
      "@odata.id": "https://graph.microsoft.com/beta/directoryObjects/07eaa5c7-c9b6-45cf-8ff7-3147d5122caa"
    }
  ]
}
```