---
title: Crear iosVppAppAssignedDeviceLicense
description: Crear un nuevo objeto iosVppAppAssignedDeviceLicense.
ms.openlocfilehash: 968f272fae21ccf78d41b384c34675f6a5d3f4c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089082"
---
# <a name="create-iosvppappassigneddevicelicense"></a><span data-ttu-id="678b4-103">Crear iosVppAppAssignedDeviceLicense</span><span class="sxs-lookup"><span data-stu-id="678b4-103">Create iosVppAppAssignedDeviceLicense</span></span>

> <span data-ttu-id="678b4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="678b4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="678b4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="678b4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="678b4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="678b4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="678b4-107">Crear un nuevo objeto [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="678b4-107">Create a new [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="678b4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="678b4-108">Prerequisites</span></span>
<span data-ttu-id="678b4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="678b4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="678b4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="678b4-111">Permission type</span></span>|<span data-ttu-id="678b4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="678b4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="678b4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="678b4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="678b4-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="678b4-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="678b4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="678b4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="678b4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="678b4-116">Not supported.</span></span>|
|<span data-ttu-id="678b4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="678b4-117">Application</span></span>|<span data-ttu-id="678b4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="678b4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="678b4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="678b4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

## <a name="request-headers"></a><span data-ttu-id="678b4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="678b4-120">Request headers</span></span>
|<span data-ttu-id="678b4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="678b4-121">Header</span></span>|<span data-ttu-id="678b4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="678b4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="678b4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="678b4-123">Authorization</span></span>|<span data-ttu-id="678b4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="678b4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="678b4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="678b4-125">Accept</span></span>|<span data-ttu-id="678b4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="678b4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="678b4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="678b4-127">Request body</span></span>
<span data-ttu-id="678b4-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosVppAppAssignedDeviceLicense.</span><span class="sxs-lookup"><span data-stu-id="678b4-128">In the request body, supply a JSON representation for the iosVppAppAssignedDeviceLicense object.</span></span>

<span data-ttu-id="678b4-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosVppAppAssignedDeviceLicense.</span><span class="sxs-lookup"><span data-stu-id="678b4-129">The following table shows the properties that are required when you create the iosVppAppAssignedDeviceLicense.</span></span>

|<span data-ttu-id="678b4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="678b4-130">Property</span></span>|<span data-ttu-id="678b4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="678b4-131">Type</span></span>|<span data-ttu-id="678b4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="678b4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="678b4-133">id</span><span class="sxs-lookup"><span data-stu-id="678b4-133">id</span></span>|<span data-ttu-id="678b4-134">String</span><span class="sxs-lookup"><span data-stu-id="678b4-134">String</span></span>|<span data-ttu-id="678b4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="678b4-135">Key of the entity.</span></span> <span data-ttu-id="678b4-136">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="678b4-136">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="678b4-137">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="678b4-137">userEmailAddress</span></span>|<span data-ttu-id="678b4-138">String</span><span class="sxs-lookup"><span data-stu-id="678b4-138">String</span></span>|<span data-ttu-id="678b4-139">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="678b4-139">The user email address.</span></span> <span data-ttu-id="678b4-140">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="678b4-140">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="678b4-141">userId</span><span class="sxs-lookup"><span data-stu-id="678b4-141">userId</span></span>|<span data-ttu-id="678b4-142">String</span><span class="sxs-lookup"><span data-stu-id="678b4-142">String</span></span>|<span data-ttu-id="678b4-143">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="678b4-143">The user ID.</span></span> <span data-ttu-id="678b4-144">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="678b4-144">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="678b4-145">userName</span><span class="sxs-lookup"><span data-stu-id="678b4-145">userName</span></span>|<span data-ttu-id="678b4-146">String</span><span class="sxs-lookup"><span data-stu-id="678b4-146">String</span></span>|<span data-ttu-id="678b4-147">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="678b4-147">The user name.</span></span> <span data-ttu-id="678b4-148">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="678b4-148">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="678b4-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="678b4-149">userPrincipalName</span></span>|<span data-ttu-id="678b4-150">String</span><span class="sxs-lookup"><span data-stu-id="678b4-150">String</span></span>|<span data-ttu-id="678b4-151">El nombre principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="678b4-151">The user principal name.</span></span> <span data-ttu-id="678b4-152">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="678b4-152">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="678b4-153">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="678b4-153">managedDeviceId</span></span>|<span data-ttu-id="678b4-154">String</span><span class="sxs-lookup"><span data-stu-id="678b4-154">String</span></span>|<span data-ttu-id="678b4-155">El identificador de dispositivo administrado.</span><span class="sxs-lookup"><span data-stu-id="678b4-155">The managed device ID.</span></span>|
|<span data-ttu-id="678b4-156">deviceName</span><span class="sxs-lookup"><span data-stu-id="678b4-156">deviceName</span></span>|<span data-ttu-id="678b4-157">String</span><span class="sxs-lookup"><span data-stu-id="678b4-157">String</span></span>|<span data-ttu-id="678b4-158">El nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="678b4-158">The device name.</span></span>|



## <a name="response"></a><span data-ttu-id="678b4-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="678b4-159">Response</span></span>
<span data-ttu-id="678b4-160">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="678b4-160">If successful, this method returns a `201 Created` response code and a [iosVppAppAssignedDeviceLicense](../resources/intune-apps-iosvppappassigneddevicelicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="678b4-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="678b4-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="678b4-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="678b4-162">Request</span></span>
<span data-ttu-id="678b4-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="678b4-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
Content-type: application/json
Content-length: 327

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedDeviceLicense",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "managedDeviceId": "Managed Device Id value",
  "deviceName": "Device Name value"
}
```

### <a name="response"></a><span data-ttu-id="678b4-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="678b4-164">Response</span></span>
<span data-ttu-id="678b4-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="678b4-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





