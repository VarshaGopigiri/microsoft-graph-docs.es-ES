---
title: Actualizar androidManagedStoreAppConfiguration
description: Actualizar las propiedades de un objeto androidManagedStoreAppConfiguration.
author: tfitzmac
ms.openlocfilehash: a2643ac3f7ea23b500315a06505f5bb378ee0d58
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341261"
---
# <a name="update-androidmanagedstoreappconfiguration"></a><span data-ttu-id="56b25-103">Actualizar androidManagedStoreAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="56b25-103">Update androidManagedStoreAppConfiguration</span></span>

> <span data-ttu-id="56b25-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="56b25-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="56b25-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="56b25-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="56b25-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56b25-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56b25-107">Actualizar las propiedades de un objeto [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="56b25-107">Update the properties of a [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56b25-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56b25-108">Prerequisites</span></span>
<span data-ttu-id="56b25-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="56b25-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="56b25-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56b25-111">Permission type</span></span>|<span data-ttu-id="56b25-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56b25-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56b25-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56b25-113">Delegated (work or school account)</span></span>|<span data-ttu-id="56b25-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56b25-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="56b25-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56b25-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56b25-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56b25-116">Not supported.</span></span>|
|<span data-ttu-id="56b25-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56b25-117">Application</span></span>|<span data-ttu-id="56b25-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56b25-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56b25-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56b25-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="56b25-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56b25-120">Request headers</span></span>
|<span data-ttu-id="56b25-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56b25-121">Header</span></span>|<span data-ttu-id="56b25-122">Valor</span><span class="sxs-lookup"><span data-stu-id="56b25-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56b25-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="56b25-123">Authorization</span></span>|<span data-ttu-id="56b25-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56b25-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="56b25-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="56b25-125">Accept</span></span>|<span data-ttu-id="56b25-126">application/json</span><span class="sxs-lookup"><span data-stu-id="56b25-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56b25-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56b25-127">Request body</span></span>
<span data-ttu-id="56b25-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="56b25-128">In the request body, supply a JSON representation for the [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) object.</span></span>

<span data-ttu-id="56b25-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="56b25-129">The following table shows the properties that are required when you create the [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md).</span></span>

|<span data-ttu-id="56b25-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56b25-130">Property</span></span>|<span data-ttu-id="56b25-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="56b25-131">Type</span></span>|<span data-ttu-id="56b25-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="56b25-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56b25-133">id</span><span class="sxs-lookup"><span data-stu-id="56b25-133">id</span></span>|<span data-ttu-id="56b25-134">String</span><span class="sxs-lookup"><span data-stu-id="56b25-134">String</span></span>|<span data-ttu-id="56b25-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56b25-135">Key of the entity.</span></span> <span data-ttu-id="56b25-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-137">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="56b25-137">targetedMobileApps</span></span>|<span data-ttu-id="56b25-138">Colección string</span><span class="sxs-lookup"><span data-stu-id="56b25-138">String collection</span></span>|<span data-ttu-id="56b25-139">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="56b25-139">the associated app.</span></span> <span data-ttu-id="56b25-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="56b25-141">roleScopeTagIds</span></span>|<span data-ttu-id="56b25-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="56b25-142">String collection</span></span>|<span data-ttu-id="56b25-143">Lista de etiquetas de ámbito para esta entidad de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56b25-143">List of Scope Tags for this App configuration entity.</span></span> <span data-ttu-id="56b25-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="56b25-145">createdDateTime</span></span>|<span data-ttu-id="56b25-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56b25-146">DateTimeOffset</span></span>|<span data-ttu-id="56b25-147">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="56b25-147">DateTime the object was created.</span></span> <span data-ttu-id="56b25-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-149">descripción</span><span class="sxs-lookup"><span data-stu-id="56b25-149">description</span></span>|<span data-ttu-id="56b25-150">String</span><span class="sxs-lookup"><span data-stu-id="56b25-150">String</span></span>|<span data-ttu-id="56b25-151">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56b25-151">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="56b25-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="56b25-153">lastModifiedDateTime</span></span>|<span data-ttu-id="56b25-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56b25-154">DateTimeOffset</span></span>|<span data-ttu-id="56b25-155">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="56b25-155">DateTime the object was last modified.</span></span> <span data-ttu-id="56b25-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-157">displayName</span><span class="sxs-lookup"><span data-stu-id="56b25-157">displayName</span></span>|<span data-ttu-id="56b25-158">String</span><span class="sxs-lookup"><span data-stu-id="56b25-158">String</span></span>|<span data-ttu-id="56b25-159">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56b25-159">Admin provided name of the device configuration.</span></span> <span data-ttu-id="56b25-160">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-160">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-161">versión</span><span class="sxs-lookup"><span data-stu-id="56b25-161">version</span></span>|<span data-ttu-id="56b25-162">Int32</span><span class="sxs-lookup"><span data-stu-id="56b25-162">Int32</span></span>|<span data-ttu-id="56b25-163">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56b25-163">Version of the device configuration.</span></span> <span data-ttu-id="56b25-164">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-164">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="56b25-165">packageId</span><span class="sxs-lookup"><span data-stu-id="56b25-165">packageId</span></span>|<span data-ttu-id="56b25-166">String</span><span class="sxs-lookup"><span data-stu-id="56b25-166">String</span></span>|<span data-ttu-id="56b25-167">Android Enterprise configuración paquete identificador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56b25-167">Android Enterprise app configuration package id.</span></span>|
|<span data-ttu-id="56b25-168">payloadJson</span><span class="sxs-lookup"><span data-stu-id="56b25-168">payloadJson</span></span>|<span data-ttu-id="56b25-169">String</span><span class="sxs-lookup"><span data-stu-id="56b25-169">String</span></span>|<span data-ttu-id="56b25-170">Android Enterprise aplicación configuración JSON carga.</span><span class="sxs-lookup"><span data-stu-id="56b25-170">Android Enterprise app configuration JSON payload.</span></span>|
|<span data-ttu-id="56b25-171">permissionActions</span><span class="sxs-lookup"><span data-stu-id="56b25-171">permissionActions</span></span>|<span data-ttu-id="56b25-172">colección de [androidPermissionAction](../resources/intune-apps-androidpermissionaction.md)</span><span class="sxs-lookup"><span data-stu-id="56b25-172">[androidPermissionAction](../resources/intune-apps-androidpermissionaction.md) collection</span></span>|<span data-ttu-id="56b25-173">Lista de permisos de aplicación de Android y acciones de permiso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="56b25-173">List of Android app permissions and corresponding permission actions.</span></span>|



## <a name="response"></a><span data-ttu-id="56b25-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56b25-174">Response</span></span>
<span data-ttu-id="56b25-175">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56b25-175">If successful, this method returns a `200 OK` response code and an updated [androidManagedStoreAppConfiguration](../resources/intune-apps-androidmanagedstoreappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56b25-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56b25-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="56b25-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56b25-177">Request</span></span>
<span data-ttu-id="56b25-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56b25-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
Content-type: application/json
Content-length: 549

{
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

### <a name="response"></a><span data-ttu-id="56b25-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56b25-179">Response</span></span>
<span data-ttu-id="56b25-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56b25-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





