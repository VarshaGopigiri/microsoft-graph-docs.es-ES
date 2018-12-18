---
title: Crear iosStoreApp
description: Cree un objeto iosStoreApp.
author: tfitzmac
ms.openlocfilehash: 9c7b39239861a29f640077c10188c84493d1a6b4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332819"
---
# <a name="create-iosstoreapp"></a><span data-ttu-id="ac62e-103">Crear iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="ac62e-103">Create iosStoreApp</span></span>

> <span data-ttu-id="ac62e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ac62e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ac62e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ac62e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ac62e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ac62e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ac62e-107">Cree un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-107">Create a new [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ac62e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ac62e-108">Prerequisites</span></span>
<span data-ttu-id="ac62e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ac62e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ac62e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac62e-111">Permission type</span></span>|<span data-ttu-id="ac62e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac62e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ac62e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac62e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ac62e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ac62e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ac62e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac62e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ac62e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac62e-116">Not supported.</span></span>|
|<span data-ttu-id="ac62e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac62e-117">Application</span></span>|<span data-ttu-id="ac62e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac62e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ac62e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac62e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="ac62e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac62e-120">Request headers</span></span>
|<span data-ttu-id="ac62e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac62e-121">Header</span></span>|<span data-ttu-id="ac62e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ac62e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ac62e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ac62e-123">Authorization</span></span>|<span data-ttu-id="ac62e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ac62e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ac62e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ac62e-125">Accept</span></span>|<span data-ttu-id="ac62e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ac62e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ac62e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac62e-127">Request body</span></span>
<span data-ttu-id="ac62e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="ac62e-128">In the request body, supply a JSON representation for the iosStoreApp object.</span></span>

<span data-ttu-id="ac62e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="ac62e-129">The following table shows the properties that are required when you create the iosStoreApp.</span></span>

|<span data-ttu-id="ac62e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac62e-130">Property</span></span>|<span data-ttu-id="ac62e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac62e-131">Type</span></span>|<span data-ttu-id="ac62e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac62e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ac62e-133">id</span><span class="sxs-lookup"><span data-stu-id="ac62e-133">id</span></span>|<span data-ttu-id="ac62e-134">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-134">String</span></span>|<span data-ttu-id="ac62e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ac62e-135">Key of the entity.</span></span> <span data-ttu-id="ac62e-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-137">displayName</span><span class="sxs-lookup"><span data-stu-id="ac62e-137">displayName</span></span>|<span data-ttu-id="ac62e-138">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-138">String</span></span>|<span data-ttu-id="ac62e-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="ac62e-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="ac62e-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-141">descripción</span><span class="sxs-lookup"><span data-stu-id="ac62e-141">description</span></span>|<span data-ttu-id="ac62e-142">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-142">String</span></span>|<span data-ttu-id="ac62e-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-143">The description of the app.</span></span> <span data-ttu-id="ac62e-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-145">publicador</span><span class="sxs-lookup"><span data-stu-id="ac62e-145">publisher</span></span>|<span data-ttu-id="ac62e-146">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-146">String</span></span>|<span data-ttu-id="ac62e-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-147">The publisher of the app.</span></span> <span data-ttu-id="ac62e-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="ac62e-149">largeIcon</span></span>|[<span data-ttu-id="ac62e-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="ac62e-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="ac62e-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="ac62e-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="ac62e-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ac62e-153">createdDateTime</span></span>|<span data-ttu-id="ac62e-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac62e-154">DateTimeOffset</span></span>|<span data-ttu-id="ac62e-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-155">The date and time the app was created.</span></span> <span data-ttu-id="ac62e-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ac62e-157">lastModifiedDateTime</span></span>|<span data-ttu-id="ac62e-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac62e-158">DateTimeOffset</span></span>|<span data-ttu-id="ac62e-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-159">The date and time the app was last modified.</span></span> <span data-ttu-id="ac62e-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="ac62e-161">isFeatured</span></span>|<span data-ttu-id="ac62e-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="ac62e-162">Boolean</span></span>|<span data-ttu-id="ac62e-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="ac62e-164">privacyInformationUrl</span></span>|<span data-ttu-id="ac62e-165">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-165">String</span></span>|<span data-ttu-id="ac62e-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="ac62e-166">The privacy statement Url.</span></span> <span data-ttu-id="ac62e-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="ac62e-168">informationUrl</span></span>|<span data-ttu-id="ac62e-169">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-169">String</span></span>|<span data-ttu-id="ac62e-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ac62e-170">The more information Url.</span></span> <span data-ttu-id="ac62e-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-172">owner</span><span class="sxs-lookup"><span data-stu-id="ac62e-172">owner</span></span>|<span data-ttu-id="ac62e-173">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-173">String</span></span>|<span data-ttu-id="ac62e-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-174">The owner of the app.</span></span> <span data-ttu-id="ac62e-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-176">developer</span><span class="sxs-lookup"><span data-stu-id="ac62e-176">developer</span></span>|<span data-ttu-id="ac62e-177">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-177">String</span></span>|<span data-ttu-id="ac62e-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-178">The developer of the app.</span></span> <span data-ttu-id="ac62e-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-180">notas</span><span class="sxs-lookup"><span data-stu-id="ac62e-180">notes</span></span>|<span data-ttu-id="ac62e-181">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-181">String</span></span>|<span data-ttu-id="ac62e-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-182">Notes for the app.</span></span> <span data-ttu-id="ac62e-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="ac62e-184">uploadState</span></span>|<span data-ttu-id="ac62e-185">Int32</span><span class="sxs-lookup"><span data-stu-id="ac62e-185">Int32</span></span>|<span data-ttu-id="ac62e-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="ac62e-186">The upload state.</span></span> <span data-ttu-id="ac62e-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="ac62e-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="ac62e-188">publishingState</span></span>|[<span data-ttu-id="ac62e-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="ac62e-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="ac62e-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-190">The publishing state for the app.</span></span> <span data-ttu-id="ac62e-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="ac62e-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="ac62e-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac62e-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="ac62e-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="ac62e-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="ac62e-194">bundleId</span><span class="sxs-lookup"><span data-stu-id="ac62e-194">bundleId</span></span>|<span data-ttu-id="ac62e-195">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-195">String</span></span>|<span data-ttu-id="ac62e-196">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="ac62e-196">The Identity Name.</span></span>|
|<span data-ttu-id="ac62e-197">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="ac62e-197">appStoreUrl</span></span>|<span data-ttu-id="ac62e-198">String</span><span class="sxs-lookup"><span data-stu-id="ac62e-198">String</span></span>|<span data-ttu-id="ac62e-199">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="ac62e-199">The Apple App Store URL</span></span>|
|<span data-ttu-id="ac62e-200">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="ac62e-200">applicableDeviceType</span></span>|[<span data-ttu-id="ac62e-201">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="ac62e-201">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="ac62e-202">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac62e-202">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="ac62e-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ac62e-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="ac62e-204">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ac62e-204">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="ac62e-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="ac62e-205">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="ac62e-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac62e-206">Response</span></span>
<span data-ttu-id="ac62e-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac62e-207">If successful, this method returns a `201 Created` response code and a [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ac62e-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac62e-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="ac62e-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac62e-209">Request</span></span>
<span data-ttu-id="ac62e-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac62e-210">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1092

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
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

### <a name="response"></a><span data-ttu-id="ac62e-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac62e-211">Response</span></span>
<span data-ttu-id="ac62e-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac62e-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1200

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
  "id": "a04adbe2-dbe2-a04a-e2db-4aa0e2db4aa0",
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





