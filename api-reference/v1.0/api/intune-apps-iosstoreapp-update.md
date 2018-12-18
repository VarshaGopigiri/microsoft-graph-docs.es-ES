---
title: Actualizar iosStoreApp
description: Actualice las propiedades de un objeto iosStoreApp.
author: tfitzmac
ms.openlocfilehash: 8d1195120e1eab46f1e7a1b3ad95e6734d74e57f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360504"
---
# <a name="update-iosstoreapp"></a><span data-ttu-id="2be18-103">Actualizar iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="2be18-103">Update iosStoreApp</span></span>

> <span data-ttu-id="2be18-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2be18-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2be18-105">Actualice las propiedades de un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-105">Update the properties of a [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2be18-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2be18-106">Prerequisites</span></span>
<span data-ttu-id="2be18-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2be18-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2be18-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2be18-109">Permission type</span></span>|<span data-ttu-id="2be18-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2be18-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2be18-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2be18-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2be18-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2be18-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2be18-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2be18-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2be18-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2be18-114">Not supported.</span></span>|
|<span data-ttu-id="2be18-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2be18-115">Application</span></span>|<span data-ttu-id="2be18-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2be18-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2be18-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2be18-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="2be18-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2be18-118">Request headers</span></span>
|<span data-ttu-id="2be18-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2be18-119">Header</span></span>|<span data-ttu-id="2be18-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2be18-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2be18-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2be18-121">Authorization</span></span>|<span data-ttu-id="2be18-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2be18-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2be18-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2be18-123">Accept</span></span>|<span data-ttu-id="2be18-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2be18-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2be18-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2be18-125">Request body</span></span>
<span data-ttu-id="2be18-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-126">In the request body, supply a JSON representation for the [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>

<span data-ttu-id="2be18-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-127">The following table shows the properties that are required when you create the [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span></span>

|<span data-ttu-id="2be18-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2be18-128">Property</span></span>|<span data-ttu-id="2be18-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2be18-129">Type</span></span>|<span data-ttu-id="2be18-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2be18-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2be18-131">id</span><span class="sxs-lookup"><span data-stu-id="2be18-131">id</span></span>|<span data-ttu-id="2be18-132">String</span><span class="sxs-lookup"><span data-stu-id="2be18-132">String</span></span>|<span data-ttu-id="2be18-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2be18-133">Key of the entity.</span></span> <span data-ttu-id="2be18-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-135">displayName</span><span class="sxs-lookup"><span data-stu-id="2be18-135">displayName</span></span>|<span data-ttu-id="2be18-136">String</span><span class="sxs-lookup"><span data-stu-id="2be18-136">String</span></span>|<span data-ttu-id="2be18-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="2be18-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="2be18-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-139">descripción</span><span class="sxs-lookup"><span data-stu-id="2be18-139">description</span></span>|<span data-ttu-id="2be18-140">String</span><span class="sxs-lookup"><span data-stu-id="2be18-140">String</span></span>|<span data-ttu-id="2be18-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-141">The description of the app.</span></span> <span data-ttu-id="2be18-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-143">publicador</span><span class="sxs-lookup"><span data-stu-id="2be18-143">publisher</span></span>|<span data-ttu-id="2be18-144">String</span><span class="sxs-lookup"><span data-stu-id="2be18-144">String</span></span>|<span data-ttu-id="2be18-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-145">The publisher of the app.</span></span> <span data-ttu-id="2be18-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="2be18-147">largeIcon</span></span>|[<span data-ttu-id="2be18-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="2be18-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="2be18-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="2be18-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="2be18-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2be18-151">createdDateTime</span></span>|<span data-ttu-id="2be18-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2be18-152">DateTimeOffset</span></span>|<span data-ttu-id="2be18-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-153">The date and time the app was created.</span></span> <span data-ttu-id="2be18-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2be18-155">lastModifiedDateTime</span></span>|<span data-ttu-id="2be18-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2be18-156">DateTimeOffset</span></span>|<span data-ttu-id="2be18-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-157">The date and time the app was last modified.</span></span> <span data-ttu-id="2be18-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="2be18-159">isFeatured</span></span>|<span data-ttu-id="2be18-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="2be18-160">Boolean</span></span>|<span data-ttu-id="2be18-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="2be18-162">privacyInformationUrl</span></span>|<span data-ttu-id="2be18-163">String</span><span class="sxs-lookup"><span data-stu-id="2be18-163">String</span></span>|<span data-ttu-id="2be18-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="2be18-164">The privacy statement Url.</span></span> <span data-ttu-id="2be18-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="2be18-166">informationUrl</span></span>|<span data-ttu-id="2be18-167">String</span><span class="sxs-lookup"><span data-stu-id="2be18-167">String</span></span>|<span data-ttu-id="2be18-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2be18-168">The more information Url.</span></span> <span data-ttu-id="2be18-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-170">owner</span><span class="sxs-lookup"><span data-stu-id="2be18-170">owner</span></span>|<span data-ttu-id="2be18-171">String</span><span class="sxs-lookup"><span data-stu-id="2be18-171">String</span></span>|<span data-ttu-id="2be18-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-172">The owner of the app.</span></span> <span data-ttu-id="2be18-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-174">developer</span><span class="sxs-lookup"><span data-stu-id="2be18-174">developer</span></span>|<span data-ttu-id="2be18-175">String</span><span class="sxs-lookup"><span data-stu-id="2be18-175">String</span></span>|<span data-ttu-id="2be18-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-176">The developer of the app.</span></span> <span data-ttu-id="2be18-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-178">notas</span><span class="sxs-lookup"><span data-stu-id="2be18-178">notes</span></span>|<span data-ttu-id="2be18-179">String</span><span class="sxs-lookup"><span data-stu-id="2be18-179">String</span></span>|<span data-ttu-id="2be18-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-180">Notes for the app.</span></span> <span data-ttu-id="2be18-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2be18-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="2be18-182">publishingState</span></span>|[<span data-ttu-id="2be18-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="2be18-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="2be18-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-184">The publishing state for the app.</span></span> <span data-ttu-id="2be18-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="2be18-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="2be18-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2be18-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="2be18-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="2be18-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="2be18-188">bundleId</span><span class="sxs-lookup"><span data-stu-id="2be18-188">bundleId</span></span>|<span data-ttu-id="2be18-189">String</span><span class="sxs-lookup"><span data-stu-id="2be18-189">String</span></span>|<span data-ttu-id="2be18-190">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="2be18-190">The Identity Name.</span></span>|
|<span data-ttu-id="2be18-191">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="2be18-191">appStoreUrl</span></span>|<span data-ttu-id="2be18-192">String</span><span class="sxs-lookup"><span data-stu-id="2be18-192">String</span></span>|<span data-ttu-id="2be18-193">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="2be18-193">The Apple App Store URL</span></span>|
|<span data-ttu-id="2be18-194">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="2be18-194">applicableDeviceType</span></span>|[<span data-ttu-id="2be18-195">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="2be18-195">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="2be18-196">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be18-196">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="2be18-197">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2be18-197">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="2be18-198">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2be18-198">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="2be18-199">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="2be18-199">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="2be18-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2be18-200">Response</span></span>
<span data-ttu-id="2be18-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2be18-201">If successful, this method returns a `200 OK` response code and an updated [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2be18-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2be18-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="2be18-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2be18-203">Request</span></span>
<span data-ttu-id="2be18-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be18-204">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1006

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
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
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

### <a name="response"></a><span data-ttu-id="2be18-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2be18-205">Response</span></span>
<span data-ttu-id="2be18-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2be18-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1178

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



