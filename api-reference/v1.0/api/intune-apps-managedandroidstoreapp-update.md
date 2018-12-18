---
title: Actualizar managedAndroidStoreApp
description: Actualice las propiedades de un objeto managedAndroidStoreApp.
author: tfitzmac
ms.openlocfilehash: c592238c7c48939b47dfc772a93dea4f07f7bf06
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327646"
---
# <a name="update-managedandroidstoreapp"></a><span data-ttu-id="3e37b-103">Actualizar managedAndroidStoreApp</span><span class="sxs-lookup"><span data-stu-id="3e37b-103">Update managedAndroidStoreApp</span></span>

> <span data-ttu-id="3e37b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3e37b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3e37b-105">Actualice las propiedades de un objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-105">Update the properties of a [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3e37b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3e37b-106">Prerequisites</span></span>
<span data-ttu-id="3e37b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3e37b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3e37b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3e37b-109">Permission type</span></span>|<span data-ttu-id="3e37b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3e37b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3e37b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3e37b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3e37b-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3e37b-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3e37b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3e37b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3e37b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3e37b-114">Not supported.</span></span>|
|<span data-ttu-id="3e37b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3e37b-115">Application</span></span>|<span data-ttu-id="3e37b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3e37b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3e37b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3e37b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="3e37b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3e37b-118">Request headers</span></span>
|<span data-ttu-id="3e37b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e37b-119">Header</span></span>|<span data-ttu-id="3e37b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3e37b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3e37b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3e37b-121">Authorization</span></span>|<span data-ttu-id="3e37b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3e37b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3e37b-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3e37b-123">Accept</span></span>|<span data-ttu-id="3e37b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3e37b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3e37b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3e37b-125">Request body</span></span>
<span data-ttu-id="3e37b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-126">In the request body, supply a JSON representation for the [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object.</span></span>

<span data-ttu-id="3e37b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-127">The following table shows the properties that are required when you create the [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span></span>

|<span data-ttu-id="3e37b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3e37b-128">Property</span></span>|<span data-ttu-id="3e37b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e37b-129">Type</span></span>|<span data-ttu-id="3e37b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e37b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3e37b-131">id</span><span class="sxs-lookup"><span data-stu-id="3e37b-131">id</span></span>|<span data-ttu-id="3e37b-132">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-132">String</span></span>|<span data-ttu-id="3e37b-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3e37b-133">Key of the entity.</span></span> <span data-ttu-id="3e37b-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-135">displayName</span><span class="sxs-lookup"><span data-stu-id="3e37b-135">displayName</span></span>|<span data-ttu-id="3e37b-136">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-136">String</span></span>|<span data-ttu-id="3e37b-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="3e37b-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="3e37b-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-139">descripción</span><span class="sxs-lookup"><span data-stu-id="3e37b-139">description</span></span>|<span data-ttu-id="3e37b-140">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-140">String</span></span>|<span data-ttu-id="3e37b-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-141">The description of the app.</span></span> <span data-ttu-id="3e37b-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-143">publicador</span><span class="sxs-lookup"><span data-stu-id="3e37b-143">publisher</span></span>|<span data-ttu-id="3e37b-144">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-144">String</span></span>|<span data-ttu-id="3e37b-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-145">The publisher of the app.</span></span> <span data-ttu-id="3e37b-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="3e37b-147">largeIcon</span></span>|[<span data-ttu-id="3e37b-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="3e37b-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="3e37b-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="3e37b-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="3e37b-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3e37b-151">createdDateTime</span></span>|<span data-ttu-id="3e37b-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3e37b-152">DateTimeOffset</span></span>|<span data-ttu-id="3e37b-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-153">The date and time the app was created.</span></span> <span data-ttu-id="3e37b-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3e37b-155">lastModifiedDateTime</span></span>|<span data-ttu-id="3e37b-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3e37b-156">DateTimeOffset</span></span>|<span data-ttu-id="3e37b-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-157">The date and time the app was last modified.</span></span> <span data-ttu-id="3e37b-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="3e37b-159">isFeatured</span></span>|<span data-ttu-id="3e37b-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="3e37b-160">Boolean</span></span>|<span data-ttu-id="3e37b-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="3e37b-162">privacyInformationUrl</span></span>|<span data-ttu-id="3e37b-163">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-163">String</span></span>|<span data-ttu-id="3e37b-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="3e37b-164">The privacy statement Url.</span></span> <span data-ttu-id="3e37b-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="3e37b-166">informationUrl</span></span>|<span data-ttu-id="3e37b-167">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-167">String</span></span>|<span data-ttu-id="3e37b-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3e37b-168">The more information Url.</span></span> <span data-ttu-id="3e37b-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-170">owner</span><span class="sxs-lookup"><span data-stu-id="3e37b-170">owner</span></span>|<span data-ttu-id="3e37b-171">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-171">String</span></span>|<span data-ttu-id="3e37b-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-172">The owner of the app.</span></span> <span data-ttu-id="3e37b-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-174">developer</span><span class="sxs-lookup"><span data-stu-id="3e37b-174">developer</span></span>|<span data-ttu-id="3e37b-175">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-175">String</span></span>|<span data-ttu-id="3e37b-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-176">The developer of the app.</span></span> <span data-ttu-id="3e37b-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-178">notas</span><span class="sxs-lookup"><span data-stu-id="3e37b-178">notes</span></span>|<span data-ttu-id="3e37b-179">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-179">String</span></span>|<span data-ttu-id="3e37b-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-180">Notes for the app.</span></span> <span data-ttu-id="3e37b-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3e37b-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="3e37b-182">publishingState</span></span>|[<span data-ttu-id="3e37b-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="3e37b-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="3e37b-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-184">The publishing state for the app.</span></span> <span data-ttu-id="3e37b-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="3e37b-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="3e37b-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="3e37b-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="3e37b-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="3e37b-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="3e37b-188">appAvailability</span></span>|[<span data-ttu-id="3e37b-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="3e37b-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="3e37b-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-190">The Application's availability.</span></span> <span data-ttu-id="3e37b-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="3e37b-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="3e37b-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="3e37b-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="3e37b-193">versión</span><span class="sxs-lookup"><span data-stu-id="3e37b-193">version</span></span>|<span data-ttu-id="3e37b-194">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-194">String</span></span>|<span data-ttu-id="3e37b-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-195">The Application's version.</span></span> <span data-ttu-id="3e37b-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="3e37b-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="3e37b-197">packageId</span><span class="sxs-lookup"><span data-stu-id="3e37b-197">packageId</span></span>|<span data-ttu-id="3e37b-198">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-198">String</span></span>|<span data-ttu-id="3e37b-199">El identificador de paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e37b-199">The app's package ID.</span></span>|
|<span data-ttu-id="3e37b-200">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="3e37b-200">appStoreUrl</span></span>|<span data-ttu-id="3e37b-201">String</span><span class="sxs-lookup"><span data-stu-id="3e37b-201">String</span></span>|<span data-ttu-id="3e37b-202">La AppStoreUrl de Android.</span><span class="sxs-lookup"><span data-stu-id="3e37b-202">The Android AppStoreUrl.</span></span>|
|<span data-ttu-id="3e37b-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3e37b-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="3e37b-204">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3e37b-204">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="3e37b-205">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="3e37b-205">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="3e37b-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e37b-206">Response</span></span>
<span data-ttu-id="3e37b-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e37b-207">If successful, this method returns a `200 OK` response code and an updated [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3e37b-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e37b-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="3e37b-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3e37b-209">Request</span></span>
<span data-ttu-id="3e37b-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e37b-210">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1016

{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  }
}
```

### <a name="response"></a><span data-ttu-id="3e37b-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e37b-211">Response</span></span>
<span data-ttu-id="3e37b-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3e37b-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1188

{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
  "id": "89e7e991-e991-89e7-91e9-e78991e9e789",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  }
}
```



