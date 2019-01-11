---
title: Crear androidForWorkApp
description: Crear un nuevo objeto androidForWorkApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0e2414c0da4d3c184d43443b7a607c6db7baffb9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853966"
---
# <a name="create-androidforworkapp"></a><span data-ttu-id="889ac-103">Crear androidForWorkApp</span><span class="sxs-lookup"><span data-stu-id="889ac-103">Create androidForWorkApp</span></span>

> <span data-ttu-id="889ac-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="889ac-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="889ac-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="889ac-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="889ac-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="889ac-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="889ac-107">Crear un nuevo objeto [androidForWorkApp](../resources/intune-apps-androidforworkapp.md) .</span><span class="sxs-lookup"><span data-stu-id="889ac-107">Create a new [androidForWorkApp](../resources/intune-apps-androidforworkapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="889ac-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="889ac-108">Prerequisites</span></span>
<span data-ttu-id="889ac-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="889ac-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="889ac-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="889ac-111">Permission type</span></span>|<span data-ttu-id="889ac-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="889ac-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="889ac-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="889ac-113">Delegated (work or school account)</span></span>|<span data-ttu-id="889ac-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="889ac-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="889ac-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="889ac-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="889ac-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="889ac-116">Not supported.</span></span>|
|<span data-ttu-id="889ac-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="889ac-117">Application</span></span>|<span data-ttu-id="889ac-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="889ac-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="889ac-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="889ac-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="889ac-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="889ac-120">Request headers</span></span>
|<span data-ttu-id="889ac-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="889ac-121">Header</span></span>|<span data-ttu-id="889ac-122">Valor</span><span class="sxs-lookup"><span data-stu-id="889ac-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="889ac-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="889ac-123">Authorization</span></span>|<span data-ttu-id="889ac-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="889ac-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="889ac-125">Accept</span><span class="sxs-lookup"><span data-stu-id="889ac-125">Accept</span></span>|<span data-ttu-id="889ac-126">application/json</span><span class="sxs-lookup"><span data-stu-id="889ac-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="889ac-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="889ac-127">Request body</span></span>
<span data-ttu-id="889ac-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidForWorkApp.</span><span class="sxs-lookup"><span data-stu-id="889ac-128">In the request body, supply a JSON representation for the androidForWorkApp object.</span></span>

<span data-ttu-id="889ac-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidForWorkApp.</span><span class="sxs-lookup"><span data-stu-id="889ac-129">The following table shows the properties that are required when you create the androidForWorkApp.</span></span>

|<span data-ttu-id="889ac-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="889ac-130">Property</span></span>|<span data-ttu-id="889ac-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="889ac-131">Type</span></span>|<span data-ttu-id="889ac-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="889ac-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="889ac-133">id</span><span class="sxs-lookup"><span data-stu-id="889ac-133">id</span></span>|<span data-ttu-id="889ac-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-134">String</span></span>|<span data-ttu-id="889ac-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="889ac-135">Key of the entity.</span></span> <span data-ttu-id="889ac-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-137">displayName</span><span class="sxs-lookup"><span data-stu-id="889ac-137">displayName</span></span>|<span data-ttu-id="889ac-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-138">String</span></span>|<span data-ttu-id="889ac-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="889ac-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="889ac-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-141">descripción</span><span class="sxs-lookup"><span data-stu-id="889ac-141">description</span></span>|<span data-ttu-id="889ac-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-142">String</span></span>|<span data-ttu-id="889ac-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-143">The description of the app.</span></span> <span data-ttu-id="889ac-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-145">publicador</span><span class="sxs-lookup"><span data-stu-id="889ac-145">publisher</span></span>|<span data-ttu-id="889ac-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-146">String</span></span>|<span data-ttu-id="889ac-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-147">The publisher of the app.</span></span> <span data-ttu-id="889ac-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="889ac-149">largeIcon</span></span>|[<span data-ttu-id="889ac-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="889ac-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="889ac-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="889ac-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="889ac-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="889ac-153">createdDateTime</span></span>|<span data-ttu-id="889ac-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="889ac-154">DateTimeOffset</span></span>|<span data-ttu-id="889ac-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-155">The date and time the app was created.</span></span> <span data-ttu-id="889ac-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="889ac-157">lastModifiedDateTime</span></span>|<span data-ttu-id="889ac-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="889ac-158">DateTimeOffset</span></span>|<span data-ttu-id="889ac-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-159">The date and time the app was last modified.</span></span> <span data-ttu-id="889ac-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="889ac-161">isFeatured</span></span>|<span data-ttu-id="889ac-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="889ac-162">Boolean</span></span>|<span data-ttu-id="889ac-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="889ac-164">privacyInformationUrl</span></span>|<span data-ttu-id="889ac-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-165">String</span></span>|<span data-ttu-id="889ac-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="889ac-166">The privacy statement Url.</span></span> <span data-ttu-id="889ac-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="889ac-168">informationUrl</span></span>|<span data-ttu-id="889ac-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-169">String</span></span>|<span data-ttu-id="889ac-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="889ac-170">The more information Url.</span></span> <span data-ttu-id="889ac-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-172">owner</span><span class="sxs-lookup"><span data-stu-id="889ac-172">owner</span></span>|<span data-ttu-id="889ac-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-173">String</span></span>|<span data-ttu-id="889ac-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-174">The owner of the app.</span></span> <span data-ttu-id="889ac-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-176">developer</span><span class="sxs-lookup"><span data-stu-id="889ac-176">developer</span></span>|<span data-ttu-id="889ac-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-177">String</span></span>|<span data-ttu-id="889ac-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-178">The developer of the app.</span></span> <span data-ttu-id="889ac-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-180">notas</span><span class="sxs-lookup"><span data-stu-id="889ac-180">notes</span></span>|<span data-ttu-id="889ac-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-181">String</span></span>|<span data-ttu-id="889ac-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-182">Notes for the app.</span></span> <span data-ttu-id="889ac-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="889ac-184">uploadState</span></span>|<span data-ttu-id="889ac-185">Int32</span><span class="sxs-lookup"><span data-stu-id="889ac-185">Int32</span></span>|<span data-ttu-id="889ac-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="889ac-186">The upload state.</span></span> <span data-ttu-id="889ac-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="889ac-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="889ac-188">publishingState</span></span>|[<span data-ttu-id="889ac-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="889ac-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="889ac-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="889ac-190">The publishing state for the app.</span></span> <span data-ttu-id="889ac-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="889ac-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="889ac-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="889ac-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="889ac-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="889ac-194">packageId</span><span class="sxs-lookup"><span data-stu-id="889ac-194">packageId</span></span>|<span data-ttu-id="889ac-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-195">String</span></span>|<span data-ttu-id="889ac-196">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="889ac-196">The package identifier.</span></span>|
|<span data-ttu-id="889ac-197">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="889ac-197">appIdentifier</span></span>|<span data-ttu-id="889ac-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-198">String</span></span>|<span data-ttu-id="889ac-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="889ac-199">The Identity Name.</span></span>|
|<span data-ttu-id="889ac-200">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="889ac-200">usedLicenseCount</span></span>|<span data-ttu-id="889ac-201">Int32</span><span class="sxs-lookup"><span data-stu-id="889ac-201">Int32</span></span>|<span data-ttu-id="889ac-202">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="889ac-202">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="889ac-203">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="889ac-203">totalLicenseCount</span></span>|<span data-ttu-id="889ac-204">Int32</span><span class="sxs-lookup"><span data-stu-id="889ac-204">Int32</span></span>|<span data-ttu-id="889ac-205">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="889ac-205">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="889ac-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="889ac-206">appStoreUrl</span></span>|<span data-ttu-id="889ac-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="889ac-207">String</span></span>|<span data-ttu-id="889ac-208">Reproducir para la dirección URL de la aplicación de almacenamiento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="889ac-208">The Play for Work Store app URL.</span></span>|



## <a name="response"></a><span data-ttu-id="889ac-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="889ac-209">Response</span></span>
<span data-ttu-id="889ac-210">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidForWorkApp](../resources/intune-apps-androidforworkapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="889ac-210">If successful, this method returns a `201 Created` response code and a [androidForWorkApp](../resources/intune-apps-androidforworkapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="889ac-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="889ac-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="889ac-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="889ac-212">Request</span></span>
<span data-ttu-id="889ac-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="889ac-213">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 855

{
  "@odata.type": "#microsoft.graph.androidForWorkApp",
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

### <a name="response"></a><span data-ttu-id="889ac-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="889ac-214">Response</span></span>
<span data-ttu-id="889ac-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="889ac-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 963

{
  "@odata.type": "#microsoft.graph.androidForWorkApp",
  "id": "c5010785-0785-c501-8507-01c5850701c5",
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





