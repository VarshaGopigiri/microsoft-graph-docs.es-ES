---
title: Actualizar mobileAppInstallSummary
description: Actualizar las propiedades de un objeto mobileAppInstallSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3886512ff2524ccf2ac424d198533ebaafae20ee
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930064"
---
# <a name="update-mobileappinstallsummary"></a><span data-ttu-id="e78a2-103">Actualizar mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="e78a2-103">Update mobileAppInstallSummary</span></span>

> <span data-ttu-id="e78a2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e78a2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e78a2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e78a2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e78a2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e78a2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e78a2-107">Actualizar las propiedades de un objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="e78a2-107">Update the properties of a [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e78a2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e78a2-108">Prerequisites</span></span>
<span data-ttu-id="e78a2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e78a2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e78a2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e78a2-111">Permission type</span></span>|<span data-ttu-id="e78a2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e78a2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e78a2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e78a2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e78a2-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e78a2-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e78a2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e78a2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e78a2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e78a2-116">Not supported.</span></span>|
|<span data-ttu-id="e78a2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e78a2-117">Application</span></span>|<span data-ttu-id="e78a2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e78a2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e78a2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e78a2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/installSummary
```

## <a name="request-headers"></a><span data-ttu-id="e78a2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e78a2-120">Request headers</span></span>
|<span data-ttu-id="e78a2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e78a2-121">Header</span></span>|<span data-ttu-id="e78a2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e78a2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e78a2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e78a2-123">Authorization</span></span>|<span data-ttu-id="e78a2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e78a2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e78a2-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e78a2-125">Accept</span></span>|<span data-ttu-id="e78a2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e78a2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e78a2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e78a2-127">Request body</span></span>
<span data-ttu-id="e78a2-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="e78a2-128">In the request body, supply a JSON representation for the [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>

<span data-ttu-id="e78a2-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="e78a2-129">The following table shows the properties that are required when you create the [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md).</span></span>

|<span data-ttu-id="e78a2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e78a2-130">Property</span></span>|<span data-ttu-id="e78a2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e78a2-131">Type</span></span>|<span data-ttu-id="e78a2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e78a2-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e78a2-133">id</span><span class="sxs-lookup"><span data-stu-id="e78a2-133">id</span></span>|<span data-ttu-id="e78a2-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e78a2-134">String</span></span>|<span data-ttu-id="e78a2-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e78a2-135">Key of the entity.</span></span>|
|<span data-ttu-id="e78a2-136">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-136">installedDeviceCount</span></span>|<span data-ttu-id="e78a2-137">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-137">Int32</span></span>|<span data-ttu-id="e78a2-138">Número de dispositivos que haya instalado correctamente esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-138">Number of Devices that have successfully installed this app.</span></span>|
|<span data-ttu-id="e78a2-139">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-139">failedDeviceCount</span></span>|<span data-ttu-id="e78a2-140">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-140">Int32</span></span>|<span data-ttu-id="e78a2-141">Número de dispositivos que no haya podido instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-141">Number of Devices that have failed to install this app.</span></span>|
|<span data-ttu-id="e78a2-142">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-142">notApplicableDeviceCount</span></span>|<span data-ttu-id="e78a2-143">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-143">Int32</span></span>|<span data-ttu-id="e78a2-144">Número de dispositivos que no son aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-144">Number of Devices that are not applicable for this app.</span></span>|
|<span data-ttu-id="e78a2-145">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-145">notInstalledDeviceCount</span></span>|<span data-ttu-id="e78a2-146">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-146">Int32</span></span>|<span data-ttu-id="e78a2-147">Número de dispositivos que no tienen esta aplicación instalada.</span><span class="sxs-lookup"><span data-stu-id="e78a2-147">Number of Devices that does not have this app installed.</span></span>|
|<span data-ttu-id="e78a2-148">pendingInstallDeviceCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-148">pendingInstallDeviceCount</span></span>|<span data-ttu-id="e78a2-149">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-149">Int32</span></span>|<span data-ttu-id="e78a2-150">Número de dispositivos que hayan sido notificados para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-150">Number of Devices that have been notified to install this app.</span></span>|
|<span data-ttu-id="e78a2-151">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-151">installedUserCount</span></span>|<span data-ttu-id="e78a2-152">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-152">Int32</span></span>|<span data-ttu-id="e78a2-153">Número de usuarios cuyos dispositivos han correctas para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-153">Number of Users whose devices have all succeeded to install this app.</span></span>|
|<span data-ttu-id="e78a2-154">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-154">failedUserCount</span></span>|<span data-ttu-id="e78a2-155">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-155">Int32</span></span>|<span data-ttu-id="e78a2-156">Número de usuarios que tienen 1 o más dispositivos que no se pudo instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-156">Number of Users that have 1 or more device that failed to install this app.</span></span>|
|<span data-ttu-id="e78a2-157">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-157">notApplicableUserCount</span></span>|<span data-ttu-id="e78a2-158">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-158">Int32</span></span>|<span data-ttu-id="e78a2-159">Número de usuarios cuyos dispositivos no eran aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-159">Number of Users whose devices were all not applicable for this app.</span></span>|
|<span data-ttu-id="e78a2-160">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-160">notInstalledUserCount</span></span>|<span data-ttu-id="e78a2-161">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-161">Int32</span></span>|<span data-ttu-id="e78a2-162">Número de usuarios que tienen 1 o más dispositivos que no se han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e78a2-162">Number of Users that have 1 or more devices that did not install this app.</span></span>|
|<span data-ttu-id="e78a2-163">pendingInstallUserCount</span><span class="sxs-lookup"><span data-stu-id="e78a2-163">pendingInstallUserCount</span></span>|<span data-ttu-id="e78a2-164">Int32</span><span class="sxs-lookup"><span data-stu-id="e78a2-164">Int32</span></span>|<span data-ttu-id="e78a2-165">Número de usuarios que tienen 1 o más dispositivos que han sido notificados a instalar esta aplicación y de tener 0 dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="e78a2-165">Number of Users that have 1 or more device that have been notified to install this app and have 0 devices with failures.</span></span>|



## <a name="response"></a><span data-ttu-id="e78a2-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e78a2-166">Response</span></span>
<span data-ttu-id="e78a2-167">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e78a2-167">If successful, this method returns a `200 OK` response code and an updated [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e78a2-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e78a2-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="e78a2-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e78a2-169">Request</span></span>
<span data-ttu-id="e78a2-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e78a2-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/installSummary
Content-type: application/json
Content-length: 312

{
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notApplicableDeviceCount": 8,
  "notInstalledDeviceCount": 7,
  "pendingInstallDeviceCount": 9,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notApplicableUserCount": 6,
  "notInstalledUserCount": 5,
  "pendingInstallUserCount": 7
}
```

### <a name="response"></a><span data-ttu-id="e78a2-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e78a2-171">Response</span></span>
<span data-ttu-id="e78a2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e78a2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 423

{
  "@odata.type": "#microsoft.graph.mobileAppInstallSummary",
  "id": "06a792e9-92e9-06a7-e992-a706e992a706",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notApplicableDeviceCount": 8,
  "notInstalledDeviceCount": 7,
  "pendingInstallDeviceCount": 9,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notApplicableUserCount": 6,
  "notInstalledUserCount": 5,
  "pendingInstallUserCount": 7
}
```





