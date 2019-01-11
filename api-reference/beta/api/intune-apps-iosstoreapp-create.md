---
title: Crear iosStoreApp
description: Cree un objeto iosStoreApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a600146fac5e1f9af704bd9acfb65cb622fea08a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825254"
---
# <a name="create-iosstoreapp"></a><span data-ttu-id="e6789-103">Crear iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="e6789-103">Create iosStoreApp</span></span>

> <span data-ttu-id="e6789-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6789-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6789-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6789-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e6789-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6789-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6789-107">Cree un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-107">Create a new [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6789-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6789-108">Prerequisites</span></span>
<span data-ttu-id="e6789-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6789-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6789-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6789-111">Permission type</span></span>|<span data-ttu-id="e6789-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6789-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6789-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6789-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e6789-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6789-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e6789-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6789-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6789-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6789-116">Not supported.</span></span>|
|<span data-ttu-id="e6789-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6789-117">Application</span></span>|<span data-ttu-id="e6789-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6789-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6789-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6789-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="e6789-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6789-120">Request headers</span></span>
|<span data-ttu-id="e6789-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6789-121">Header</span></span>|<span data-ttu-id="e6789-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e6789-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6789-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e6789-123">Authorization</span></span>|<span data-ttu-id="e6789-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6789-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6789-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e6789-125">Accept</span></span>|<span data-ttu-id="e6789-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e6789-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6789-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6789-127">Request body</span></span>
<span data-ttu-id="e6789-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="e6789-128">In the request body, supply a JSON representation for the iosStoreApp object.</span></span>

<span data-ttu-id="e6789-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="e6789-129">The following table shows the properties that are required when you create the iosStoreApp.</span></span>

|<span data-ttu-id="e6789-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6789-130">Property</span></span>|<span data-ttu-id="e6789-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6789-131">Type</span></span>|<span data-ttu-id="e6789-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6789-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6789-133">id</span><span class="sxs-lookup"><span data-stu-id="e6789-133">id</span></span>|<span data-ttu-id="e6789-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-134">String</span></span>|<span data-ttu-id="e6789-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e6789-135">Key of the entity.</span></span> <span data-ttu-id="e6789-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-137">displayName</span><span class="sxs-lookup"><span data-stu-id="e6789-137">displayName</span></span>|<span data-ttu-id="e6789-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-138">String</span></span>|<span data-ttu-id="e6789-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e6789-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e6789-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-141">descripción</span><span class="sxs-lookup"><span data-stu-id="e6789-141">description</span></span>|<span data-ttu-id="e6789-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-142">String</span></span>|<span data-ttu-id="e6789-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-143">The description of the app.</span></span> <span data-ttu-id="e6789-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-145">publicador</span><span class="sxs-lookup"><span data-stu-id="e6789-145">publisher</span></span>|<span data-ttu-id="e6789-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-146">String</span></span>|<span data-ttu-id="e6789-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-147">The publisher of the app.</span></span> <span data-ttu-id="e6789-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e6789-149">largeIcon</span></span>|[<span data-ttu-id="e6789-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e6789-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="e6789-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e6789-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e6789-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e6789-153">createdDateTime</span></span>|<span data-ttu-id="e6789-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6789-154">DateTimeOffset</span></span>|<span data-ttu-id="e6789-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-155">The date and time the app was created.</span></span> <span data-ttu-id="e6789-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e6789-157">lastModifiedDateTime</span></span>|<span data-ttu-id="e6789-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6789-158">DateTimeOffset</span></span>|<span data-ttu-id="e6789-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-159">The date and time the app was last modified.</span></span> <span data-ttu-id="e6789-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e6789-161">isFeatured</span></span>|<span data-ttu-id="e6789-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="e6789-162">Boolean</span></span>|<span data-ttu-id="e6789-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e6789-164">privacyInformationUrl</span></span>|<span data-ttu-id="e6789-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-165">String</span></span>|<span data-ttu-id="e6789-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e6789-166">The privacy statement Url.</span></span> <span data-ttu-id="e6789-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e6789-168">informationUrl</span></span>|<span data-ttu-id="e6789-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-169">String</span></span>|<span data-ttu-id="e6789-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e6789-170">The more information Url.</span></span> <span data-ttu-id="e6789-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-172">owner</span><span class="sxs-lookup"><span data-stu-id="e6789-172">owner</span></span>|<span data-ttu-id="e6789-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-173">String</span></span>|<span data-ttu-id="e6789-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-174">The owner of the app.</span></span> <span data-ttu-id="e6789-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-176">developer</span><span class="sxs-lookup"><span data-stu-id="e6789-176">developer</span></span>|<span data-ttu-id="e6789-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-177">String</span></span>|<span data-ttu-id="e6789-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-178">The developer of the app.</span></span> <span data-ttu-id="e6789-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-180">notas</span><span class="sxs-lookup"><span data-stu-id="e6789-180">notes</span></span>|<span data-ttu-id="e6789-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-181">String</span></span>|<span data-ttu-id="e6789-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-182">Notes for the app.</span></span> <span data-ttu-id="e6789-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="e6789-184">uploadState</span></span>|<span data-ttu-id="e6789-185">Int32</span><span class="sxs-lookup"><span data-stu-id="e6789-185">Int32</span></span>|<span data-ttu-id="e6789-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="e6789-186">The upload state.</span></span> <span data-ttu-id="e6789-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e6789-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="e6789-188">publishingState</span></span>|[<span data-ttu-id="e6789-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="e6789-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="e6789-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-190">The publishing state for the app.</span></span> <span data-ttu-id="e6789-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e6789-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e6789-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e6789-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="e6789-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e6789-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="e6789-194">bundleId</span><span class="sxs-lookup"><span data-stu-id="e6789-194">bundleId</span></span>|<span data-ttu-id="e6789-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-195">String</span></span>|<span data-ttu-id="e6789-196">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e6789-196">The Identity Name.</span></span>|
|<span data-ttu-id="e6789-197">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="e6789-197">appStoreUrl</span></span>|<span data-ttu-id="e6789-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6789-198">String</span></span>|<span data-ttu-id="e6789-199">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="e6789-199">The Apple App Store URL</span></span>|
|<span data-ttu-id="e6789-200">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="e6789-200">applicableDeviceType</span></span>|[<span data-ttu-id="e6789-201">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="e6789-201">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="e6789-202">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6789-202">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="e6789-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e6789-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="e6789-204">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e6789-204">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="e6789-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="e6789-205">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="e6789-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6789-206">Response</span></span>
<span data-ttu-id="e6789-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6789-207">If successful, this method returns a `201 Created` response code and a [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6789-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6789-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6789-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6789-209">Request</span></span>
<span data-ttu-id="e6789-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6789-210">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="e6789-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6789-211">Response</span></span>
<span data-ttu-id="e6789-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6789-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





