---
title: Activar directoryRole
description: Activa un rol del directorio. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo los administradores de empresa y los roles de Active directory de los usuarios implícitos están activados de forma predeterminada. Para obtener acceso a los miembros a otra función de Active directory, se debe activar primero con la plantilla de rol correspondiente de Active directory (directoryRoleTemplate).
ms.openlocfilehash: 2a81bedaf4998e44825abc5e2cf0a93ec8708f96
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085571"
---
# <a name="activate-directoryrole"></a><span data-ttu-id="eec17-106">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="eec17-106">Activate directoryRole</span></span>

> <span data-ttu-id="eec17-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eec17-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eec17-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eec17-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eec17-109">Activa un rol del directorio.</span><span class="sxs-lookup"><span data-stu-id="eec17-109">Activate a directory role.</span></span> <span data-ttu-id="eec17-110">Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="eec17-110">To read a directory role or update its members, it must first be activated in the tenant.</span></span> <span data-ttu-id="eec17-111">Sólo los administradores de empresa y los roles de Active directory de los usuarios implícitos están activados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="eec17-111">Only the Company Administrators  and the implicit Users directory roles are activated by default.</span></span> <span data-ttu-id="eec17-112">Para obtener acceso a los miembros a otra función de Active directory, se debe activar primero con la plantilla de rol correspondiente de Active directory ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="eec17-112">To access and assign members to another directory role, you must first activate it with its corresponding directory role template ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span></span>

## <a name="permissions"></a><span data-ttu-id="eec17-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="eec17-113">Permissions</span></span>
<span data-ttu-id="eec17-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eec17-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eec17-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eec17-116">Permission type</span></span>      | <span data-ttu-id="eec17-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eec17-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eec17-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eec17-118">Delegated (work or school account)</span></span> | <span data-ttu-id="eec17-119">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eec17-119">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eec17-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eec17-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eec17-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eec17-121">Not supported.</span></span>    |
|<span data-ttu-id="eec17-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eec17-122">Application</span></span> | <span data-ttu-id="eec17-123">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eec17-123">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eec17-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eec17-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
## <a name="request-headers"></a><span data-ttu-id="eec17-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eec17-125">Request headers</span></span>
| <span data-ttu-id="eec17-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="eec17-126">Name</span></span>       | <span data-ttu-id="eec17-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="eec17-127">Type</span></span> | <span data-ttu-id="eec17-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="eec17-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="eec17-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="eec17-129">Authorization</span></span>  | <span data-ttu-id="eec17-130">string</span><span class="sxs-lookup"><span data-stu-id="eec17-130">string</span></span>  | <span data-ttu-id="eec17-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eec17-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eec17-133">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="eec17-133">Request body</span></span>
<span data-ttu-id="eec17-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="eec17-134">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>

<span data-ttu-id="eec17-135">En la tabla siguiente, se muestran las propiedades necesarias al activar un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="eec17-135">The following table shows the properties that are required when you activate a directory role.</span></span>

|<span data-ttu-id="eec17-136">Parámetro obligatorio</span><span class="sxs-lookup"><span data-stu-id="eec17-136">Required parameter</span></span> | <span data-ttu-id="eec17-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="eec17-137">Type</span></span> | <span data-ttu-id="eec17-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="eec17-138">Description</span></span>|
|:---------|:---------|:---------|
|<span data-ttu-id="eec17-139">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="eec17-139">roleTemplateId</span></span> | <span data-ttu-id="eec17-140">string</span><span class="sxs-lookup"><span data-stu-id="eec17-140">string</span></span> | <span data-ttu-id="eec17-p106">El identificador de la [directoryRoleTemplate](../resources/directoryroletemplate.md) en que se basa el rol. Es la única propiedad que se puede especificar en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eec17-p106">The ID of the [directoryRoleTemplate](../resources/directoryroletemplate.md) that the role is based on. This is the only property that may be specified in the request.</span></span>|

## <a name="response"></a><span data-ttu-id="eec17-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eec17-143">Response</span></span>

<span data-ttu-id="eec17-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eec17-144">If successful, this method returns `201 Created` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eec17-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eec17-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eec17-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eec17-146">Request</span></span>
<span data-ttu-id="eec17-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eec17-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryrole_from_directoryroles"
}-->
```http
POST https://graph.microsoft.com/beta/directoryRoles
Content-type: application/json
Content-length: 153

{
  "description": "description-value",
  "displayName": "displayName-value",
  "roleTemplateId": "roleTemplateId-value"
}
```
<span data-ttu-id="eec17-148">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="eec17-148">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="eec17-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eec17-149">Response</span></span>
<span data-ttu-id="eec17-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eec17-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 175

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
