---
title: Crear androidForWorkMobileAppConfiguration
description: Crear un nuevo objeto androidForWorkMobileAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 013c4856bc40614b49108715b0d66b4af8f93890
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844417"
---
# <a name="create-androidforworkmobileappconfiguration"></a><span data-ttu-id="778b6-103">Crear androidForWorkMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="778b6-103">Create androidForWorkMobileAppConfiguration</span></span>

> <span data-ttu-id="778b6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="778b6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="778b6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="778b6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="778b6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="778b6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="778b6-107">Crear un nuevo objeto [androidForWorkMobileAppConfiguration](../resources/intune-apps-androidforworkmobileappconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="778b6-107">Create a new [androidForWorkMobileAppConfiguration](../resources/intune-apps-androidforworkmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="778b6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="778b6-108">Prerequisites</span></span>
<span data-ttu-id="778b6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="778b6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="778b6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="778b6-111">Permission type</span></span>|<span data-ttu-id="778b6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="778b6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="778b6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="778b6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="778b6-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="778b6-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="778b6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="778b6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="778b6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="778b6-116">Not supported.</span></span>|
|<span data-ttu-id="778b6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="778b6-117">Application</span></span>|<span data-ttu-id="778b6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="778b6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="778b6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="778b6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="778b6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="778b6-120">Request headers</span></span>
|<span data-ttu-id="778b6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="778b6-121">Header</span></span>|<span data-ttu-id="778b6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="778b6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="778b6-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="778b6-123">Authorization</span></span>|<span data-ttu-id="778b6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="778b6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="778b6-125">Accept</span><span class="sxs-lookup"><span data-stu-id="778b6-125">Accept</span></span>|<span data-ttu-id="778b6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="778b6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="778b6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="778b6-127">Request body</span></span>
<span data-ttu-id="778b6-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidForWorkMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="778b6-128">In the request body, supply a JSON representation for the androidForWorkMobileAppConfiguration object.</span></span>

<span data-ttu-id="778b6-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidForWorkMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="778b6-129">The following table shows the properties that are required when you create the androidForWorkMobileAppConfiguration.</span></span>

|<span data-ttu-id="778b6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="778b6-130">Property</span></span>|<span data-ttu-id="778b6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="778b6-131">Type</span></span>|<span data-ttu-id="778b6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="778b6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="778b6-133">id</span><span class="sxs-lookup"><span data-stu-id="778b6-133">id</span></span>|<span data-ttu-id="778b6-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="778b6-134">String</span></span>|<span data-ttu-id="778b6-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="778b6-135">Key of the entity.</span></span> <span data-ttu-id="778b6-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-137">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="778b6-137">targetedMobileApps</span></span>|<span data-ttu-id="778b6-138">Colección string</span><span class="sxs-lookup"><span data-stu-id="778b6-138">String collection</span></span>|<span data-ttu-id="778b6-139">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="778b6-139">the associated app.</span></span> <span data-ttu-id="778b6-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="778b6-141">roleScopeTagIds</span></span>|<span data-ttu-id="778b6-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="778b6-142">String collection</span></span>|<span data-ttu-id="778b6-143">Lista de etiquetas de ámbito para esta entidad de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="778b6-143">List of Scope Tags for this App configuration entity.</span></span> <span data-ttu-id="778b6-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="778b6-145">createdDateTime</span></span>|<span data-ttu-id="778b6-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="778b6-146">DateTimeOffset</span></span>|<span data-ttu-id="778b6-147">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="778b6-147">DateTime the object was created.</span></span> <span data-ttu-id="778b6-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-149">descripción</span><span class="sxs-lookup"><span data-stu-id="778b6-149">description</span></span>|<span data-ttu-id="778b6-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="778b6-150">String</span></span>|<span data-ttu-id="778b6-151">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="778b6-151">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="778b6-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="778b6-153">lastModifiedDateTime</span></span>|<span data-ttu-id="778b6-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="778b6-154">DateTimeOffset</span></span>|<span data-ttu-id="778b6-155">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="778b6-155">DateTime the object was last modified.</span></span> <span data-ttu-id="778b6-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-157">displayName</span><span class="sxs-lookup"><span data-stu-id="778b6-157">displayName</span></span>|<span data-ttu-id="778b6-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="778b6-158">String</span></span>|<span data-ttu-id="778b6-159">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="778b6-159">Admin provided name of the device configuration.</span></span> <span data-ttu-id="778b6-160">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-160">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-161">versión</span><span class="sxs-lookup"><span data-stu-id="778b6-161">version</span></span>|<span data-ttu-id="778b6-162">Int32</span><span class="sxs-lookup"><span data-stu-id="778b6-162">Int32</span></span>|<span data-ttu-id="778b6-163">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="778b6-163">Version of the device configuration.</span></span> <span data-ttu-id="778b6-164">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-164">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="778b6-165">packageId</span><span class="sxs-lookup"><span data-stu-id="778b6-165">packageId</span></span>|<span data-ttu-id="778b6-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="778b6-166">String</span></span>|<span data-ttu-id="778b6-167">Identificador de paquete de configuración de aplicación de Android para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="778b6-167">Android For Work app configuration package id.</span></span>|
|<span data-ttu-id="778b6-168">payloadJson</span><span class="sxs-lookup"><span data-stu-id="778b6-168">payloadJson</span></span>|<span data-ttu-id="778b6-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="778b6-169">String</span></span>|<span data-ttu-id="778b6-170">Carga JSON de configuración de aplicación de Android para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="778b6-170">Android For Work app configuration JSON payload.</span></span>|
|<span data-ttu-id="778b6-171">permissionActions</span><span class="sxs-lookup"><span data-stu-id="778b6-171">permissionActions</span></span>|<span data-ttu-id="778b6-172">colección de [androidPermissionAction](../resources/intune-apps-androidpermissionaction.md)</span><span class="sxs-lookup"><span data-stu-id="778b6-172">[androidPermissionAction](../resources/intune-apps-androidpermissionaction.md) collection</span></span>|<span data-ttu-id="778b6-173">Lista de permisos de aplicación de Android y acciones de permiso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="778b6-173">List of Android app permissions and corresponding permission actions.</span></span>|



## <a name="response"></a><span data-ttu-id="778b6-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="778b6-174">Response</span></span>
<span data-ttu-id="778b6-175">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidForWorkMobileAppConfiguration](../resources/intune-apps-androidforworkmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="778b6-175">If successful, this method returns a `201 Created` response code and a [androidForWorkMobileAppConfiguration](../resources/intune-apps-androidforworkmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="778b6-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="778b6-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="778b6-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="778b6-177">Request</span></span>
<span data-ttu-id="778b6-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="778b6-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations
Content-type: application/json
Content-length: 624

{
  "@odata.type": "#microsoft.graph.androidForWorkMobileAppConfiguration",
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

### <a name="response"></a><span data-ttu-id="778b6-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="778b6-179">Response</span></span>
<span data-ttu-id="778b6-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="778b6-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 732

{
  "@odata.type": "#microsoft.graph.androidForWorkMobileAppConfiguration",
  "id": "6204ae6d-ae6d-6204-6dae-04626dae0462",
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





