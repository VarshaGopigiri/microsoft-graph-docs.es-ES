---
title: Crear androidManagedStoreApp
description: Crear un nuevo objeto androidManagedStoreApp.
ms.openlocfilehash: 51713d6cc0420f27c17373695825e30c7d46b096
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091030"
---
# <a name="create-androidmanagedstoreapp"></a><span data-ttu-id="39bd9-103">Crear androidManagedStoreApp</span><span class="sxs-lookup"><span data-stu-id="39bd9-103">Create androidManagedStoreApp</span></span>

> <span data-ttu-id="39bd9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39bd9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39bd9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39bd9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="39bd9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39bd9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39bd9-107">Crear un nuevo objeto [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) .</span><span class="sxs-lookup"><span data-stu-id="39bd9-107">Create a new [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39bd9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39bd9-108">Prerequisites</span></span>
<span data-ttu-id="39bd9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39bd9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39bd9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39bd9-111">Permission type</span></span>|<span data-ttu-id="39bd9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39bd9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39bd9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39bd9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="39bd9-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39bd9-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="39bd9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39bd9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39bd9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39bd9-116">Not supported.</span></span>|
|<span data-ttu-id="39bd9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39bd9-117">Application</span></span>|<span data-ttu-id="39bd9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39bd9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39bd9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39bd9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="39bd9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39bd9-120">Request headers</span></span>
|<span data-ttu-id="39bd9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39bd9-121">Header</span></span>|<span data-ttu-id="39bd9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="39bd9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39bd9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="39bd9-123">Authorization</span></span>|<span data-ttu-id="39bd9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39bd9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39bd9-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="39bd9-125">Accept</span></span>|<span data-ttu-id="39bd9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="39bd9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39bd9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39bd9-127">Request body</span></span>
<span data-ttu-id="39bd9-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidManagedStoreApp.</span><span class="sxs-lookup"><span data-stu-id="39bd9-128">In the request body, supply a JSON representation for the androidManagedStoreApp object.</span></span>

<span data-ttu-id="39bd9-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidManagedStoreApp.</span><span class="sxs-lookup"><span data-stu-id="39bd9-129">The following table shows the properties that are required when you create the androidManagedStoreApp.</span></span>

|<span data-ttu-id="39bd9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39bd9-130">Property</span></span>|<span data-ttu-id="39bd9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="39bd9-131">Type</span></span>|<span data-ttu-id="39bd9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="39bd9-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39bd9-133">id</span><span class="sxs-lookup"><span data-stu-id="39bd9-133">id</span></span>|<span data-ttu-id="39bd9-134">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-134">String</span></span>|<span data-ttu-id="39bd9-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39bd9-135">Key of the entity.</span></span> <span data-ttu-id="39bd9-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-137">displayName</span><span class="sxs-lookup"><span data-stu-id="39bd9-137">displayName</span></span>|<span data-ttu-id="39bd9-138">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-138">String</span></span>|<span data-ttu-id="39bd9-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="39bd9-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="39bd9-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-141">descripción</span><span class="sxs-lookup"><span data-stu-id="39bd9-141">description</span></span>|<span data-ttu-id="39bd9-142">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-142">String</span></span>|<span data-ttu-id="39bd9-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-143">The description of the app.</span></span> <span data-ttu-id="39bd9-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-145">publicador</span><span class="sxs-lookup"><span data-stu-id="39bd9-145">publisher</span></span>|<span data-ttu-id="39bd9-146">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-146">String</span></span>|<span data-ttu-id="39bd9-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-147">The publisher of the app.</span></span> <span data-ttu-id="39bd9-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="39bd9-149">largeIcon</span></span>|[<span data-ttu-id="39bd9-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="39bd9-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="39bd9-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="39bd9-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="39bd9-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="39bd9-153">createdDateTime</span></span>|<span data-ttu-id="39bd9-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39bd9-154">DateTimeOffset</span></span>|<span data-ttu-id="39bd9-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-155">The date and time the app was created.</span></span> <span data-ttu-id="39bd9-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="39bd9-157">lastModifiedDateTime</span></span>|<span data-ttu-id="39bd9-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39bd9-158">DateTimeOffset</span></span>|<span data-ttu-id="39bd9-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-159">The date and time the app was last modified.</span></span> <span data-ttu-id="39bd9-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="39bd9-161">isFeatured</span></span>|<span data-ttu-id="39bd9-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="39bd9-162">Boolean</span></span>|<span data-ttu-id="39bd9-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="39bd9-164">privacyInformationUrl</span></span>|<span data-ttu-id="39bd9-165">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-165">String</span></span>|<span data-ttu-id="39bd9-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="39bd9-166">The privacy statement Url.</span></span> <span data-ttu-id="39bd9-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="39bd9-168">informationUrl</span></span>|<span data-ttu-id="39bd9-169">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-169">String</span></span>|<span data-ttu-id="39bd9-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="39bd9-170">The more information Url.</span></span> <span data-ttu-id="39bd9-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-172">owner</span><span class="sxs-lookup"><span data-stu-id="39bd9-172">owner</span></span>|<span data-ttu-id="39bd9-173">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-173">String</span></span>|<span data-ttu-id="39bd9-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-174">The owner of the app.</span></span> <span data-ttu-id="39bd9-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-176">developer</span><span class="sxs-lookup"><span data-stu-id="39bd9-176">developer</span></span>|<span data-ttu-id="39bd9-177">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-177">String</span></span>|<span data-ttu-id="39bd9-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-178">The developer of the app.</span></span> <span data-ttu-id="39bd9-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-180">notas</span><span class="sxs-lookup"><span data-stu-id="39bd9-180">notes</span></span>|<span data-ttu-id="39bd9-181">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-181">String</span></span>|<span data-ttu-id="39bd9-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-182">Notes for the app.</span></span> <span data-ttu-id="39bd9-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="39bd9-184">uploadState</span></span>|<span data-ttu-id="39bd9-185">Int32</span><span class="sxs-lookup"><span data-stu-id="39bd9-185">Int32</span></span>|<span data-ttu-id="39bd9-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="39bd9-186">The upload state.</span></span> <span data-ttu-id="39bd9-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="39bd9-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="39bd9-188">publishingState</span></span>|[<span data-ttu-id="39bd9-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="39bd9-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="39bd9-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39bd9-190">The publishing state for the app.</span></span> <span data-ttu-id="39bd9-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="39bd9-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="39bd9-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="39bd9-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="39bd9-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="39bd9-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="39bd9-194">packageId</span><span class="sxs-lookup"><span data-stu-id="39bd9-194">packageId</span></span>|<span data-ttu-id="39bd9-195">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-195">String</span></span>|<span data-ttu-id="39bd9-196">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="39bd9-196">The package identifier.</span></span>|
|<span data-ttu-id="39bd9-197">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="39bd9-197">appIdentifier</span></span>|<span data-ttu-id="39bd9-198">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-198">String</span></span>|<span data-ttu-id="39bd9-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="39bd9-199">The Identity Name.</span></span>|
|<span data-ttu-id="39bd9-200">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="39bd9-200">usedLicenseCount</span></span>|<span data-ttu-id="39bd9-201">Int32</span><span class="sxs-lookup"><span data-stu-id="39bd9-201">Int32</span></span>|<span data-ttu-id="39bd9-202">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="39bd9-202">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="39bd9-203">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="39bd9-203">totalLicenseCount</span></span>|<span data-ttu-id="39bd9-204">Int32</span><span class="sxs-lookup"><span data-stu-id="39bd9-204">Int32</span></span>|<span data-ttu-id="39bd9-205">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="39bd9-205">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="39bd9-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="39bd9-206">appStoreUrl</span></span>|<span data-ttu-id="39bd9-207">String</span><span class="sxs-lookup"><span data-stu-id="39bd9-207">String</span></span>|<span data-ttu-id="39bd9-208">Reproducir para la dirección URL de la aplicación de almacenamiento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="39bd9-208">The Play for Work Store app URL.</span></span>|



## <a name="response"></a><span data-ttu-id="39bd9-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39bd9-209">Response</span></span>
<span data-ttu-id="39bd9-210">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39bd9-210">If successful, this method returns a `201 Created` response code and a [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39bd9-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39bd9-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="39bd9-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39bd9-212">Request</span></span>
<span data-ttu-id="39bd9-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39bd9-213">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 860

{
  "@odata.type": "#microsoft.graph.androidManagedStoreApp",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "appStoreUrl": "https://example.com/appStoreUrl/"
}
```

### <a name="response"></a><span data-ttu-id="39bd9-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39bd9-214">Response</span></span>
<span data-ttu-id="39bd9-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39bd9-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 968

{
  "@odata.type": "#microsoft.graph.androidManagedStoreApp",
  "id": "87247525-7525-8724-2575-248725752487",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "appStoreUrl": "https://example.com/appStoreUrl/"
}
```





