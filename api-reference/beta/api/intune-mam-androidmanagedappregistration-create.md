---
title: Crear androidManagedAppRegistration
description: Cree un objeto androidManagedAppRegistration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 21215cddf0966a6a209e10609ac5620053daa919
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974206"
---
# <a name="create-androidmanagedappregistration"></a><span data-ttu-id="63c50-103">Crear androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="63c50-103">Create androidManagedAppRegistration</span></span>

> <span data-ttu-id="63c50-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63c50-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63c50-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63c50-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63c50-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63c50-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63c50-107">Cree un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="63c50-107">Create a new [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63c50-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63c50-108">Prerequisites</span></span>
<span data-ttu-id="63c50-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63c50-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63c50-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63c50-111">Permission type</span></span>|<span data-ttu-id="63c50-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63c50-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63c50-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63c50-113">Delegated (work or school account)</span></span>|<span data-ttu-id="63c50-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63c50-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="63c50-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63c50-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63c50-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63c50-116">Not supported.</span></span>|
|<span data-ttu-id="63c50-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63c50-117">Application</span></span>|<span data-ttu-id="63c50-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63c50-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63c50-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63c50-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="63c50-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63c50-120">Request headers</span></span>
|<span data-ttu-id="63c50-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63c50-121">Header</span></span>|<span data-ttu-id="63c50-122">Valor</span><span class="sxs-lookup"><span data-stu-id="63c50-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63c50-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="63c50-123">Authorization</span></span>|<span data-ttu-id="63c50-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63c50-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63c50-125">Accept</span><span class="sxs-lookup"><span data-stu-id="63c50-125">Accept</span></span>|<span data-ttu-id="63c50-126">application/json</span><span class="sxs-lookup"><span data-stu-id="63c50-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63c50-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63c50-127">Request body</span></span>
<span data-ttu-id="63c50-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="63c50-128">In the request body, supply a JSON representation for the androidManagedAppRegistration object.</span></span>

<span data-ttu-id="63c50-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="63c50-129">The following table shows the properties that are required when you create the androidManagedAppRegistration.</span></span>

|<span data-ttu-id="63c50-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63c50-130">Property</span></span>|<span data-ttu-id="63c50-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="63c50-131">Type</span></span>|<span data-ttu-id="63c50-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="63c50-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63c50-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="63c50-133">createdDateTime</span></span>|<span data-ttu-id="63c50-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63c50-134">DateTimeOffset</span></span>|<span data-ttu-id="63c50-135">Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-135">Date and time of creation Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-136">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="63c50-136">lastSyncDateTime</span></span>|<span data-ttu-id="63c50-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63c50-137">DateTimeOffset</span></span>|<span data-ttu-id="63c50-138">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="63c50-138">Date and time of last the app synced with management service.</span></span> <span data-ttu-id="63c50-139">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-139">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-140">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="63c50-140">applicationVersion</span></span>|<span data-ttu-id="63c50-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-141">String</span></span>|<span data-ttu-id="63c50-142">Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-142">App version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-143">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="63c50-143">managementSdkVersion</span></span>|<span data-ttu-id="63c50-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-144">String</span></span>|<span data-ttu-id="63c50-145">Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-145">App management SDK version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-146">platformVersion</span><span class="sxs-lookup"><span data-stu-id="63c50-146">platformVersion</span></span>|<span data-ttu-id="63c50-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-147">String</span></span>|<span data-ttu-id="63c50-148">Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-148">Operating System version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-149">deviceType</span><span class="sxs-lookup"><span data-stu-id="63c50-149">deviceType</span></span>|<span data-ttu-id="63c50-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-150">String</span></span>|<span data-ttu-id="63c50-151">Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-151">Host device type Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-152">deviceTag</span><span class="sxs-lookup"><span data-stu-id="63c50-152">deviceTag</span></span>|<span data-ttu-id="63c50-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-153">String</span></span>|<span data-ttu-id="63c50-154">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c50-154">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="63c50-155">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="63c50-155">Not guaranteed to relate apps in all conditions.</span></span> <span data-ttu-id="63c50-156">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-156">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-157">deviceName</span><span class="sxs-lookup"><span data-stu-id="63c50-157">deviceName</span></span>|<span data-ttu-id="63c50-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-158">String</span></span>|<span data-ttu-id="63c50-159">Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-159">Host device name Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-160">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="63c50-160">managedDeviceId</span></span>|<span data-ttu-id="63c50-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-161">String</span></span>|<span data-ttu-id="63c50-162">El identificador de dispositivo administrado del dispositivo host.</span><span class="sxs-lookup"><span data-stu-id="63c50-162">The Managed Device identifier of the host device.</span></span> <span data-ttu-id="63c50-163">Valor puede estar vacío, incluso cuando se administra el dispositivo host.</span><span class="sxs-lookup"><span data-stu-id="63c50-163">Value could be empty even when the host device is managed.</span></span> <span data-ttu-id="63c50-164">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-164">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-165">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="63c50-165">azureADDeviceId</span></span>|<span data-ttu-id="63c50-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-166">String</span></span>|<span data-ttu-id="63c50-167">El identificador de dispositivo de Azure Active Directory del dispositivo host.</span><span class="sxs-lookup"><span data-stu-id="63c50-167">The Azure Active Directory Device identifier of the host device.</span></span> <span data-ttu-id="63c50-168">Valor puede estar vacío, incluso cuando el dispositivo de host es Azure Active Directory registrada.</span><span class="sxs-lookup"><span data-stu-id="63c50-168">Value could be empty even when the host device is Azure Active Directory registered.</span></span> <span data-ttu-id="63c50-169">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-169">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-170">deviceModel</span><span class="sxs-lookup"><span data-stu-id="63c50-170">deviceModel</span></span>|<span data-ttu-id="63c50-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-171">String</span></span>|<span data-ttu-id="63c50-172">El modelo de dispositivo para el actual registro de la aplicación heredada de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-172">The device model for the current app registration  Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-173">entradas deviceManufacturer</span><span class="sxs-lookup"><span data-stu-id="63c50-173">deviceManufacturer</span></span>|<span data-ttu-id="63c50-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-174">String</span></span>|<span data-ttu-id="63c50-175">El fabricante del dispositivo para el actual registro de la aplicación heredada de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-175">The device manufacturer for the current app registration  Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-176">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="63c50-176">flaggedReasons</span></span>|<span data-ttu-id="63c50-177">colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-177">[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="63c50-178">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="63c50-178">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="63c50-179">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="63c50-179">E.g.</span></span> <span data-ttu-id="63c50-180">aplicación que se está ejecutando en el dispositivo raíz Inherited desde [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="63c50-180">app running on rooted device Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span></span> <span data-ttu-id="63c50-181">Los valores posibles son: `none` y `rootedDevice`.</span><span class="sxs-lookup"><span data-stu-id="63c50-181">Possible values are: `none`, `rootedDevice`.</span></span>|
|<span data-ttu-id="63c50-182">userId</span><span class="sxs-lookup"><span data-stu-id="63c50-182">userId</span></span>|<span data-ttu-id="63c50-183">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-183">String</span></span>|<span data-ttu-id="63c50-184">Identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63c50-184">The user Id to who this app registration belongs.</span></span> <span data-ttu-id="63c50-185">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-185">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-186">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="63c50-186">appIdentifier</span></span>|[<span data-ttu-id="63c50-187">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="63c50-187">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="63c50-188">Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-188">The app package Identifier Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-189">id</span><span class="sxs-lookup"><span data-stu-id="63c50-189">id</span></span>|<span data-ttu-id="63c50-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-190">String</span></span>|<span data-ttu-id="63c50-191">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63c50-191">Key of the entity.</span></span> <span data-ttu-id="63c50-192">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="63c50-192">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="63c50-193">version</span><span class="sxs-lookup"><span data-stu-id="63c50-193">version</span></span>|<span data-ttu-id="63c50-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c50-194">String</span></span>|<span data-ttu-id="63c50-195">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63c50-195">Version of the entity.</span></span> <span data-ttu-id="63c50-196">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="63c50-196">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="63c50-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63c50-197">Response</span></span>
<span data-ttu-id="63c50-198">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63c50-198">If successful, this method returns a `201 Created` response code and a [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63c50-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63c50-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="63c50-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63c50-200">Request</span></span>
<span data-ttu-id="63c50-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63c50-201">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedAppRegistrations
Content-type: application/json
Content-length: 837

{
  "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
  "managedDeviceId": "Managed Device Id value",
  "azureADDeviceId": "Azure ADDevice Id value",
  "deviceModel": "Device Model value",
  "deviceManufacturer": "Device Manufacturer value",
  "flaggedReasons": [
    "rootedDevice"
  ],
  "userId": "User Id value",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
    "packageId": "Package Id value"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="63c50-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63c50-202">Response</span></span>
<span data-ttu-id="63c50-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63c50-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 945

{
  "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
  "managedDeviceId": "Managed Device Id value",
  "azureADDeviceId": "Azure ADDevice Id value",
  "deviceModel": "Device Model value",
  "deviceManufacturer": "Device Manufacturer value",
  "flaggedReasons": [
    "rootedDevice"
  ],
  "userId": "User Id value",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
    "packageId": "Package Id value"
  },
  "id": "0e064997-4997-0e06-9749-060e9749060e",
  "version": "Version value"
}
```





