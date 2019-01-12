---
title: Activar directoryRole
description: Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente (directoryRoleTemplate).
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 5d127580c0a4851c5a991ccc0646007ddf1298a5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924919"
---
# <a name="activate-directoryrole"></a><span data-ttu-id="dd1a6-106">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="dd1a6-106">Activate directoryRole</span></span>

<span data-ttu-id="dd1a6-p102">Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="dd1a6-p102">Activate a directory role. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators and the implicit Users directory roles are activated by default. To access and assign members to another directory role, you must first activate it with its corresponding directory role template ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span></span>

## <a name="permissions"></a><span data-ttu-id="dd1a6-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd1a6-111">Permissions</span></span>
<span data-ttu-id="dd1a6-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd1a6-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dd1a6-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd1a6-114">Permission type</span></span>      | <span data-ttu-id="dd1a6-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd1a6-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd1a6-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd1a6-116">Delegated (work or school account)</span></span> | <span data-ttu-id="dd1a6-117">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dd1a6-117">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="dd1a6-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd1a6-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd1a6-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-119">Not supported.</span></span>    |
|<span data-ttu-id="dd1a6-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd1a6-120">Application</span></span> | <span data-ttu-id="dd1a6-121">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd1a6-121">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd1a6-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd1a6-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
## <a name="request-headers"></a><span data-ttu-id="dd1a6-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd1a6-123">Request headers</span></span>
| <span data-ttu-id="dd1a6-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd1a6-124">Name</span></span>       | <span data-ttu-id="dd1a6-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd1a6-125">Type</span></span> | <span data-ttu-id="dd1a6-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd1a6-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dd1a6-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="dd1a6-127">Authorization</span></span>  | <span data-ttu-id="dd1a6-128">string</span><span class="sxs-lookup"><span data-stu-id="dd1a6-128">string</span></span>  | <span data-ttu-id="dd1a6-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dd1a6-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="dd1a6-131">Content-Type</span></span>  | <span data-ttu-id="dd1a6-132">string</span><span class="sxs-lookup"><span data-stu-id="dd1a6-132">string</span></span>  | <span data-ttu-id="dd1a6-133">application/json</span><span class="sxs-lookup"><span data-stu-id="dd1a6-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="dd1a6-134">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd1a6-134">Request body</span></span>
<span data-ttu-id="dd1a6-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="dd1a6-135">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>

<span data-ttu-id="dd1a6-136">En la tabla siguiente, se muestran las propiedades necesarias al activar un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-136">The following table shows the properties that are required when you activate a directory role.</span></span>

|<span data-ttu-id="dd1a6-137">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dd1a6-137">Parameter</span></span> | <span data-ttu-id="dd1a6-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd1a6-138">Type</span></span> | <span data-ttu-id="dd1a6-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd1a6-139">Description</span></span>|
|:---------|:---------|:---------|
|<span data-ttu-id="dd1a6-140">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="dd1a6-140">roleTemplateId</span></span> | <span data-ttu-id="dd1a6-141">string</span><span class="sxs-lookup"><span data-stu-id="dd1a6-141">string</span></span> | <span data-ttu-id="dd1a6-142">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-142">Required.</span></span> <span data-ttu-id="dd1a6-143">El identificador de [directoryRoleTemplate](../resources/directoryroletemplate.md) que se basa el rol.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-143">The ID of the [directoryRoleTemplate](../resources/directoryroletemplate.md) that the role is based on.</span></span> <span data-ttu-id="dd1a6-144">Esta es la única propiedad que se puede especificar en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-144">This is the only property that may be specified in the request.</span></span>|

## <a name="response"></a><span data-ttu-id="dd1a6-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd1a6-145">Response</span></span>

<span data-ttu-id="dd1a6-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-146">If successful, this method returns `201 Created` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd1a6-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd1a6-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dd1a6-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd1a6-148">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryrole_from_directoryroles"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles
Content-type: application/json

{
  "roleTemplateId": "roleTemplateId-value"
}
```
<span data-ttu-id="dd1a6-149">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="dd1a6-149">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="dd1a6-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd1a6-150">Response</span></span>
<span data-ttu-id="dd1a6-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dd1a6-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "description": "description-value",
  "displayName": "displayName-value",
  "roleTemplateId": "roleTemplateId-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create directoryRole",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
