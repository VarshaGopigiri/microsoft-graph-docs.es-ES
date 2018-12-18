---
title: Crear androidManagedStoreAppConfiguration
description: Crear un nuevo objeto androidManagedStoreAppConfiguration.
author: tfitzmac
ms.openlocfilehash: 1eb403a9547808969694b4e3712d4b2bcd1995f0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361071"
---
# <a name="create-androidmanagedstoreappconfiguration"></a><span data-ttu-id="664a5-103">Crear androidManagedStoreAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="664a5-103">Create androidManagedStoreAppConfiguration</span></span>

> <span data-ttu-id="664a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="664a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="664a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="664a5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="664a5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="664a5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="664a5-107">Crear un nuevo objeto [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="664a5-107">Create a new [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="664a5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="664a5-108">Prerequisites</span></span>
<span data-ttu-id="664a5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="664a5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="664a5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="664a5-111">Permission type</span></span>|<span data-ttu-id="664a5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="664a5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="664a5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="664a5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="664a5-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="664a5-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="664a5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="664a5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="664a5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="664a5-116">Not supported.</span></span>|
|<span data-ttu-id="664a5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="664a5-117">Application</span></span>|<span data-ttu-id="664a5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="664a5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="664a5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="664a5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="664a5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="664a5-120">Request headers</span></span>
|<span data-ttu-id="664a5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="664a5-121">Header</span></span>|<span data-ttu-id="664a5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="664a5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="664a5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="664a5-123">Authorization</span></span>|<span data-ttu-id="664a5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="664a5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="664a5-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="664a5-125">Accept</span></span>|<span data-ttu-id="664a5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="664a5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="664a5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="664a5-127">Request body</span></span>
<span data-ttu-id="664a5-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidManagedStoreAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="664a5-128">In the request body, supply a JSON representation for the androidManagedStoreAppConfiguration object.</span></span>

<span data-ttu-id="664a5-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidManagedStoreAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="664a5-129">The following table shows the properties that are required when you create the androidManagedStoreAppConfiguration.</span></span>

|<span data-ttu-id="664a5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="664a5-130">Property</span></span>|<span data-ttu-id="664a5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="664a5-131">Type</span></span>|<span data-ttu-id="664a5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="664a5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="664a5-133">id</span><span class="sxs-lookup"><span data-stu-id="664a5-133">id</span></span>|<span data-ttu-id="664a5-134">String</span><span class="sxs-lookup"><span data-stu-id="664a5-134">String</span></span>|<span data-ttu-id="664a5-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="664a5-135">Key of the entity.</span></span> <span data-ttu-id="664a5-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-137">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="664a5-137">targetedMobileApps</span></span>|<span data-ttu-id="664a5-138">Colección string</span><span class="sxs-lookup"><span data-stu-id="664a5-138">String collection</span></span>|<span data-ttu-id="664a5-139">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="664a5-139">the associated app.</span></span> <span data-ttu-id="664a5-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="664a5-141">roleScopeTagIds</span></span>|<span data-ttu-id="664a5-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="664a5-142">String collection</span></span>|<span data-ttu-id="664a5-143">Lista de etiquetas de ámbito para esta entidad de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="664a5-143">List of Scope Tags for this App configuration entity.</span></span> <span data-ttu-id="664a5-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="664a5-145">createdDateTime</span></span>|<span data-ttu-id="664a5-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="664a5-146">DateTimeOffset</span></span>|<span data-ttu-id="664a5-147">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="664a5-147">DateTime the object was created.</span></span> <span data-ttu-id="664a5-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-149">descripción</span><span class="sxs-lookup"><span data-stu-id="664a5-149">description</span></span>|<span data-ttu-id="664a5-150">String</span><span class="sxs-lookup"><span data-stu-id="664a5-150">String</span></span>|<span data-ttu-id="664a5-151">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="664a5-151">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="664a5-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="664a5-153">lastModifiedDateTime</span></span>|<span data-ttu-id="664a5-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="664a5-154">DateTimeOffset</span></span>|<span data-ttu-id="664a5-155">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="664a5-155">DateTime the object was last modified.</span></span> <span data-ttu-id="664a5-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-157">displayName</span><span class="sxs-lookup"><span data-stu-id="664a5-157">displayName</span></span>|<span data-ttu-id="664a5-158">String</span><span class="sxs-lookup"><span data-stu-id="664a5-158">String</span></span>|<span data-ttu-id="664a5-159">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="664a5-159">Admin provided name of the device configuration.</span></span> <span data-ttu-id="664a5-160">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-160">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-161">versión</span><span class="sxs-lookup"><span data-stu-id="664a5-161">version</span></span>|<span data-ttu-id="664a5-162">Int32</span><span class="sxs-lookup"><span data-stu-id="664a5-162">Int32</span></span>|<span data-ttu-id="664a5-163">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="664a5-163">Version of the device configuration.</span></span> <span data-ttu-id="664a5-164">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-164">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="664a5-165">packageId</span><span class="sxs-lookup"><span data-stu-id="664a5-165">packageId</span></span>|<span data-ttu-id="664a5-166">String</span><span class="sxs-lookup"><span data-stu-id="664a5-166">String</span></span>|<span data-ttu-id="664a5-167">Android Enterprise configuración paquete identificador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="664a5-167">Android Enterprise app configuration package id.</span></span>|
|<span data-ttu-id="664a5-168">payloadJson</span><span class="sxs-lookup"><span data-stu-id="664a5-168">payloadJson</span></span>|<span data-ttu-id="664a5-169">String</span><span class="sxs-lookup"><span data-stu-id="664a5-169">String</span></span>|<span data-ttu-id="664a5-170">Android Enterprise aplicación configuración JSON carga.</span><span class="sxs-lookup"><span data-stu-id="664a5-170">Android Enterprise app configuration JSON payload.</span></span>|
|<span data-ttu-id="664a5-171">permissionActions</span><span class="sxs-lookup"><span data-stu-id="664a5-171">permissionActions</span></span>|<span data-ttu-id="664a5-172">colección de [androidPermissionAction](../resources/intune-apps-androidpermissionaction.md)</span><span class="sxs-lookup"><span data-stu-id="664a5-172">[androidPermissionAction](../resources/intune-apps-androidpermissionaction.md) collection</span></span>|<span data-ttu-id="664a5-173">Lista de permisos de aplicación de Android y acciones de permiso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="664a5-173">List of Android app permissions and corresponding permission actions.</span></span>|



## <a name="response"></a><span data-ttu-id="664a5-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="664a5-174">Response</span></span>
<span data-ttu-id="664a5-175">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="664a5-175">If successful, this method returns a `201 Created` response code and a [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="664a5-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="664a5-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="664a5-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="664a5-177">Request</span></span>
<span data-ttu-id="664a5-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="664a5-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations
Content-type: application/json
Content-length: 623

{
  "@odata.type": "#microsoft.graph.androidManagedStoreAppConfiguration",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "packageId": "Package Id value",
  "payloadJson": "Payload Json value",
  "permissionActions": [
    {
      "@odata.type": "microsoft.graph.androidPermissionAction",
      "permission": "Permission value",
      "action": "autoGrant"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="664a5-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="664a5-179">Response</span></span>
<span data-ttu-id="664a5-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="664a5-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 731

{
  "@odata.type": "#microsoft.graph.androidManagedStoreAppConfiguration",
  "id": "919a9335-9335-919a-3593-9a9135939a91",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "packageId": "Package Id value",
  "payloadJson": "Payload Json value",
  "permissionActions": [
    {
      "@odata.type": "microsoft.graph.androidPermissionAction",
      "permission": "Permission value",
      "action": "autoGrant"
    }
  ]
}
```





