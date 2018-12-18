---
title: Crear androidStoreApp
description: Cree un objeto androidStoreApp.
author: tfitzmac
ms.openlocfilehash: 3a28a00433d6a5cda83892efcc12284f7c10480a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358670"
---
# <a name="create-androidstoreapp"></a><span data-ttu-id="38ac9-103">Crear androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="38ac9-103">Create androidStoreApp</span></span>

> <span data-ttu-id="38ac9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38ac9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38ac9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38ac9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="38ac9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="38ac9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="38ac9-107">Cree un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-107">Create a new [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="38ac9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="38ac9-108">Prerequisites</span></span>
<span data-ttu-id="38ac9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38ac9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38ac9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38ac9-111">Permission type</span></span>|<span data-ttu-id="38ac9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38ac9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="38ac9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38ac9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="38ac9-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="38ac9-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="38ac9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38ac9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="38ac9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38ac9-116">Not supported.</span></span>|
|<span data-ttu-id="38ac9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38ac9-117">Application</span></span>|<span data-ttu-id="38ac9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38ac9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="38ac9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38ac9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="38ac9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38ac9-120">Request headers</span></span>
|<span data-ttu-id="38ac9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38ac9-121">Header</span></span>|<span data-ttu-id="38ac9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="38ac9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="38ac9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="38ac9-123">Authorization</span></span>|<span data-ttu-id="38ac9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="38ac9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="38ac9-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="38ac9-125">Accept</span></span>|<span data-ttu-id="38ac9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="38ac9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="38ac9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38ac9-127">Request body</span></span>
<span data-ttu-id="38ac9-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="38ac9-128">In the request body, supply a JSON representation for the androidStoreApp object.</span></span>

<span data-ttu-id="38ac9-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="38ac9-129">The following table shows the properties that are required when you create the androidStoreApp.</span></span>

|<span data-ttu-id="38ac9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38ac9-130">Property</span></span>|<span data-ttu-id="38ac9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="38ac9-131">Type</span></span>|<span data-ttu-id="38ac9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="38ac9-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="38ac9-133">id</span><span class="sxs-lookup"><span data-stu-id="38ac9-133">id</span></span>|<span data-ttu-id="38ac9-134">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-134">String</span></span>|<span data-ttu-id="38ac9-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="38ac9-135">Key of the entity.</span></span> <span data-ttu-id="38ac9-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-137">displayName</span><span class="sxs-lookup"><span data-stu-id="38ac9-137">displayName</span></span>|<span data-ttu-id="38ac9-138">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-138">String</span></span>|<span data-ttu-id="38ac9-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="38ac9-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="38ac9-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-141">descripción</span><span class="sxs-lookup"><span data-stu-id="38ac9-141">description</span></span>|<span data-ttu-id="38ac9-142">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-142">String</span></span>|<span data-ttu-id="38ac9-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-143">The description of the app.</span></span> <span data-ttu-id="38ac9-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-145">publicador</span><span class="sxs-lookup"><span data-stu-id="38ac9-145">publisher</span></span>|<span data-ttu-id="38ac9-146">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-146">String</span></span>|<span data-ttu-id="38ac9-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-147">The publisher of the app.</span></span> <span data-ttu-id="38ac9-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="38ac9-149">largeIcon</span></span>|[<span data-ttu-id="38ac9-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="38ac9-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="38ac9-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="38ac9-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="38ac9-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="38ac9-153">createdDateTime</span></span>|<span data-ttu-id="38ac9-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="38ac9-154">DateTimeOffset</span></span>|<span data-ttu-id="38ac9-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-155">The date and time the app was created.</span></span> <span data-ttu-id="38ac9-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="38ac9-157">lastModifiedDateTime</span></span>|<span data-ttu-id="38ac9-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="38ac9-158">DateTimeOffset</span></span>|<span data-ttu-id="38ac9-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-159">The date and time the app was last modified.</span></span> <span data-ttu-id="38ac9-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="38ac9-161">isFeatured</span></span>|<span data-ttu-id="38ac9-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="38ac9-162">Boolean</span></span>|<span data-ttu-id="38ac9-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="38ac9-164">privacyInformationUrl</span></span>|<span data-ttu-id="38ac9-165">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-165">String</span></span>|<span data-ttu-id="38ac9-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="38ac9-166">The privacy statement Url.</span></span> <span data-ttu-id="38ac9-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="38ac9-168">informationUrl</span></span>|<span data-ttu-id="38ac9-169">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-169">String</span></span>|<span data-ttu-id="38ac9-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="38ac9-170">The more information Url.</span></span> <span data-ttu-id="38ac9-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-172">owner</span><span class="sxs-lookup"><span data-stu-id="38ac9-172">owner</span></span>|<span data-ttu-id="38ac9-173">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-173">String</span></span>|<span data-ttu-id="38ac9-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-174">The owner of the app.</span></span> <span data-ttu-id="38ac9-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-176">developer</span><span class="sxs-lookup"><span data-stu-id="38ac9-176">developer</span></span>|<span data-ttu-id="38ac9-177">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-177">String</span></span>|<span data-ttu-id="38ac9-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-178">The developer of the app.</span></span> <span data-ttu-id="38ac9-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-180">notas</span><span class="sxs-lookup"><span data-stu-id="38ac9-180">notes</span></span>|<span data-ttu-id="38ac9-181">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-181">String</span></span>|<span data-ttu-id="38ac9-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-182">Notes for the app.</span></span> <span data-ttu-id="38ac9-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="38ac9-184">uploadState</span></span>|<span data-ttu-id="38ac9-185">Int32</span><span class="sxs-lookup"><span data-stu-id="38ac9-185">Int32</span></span>|<span data-ttu-id="38ac9-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="38ac9-186">The upload state.</span></span> <span data-ttu-id="38ac9-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="38ac9-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="38ac9-188">publishingState</span></span>|[<span data-ttu-id="38ac9-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="38ac9-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="38ac9-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38ac9-190">The publishing state for the app.</span></span> <span data-ttu-id="38ac9-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="38ac9-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="38ac9-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="38ac9-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="38ac9-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="38ac9-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="38ac9-194">packageId</span><span class="sxs-lookup"><span data-stu-id="38ac9-194">packageId</span></span>|<span data-ttu-id="38ac9-195">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-195">String</span></span>|<span data-ttu-id="38ac9-196">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="38ac9-196">The package identifier.</span></span>|
|<span data-ttu-id="38ac9-197">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="38ac9-197">appIdentifier</span></span>|<span data-ttu-id="38ac9-198">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-198">String</span></span>|<span data-ttu-id="38ac9-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="38ac9-199">The Identity Name.</span></span>|
|<span data-ttu-id="38ac9-200">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="38ac9-200">appStoreUrl</span></span>|<span data-ttu-id="38ac9-201">String</span><span class="sxs-lookup"><span data-stu-id="38ac9-201">String</span></span>|<span data-ttu-id="38ac9-202">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="38ac9-202">The Android app store URL.</span></span>|
|<span data-ttu-id="38ac9-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="38ac9-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="38ac9-204">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="38ac9-204">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="38ac9-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="38ac9-205">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="38ac9-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38ac9-206">Response</span></span>
<span data-ttu-id="38ac9-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38ac9-207">If successful, this method returns a `201 Created` response code and a [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38ac9-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38ac9-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="38ac9-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38ac9-209">Request</span></span>
<span data-ttu-id="38ac9-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38ac9-210">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1182

{
  "@odata.type": "#microsoft.graph.androidStoreApp",
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
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
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

### <a name="response"></a><span data-ttu-id="38ac9-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38ac9-211">Response</span></span>
<span data-ttu-id="38ac9-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38ac9-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1290

{
  "@odata.type": "#microsoft.graph.androidStoreApp",
  "id": "1f2b7654-7654-1f2b-5476-2b1f54762b1f",
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
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
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





