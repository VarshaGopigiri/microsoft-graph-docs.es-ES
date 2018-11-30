---
title: Actualizar managedAndroidStoreApp
description: Actualice las propiedades de un objeto managedAndroidStoreApp.
ms.openlocfilehash: c8fbca85fce75475f0ccc0e38ffcdd08ec76a215
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088069"
---
# <a name="update-managedandroidstoreapp"></a><span data-ttu-id="bb215-103">Actualizar managedAndroidStoreApp</span><span class="sxs-lookup"><span data-stu-id="bb215-103">Update managedAndroidStoreApp</span></span>

> <span data-ttu-id="bb215-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb215-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb215-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb215-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bb215-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bb215-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb215-107">Actualice las propiedades de un objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-107">Update the properties of a [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb215-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bb215-108">Prerequisites</span></span>
<span data-ttu-id="bb215-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb215-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb215-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb215-111">Permission type</span></span>|<span data-ttu-id="bb215-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb215-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb215-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb215-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bb215-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb215-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bb215-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb215-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb215-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb215-116">Not supported.</span></span>|
|<span data-ttu-id="bb215-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb215-117">Application</span></span>|<span data-ttu-id="bb215-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb215-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb215-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb215-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="bb215-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb215-120">Request headers</span></span>
|<span data-ttu-id="bb215-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb215-121">Header</span></span>|<span data-ttu-id="bb215-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bb215-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb215-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bb215-123">Authorization</span></span>|<span data-ttu-id="bb215-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bb215-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb215-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bb215-125">Accept</span></span>|<span data-ttu-id="bb215-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bb215-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb215-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb215-127">Request body</span></span>
<span data-ttu-id="bb215-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-128">In the request body, supply a JSON representation for the [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object.</span></span>

<span data-ttu-id="bb215-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-129">The following table shows the properties that are required when you create the [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span></span>

|<span data-ttu-id="bb215-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb215-130">Property</span></span>|<span data-ttu-id="bb215-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb215-131">Type</span></span>|<span data-ttu-id="bb215-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb215-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bb215-133">id</span><span class="sxs-lookup"><span data-stu-id="bb215-133">id</span></span>|<span data-ttu-id="bb215-134">String</span><span class="sxs-lookup"><span data-stu-id="bb215-134">String</span></span>|<span data-ttu-id="bb215-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bb215-135">Key of the entity.</span></span> <span data-ttu-id="bb215-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-137">displayName</span><span class="sxs-lookup"><span data-stu-id="bb215-137">displayName</span></span>|<span data-ttu-id="bb215-138">String</span><span class="sxs-lookup"><span data-stu-id="bb215-138">String</span></span>|<span data-ttu-id="bb215-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="bb215-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="bb215-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-141">descripción</span><span class="sxs-lookup"><span data-stu-id="bb215-141">description</span></span>|<span data-ttu-id="bb215-142">String</span><span class="sxs-lookup"><span data-stu-id="bb215-142">String</span></span>|<span data-ttu-id="bb215-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-143">The description of the app.</span></span> <span data-ttu-id="bb215-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-145">publicador</span><span class="sxs-lookup"><span data-stu-id="bb215-145">publisher</span></span>|<span data-ttu-id="bb215-146">String</span><span class="sxs-lookup"><span data-stu-id="bb215-146">String</span></span>|<span data-ttu-id="bb215-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-147">The publisher of the app.</span></span> <span data-ttu-id="bb215-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="bb215-149">largeIcon</span></span>|[<span data-ttu-id="bb215-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="bb215-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="bb215-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="bb215-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="bb215-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bb215-153">createdDateTime</span></span>|<span data-ttu-id="bb215-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb215-154">DateTimeOffset</span></span>|<span data-ttu-id="bb215-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-155">The date and time the app was created.</span></span> <span data-ttu-id="bb215-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bb215-157">lastModifiedDateTime</span></span>|<span data-ttu-id="bb215-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb215-158">DateTimeOffset</span></span>|<span data-ttu-id="bb215-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-159">The date and time the app was last modified.</span></span> <span data-ttu-id="bb215-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="bb215-161">isFeatured</span></span>|<span data-ttu-id="bb215-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="bb215-162">Boolean</span></span>|<span data-ttu-id="bb215-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="bb215-164">privacyInformationUrl</span></span>|<span data-ttu-id="bb215-165">String</span><span class="sxs-lookup"><span data-stu-id="bb215-165">String</span></span>|<span data-ttu-id="bb215-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="bb215-166">The privacy statement Url.</span></span> <span data-ttu-id="bb215-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="bb215-168">informationUrl</span></span>|<span data-ttu-id="bb215-169">String</span><span class="sxs-lookup"><span data-stu-id="bb215-169">String</span></span>|<span data-ttu-id="bb215-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="bb215-170">The more information Url.</span></span> <span data-ttu-id="bb215-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-172">owner</span><span class="sxs-lookup"><span data-stu-id="bb215-172">owner</span></span>|<span data-ttu-id="bb215-173">String</span><span class="sxs-lookup"><span data-stu-id="bb215-173">String</span></span>|<span data-ttu-id="bb215-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-174">The owner of the app.</span></span> <span data-ttu-id="bb215-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-176">developer</span><span class="sxs-lookup"><span data-stu-id="bb215-176">developer</span></span>|<span data-ttu-id="bb215-177">String</span><span class="sxs-lookup"><span data-stu-id="bb215-177">String</span></span>|<span data-ttu-id="bb215-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-178">The developer of the app.</span></span> <span data-ttu-id="bb215-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-180">notas</span><span class="sxs-lookup"><span data-stu-id="bb215-180">notes</span></span>|<span data-ttu-id="bb215-181">String</span><span class="sxs-lookup"><span data-stu-id="bb215-181">String</span></span>|<span data-ttu-id="bb215-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-182">Notes for the app.</span></span> <span data-ttu-id="bb215-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="bb215-184">uploadState</span></span>|<span data-ttu-id="bb215-185">Int32</span><span class="sxs-lookup"><span data-stu-id="bb215-185">Int32</span></span>|<span data-ttu-id="bb215-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="bb215-186">The upload state.</span></span> <span data-ttu-id="bb215-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb215-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="bb215-188">publishingState</span></span>|[<span data-ttu-id="bb215-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="bb215-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="bb215-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-190">The publishing state for the app.</span></span> <span data-ttu-id="bb215-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="bb215-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="bb215-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="bb215-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="bb215-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="bb215-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="bb215-194">appAvailability</span></span>|[<span data-ttu-id="bb215-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="bb215-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="bb215-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-196">The Application's availability.</span></span> <span data-ttu-id="bb215-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb215-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="bb215-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="bb215-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="bb215-199">versión</span><span class="sxs-lookup"><span data-stu-id="bb215-199">version</span></span>|<span data-ttu-id="bb215-200">String</span><span class="sxs-lookup"><span data-stu-id="bb215-200">String</span></span>|<span data-ttu-id="bb215-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-201">The Application's version.</span></span> <span data-ttu-id="bb215-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="bb215-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="bb215-203">packageId</span><span class="sxs-lookup"><span data-stu-id="bb215-203">packageId</span></span>|<span data-ttu-id="bb215-204">String</span><span class="sxs-lookup"><span data-stu-id="bb215-204">String</span></span>|<span data-ttu-id="bb215-205">El identificador de paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb215-205">The app's package ID.</span></span>|
|<span data-ttu-id="bb215-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="bb215-206">appStoreUrl</span></span>|<span data-ttu-id="bb215-207">String</span><span class="sxs-lookup"><span data-stu-id="bb215-207">String</span></span>|<span data-ttu-id="bb215-208">La AppStoreUrl de Android.</span><span class="sxs-lookup"><span data-stu-id="bb215-208">The Android AppStoreUrl.</span></span>|
|<span data-ttu-id="bb215-209">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bb215-209">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="bb215-210">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bb215-210">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="bb215-211">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="bb215-211">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="bb215-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb215-212">Response</span></span>
<span data-ttu-id="bb215-213">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb215-213">If successful, this method returns a `200 OK` response code and an updated [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb215-214">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb215-214">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb215-215">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb215-215">Request</span></span>
<span data-ttu-id="bb215-216">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb215-216">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1155

{
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "uploadState": 11,
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
    "v5_1": true,
    "v6_0": true,
    "v7_0": true,
    "v7_1": true,
    "v8_0": true,
    "v8_1": true,
    "v9_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="bb215-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb215-217">Response</span></span>
<span data-ttu-id="bb215-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb215-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1324

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
  "uploadState": 11,
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
    "v5_1": true,
    "v6_0": true,
    "v7_0": true,
    "v7_1": true,
    "v8_0": true,
    "v8_1": true,
    "v9_0": true
  }
}
```





