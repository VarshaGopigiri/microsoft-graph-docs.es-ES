---
title: Actualizar device
description: Actualiza las propiedades de un dispositivo registrado.
ms.openlocfilehash: cb2f23a5c36b22b65503ea0e8ac93af443c13e08
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029657"
---
# <a name="update-device"></a><span data-ttu-id="6f0b0-103">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="6f0b0-103">Update device</span></span>

<span data-ttu-id="6f0b0-104">Actualiza las propiedades de un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-104">Update the properties of a registered device.</span></span>

<span data-ttu-id="6f0b0-105">Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="6f0b0-105">Only certain properties of a device can be updated through approved Mobile Device Managment (MDM) apps.</span></span>

## <a name="permissions"></a><span data-ttu-id="6f0b0-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f0b0-106">Permissions</span></span>
<span data-ttu-id="6f0b0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6f0b0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6f0b0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f0b0-109">Permission type</span></span>      | <span data-ttu-id="6f0b0-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f0b0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-111">Delegated (work or school account)</span></span> | <span data-ttu-id="6f0b0-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6f0b0-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="6f0b0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f0b0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-114">Not supported.</span></span> |
|<span data-ttu-id="6f0b0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f0b0-115">Application</span></span> | <span data-ttu-id="6f0b0-116">No se admite</span><span class="sxs-lookup"><span data-stu-id="6f0b0-116">Not supported</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f0b0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f0b0-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> <span data-ttu-id="6f0b0-118">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="6f0b0-118">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6f0b0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f0b0-119">Request headers</span></span>
| <span data-ttu-id="6f0b0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f0b0-120">Name</span></span>       | <span data-ttu-id="6f0b0-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f0b0-121">Type</span></span> | <span data-ttu-id="6f0b0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f0b0-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6f0b0-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f0b0-123">Authorization</span></span>  | <span data-ttu-id="6f0b0-124">string</span><span class="sxs-lookup"><span data-stu-id="6f0b0-124">string</span></span>  | <span data-ttu-id="6f0b0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6f0b0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f0b0-127">Request body</span></span>

<span data-ttu-id="6f0b0-128">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-128">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span> <span data-ttu-id="6f0b0-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="6f0b0-130">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-130">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6f0b0-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f0b0-131">Property</span></span>     | <span data-ttu-id="6f0b0-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f0b0-132">Type</span></span>   |<span data-ttu-id="6f0b0-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f0b0-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6f0b0-134">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="6f0b0-134">accountEnabled</span></span>|<span data-ttu-id="6f0b0-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="6f0b0-135">Boolean</span></span>| <span data-ttu-id="6f0b0-136">**true** si la cuenta está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-136">**true** if the account is enabled; otherwise, **false**.</span></span> |
|<span data-ttu-id="6f0b0-137">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="6f0b0-137">operatingSystem</span></span>|<span data-ttu-id="6f0b0-138">String</span><span class="sxs-lookup"><span data-stu-id="6f0b0-138">String</span></span>|<span data-ttu-id="6f0b0-139">Tipo de sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-139">The type of operating system on the device.</span></span>|
|<span data-ttu-id="6f0b0-140">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="6f0b0-140">operatingSystemVersion</span></span>|<span data-ttu-id="6f0b0-141">String</span><span class="sxs-lookup"><span data-stu-id="6f0b0-141">String</span></span>|<span data-ttu-id="6f0b0-142">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-142">The version of the operating system on the device</span></span>|
|<span data-ttu-id="6f0b0-143">displayName</span><span class="sxs-lookup"><span data-stu-id="6f0b0-143">displayName</span></span>|<span data-ttu-id="6f0b0-144">String</span><span class="sxs-lookup"><span data-stu-id="6f0b0-144">String</span></span>|<span data-ttu-id="6f0b0-145">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-145">The display name for the device.</span></span>|
|<span data-ttu-id="6f0b0-146">isCompliant</span><span class="sxs-lookup"><span data-stu-id="6f0b0-146">isCompliant</span></span>|<span data-ttu-id="6f0b0-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="6f0b0-147">Boolean</span></span>|<span data-ttu-id="6f0b0-148">**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-148">**true** if the device complies with Mobile Device Management (MDM) policies; otherwise, **false**.</span></span> <span data-ttu-id="6f0b0-149">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-149">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |
|<span data-ttu-id="6f0b0-150">isManaged</span><span class="sxs-lookup"><span data-stu-id="6f0b0-150">isManaged</span></span>|<span data-ttu-id="6f0b0-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="6f0b0-151">Boolean</span></span>|<span data-ttu-id="6f0b0-152">**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-152">**true** if the device is managed by a Mobile Device Management (MDM) app; otherwise, **false**.</span></span> <span data-ttu-id="6f0b0-153">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-153">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |

## <a name="response"></a><span data-ttu-id="6f0b0-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f0b0-154">Response</span></span>

<span data-ttu-id="6f0b0-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-155">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="6f0b0-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f0b0-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6f0b0-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f0b0-157">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_device"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/devices/{id}
Content-type: application/json
Content-length: 31

{
  "accountEnabled": false
}
```
##### <a name="response"></a><span data-ttu-id="6f0b0-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f0b0-158">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
