---
title: Actualizar managedIOSStoreApp
description: Actualice las propiedades de un objeto managedIOSStoreApp.
ms.openlocfilehash: feb77514d7b36e5915611168714d14e4c2705760
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029907"
---
# <a name="update-managediosstoreapp"></a><span data-ttu-id="5cebe-103">Actualizar managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="5cebe-103">Update managedIOSStoreApp</span></span>

> <span data-ttu-id="5cebe-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5cebe-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5cebe-105">Actualice las propiedades de un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-105">Update the properties of a [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5cebe-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5cebe-106">Prerequisites</span></span>
<span data-ttu-id="5cebe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5cebe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5cebe-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5cebe-109">Permission type</span></span>|<span data-ttu-id="5cebe-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5cebe-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5cebe-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5cebe-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5cebe-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cebe-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5cebe-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5cebe-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5cebe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5cebe-114">Not supported.</span></span>|
|<span data-ttu-id="5cebe-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5cebe-115">Application</span></span>|<span data-ttu-id="5cebe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5cebe-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5cebe-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5cebe-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="5cebe-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5cebe-118">Request headers</span></span>
|<span data-ttu-id="5cebe-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cebe-119">Header</span></span>|<span data-ttu-id="5cebe-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5cebe-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5cebe-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="5cebe-121">Authorization</span></span>|<span data-ttu-id="5cebe-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5cebe-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5cebe-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5cebe-123">Accept</span></span>|<span data-ttu-id="5cebe-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5cebe-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5cebe-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5cebe-125">Request body</span></span>
<span data-ttu-id="5cebe-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-126">In the request body, supply a JSON representation for the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>

<span data-ttu-id="5cebe-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-127">The following table shows the properties that are required when you create the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span></span>

|<span data-ttu-id="5cebe-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5cebe-128">Property</span></span>|<span data-ttu-id="5cebe-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cebe-129">Type</span></span>|<span data-ttu-id="5cebe-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cebe-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5cebe-131">id</span><span class="sxs-lookup"><span data-stu-id="5cebe-131">id</span></span>|<span data-ttu-id="5cebe-132">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-132">String</span></span>|<span data-ttu-id="5cebe-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5cebe-133">Key of the entity.</span></span> <span data-ttu-id="5cebe-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-135">displayName</span><span class="sxs-lookup"><span data-stu-id="5cebe-135">displayName</span></span>|<span data-ttu-id="5cebe-136">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-136">String</span></span>|<span data-ttu-id="5cebe-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="5cebe-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="5cebe-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-139">descripción</span><span class="sxs-lookup"><span data-stu-id="5cebe-139">description</span></span>|<span data-ttu-id="5cebe-140">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-140">String</span></span>|<span data-ttu-id="5cebe-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-141">The description of the app.</span></span> <span data-ttu-id="5cebe-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-143">publicador</span><span class="sxs-lookup"><span data-stu-id="5cebe-143">publisher</span></span>|<span data-ttu-id="5cebe-144">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-144">String</span></span>|<span data-ttu-id="5cebe-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-145">The publisher of the app.</span></span> <span data-ttu-id="5cebe-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="5cebe-147">largeIcon</span></span>|[<span data-ttu-id="5cebe-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5cebe-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="5cebe-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="5cebe-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="5cebe-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5cebe-151">createdDateTime</span></span>|<span data-ttu-id="5cebe-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5cebe-152">DateTimeOffset</span></span>|<span data-ttu-id="5cebe-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-153">The date and time the app was created.</span></span> <span data-ttu-id="5cebe-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5cebe-155">lastModifiedDateTime</span></span>|<span data-ttu-id="5cebe-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5cebe-156">DateTimeOffset</span></span>|<span data-ttu-id="5cebe-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-157">The date and time the app was last modified.</span></span> <span data-ttu-id="5cebe-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="5cebe-159">isFeatured</span></span>|<span data-ttu-id="5cebe-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cebe-160">Boolean</span></span>|<span data-ttu-id="5cebe-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="5cebe-162">privacyInformationUrl</span></span>|<span data-ttu-id="5cebe-163">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-163">String</span></span>|<span data-ttu-id="5cebe-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="5cebe-164">The privacy statement Url.</span></span> <span data-ttu-id="5cebe-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="5cebe-166">informationUrl</span></span>|<span data-ttu-id="5cebe-167">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-167">String</span></span>|<span data-ttu-id="5cebe-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5cebe-168">The more information Url.</span></span> <span data-ttu-id="5cebe-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-170">owner</span><span class="sxs-lookup"><span data-stu-id="5cebe-170">owner</span></span>|<span data-ttu-id="5cebe-171">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-171">String</span></span>|<span data-ttu-id="5cebe-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-172">The owner of the app.</span></span> <span data-ttu-id="5cebe-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-174">developer</span><span class="sxs-lookup"><span data-stu-id="5cebe-174">developer</span></span>|<span data-ttu-id="5cebe-175">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-175">String</span></span>|<span data-ttu-id="5cebe-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-176">The developer of the app.</span></span> <span data-ttu-id="5cebe-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-178">notas</span><span class="sxs-lookup"><span data-stu-id="5cebe-178">notes</span></span>|<span data-ttu-id="5cebe-179">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-179">String</span></span>|<span data-ttu-id="5cebe-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-180">Notes for the app.</span></span> <span data-ttu-id="5cebe-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="5cebe-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="5cebe-182">publishingState</span></span>|[<span data-ttu-id="5cebe-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="5cebe-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="5cebe-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-184">The publishing state for the app.</span></span> <span data-ttu-id="5cebe-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="5cebe-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="5cebe-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="5cebe-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="5cebe-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="5cebe-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="5cebe-188">appAvailability</span></span>|[<span data-ttu-id="5cebe-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="5cebe-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="5cebe-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-190">The Application's availability.</span></span> <span data-ttu-id="5cebe-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="5cebe-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="5cebe-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="5cebe-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="5cebe-193">versión</span><span class="sxs-lookup"><span data-stu-id="5cebe-193">version</span></span>|<span data-ttu-id="5cebe-194">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-194">String</span></span>|<span data-ttu-id="5cebe-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-195">The Application's version.</span></span> <span data-ttu-id="5cebe-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="5cebe-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="5cebe-197">bundleId</span><span class="sxs-lookup"><span data-stu-id="5cebe-197">bundleId</span></span>|<span data-ttu-id="5cebe-198">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-198">String</span></span>|<span data-ttu-id="5cebe-199">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-199">The app's Bundle ID.</span></span>|
|<span data-ttu-id="5cebe-200">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="5cebe-200">appStoreUrl</span></span>|<span data-ttu-id="5cebe-201">String</span><span class="sxs-lookup"><span data-stu-id="5cebe-201">String</span></span>|<span data-ttu-id="5cebe-202">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="5cebe-202">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="5cebe-203">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="5cebe-203">applicableDeviceType</span></span>|[<span data-ttu-id="5cebe-204">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="5cebe-204">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="5cebe-205">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cebe-205">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="5cebe-206">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5cebe-206">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="5cebe-207">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5cebe-207">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="5cebe-208">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="5cebe-208">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="5cebe-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cebe-209">Response</span></span>
<span data-ttu-id="5cebe-210">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5cebe-210">If successful, this method returns a `200 OK` response code and an updated [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5cebe-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5cebe-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="5cebe-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5cebe-212">Request</span></span>
<span data-ttu-id="5cebe-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5cebe-213">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1084

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="5cebe-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cebe-214">Response</span></span>
<span data-ttu-id="5cebe-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5cebe-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1256

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
  "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true
  }
}
```


