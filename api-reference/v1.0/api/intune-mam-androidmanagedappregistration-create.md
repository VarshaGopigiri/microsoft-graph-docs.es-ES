---
title: Crear androidManagedAppRegistration
description: Cree un objeto androidManagedAppRegistration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4485ab59a2a1bc4658a12e9bff4fae57fae2c898
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931996"
---
# <a name="create-androidmanagedappregistration"></a><span data-ttu-id="24aaf-103">Crear androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="24aaf-103">Create androidManagedAppRegistration</span></span>

> <span data-ttu-id="24aaf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="24aaf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="24aaf-105">Cree un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="24aaf-105">Create a new [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="24aaf-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="24aaf-106">Prerequisites</span></span>
<span data-ttu-id="24aaf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="24aaf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="24aaf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="24aaf-109">Permission type</span></span>|<span data-ttu-id="24aaf-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="24aaf-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="24aaf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="24aaf-111">Delegated (work or school account)</span></span>|<span data-ttu-id="24aaf-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24aaf-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="24aaf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="24aaf-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="24aaf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24aaf-114">Not supported.</span></span>|
|<span data-ttu-id="24aaf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="24aaf-115">Application</span></span>|<span data-ttu-id="24aaf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24aaf-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="24aaf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="24aaf-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="24aaf-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="24aaf-118">Request headers</span></span>
|<span data-ttu-id="24aaf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24aaf-119">Header</span></span>|<span data-ttu-id="24aaf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="24aaf-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="24aaf-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="24aaf-121">Authorization</span></span>|<span data-ttu-id="24aaf-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="24aaf-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="24aaf-123">Accept</span><span class="sxs-lookup"><span data-stu-id="24aaf-123">Accept</span></span>|<span data-ttu-id="24aaf-124">application/json</span><span class="sxs-lookup"><span data-stu-id="24aaf-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="24aaf-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="24aaf-125">Request body</span></span>
<span data-ttu-id="24aaf-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="24aaf-126">In the request body, supply a JSON representation for the androidManagedAppRegistration object.</span></span>

<span data-ttu-id="24aaf-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="24aaf-127">The following table shows the properties that are required when you create the androidManagedAppRegistration.</span></span>

|<span data-ttu-id="24aaf-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="24aaf-128">Property</span></span>|<span data-ttu-id="24aaf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="24aaf-129">Type</span></span>|<span data-ttu-id="24aaf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="24aaf-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="24aaf-131">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="24aaf-131">createdDateTime</span></span>|<span data-ttu-id="24aaf-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="24aaf-132">DateTimeOffset</span></span>|<span data-ttu-id="24aaf-133">Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-133">Date and time of creation Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-134">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="24aaf-134">lastSyncDateTime</span></span>|<span data-ttu-id="24aaf-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="24aaf-135">DateTimeOffset</span></span>|<span data-ttu-id="24aaf-136">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="24aaf-136">Date and time of last the app synced with management service.</span></span> <span data-ttu-id="24aaf-137">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-137">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-138">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="24aaf-138">applicationVersion</span></span>|<span data-ttu-id="24aaf-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-139">String</span></span>|<span data-ttu-id="24aaf-140">Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-140">App version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-141">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="24aaf-141">managementSdkVersion</span></span>|<span data-ttu-id="24aaf-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-142">String</span></span>|<span data-ttu-id="24aaf-143">Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-143">App management SDK version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-144">platformVersion</span><span class="sxs-lookup"><span data-stu-id="24aaf-144">platformVersion</span></span>|<span data-ttu-id="24aaf-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-145">String</span></span>|<span data-ttu-id="24aaf-146">Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-146">Operating System version Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-147">deviceType</span><span class="sxs-lookup"><span data-stu-id="24aaf-147">deviceType</span></span>|<span data-ttu-id="24aaf-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-148">String</span></span>|<span data-ttu-id="24aaf-149">Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-149">Host device type Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-150">deviceTag</span><span class="sxs-lookup"><span data-stu-id="24aaf-150">deviceTag</span></span>|<span data-ttu-id="24aaf-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-151">String</span></span>|<span data-ttu-id="24aaf-152">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24aaf-152">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="24aaf-153">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="24aaf-153">Not guaranteed to relate apps in all conditions.</span></span> <span data-ttu-id="24aaf-154">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-154">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-155">deviceName</span><span class="sxs-lookup"><span data-stu-id="24aaf-155">deviceName</span></span>|<span data-ttu-id="24aaf-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-156">String</span></span>|<span data-ttu-id="24aaf-157">Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-157">Host device name Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-158">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="24aaf-158">flaggedReasons</span></span>|<span data-ttu-id="24aaf-159">colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-159">[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="24aaf-160">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="24aaf-160">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="24aaf-161">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="24aaf-161">E.g.</span></span> <span data-ttu-id="24aaf-162">aplicación que se está ejecutando en el dispositivo raíz Inherited desde [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="24aaf-162">app running on rooted device Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span></span> <span data-ttu-id="24aaf-163">Los valores posibles son: `none` y `rootedDevice`.</span><span class="sxs-lookup"><span data-stu-id="24aaf-163">Possible values are: `none`, `rootedDevice`.</span></span>|
|<span data-ttu-id="24aaf-164">userId</span><span class="sxs-lookup"><span data-stu-id="24aaf-164">userId</span></span>|<span data-ttu-id="24aaf-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-165">String</span></span>|<span data-ttu-id="24aaf-166">Identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24aaf-166">The user Id to who this app registration belongs.</span></span> <span data-ttu-id="24aaf-167">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-167">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-168">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="24aaf-168">appIdentifier</span></span>|[<span data-ttu-id="24aaf-169">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="24aaf-169">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="24aaf-170">Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-170">The app package Identifier Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-171">id</span><span class="sxs-lookup"><span data-stu-id="24aaf-171">id</span></span>|<span data-ttu-id="24aaf-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-172">String</span></span>|<span data-ttu-id="24aaf-173">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="24aaf-173">Key of the entity.</span></span> <span data-ttu-id="24aaf-174">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="24aaf-174">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|
|<span data-ttu-id="24aaf-175">version</span><span class="sxs-lookup"><span data-stu-id="24aaf-175">version</span></span>|<span data-ttu-id="24aaf-176">Cadena</span><span class="sxs-lookup"><span data-stu-id="24aaf-176">String</span></span>|<span data-ttu-id="24aaf-177">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="24aaf-177">Version of the entity.</span></span> <span data-ttu-id="24aaf-178">Heredado de [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="24aaf-178">Inherited from [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="24aaf-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24aaf-179">Response</span></span>
<span data-ttu-id="24aaf-180">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24aaf-180">If successful, this method returns a `201 Created` response code and a [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="24aaf-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24aaf-181">Example</span></span>
### <a name="request"></a><span data-ttu-id="24aaf-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="24aaf-182">Request</span></span>
<span data-ttu-id="24aaf-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="24aaf-183">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="24aaf-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24aaf-184">Response</span></span>
<span data-ttu-id="24aaf-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="24aaf-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



