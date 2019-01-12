---
title: Crear iosStoreApp
description: Cree un objeto iosStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9445d58373865d5b6c7008fc277c4b765b2085ba
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950980"
---
# <a name="create-iosstoreapp"></a><span data-ttu-id="fa715-103">Crear iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="fa715-103">Create iosStoreApp</span></span>

> <span data-ttu-id="fa715-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fa715-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fa715-105">Cree un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-105">Create a new [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fa715-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fa715-106">Prerequisites</span></span>
<span data-ttu-id="fa715-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fa715-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fa715-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fa715-109">Permission type</span></span>|<span data-ttu-id="fa715-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fa715-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fa715-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fa715-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fa715-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fa715-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fa715-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fa715-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fa715-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa715-114">Not supported.</span></span>|
|<span data-ttu-id="fa715-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fa715-115">Application</span></span>|<span data-ttu-id="fa715-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa715-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fa715-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fa715-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="fa715-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fa715-118">Request headers</span></span>
|<span data-ttu-id="fa715-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa715-119">Header</span></span>|<span data-ttu-id="fa715-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fa715-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fa715-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fa715-121">Authorization</span></span>|<span data-ttu-id="fa715-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fa715-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fa715-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fa715-123">Accept</span></span>|<span data-ttu-id="fa715-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fa715-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fa715-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fa715-125">Request body</span></span>
<span data-ttu-id="fa715-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="fa715-126">In the request body, supply a JSON representation for the iosStoreApp object.</span></span>

<span data-ttu-id="fa715-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="fa715-127">The following table shows the properties that are required when you create the iosStoreApp.</span></span>

|<span data-ttu-id="fa715-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa715-128">Property</span></span>|<span data-ttu-id="fa715-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa715-129">Type</span></span>|<span data-ttu-id="fa715-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa715-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fa715-131">id</span><span class="sxs-lookup"><span data-stu-id="fa715-131">id</span></span>|<span data-ttu-id="fa715-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-132">String</span></span>|<span data-ttu-id="fa715-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fa715-133">Key of the entity.</span></span> <span data-ttu-id="fa715-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-135">displayName</span><span class="sxs-lookup"><span data-stu-id="fa715-135">displayName</span></span>|<span data-ttu-id="fa715-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-136">String</span></span>|<span data-ttu-id="fa715-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="fa715-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="fa715-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-139">descripción</span><span class="sxs-lookup"><span data-stu-id="fa715-139">description</span></span>|<span data-ttu-id="fa715-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-140">String</span></span>|<span data-ttu-id="fa715-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-141">The description of the app.</span></span> <span data-ttu-id="fa715-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-143">publicador</span><span class="sxs-lookup"><span data-stu-id="fa715-143">publisher</span></span>|<span data-ttu-id="fa715-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-144">String</span></span>|<span data-ttu-id="fa715-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-145">The publisher of the app.</span></span> <span data-ttu-id="fa715-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="fa715-147">largeIcon</span></span>|[<span data-ttu-id="fa715-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="fa715-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="fa715-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="fa715-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="fa715-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fa715-151">createdDateTime</span></span>|<span data-ttu-id="fa715-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fa715-152">DateTimeOffset</span></span>|<span data-ttu-id="fa715-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-153">The date and time the app was created.</span></span> <span data-ttu-id="fa715-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fa715-155">lastModifiedDateTime</span></span>|<span data-ttu-id="fa715-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fa715-156">DateTimeOffset</span></span>|<span data-ttu-id="fa715-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-157">The date and time the app was last modified.</span></span> <span data-ttu-id="fa715-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="fa715-159">isFeatured</span></span>|<span data-ttu-id="fa715-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa715-160">Boolean</span></span>|<span data-ttu-id="fa715-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="fa715-162">privacyInformationUrl</span></span>|<span data-ttu-id="fa715-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-163">String</span></span>|<span data-ttu-id="fa715-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="fa715-164">The privacy statement Url.</span></span> <span data-ttu-id="fa715-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="fa715-166">informationUrl</span></span>|<span data-ttu-id="fa715-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-167">String</span></span>|<span data-ttu-id="fa715-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fa715-168">The more information Url.</span></span> <span data-ttu-id="fa715-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-170">owner</span><span class="sxs-lookup"><span data-stu-id="fa715-170">owner</span></span>|<span data-ttu-id="fa715-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-171">String</span></span>|<span data-ttu-id="fa715-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-172">The owner of the app.</span></span> <span data-ttu-id="fa715-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-174">developer</span><span class="sxs-lookup"><span data-stu-id="fa715-174">developer</span></span>|<span data-ttu-id="fa715-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-175">String</span></span>|<span data-ttu-id="fa715-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-176">The developer of the app.</span></span> <span data-ttu-id="fa715-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-178">notas</span><span class="sxs-lookup"><span data-stu-id="fa715-178">notes</span></span>|<span data-ttu-id="fa715-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-179">String</span></span>|<span data-ttu-id="fa715-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-180">Notes for the app.</span></span> <span data-ttu-id="fa715-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="fa715-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="fa715-182">publishingState</span></span>|[<span data-ttu-id="fa715-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="fa715-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="fa715-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-184">The publishing state for the app.</span></span> <span data-ttu-id="fa715-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="fa715-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="fa715-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="fa715-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="fa715-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="fa715-188">bundleId</span><span class="sxs-lookup"><span data-stu-id="fa715-188">bundleId</span></span>|<span data-ttu-id="fa715-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-189">String</span></span>|<span data-ttu-id="fa715-190">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="fa715-190">The Identity Name.</span></span>|
|<span data-ttu-id="fa715-191">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="fa715-191">appStoreUrl</span></span>|<span data-ttu-id="fa715-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa715-192">String</span></span>|<span data-ttu-id="fa715-193">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="fa715-193">The Apple App Store URL</span></span>|
|<span data-ttu-id="fa715-194">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="fa715-194">applicableDeviceType</span></span>|[<span data-ttu-id="fa715-195">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="fa715-195">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="fa715-196">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa715-196">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="fa715-197">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="fa715-197">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="fa715-198">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="fa715-198">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="fa715-199">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="fa715-199">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="fa715-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa715-200">Response</span></span>
<span data-ttu-id="fa715-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa715-201">If successful, this method returns a `201 Created` response code and a [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fa715-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa715-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="fa715-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fa715-203">Request</span></span>
<span data-ttu-id="fa715-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa715-204">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
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

### <a name="response"></a><span data-ttu-id="fa715-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa715-205">Response</span></span>
<span data-ttu-id="fa715-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fa715-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



