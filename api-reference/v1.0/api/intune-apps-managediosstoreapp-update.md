---
title: Actualizar managedIOSStoreApp
description: Actualice las propiedades de un objeto managedIOSStoreApp.
author: tfitzmac
ms.openlocfilehash: dc9884b591ea31dd6dc943492fc2924f032b876d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303545"
---
# <a name="update-managediosstoreapp"></a><span data-ttu-id="b7868-103">Actualizar managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="b7868-103">Update managedIOSStoreApp</span></span>

> <span data-ttu-id="b7868-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b7868-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b7868-105">Actualice las propiedades de un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-105">Update the properties of a [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b7868-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b7868-106">Prerequisites</span></span>
<span data-ttu-id="b7868-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7868-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7868-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7868-109">Permission type</span></span>|<span data-ttu-id="b7868-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7868-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b7868-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7868-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b7868-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b7868-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b7868-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7868-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b7868-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7868-114">Not supported.</span></span>|
|<span data-ttu-id="b7868-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7868-115">Application</span></span>|<span data-ttu-id="b7868-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7868-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b7868-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7868-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="b7868-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7868-118">Request headers</span></span>
|<span data-ttu-id="b7868-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7868-119">Header</span></span>|<span data-ttu-id="b7868-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7868-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b7868-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b7868-121">Authorization</span></span>|<span data-ttu-id="b7868-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b7868-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b7868-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b7868-123">Accept</span></span>|<span data-ttu-id="b7868-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b7868-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b7868-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7868-125">Request body</span></span>
<span data-ttu-id="b7868-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-126">In the request body, supply a JSON representation for the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>

<span data-ttu-id="b7868-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-127">The following table shows the properties that are required when you create the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span></span>

|<span data-ttu-id="b7868-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b7868-128">Property</span></span>|<span data-ttu-id="b7868-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7868-129">Type</span></span>|<span data-ttu-id="b7868-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7868-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b7868-131">id</span><span class="sxs-lookup"><span data-stu-id="b7868-131">id</span></span>|<span data-ttu-id="b7868-132">String</span><span class="sxs-lookup"><span data-stu-id="b7868-132">String</span></span>|<span data-ttu-id="b7868-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b7868-133">Key of the entity.</span></span> <span data-ttu-id="b7868-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-135">displayName</span><span class="sxs-lookup"><span data-stu-id="b7868-135">displayName</span></span>|<span data-ttu-id="b7868-136">String</span><span class="sxs-lookup"><span data-stu-id="b7868-136">String</span></span>|<span data-ttu-id="b7868-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="b7868-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="b7868-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-139">descripción</span><span class="sxs-lookup"><span data-stu-id="b7868-139">description</span></span>|<span data-ttu-id="b7868-140">String</span><span class="sxs-lookup"><span data-stu-id="b7868-140">String</span></span>|<span data-ttu-id="b7868-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-141">The description of the app.</span></span> <span data-ttu-id="b7868-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-143">publicador</span><span class="sxs-lookup"><span data-stu-id="b7868-143">publisher</span></span>|<span data-ttu-id="b7868-144">String</span><span class="sxs-lookup"><span data-stu-id="b7868-144">String</span></span>|<span data-ttu-id="b7868-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-145">The publisher of the app.</span></span> <span data-ttu-id="b7868-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="b7868-147">largeIcon</span></span>|[<span data-ttu-id="b7868-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="b7868-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="b7868-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="b7868-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="b7868-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b7868-151">createdDateTime</span></span>|<span data-ttu-id="b7868-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b7868-152">DateTimeOffset</span></span>|<span data-ttu-id="b7868-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-153">The date and time the app was created.</span></span> <span data-ttu-id="b7868-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b7868-155">lastModifiedDateTime</span></span>|<span data-ttu-id="b7868-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b7868-156">DateTimeOffset</span></span>|<span data-ttu-id="b7868-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-157">The date and time the app was last modified.</span></span> <span data-ttu-id="b7868-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="b7868-159">isFeatured</span></span>|<span data-ttu-id="b7868-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="b7868-160">Boolean</span></span>|<span data-ttu-id="b7868-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="b7868-162">privacyInformationUrl</span></span>|<span data-ttu-id="b7868-163">String</span><span class="sxs-lookup"><span data-stu-id="b7868-163">String</span></span>|<span data-ttu-id="b7868-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="b7868-164">The privacy statement Url.</span></span> <span data-ttu-id="b7868-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="b7868-166">informationUrl</span></span>|<span data-ttu-id="b7868-167">String</span><span class="sxs-lookup"><span data-stu-id="b7868-167">String</span></span>|<span data-ttu-id="b7868-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b7868-168">The more information Url.</span></span> <span data-ttu-id="b7868-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-170">owner</span><span class="sxs-lookup"><span data-stu-id="b7868-170">owner</span></span>|<span data-ttu-id="b7868-171">String</span><span class="sxs-lookup"><span data-stu-id="b7868-171">String</span></span>|<span data-ttu-id="b7868-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-172">The owner of the app.</span></span> <span data-ttu-id="b7868-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-174">developer</span><span class="sxs-lookup"><span data-stu-id="b7868-174">developer</span></span>|<span data-ttu-id="b7868-175">String</span><span class="sxs-lookup"><span data-stu-id="b7868-175">String</span></span>|<span data-ttu-id="b7868-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-176">The developer of the app.</span></span> <span data-ttu-id="b7868-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-178">notas</span><span class="sxs-lookup"><span data-stu-id="b7868-178">notes</span></span>|<span data-ttu-id="b7868-179">String</span><span class="sxs-lookup"><span data-stu-id="b7868-179">String</span></span>|<span data-ttu-id="b7868-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-180">Notes for the app.</span></span> <span data-ttu-id="b7868-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b7868-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="b7868-182">publishingState</span></span>|[<span data-ttu-id="b7868-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="b7868-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="b7868-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-184">The publishing state for the app.</span></span> <span data-ttu-id="b7868-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="b7868-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="b7868-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="b7868-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="b7868-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="b7868-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="b7868-188">appAvailability</span></span>|[<span data-ttu-id="b7868-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="b7868-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="b7868-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-190">The Application's availability.</span></span> <span data-ttu-id="b7868-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="b7868-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="b7868-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="b7868-193">versión</span><span class="sxs-lookup"><span data-stu-id="b7868-193">version</span></span>|<span data-ttu-id="b7868-194">String</span><span class="sxs-lookup"><span data-stu-id="b7868-194">String</span></span>|<span data-ttu-id="b7868-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-195">The Application's version.</span></span> <span data-ttu-id="b7868-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="b7868-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="b7868-197">bundleId</span><span class="sxs-lookup"><span data-stu-id="b7868-197">bundleId</span></span>|<span data-ttu-id="b7868-198">String</span><span class="sxs-lookup"><span data-stu-id="b7868-198">String</span></span>|<span data-ttu-id="b7868-199">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-199">The app's Bundle ID.</span></span>|
|<span data-ttu-id="b7868-200">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="b7868-200">appStoreUrl</span></span>|<span data-ttu-id="b7868-201">String</span><span class="sxs-lookup"><span data-stu-id="b7868-201">String</span></span>|<span data-ttu-id="b7868-202">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="b7868-202">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="b7868-203">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="b7868-203">applicableDeviceType</span></span>|[<span data-ttu-id="b7868-204">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="b7868-204">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="b7868-205">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7868-205">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="b7868-206">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b7868-206">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="b7868-207">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b7868-207">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="b7868-208">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="b7868-208">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="b7868-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7868-209">Response</span></span>
<span data-ttu-id="b7868-210">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7868-210">If successful, this method returns a `200 OK` response code and an updated [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b7868-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7868-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="b7868-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7868-212">Request</span></span>
<span data-ttu-id="b7868-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7868-213">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="b7868-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7868-214">Response</span></span>
<span data-ttu-id="b7868-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b7868-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



