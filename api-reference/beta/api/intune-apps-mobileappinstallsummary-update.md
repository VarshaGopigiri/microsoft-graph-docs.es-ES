---
title: Actualizar mobileAppInstallSummary
description: Actualizar las propiedades de un objeto mobileAppInstallSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 19bd1e61359c5d2bdaff6ee87e807bae7dba0f05
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864802"
---
# <a name="update-mobileappinstallsummary"></a><span data-ttu-id="ddce0-103">Actualizar mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="ddce0-103">Update mobileAppInstallSummary</span></span>

> <span data-ttu-id="ddce0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ddce0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ddce0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ddce0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ddce0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ddce0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ddce0-107">Actualizar las propiedades de un objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="ddce0-107">Update the properties of a [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ddce0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ddce0-108">Prerequisites</span></span>
<span data-ttu-id="ddce0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ddce0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ddce0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ddce0-111">Permission type</span></span>|<span data-ttu-id="ddce0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ddce0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ddce0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ddce0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ddce0-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ddce0-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ddce0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ddce0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ddce0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ddce0-116">Not supported.</span></span>|
|<span data-ttu-id="ddce0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ddce0-117">Application</span></span>|<span data-ttu-id="ddce0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ddce0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ddce0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddce0-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/installSummary
```

## <a name="request-headers"></a><span data-ttu-id="ddce0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddce0-120">Request headers</span></span>
|<span data-ttu-id="ddce0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddce0-121">Header</span></span>|<span data-ttu-id="ddce0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ddce0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ddce0-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ddce0-123">Authorization</span></span>|<span data-ttu-id="ddce0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ddce0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ddce0-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ddce0-125">Accept</span></span>|<span data-ttu-id="ddce0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ddce0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ddce0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ddce0-127">Request body</span></span>
<span data-ttu-id="ddce0-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="ddce0-128">In the request body, supply a JSON representation for the [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>

<span data-ttu-id="ddce0-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="ddce0-129">The following table shows the properties that are required when you create the [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md).</span></span>

|<span data-ttu-id="ddce0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ddce0-130">Property</span></span>|<span data-ttu-id="ddce0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddce0-131">Type</span></span>|<span data-ttu-id="ddce0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddce0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ddce0-133">id</span><span class="sxs-lookup"><span data-stu-id="ddce0-133">id</span></span>|<span data-ttu-id="ddce0-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ddce0-134">String</span></span>|<span data-ttu-id="ddce0-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ddce0-135">Key of the entity.</span></span>|
|<span data-ttu-id="ddce0-136">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-136">installedDeviceCount</span></span>|<span data-ttu-id="ddce0-137">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-137">Int32</span></span>|<span data-ttu-id="ddce0-138">Número de dispositivos que haya instalado correctamente esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-138">Number of Devices that have successfully installed this app.</span></span>|
|<span data-ttu-id="ddce0-139">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-139">failedDeviceCount</span></span>|<span data-ttu-id="ddce0-140">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-140">Int32</span></span>|<span data-ttu-id="ddce0-141">Número de dispositivos que no haya podido instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-141">Number of Devices that have failed to install this app.</span></span>|
|<span data-ttu-id="ddce0-142">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-142">notApplicableDeviceCount</span></span>|<span data-ttu-id="ddce0-143">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-143">Int32</span></span>|<span data-ttu-id="ddce0-144">Número de dispositivos que no son aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-144">Number of Devices that are not applicable for this app.</span></span>|
|<span data-ttu-id="ddce0-145">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-145">notInstalledDeviceCount</span></span>|<span data-ttu-id="ddce0-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-146">Int32</span></span>|<span data-ttu-id="ddce0-147">Número de dispositivos que no tienen esta aplicación instalada.</span><span class="sxs-lookup"><span data-stu-id="ddce0-147">Number of Devices that does not have this app installed.</span></span>|
|<span data-ttu-id="ddce0-148">pendingInstallDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-148">pendingInstallDeviceCount</span></span>|<span data-ttu-id="ddce0-149">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-149">Int32</span></span>|<span data-ttu-id="ddce0-150">Número de dispositivos que hayan sido notificados para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-150">Number of Devices that have been notified to install this app.</span></span>|
|<span data-ttu-id="ddce0-151">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-151">installedUserCount</span></span>|<span data-ttu-id="ddce0-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-152">Int32</span></span>|<span data-ttu-id="ddce0-153">Número de usuarios cuyos dispositivos han correctas para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-153">Number of Users whose devices have all succeeded to install this app.</span></span>|
|<span data-ttu-id="ddce0-154">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-154">failedUserCount</span></span>|<span data-ttu-id="ddce0-155">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-155">Int32</span></span>|<span data-ttu-id="ddce0-156">Número de usuarios que tienen 1 o más dispositivos que no se pudo instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-156">Number of Users that have 1 or more device that failed to install this app.</span></span>|
|<span data-ttu-id="ddce0-157">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-157">notApplicableUserCount</span></span>|<span data-ttu-id="ddce0-158">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-158">Int32</span></span>|<span data-ttu-id="ddce0-159">Número de usuarios cuyos dispositivos no eran aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-159">Number of Users whose devices were all not applicable for this app.</span></span>|
|<span data-ttu-id="ddce0-160">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-160">notInstalledUserCount</span></span>|<span data-ttu-id="ddce0-161">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-161">Int32</span></span>|<span data-ttu-id="ddce0-162">Número de usuarios que tienen 1 o más dispositivos que no se han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddce0-162">Number of Users that have 1 or more devices that did not install this app.</span></span>|
|<span data-ttu-id="ddce0-163">pendingInstallUserCount</span><span class="sxs-lookup"><span data-stu-id="ddce0-163">pendingInstallUserCount</span></span>|<span data-ttu-id="ddce0-164">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce0-164">Int32</span></span>|<span data-ttu-id="ddce0-165">Número de usuarios que tienen 1 o más dispositivos que han sido notificados a instalar esta aplicación y de tener 0 dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="ddce0-165">Number of Users that have 1 or more device that have been notified to install this app and have 0 devices with failures.</span></span>|



## <a name="response"></a><span data-ttu-id="ddce0-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddce0-166">Response</span></span>
<span data-ttu-id="ddce0-167">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddce0-167">If successful, this method returns a `200 OK` response code and an updated [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ddce0-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddce0-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="ddce0-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ddce0-169">Request</span></span>
<span data-ttu-id="ddce0-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddce0-170">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ddce0-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddce0-171">Response</span></span>
<span data-ttu-id="ddce0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ddce0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





