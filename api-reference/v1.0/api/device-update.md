---
title: Actualizar device
description: Actualiza las propiedades de un dispositivo registrado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: aaa8343307707142ca969c4257cc051e36a8cd7a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889540"
---
# <a name="update-device"></a><span data-ttu-id="55fc1-103">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="55fc1-103">Update device</span></span>

<span data-ttu-id="55fc1-104">Actualiza las propiedades de un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="55fc1-104">Update the properties of a registered device.</span></span>

<span data-ttu-id="55fc1-105">Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="55fc1-105">Only certain properties of a device can be updated through approved Mobile Device Managment (MDM) apps.</span></span>

## <a name="permissions"></a><span data-ttu-id="55fc1-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="55fc1-106">Permissions</span></span>
<span data-ttu-id="55fc1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="55fc1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="55fc1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55fc1-109">Permission type</span></span>      | <span data-ttu-id="55fc1-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55fc1-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="55fc1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55fc1-111">Delegated (work or school account)</span></span> | <span data-ttu-id="55fc1-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="55fc1-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="55fc1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55fc1-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="55fc1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55fc1-114">Not supported.</span></span> |
|<span data-ttu-id="55fc1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55fc1-115">Application</span></span> | <span data-ttu-id="55fc1-116">No se admite</span><span class="sxs-lookup"><span data-stu-id="55fc1-116">Not supported</span></span> |

## <a name="http-request"></a><span data-ttu-id="55fc1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55fc1-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> <span data-ttu-id="55fc1-118">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="55fc1-118">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="55fc1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55fc1-119">Request headers</span></span>
| <span data-ttu-id="55fc1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="55fc1-120">Name</span></span>       | <span data-ttu-id="55fc1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="55fc1-121">Type</span></span> | <span data-ttu-id="55fc1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="55fc1-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="55fc1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="55fc1-123">Authorization</span></span>  | <span data-ttu-id="55fc1-124">string</span><span class="sxs-lookup"><span data-stu-id="55fc1-124">string</span></span>  | <span data-ttu-id="55fc1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55fc1-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="55fc1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55fc1-127">Request body</span></span>

<span data-ttu-id="55fc1-128">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="55fc1-128">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span> <span data-ttu-id="55fc1-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="55fc1-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="55fc1-130">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="55fc1-130">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="55fc1-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55fc1-131">Property</span></span>     | <span data-ttu-id="55fc1-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="55fc1-132">Type</span></span>   |<span data-ttu-id="55fc1-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="55fc1-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="55fc1-134">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="55fc1-134">accountEnabled</span></span>|<span data-ttu-id="55fc1-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="55fc1-135">Boolean</span></span>| <span data-ttu-id="55fc1-136">**true** si la cuenta está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="55fc1-136">**true** if the account is enabled; otherwise, **false**.</span></span> |
|<span data-ttu-id="55fc1-137">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="55fc1-137">operatingSystem</span></span>|<span data-ttu-id="55fc1-138">String</span><span class="sxs-lookup"><span data-stu-id="55fc1-138">String</span></span>|<span data-ttu-id="55fc1-139">Tipo de sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55fc1-139">The type of operating system on the device.</span></span>|
|<span data-ttu-id="55fc1-140">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="55fc1-140">operatingSystemVersion</span></span>|<span data-ttu-id="55fc1-141">String</span><span class="sxs-lookup"><span data-stu-id="55fc1-141">String</span></span>|<span data-ttu-id="55fc1-142">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55fc1-142">The version of the operating system on the device</span></span>|
|<span data-ttu-id="55fc1-143">displayName</span><span class="sxs-lookup"><span data-stu-id="55fc1-143">displayName</span></span>|<span data-ttu-id="55fc1-144">String</span><span class="sxs-lookup"><span data-stu-id="55fc1-144">String</span></span>|<span data-ttu-id="55fc1-145">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55fc1-145">The display name for the device.</span></span>|
|<span data-ttu-id="55fc1-146">isCompliant</span><span class="sxs-lookup"><span data-stu-id="55fc1-146">isCompliant</span></span>|<span data-ttu-id="55fc1-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="55fc1-147">Boolean</span></span>|<span data-ttu-id="55fc1-148">**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="55fc1-148">**true** if the device complies with Mobile Device Management (MDM) policies; otherwise, **false**.</span></span> <span data-ttu-id="55fc1-149">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="55fc1-149">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |
|<span data-ttu-id="55fc1-150">isManaged</span><span class="sxs-lookup"><span data-stu-id="55fc1-150">isManaged</span></span>|<span data-ttu-id="55fc1-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="55fc1-151">Boolean</span></span>|<span data-ttu-id="55fc1-152">**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="55fc1-152">**true** if the device is managed by a Mobile Device Management (MDM) app; otherwise, **false**.</span></span> <span data-ttu-id="55fc1-153">Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="55fc1-153">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |

## <a name="response"></a><span data-ttu-id="55fc1-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55fc1-154">Response</span></span>

<span data-ttu-id="55fc1-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="55fc1-155">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="55fc1-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55fc1-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="55fc1-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55fc1-157">Request</span></span>

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
##### <a name="response"></a><span data-ttu-id="55fc1-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55fc1-158">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
