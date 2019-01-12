---
title: Actualizar iosVppAppAssignedDeviceLicense
description: Actualizar las propiedades de un objeto iosVppAppAssignedDeviceLicense.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b8f18e1fb8895861cd497204f9b9608f7c4f9dba
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974185"
---
# <a name="update-iosvppappassigneddevicelicense"></a><span data-ttu-id="eacd5-103">Actualizar iosVppAppAssignedDeviceLicense</span><span class="sxs-lookup"><span data-stu-id="eacd5-103">Update iosVppAppAssignedDeviceLicense</span></span>

> <span data-ttu-id="eacd5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eacd5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eacd5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eacd5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eacd5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eacd5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eacd5-107">Actualizar las propiedades de un objeto [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="eacd5-107">Update the properties of a [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eacd5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eacd5-108">Prerequisites</span></span>
<span data-ttu-id="eacd5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eacd5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eacd5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eacd5-111">Permission type</span></span>|<span data-ttu-id="eacd5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eacd5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eacd5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eacd5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="eacd5-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eacd5-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="eacd5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eacd5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eacd5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eacd5-116">Not supported.</span></span>|
|<span data-ttu-id="eacd5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eacd5-117">Application</span></span>|<span data-ttu-id="eacd5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eacd5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eacd5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eacd5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
```

## <a name="request-headers"></a><span data-ttu-id="eacd5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eacd5-120">Request headers</span></span>
|<span data-ttu-id="eacd5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eacd5-121">Header</span></span>|<span data-ttu-id="eacd5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eacd5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eacd5-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="eacd5-123">Authorization</span></span>|<span data-ttu-id="eacd5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eacd5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eacd5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="eacd5-125">Accept</span></span>|<span data-ttu-id="eacd5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="eacd5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eacd5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eacd5-127">Request body</span></span>
<span data-ttu-id="eacd5-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="eacd5-128">In the request body, supply a JSON representation for the [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) object.</span></span>

<span data-ttu-id="eacd5-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md).</span><span class="sxs-lookup"><span data-stu-id="eacd5-129">The following table shows the properties that are required when you create the [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md).</span></span>

|<span data-ttu-id="eacd5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eacd5-130">Property</span></span>|<span data-ttu-id="eacd5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="eacd5-131">Type</span></span>|<span data-ttu-id="eacd5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="eacd5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eacd5-133">id</span><span class="sxs-lookup"><span data-stu-id="eacd5-133">id</span></span>|<span data-ttu-id="eacd5-134">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-134">String</span></span>|<span data-ttu-id="eacd5-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="eacd5-135">Key of the entity.</span></span> <span data-ttu-id="eacd5-136">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="eacd5-136">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="eacd5-137">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="eacd5-137">userEmailAddress</span></span>|<span data-ttu-id="eacd5-138">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-138">String</span></span>|<span data-ttu-id="eacd5-139">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="eacd5-139">The user email address.</span></span> <span data-ttu-id="eacd5-140">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="eacd5-140">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="eacd5-141">userId</span><span class="sxs-lookup"><span data-stu-id="eacd5-141">userId</span></span>|<span data-ttu-id="eacd5-142">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-142">String</span></span>|<span data-ttu-id="eacd5-143">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="eacd5-143">The user ID.</span></span> <span data-ttu-id="eacd5-144">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="eacd5-144">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="eacd5-145">userName</span><span class="sxs-lookup"><span data-stu-id="eacd5-145">userName</span></span>|<span data-ttu-id="eacd5-146">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-146">String</span></span>|<span data-ttu-id="eacd5-147">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="eacd5-147">The user name.</span></span> <span data-ttu-id="eacd5-148">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="eacd5-148">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="eacd5-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="eacd5-149">userPrincipalName</span></span>|<span data-ttu-id="eacd5-150">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-150">String</span></span>|<span data-ttu-id="eacd5-151">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="eacd5-151">The user principal name.</span></span> <span data-ttu-id="eacd5-152">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="eacd5-152">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="eacd5-153">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="eacd5-153">managedDeviceId</span></span>|<span data-ttu-id="eacd5-154">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-154">String</span></span>|<span data-ttu-id="eacd5-155">El identificador de dispositivo administrado.</span><span class="sxs-lookup"><span data-stu-id="eacd5-155">The managed device ID.</span></span>|
|<span data-ttu-id="eacd5-156">deviceName</span><span class="sxs-lookup"><span data-stu-id="eacd5-156">deviceName</span></span>|<span data-ttu-id="eacd5-157">String</span><span class="sxs-lookup"><span data-stu-id="eacd5-157">String</span></span>|<span data-ttu-id="eacd5-158">El nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eacd5-158">The device name.</span></span>|



## <a name="response"></a><span data-ttu-id="eacd5-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eacd5-159">Response</span></span>
<span data-ttu-id="eacd5-160">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eacd5-160">If successful, this method returns a `200 OK` response code and an updated [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eacd5-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eacd5-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="eacd5-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eacd5-162">Request</span></span>
<span data-ttu-id="eacd5-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eacd5-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
Content-type: application/json
Content-length: 258

{
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "managedDeviceId": "Managed Device Id value",
  "deviceName": "Device Name value"
}
```

### <a name="response"></a><span data-ttu-id="eacd5-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eacd5-164">Response</span></span>
<span data-ttu-id="eacd5-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eacd5-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 376

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedDeviceLicense",
  "id": "bed943d0-43d0-bed9-d043-d9bed043d9be",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "managedDeviceId": "Managed Device Id value",
  "deviceName": "Device Name value"
}
```





