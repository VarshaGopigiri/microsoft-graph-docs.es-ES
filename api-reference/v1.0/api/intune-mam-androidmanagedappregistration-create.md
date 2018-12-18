---
title: Crear androidManagedAppRegistration
description: Cree un objeto androidManagedAppRegistration.
author: tfitzmac
ms.openlocfilehash: c05c698179f2f8fa54ab12282be6e397b9275408
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339511"
---
# <a name="create-androidmanagedappregistration"></a><span data-ttu-id="8eab6-103">Crear androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="8eab6-103">Create androidManagedAppRegistration</span></span>

> <span data-ttu-id="8eab6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8eab6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8eab6-105">Cree un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8eab6-105">Create a new [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8eab6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8eab6-106">Prerequisites</span></span>
<span data-ttu-id="8eab6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8eab6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8eab6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8eab6-109">Permission type</span></span>|<span data-ttu-id="8eab6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8eab6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8eab6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8eab6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8eab6-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8eab6-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8eab6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8eab6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8eab6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8eab6-114">Not supported.</span></span>|
|<span data-ttu-id="8eab6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8eab6-115">Application</span></span>|<span data-ttu-id="8eab6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8eab6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8eab6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8eab6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="8eab6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8eab6-118">Request headers</span></span>
|<span data-ttu-id="8eab6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8eab6-119">Header</span></span>|<span data-ttu-id="8eab6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8eab6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8eab6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="8eab6-121">Authorization</span></span>|<span data-ttu-id="8eab6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8eab6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8eab6-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8eab6-123">Accept</span></span>|<span data-ttu-id="8eab6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8eab6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8eab6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8eab6-125">Request body</span></span>
<span data-ttu-id="8eab6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="8eab6-126">In the request body, supply a JSON representation for the androidManagedAppRegistration object.</span></span>

<span data-ttu-id="8eab6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="8eab6-127">The following table shows the properties that are required when you create the androidManagedAppRegistration.</span></span>

|<span data-ttu-id="8eab6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8eab6-128">Property</span></span>|<span data-ttu-id="8eab6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8eab6-129">Type</span></span>|<span data-ttu-id="8eab6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8eab6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8eab6-131">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8eab6-131">createdDateTime</span></span>|<span data-ttu-id="8eab6-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8eab6-132">DateTimeOffset</span></span>|<span data-ttu-id="8eab6-133">Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-133">Date and time of creation Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-134">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="8eab6-134">lastSyncDateTime</span></span>|<span data-ttu-id="8eab6-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8eab6-135">DateTimeOffset</span></span>|<span data-ttu-id="8eab6-136">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="8eab6-136">Date and time of last the app synced with management service.</span></span> <span data-ttu-id="8eab6-137">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-137">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-138">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="8eab6-138">applicationVersion</span></span>|<span data-ttu-id="8eab6-139">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-139">String</span></span>|<span data-ttu-id="8eab6-140">Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-140">App version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-141">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="8eab6-141">managementSdkVersion</span></span>|<span data-ttu-id="8eab6-142">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-142">String</span></span>|<span data-ttu-id="8eab6-143">Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-143">App management SDK version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-144">platformVersion</span><span class="sxs-lookup"><span data-stu-id="8eab6-144">platformVersion</span></span>|<span data-ttu-id="8eab6-145">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-145">String</span></span>|<span data-ttu-id="8eab6-146">Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-146">Operating System version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-147">deviceType</span><span class="sxs-lookup"><span data-stu-id="8eab6-147">deviceType</span></span>|<span data-ttu-id="8eab6-148">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-148">String</span></span>|<span data-ttu-id="8eab6-149">Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-149">Host device type Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-150">deviceTag</span><span class="sxs-lookup"><span data-stu-id="8eab6-150">deviceTag</span></span>|<span data-ttu-id="8eab6-151">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-151">String</span></span>|<span data-ttu-id="8eab6-152">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8eab6-152">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="8eab6-153">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="8eab6-153">Not guaranteed to relate apps in all conditions.</span></span> <span data-ttu-id="8eab6-154">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-154">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-155">deviceName</span><span class="sxs-lookup"><span data-stu-id="8eab6-155">deviceName</span></span>|<span data-ttu-id="8eab6-156">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-156">String</span></span>|<span data-ttu-id="8eab6-157">Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-157">Host device name Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-158">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="8eab6-158">flaggedReasons</span></span>|<span data-ttu-id="8eab6-159">colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-159">[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="8eab6-160">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8eab6-160">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="8eab6-161">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="8eab6-161">E.g.</span></span> <span data-ttu-id="8eab6-162">aplicación que se está ejecutando en el dispositivo raíz Inherited desde [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8eab6-162">app running on rooted device Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span></span> <span data-ttu-id="8eab6-163">Los valores posibles son: `none` y `rootedDevice`.</span><span class="sxs-lookup"><span data-stu-id="8eab6-163">Possible values are: `none`, `rootedDevice`.</span></span>|
|<span data-ttu-id="8eab6-164">userId</span><span class="sxs-lookup"><span data-stu-id="8eab6-164">userId</span></span>|<span data-ttu-id="8eab6-165">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-165">String</span></span>|<span data-ttu-id="8eab6-166">Identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8eab6-166">The user Id to who this app registration belongs.</span></span> <span data-ttu-id="8eab6-167">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-167">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-168">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="8eab6-168">appIdentifier</span></span>|[<span data-ttu-id="8eab6-169">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="8eab6-169">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="8eab6-170">Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-170">The app package Identifier Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-171">id</span><span class="sxs-lookup"><span data-stu-id="8eab6-171">id</span></span>|<span data-ttu-id="8eab6-172">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-172">String</span></span>|<span data-ttu-id="8eab6-173">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8eab6-173">Key of the entity.</span></span> <span data-ttu-id="8eab6-174">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8eab6-174">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="8eab6-175">version</span><span class="sxs-lookup"><span data-stu-id="8eab6-175">version</span></span>|<span data-ttu-id="8eab6-176">String</span><span class="sxs-lookup"><span data-stu-id="8eab6-176">String</span></span>|<span data-ttu-id="8eab6-177">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8eab6-177">Version of the entity.</span></span> <span data-ttu-id="8eab6-178">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8eab6-178">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="8eab6-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8eab6-179">Response</span></span>
<span data-ttu-id="8eab6-180">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8eab6-180">If successful, this method returns a `201 Created` response code and a [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8eab6-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8eab6-181">Example</span></span>
### <a name="request"></a><span data-ttu-id="8eab6-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8eab6-182">Request</span></span>
<span data-ttu-id="8eab6-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8eab6-183">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
Content-type: application/json
Content-length: 645

{
  "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
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

### <a name="response"></a><span data-ttu-id="8eab6-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8eab6-184">Response</span></span>
<span data-ttu-id="8eab6-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8eab6-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 753

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



