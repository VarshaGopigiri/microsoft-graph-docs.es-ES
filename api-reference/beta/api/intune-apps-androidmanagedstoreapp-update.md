---
title: Actualizar androidManagedStoreApp
description: Actualizar las propiedades de un objeto androidManagedStoreApp.
ms.openlocfilehash: c3c2edde22e1b6538b08930507136e15d470e221
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089114"
---
# <a name="update-androidmanagedstoreapp"></a><span data-ttu-id="e47d3-103">Actualizar androidManagedStoreApp</span><span class="sxs-lookup"><span data-stu-id="e47d3-103">Update androidManagedStoreApp</span></span>

> <span data-ttu-id="e47d3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e47d3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e47d3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e47d3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e47d3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e47d3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e47d3-107">Actualizar las propiedades de un objeto [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) .</span><span class="sxs-lookup"><span data-stu-id="e47d3-107">Update the properties of a [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e47d3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e47d3-108">Prerequisites</span></span>
<span data-ttu-id="e47d3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e47d3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e47d3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e47d3-111">Permission type</span></span>|<span data-ttu-id="e47d3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e47d3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e47d3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e47d3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e47d3-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e47d3-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e47d3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e47d3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e47d3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e47d3-116">Not supported.</span></span>|
|<span data-ttu-id="e47d3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e47d3-117">Application</span></span>|<span data-ttu-id="e47d3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e47d3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e47d3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e47d3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="e47d3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e47d3-120">Request headers</span></span>
|<span data-ttu-id="e47d3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e47d3-121">Header</span></span>|<span data-ttu-id="e47d3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e47d3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e47d3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e47d3-123">Authorization</span></span>|<span data-ttu-id="e47d3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e47d3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e47d3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e47d3-125">Accept</span></span>|<span data-ttu-id="e47d3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e47d3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e47d3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e47d3-127">Request body</span></span>
<span data-ttu-id="e47d3-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) .</span><span class="sxs-lookup"><span data-stu-id="e47d3-128">In the request body, supply a JSON representation for the [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object.</span></span>

<span data-ttu-id="e47d3-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-129">The following table shows the properties that are required when you create the [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md).</span></span>

|<span data-ttu-id="e47d3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e47d3-130">Property</span></span>|<span data-ttu-id="e47d3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e47d3-131">Type</span></span>|<span data-ttu-id="e47d3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e47d3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e47d3-133">id</span><span class="sxs-lookup"><span data-stu-id="e47d3-133">id</span></span>|<span data-ttu-id="e47d3-134">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-134">String</span></span>|<span data-ttu-id="e47d3-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e47d3-135">Key of the entity.</span></span> <span data-ttu-id="e47d3-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-137">displayName</span><span class="sxs-lookup"><span data-stu-id="e47d3-137">displayName</span></span>|<span data-ttu-id="e47d3-138">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-138">String</span></span>|<span data-ttu-id="e47d3-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e47d3-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e47d3-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-141">descripción</span><span class="sxs-lookup"><span data-stu-id="e47d3-141">description</span></span>|<span data-ttu-id="e47d3-142">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-142">String</span></span>|<span data-ttu-id="e47d3-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-143">The description of the app.</span></span> <span data-ttu-id="e47d3-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-145">publicador</span><span class="sxs-lookup"><span data-stu-id="e47d3-145">publisher</span></span>|<span data-ttu-id="e47d3-146">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-146">String</span></span>|<span data-ttu-id="e47d3-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-147">The publisher of the app.</span></span> <span data-ttu-id="e47d3-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e47d3-149">largeIcon</span></span>|[<span data-ttu-id="e47d3-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e47d3-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="e47d3-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e47d3-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e47d3-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e47d3-153">createdDateTime</span></span>|<span data-ttu-id="e47d3-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e47d3-154">DateTimeOffset</span></span>|<span data-ttu-id="e47d3-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-155">The date and time the app was created.</span></span> <span data-ttu-id="e47d3-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e47d3-157">lastModifiedDateTime</span></span>|<span data-ttu-id="e47d3-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e47d3-158">DateTimeOffset</span></span>|<span data-ttu-id="e47d3-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-159">The date and time the app was last modified.</span></span> <span data-ttu-id="e47d3-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e47d3-161">isFeatured</span></span>|<span data-ttu-id="e47d3-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="e47d3-162">Boolean</span></span>|<span data-ttu-id="e47d3-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e47d3-164">privacyInformationUrl</span></span>|<span data-ttu-id="e47d3-165">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-165">String</span></span>|<span data-ttu-id="e47d3-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e47d3-166">The privacy statement Url.</span></span> <span data-ttu-id="e47d3-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e47d3-168">informationUrl</span></span>|<span data-ttu-id="e47d3-169">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-169">String</span></span>|<span data-ttu-id="e47d3-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e47d3-170">The more information Url.</span></span> <span data-ttu-id="e47d3-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-172">owner</span><span class="sxs-lookup"><span data-stu-id="e47d3-172">owner</span></span>|<span data-ttu-id="e47d3-173">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-173">String</span></span>|<span data-ttu-id="e47d3-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-174">The owner of the app.</span></span> <span data-ttu-id="e47d3-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-176">developer</span><span class="sxs-lookup"><span data-stu-id="e47d3-176">developer</span></span>|<span data-ttu-id="e47d3-177">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-177">String</span></span>|<span data-ttu-id="e47d3-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-178">The developer of the app.</span></span> <span data-ttu-id="e47d3-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-180">notas</span><span class="sxs-lookup"><span data-stu-id="e47d3-180">notes</span></span>|<span data-ttu-id="e47d3-181">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-181">String</span></span>|<span data-ttu-id="e47d3-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-182">Notes for the app.</span></span> <span data-ttu-id="e47d3-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="e47d3-184">uploadState</span></span>|<span data-ttu-id="e47d3-185">Int32</span><span class="sxs-lookup"><span data-stu-id="e47d3-185">Int32</span></span>|<span data-ttu-id="e47d3-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="e47d3-186">The upload state.</span></span> <span data-ttu-id="e47d3-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e47d3-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="e47d3-188">publishingState</span></span>|[<span data-ttu-id="e47d3-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="e47d3-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="e47d3-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e47d3-190">The publishing state for the app.</span></span> <span data-ttu-id="e47d3-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e47d3-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e47d3-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e47d3-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="e47d3-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e47d3-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="e47d3-194">packageId</span><span class="sxs-lookup"><span data-stu-id="e47d3-194">packageId</span></span>|<span data-ttu-id="e47d3-195">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-195">String</span></span>|<span data-ttu-id="e47d3-196">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="e47d3-196">The package identifier.</span></span>|
|<span data-ttu-id="e47d3-197">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="e47d3-197">appIdentifier</span></span>|<span data-ttu-id="e47d3-198">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-198">String</span></span>|<span data-ttu-id="e47d3-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e47d3-199">The Identity Name.</span></span>|
|<span data-ttu-id="e47d3-200">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="e47d3-200">usedLicenseCount</span></span>|<span data-ttu-id="e47d3-201">Int32</span><span class="sxs-lookup"><span data-stu-id="e47d3-201">Int32</span></span>|<span data-ttu-id="e47d3-202">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="e47d3-202">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="e47d3-203">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="e47d3-203">totalLicenseCount</span></span>|<span data-ttu-id="e47d3-204">Int32</span><span class="sxs-lookup"><span data-stu-id="e47d3-204">Int32</span></span>|<span data-ttu-id="e47d3-205">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="e47d3-205">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="e47d3-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="e47d3-206">appStoreUrl</span></span>|<span data-ttu-id="e47d3-207">String</span><span class="sxs-lookup"><span data-stu-id="e47d3-207">String</span></span>|<span data-ttu-id="e47d3-208">Reproducir para la dirección URL de la aplicación de almacenamiento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e47d3-208">The Play for Work Store app URL.</span></span>|



## <a name="response"></a><span data-ttu-id="e47d3-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e47d3-209">Response</span></span>
<span data-ttu-id="e47d3-210">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e47d3-210">If successful, this method returns a `200 OK` response code and an updated [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e47d3-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e47d3-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="e47d3-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e47d3-212">Request</span></span>
<span data-ttu-id="e47d3-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e47d3-213">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 799

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
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "appStoreUrl": "https://example.com/appStoreUrl/"
}
```

### <a name="response"></a><span data-ttu-id="e47d3-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e47d3-214">Response</span></span>
<span data-ttu-id="e47d3-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e47d3-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





