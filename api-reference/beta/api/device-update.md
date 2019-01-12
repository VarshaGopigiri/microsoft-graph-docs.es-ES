---
title: Actualizar device
description: Actualizar las propiedades de un dispositivo.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 42471e32eac050b84e36477c1cd48fd06feb4244
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916379"
---
# <a name="update-device"></a><span data-ttu-id="9f1d9-103">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="9f1d9-103">Update device</span></span>

> <span data-ttu-id="9f1d9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9f1d9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9f1d9-106">Actualizar las propiedades de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-106">Update the properties of a device.</span></span>

<span data-ttu-id="9f1d9-107">Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="9f1d9-107">Only certain properties of a device can be updated through approved Mobile Device Managment (MDM) apps.</span></span>

## <a name="permissions"></a><span data-ttu-id="9f1d9-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="9f1d9-108">Permissions</span></span>
<span data-ttu-id="9f1d9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f1d9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9f1d9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f1d9-111">Permission type</span></span>      | <span data-ttu-id="9f1d9-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f1d9-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9f1d9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f1d9-113">Delegated (work or school account)</span></span> | <span data-ttu-id="9f1d9-114">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9f1d9-114">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="9f1d9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f1d9-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9f1d9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-116">Not supported.</span></span> |
|<span data-ttu-id="9f1d9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f1d9-117">Application</span></span> | <span data-ttu-id="9f1d9-118">No se admite</span><span class="sxs-lookup"><span data-stu-id="9f1d9-118">Not supported</span></span> |

## <a name="http-request"></a><span data-ttu-id="9f1d9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f1d9-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```

> <span data-ttu-id="9f1d9-120">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="9f1d9-120">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9f1d9-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f1d9-121">Request headers</span></span>
| <span data-ttu-id="9f1d9-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9f1d9-122">Name</span></span>       | <span data-ttu-id="9f1d9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f1d9-123">Type</span></span> | <span data-ttu-id="9f1d9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f1d9-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9f1d9-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="9f1d9-125">Authorization</span></span>  | <span data-ttu-id="9f1d9-126">string</span><span class="sxs-lookup"><span data-stu-id="9f1d9-126">string</span></span>  | <span data-ttu-id="9f1d9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9f1d9-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f1d9-129">Request body</span></span>

<span data-ttu-id="9f1d9-130">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-130">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span> <span data-ttu-id="9f1d9-131">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-131">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="9f1d9-132">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-132">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9f1d9-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f1d9-133">Property</span></span>     | <span data-ttu-id="9f1d9-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f1d9-134">Type</span></span>   |<span data-ttu-id="9f1d9-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f1d9-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9f1d9-136">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="9f1d9-136">accountEnabled</span></span>|<span data-ttu-id="9f1d9-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f1d9-137">Boolean</span></span>| <span data-ttu-id="9f1d9-138">**true** si la cuenta está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-138">**true** if the account is enabled; otherwise, **false**.</span></span> |
|<span data-ttu-id="9f1d9-139">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="9f1d9-139">operatingSystem</span></span>|<span data-ttu-id="9f1d9-140">String</span><span class="sxs-lookup"><span data-stu-id="9f1d9-140">String</span></span>|<span data-ttu-id="9f1d9-141">Tipo de sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-141">The type of operating system on the device.</span></span>|
|<span data-ttu-id="9f1d9-142">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="9f1d9-142">operatingSystemVersion</span></span>|<span data-ttu-id="9f1d9-143">String</span><span class="sxs-lookup"><span data-stu-id="9f1d9-143">String</span></span>|<span data-ttu-id="9f1d9-144">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-144">The version of the operating system on the device</span></span>|
|<span data-ttu-id="9f1d9-145">displayName</span><span class="sxs-lookup"><span data-stu-id="9f1d9-145">displayName</span></span>|<span data-ttu-id="9f1d9-146">String</span><span class="sxs-lookup"><span data-stu-id="9f1d9-146">String</span></span>|<span data-ttu-id="9f1d9-147">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-147">The display name for the device.</span></span>|
|<span data-ttu-id="9f1d9-148">isCompliant</span><span class="sxs-lookup"><span data-stu-id="9f1d9-148">isCompliant</span></span>|<span data-ttu-id="9f1d9-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1d9-149">Boolean</span></span>|<span data-ttu-id="9f1d9-150">**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-150">**true** if the device complies with Mobile Device Management (MDM) policies; otherwise, **false**.</span></span> <span data-ttu-id="9f1d9-151">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-151">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |
|<span data-ttu-id="9f1d9-152">isManaged</span><span class="sxs-lookup"><span data-stu-id="9f1d9-152">isManaged</span></span>|<span data-ttu-id="9f1d9-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1d9-153">Boolean</span></span>|<span data-ttu-id="9f1d9-154">**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-154">**true** if the device is managed by a Mobile Device Management (MDM) app; otherwise, **false**.</span></span> <span data-ttu-id="9f1d9-155">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-155">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |

<span data-ttu-id="9f1d9-156">Puesto que el recurso de **dispositivo** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia de **dispositivo** existente.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-156">Since the **device** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **device** instance.</span></span>

## <a name="response"></a><span data-ttu-id="9f1d9-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f1d9-157">Response</span></span>

<span data-ttu-id="9f1d9-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-158">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="9f1d9-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f1d9-159">Example</span></span>

##### <a name="request"></a><span data-ttu-id="9f1d9-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f1d9-160">Request</span></span>

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
##### <a name="response"></a><span data-ttu-id="9f1d9-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f1d9-161">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="9f1d9-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f1d9-162">See also</span></span>

- [<span data-ttu-id="9f1d9-163">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="9f1d9-163">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="9f1d9-164">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="9f1d9-164">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="9f1d9-165">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="9f1d9-165">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
