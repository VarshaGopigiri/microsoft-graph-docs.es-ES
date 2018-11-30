---
title: Actualizar device
description: Actualizar las propiedades de un dispositivo.
ms.openlocfilehash: 2f8a5097aa9ee0413b7868753b5b0a0dfdf9d071
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087788"
---
# <a name="update-device"></a><span data-ttu-id="dd498-103">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="dd498-103">Update device</span></span>

> <span data-ttu-id="dd498-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dd498-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dd498-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dd498-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dd498-106">Actualizar las propiedades de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd498-106">Update the properties of a device.</span></span>

<span data-ttu-id="dd498-107">Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="dd498-107">Only certain properties of a device can be updated through approved Mobile Device Managment (MDM) apps.</span></span>

## <a name="permissions"></a><span data-ttu-id="dd498-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd498-108">Permissions</span></span>
<span data-ttu-id="dd498-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd498-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dd498-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd498-111">Permission type</span></span>      | <span data-ttu-id="dd498-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd498-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd498-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd498-113">Delegated (work or school account)</span></span> | <span data-ttu-id="dd498-114">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dd498-114">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="dd498-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd498-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd498-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd498-116">Not supported.</span></span> |
|<span data-ttu-id="dd498-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd498-117">Application</span></span> | <span data-ttu-id="dd498-118">No se admite</span><span class="sxs-lookup"><span data-stu-id="dd498-118">Not supported</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd498-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd498-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```

> <span data-ttu-id="dd498-120">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="dd498-120">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dd498-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd498-121">Request headers</span></span>
| <span data-ttu-id="dd498-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd498-122">Name</span></span>       | <span data-ttu-id="dd498-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd498-123">Type</span></span> | <span data-ttu-id="dd498-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd498-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="dd498-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd498-125">Authorization</span></span>  | <span data-ttu-id="dd498-126">string</span><span class="sxs-lookup"><span data-stu-id="dd498-126">string</span></span>  | <span data-ttu-id="dd498-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd498-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dd498-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd498-129">Request body</span></span>

<span data-ttu-id="dd498-130">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="dd498-130">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span> <span data-ttu-id="dd498-131">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd498-131">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="dd498-132">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="dd498-132">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="dd498-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd498-133">Property</span></span>     | <span data-ttu-id="dd498-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd498-134">Type</span></span>   |<span data-ttu-id="dd498-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd498-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dd498-136">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="dd498-136">accountEnabled</span></span>|<span data-ttu-id="dd498-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="dd498-137">Boolean</span></span>| <span data-ttu-id="dd498-138">**true** si la cuenta está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dd498-138">**true** if the account is enabled; otherwise, **false**.</span></span> |
|<span data-ttu-id="dd498-139">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="dd498-139">operatingSystem</span></span>|<span data-ttu-id="dd498-140">String</span><span class="sxs-lookup"><span data-stu-id="dd498-140">String</span></span>|<span data-ttu-id="dd498-141">Tipo de sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd498-141">The type of operating system on the device.</span></span>|
|<span data-ttu-id="dd498-142">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="dd498-142">operatingSystemVersion</span></span>|<span data-ttu-id="dd498-143">String</span><span class="sxs-lookup"><span data-stu-id="dd498-143">String</span></span>|<span data-ttu-id="dd498-144">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd498-144">The version of the operating system on the device</span></span>|
|<span data-ttu-id="dd498-145">displayName</span><span class="sxs-lookup"><span data-stu-id="dd498-145">displayName</span></span>|<span data-ttu-id="dd498-146">String</span><span class="sxs-lookup"><span data-stu-id="dd498-146">String</span></span>|<span data-ttu-id="dd498-147">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd498-147">The display name for the device.</span></span>|
|<span data-ttu-id="dd498-148">isCompliant</span><span class="sxs-lookup"><span data-stu-id="dd498-148">isCompliant</span></span>|<span data-ttu-id="dd498-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="dd498-149">Boolean</span></span>|<span data-ttu-id="dd498-150">**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dd498-150">**true** if the device complies with Mobile Device Management (MDM) policies; otherwise, **false**.</span></span> <span data-ttu-id="dd498-151">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="dd498-151">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |
|<span data-ttu-id="dd498-152">isManaged</span><span class="sxs-lookup"><span data-stu-id="dd498-152">isManaged</span></span>|<span data-ttu-id="dd498-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="dd498-153">Boolean</span></span>|<span data-ttu-id="dd498-154">**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dd498-154">**true** if the device is managed by a Mobile Device Management (MDM) app; otherwise, **false**.</span></span> <span data-ttu-id="dd498-155">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="dd498-155">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |

<span data-ttu-id="dd498-156">Puesto que el recurso de **dispositivo** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia de **dispositivo** existente.</span><span class="sxs-lookup"><span data-stu-id="dd498-156">Since the **device** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **device** instance.</span></span>

## <a name="response"></a><span data-ttu-id="dd498-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd498-157">Response</span></span>

<span data-ttu-id="dd498-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="dd498-158">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="dd498-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd498-159">Example</span></span>

##### <a name="request"></a><span data-ttu-id="dd498-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd498-160">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_device"
}-->
```http
PATCH https://graph.microsoft.com/beta/devices/{id}
Content-type: application/json
Content-length: 31

{
  "accountEnabled": false
}
```
##### <a name="response"></a><span data-ttu-id="dd498-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd498-161">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="dd498-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd498-162">See also</span></span>

- [<span data-ttu-id="dd498-163">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="dd498-163">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="dd498-164">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="dd498-164">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="dd498-165">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="dd498-165">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
