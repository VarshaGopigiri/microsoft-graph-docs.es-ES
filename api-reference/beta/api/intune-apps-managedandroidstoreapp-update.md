---
title: Actualizar managedAndroidStoreApp
description: Actualice las propiedades de un objeto managedAndroidStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 00b9988df08715d469f3bd0ed1d3b47529620b69
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980534"
---
# <a name="update-managedandroidstoreapp"></a><span data-ttu-id="23ebe-103">Actualizar managedAndroidStoreApp</span><span class="sxs-lookup"><span data-stu-id="23ebe-103">Update managedAndroidStoreApp</span></span>

> <span data-ttu-id="23ebe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="23ebe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="23ebe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="23ebe-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="23ebe-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="23ebe-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="23ebe-107">Actualice las propiedades de un objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-107">Update the properties of a [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="23ebe-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="23ebe-108">Prerequisites</span></span>
<span data-ttu-id="23ebe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="23ebe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="23ebe-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="23ebe-111">Permission type</span></span>|<span data-ttu-id="23ebe-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="23ebe-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="23ebe-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="23ebe-113">Delegated (work or school account)</span></span>|<span data-ttu-id="23ebe-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="23ebe-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="23ebe-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="23ebe-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="23ebe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23ebe-116">Not supported.</span></span>|
|<span data-ttu-id="23ebe-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="23ebe-117">Application</span></span>|<span data-ttu-id="23ebe-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23ebe-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="23ebe-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="23ebe-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="23ebe-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="23ebe-120">Request headers</span></span>
|<span data-ttu-id="23ebe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23ebe-121">Header</span></span>|<span data-ttu-id="23ebe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="23ebe-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="23ebe-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="23ebe-123">Authorization</span></span>|<span data-ttu-id="23ebe-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="23ebe-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="23ebe-125">Accept</span><span class="sxs-lookup"><span data-stu-id="23ebe-125">Accept</span></span>|<span data-ttu-id="23ebe-126">application/json</span><span class="sxs-lookup"><span data-stu-id="23ebe-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="23ebe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="23ebe-127">Request body</span></span>
<span data-ttu-id="23ebe-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-128">In the request body, supply a JSON representation for the [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object.</span></span>

<span data-ttu-id="23ebe-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-129">The following table shows the properties that are required when you create the [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span></span>

|<span data-ttu-id="23ebe-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="23ebe-130">Property</span></span>|<span data-ttu-id="23ebe-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="23ebe-131">Type</span></span>|<span data-ttu-id="23ebe-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="23ebe-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="23ebe-133">id</span><span class="sxs-lookup"><span data-stu-id="23ebe-133">id</span></span>|<span data-ttu-id="23ebe-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-134">String</span></span>|<span data-ttu-id="23ebe-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="23ebe-135">Key of the entity.</span></span> <span data-ttu-id="23ebe-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-137">displayName</span><span class="sxs-lookup"><span data-stu-id="23ebe-137">displayName</span></span>|<span data-ttu-id="23ebe-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-138">String</span></span>|<span data-ttu-id="23ebe-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="23ebe-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="23ebe-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-141">descripción</span><span class="sxs-lookup"><span data-stu-id="23ebe-141">description</span></span>|<span data-ttu-id="23ebe-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-142">String</span></span>|<span data-ttu-id="23ebe-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-143">The description of the app.</span></span> <span data-ttu-id="23ebe-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-145">publicador</span><span class="sxs-lookup"><span data-stu-id="23ebe-145">publisher</span></span>|<span data-ttu-id="23ebe-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-146">String</span></span>|<span data-ttu-id="23ebe-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-147">The publisher of the app.</span></span> <span data-ttu-id="23ebe-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="23ebe-149">largeIcon</span></span>|[<span data-ttu-id="23ebe-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="23ebe-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="23ebe-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="23ebe-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="23ebe-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="23ebe-153">createdDateTime</span></span>|<span data-ttu-id="23ebe-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23ebe-154">DateTimeOffset</span></span>|<span data-ttu-id="23ebe-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-155">The date and time the app was created.</span></span> <span data-ttu-id="23ebe-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="23ebe-157">lastModifiedDateTime</span></span>|<span data-ttu-id="23ebe-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23ebe-158">DateTimeOffset</span></span>|<span data-ttu-id="23ebe-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-159">The date and time the app was last modified.</span></span> <span data-ttu-id="23ebe-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="23ebe-161">isFeatured</span></span>|<span data-ttu-id="23ebe-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="23ebe-162">Boolean</span></span>|<span data-ttu-id="23ebe-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="23ebe-164">privacyInformationUrl</span></span>|<span data-ttu-id="23ebe-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-165">String</span></span>|<span data-ttu-id="23ebe-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="23ebe-166">The privacy statement Url.</span></span> <span data-ttu-id="23ebe-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="23ebe-168">informationUrl</span></span>|<span data-ttu-id="23ebe-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-169">String</span></span>|<span data-ttu-id="23ebe-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="23ebe-170">The more information Url.</span></span> <span data-ttu-id="23ebe-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-172">owner</span><span class="sxs-lookup"><span data-stu-id="23ebe-172">owner</span></span>|<span data-ttu-id="23ebe-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-173">String</span></span>|<span data-ttu-id="23ebe-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-174">The owner of the app.</span></span> <span data-ttu-id="23ebe-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-176">developer</span><span class="sxs-lookup"><span data-stu-id="23ebe-176">developer</span></span>|<span data-ttu-id="23ebe-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-177">String</span></span>|<span data-ttu-id="23ebe-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-178">The developer of the app.</span></span> <span data-ttu-id="23ebe-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-180">notas</span><span class="sxs-lookup"><span data-stu-id="23ebe-180">notes</span></span>|<span data-ttu-id="23ebe-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-181">String</span></span>|<span data-ttu-id="23ebe-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-182">Notes for the app.</span></span> <span data-ttu-id="23ebe-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="23ebe-184">uploadState</span></span>|<span data-ttu-id="23ebe-185">Int32</span><span class="sxs-lookup"><span data-stu-id="23ebe-185">Int32</span></span>|<span data-ttu-id="23ebe-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="23ebe-186">The upload state.</span></span> <span data-ttu-id="23ebe-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="23ebe-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="23ebe-188">publishingState</span></span>|[<span data-ttu-id="23ebe-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="23ebe-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="23ebe-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-190">The publishing state for the app.</span></span> <span data-ttu-id="23ebe-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="23ebe-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="23ebe-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="23ebe-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="23ebe-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="23ebe-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="23ebe-194">appAvailability</span></span>|[<span data-ttu-id="23ebe-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="23ebe-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="23ebe-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-196">The Application's availability.</span></span> <span data-ttu-id="23ebe-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="23ebe-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="23ebe-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="23ebe-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="23ebe-199">versión</span><span class="sxs-lookup"><span data-stu-id="23ebe-199">version</span></span>|<span data-ttu-id="23ebe-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-200">String</span></span>|<span data-ttu-id="23ebe-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-201">The Application's version.</span></span> <span data-ttu-id="23ebe-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="23ebe-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="23ebe-203">packageId</span><span class="sxs-lookup"><span data-stu-id="23ebe-203">packageId</span></span>|<span data-ttu-id="23ebe-204">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-204">String</span></span>|<span data-ttu-id="23ebe-205">El identificador de paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23ebe-205">The app's package ID.</span></span>|
|<span data-ttu-id="23ebe-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="23ebe-206">appStoreUrl</span></span>|<span data-ttu-id="23ebe-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="23ebe-207">String</span></span>|<span data-ttu-id="23ebe-208">La AppStoreUrl de Android.</span><span class="sxs-lookup"><span data-stu-id="23ebe-208">The Android AppStoreUrl.</span></span>|
|<span data-ttu-id="23ebe-209">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="23ebe-209">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="23ebe-210">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="23ebe-210">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="23ebe-211">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="23ebe-211">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="23ebe-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23ebe-212">Response</span></span>
<span data-ttu-id="23ebe-213">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23ebe-213">If successful, this method returns a `200 OK` response code and an updated [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="23ebe-214">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23ebe-214">Example</span></span>
### <a name="request"></a><span data-ttu-id="23ebe-215">Solicitud</span><span class="sxs-lookup"><span data-stu-id="23ebe-215">Request</span></span>
<span data-ttu-id="23ebe-216">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="23ebe-216">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="23ebe-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23ebe-217">Response</span></span>
<span data-ttu-id="23ebe-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="23ebe-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





