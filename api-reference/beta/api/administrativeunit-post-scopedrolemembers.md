---
title: Agregar un scopedRoleMember
description: 'Agregar un nuevo scopedRoleMembership. Nota: Actualmente se admiten sólo los roles de *Administrador de la cuenta de usuario* y *Administrador de departamento de soporte técnico* para las pertenencias a funciones con ámbito.'
ms.openlocfilehash: bab8b1ba5d9093617f1aafb48d84f41badef2566
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084076"
---
# <a name="add-a-scopedrolemember"></a><span data-ttu-id="14d01-104">Agregar un scopedRoleMember</span><span class="sxs-lookup"><span data-stu-id="14d01-104">Add a scopedRoleMember</span></span>

> <span data-ttu-id="14d01-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14d01-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14d01-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14d01-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="14d01-107">Agregar un nuevo [scopedRoleMembership](../resources/scopedrolemembership.md).</span><span class="sxs-lookup"><span data-stu-id="14d01-107">Add a new [scopedRoleMembership](../resources/scopedrolemembership.md).</span></span> <span data-ttu-id="14d01-108">Nota: Actualmente se admiten sólo los roles de *Administrador de la cuenta de usuario* y *Administrador de departamento de soporte técnico* para las pertenencias a funciones con ámbito.</span><span class="sxs-lookup"><span data-stu-id="14d01-108">NOTE: Only the *User account administrator* and *Helpdesk administrator* roles are currently supported for scoped-role memberships.</span></span>

## <a name="permissions"></a><span data-ttu-id="14d01-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="14d01-109">Permissions</span></span>
<span data-ttu-id="14d01-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="14d01-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="14d01-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="14d01-112">Permission type</span></span>      | <span data-ttu-id="14d01-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="14d01-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="14d01-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="14d01-114">Delegated (work or school account)</span></span> | <span data-ttu-id="14d01-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="14d01-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="14d01-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14d01-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="14d01-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="14d01-117">Not supported.</span></span>    |
|<span data-ttu-id="14d01-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="14d01-118">Application</span></span> | <span data-ttu-id="14d01-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="14d01-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="14d01-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="14d01-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /administrativeUnits/{id}/scopedRoleMembers
```
## <a name="request-headers"></a><span data-ttu-id="14d01-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="14d01-121">Request headers</span></span>
| <span data-ttu-id="14d01-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="14d01-122">Name</span></span>      |<span data-ttu-id="14d01-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="14d01-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="14d01-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="14d01-124">Authorization</span></span>  | <span data-ttu-id="14d01-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="14d01-p105">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="14d01-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="14d01-127">Request body</span></span>
<span data-ttu-id="14d01-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [scopedRoleMembership](../resources/scopedrolemembership.md) .</span><span class="sxs-lookup"><span data-stu-id="14d01-128">In the request body, supply a JSON representation of [scopedRoleMembership](../resources/scopedrolemembership.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="14d01-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14d01-129">Response</span></span>

<span data-ttu-id="14d01-130">Si tiene éxito, este método devuelve `201 Created` objeto de código y [scopedRoleMembership](../resources/scopedrolemembership.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14d01-130">If successful, this method returns `201 Created` response code and [scopedRoleMembership](../resources/scopedrolemembership.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="14d01-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14d01-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="14d01-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="14d01-132">Request</span></span>
<span data-ttu-id="14d01-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="14d01-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_scopedrolemembership_from_administrativeunit"
}-->
```http
POST https://graph.microsoft.com/beta/administrativeUnits/{id}/scopedRoleMembers
Content-type: application/json
Content-length: 272

{
  "roleId": "roleId-value",
  "roleMemberInfo": {
    "id": "id-value"
  }
}
```
<span data-ttu-id="14d01-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [scopedRoleMembership](../resources/scopedrolemembership.md) .</span><span class="sxs-lookup"><span data-stu-id="14d01-134">In the request body, supply a JSON representation of [scopedRoleMembership](../resources/scopedrolemembership.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="14d01-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14d01-135">Response</span></span>
<span data-ttu-id="14d01-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="14d01-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.scopedrolemembership"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 294

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#scopedRoleMemberships/$entity",
  "administrativeUnitId": "administrativeUnitId-value",
  "roleId": "roleId-value",
  "roleMemberInfo": {
    "id": "id-value",
    "displayName": "displayName-value",
    "userPrincipalName": "userPrincipalName-value"
  },
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create scopedRoleMembership",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->