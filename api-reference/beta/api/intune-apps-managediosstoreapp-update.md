---
title: Actualizar managedIOSStoreApp
description: Actualice las propiedades de un objeto managedIOSStoreApp.
ms.openlocfilehash: f65cfb1c45b376db753c73c3fe1fa58b0f5af309
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083341"
---
# <a name="update-managediosstoreapp"></a><span data-ttu-id="c4088-103">Actualizar managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="c4088-103">Update managedIOSStoreApp</span></span>

> <span data-ttu-id="c4088-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c4088-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c4088-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c4088-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c4088-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c4088-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c4088-107">Actualice las propiedades de un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-107">Update the properties of a [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c4088-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c4088-108">Prerequisites</span></span>
<span data-ttu-id="c4088-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c4088-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c4088-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c4088-111">Permission type</span></span>|<span data-ttu-id="c4088-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c4088-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c4088-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c4088-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c4088-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4088-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c4088-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c4088-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c4088-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4088-116">Not supported.</span></span>|
|<span data-ttu-id="c4088-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c4088-117">Application</span></span>|<span data-ttu-id="c4088-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4088-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c4088-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c4088-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="c4088-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c4088-120">Request headers</span></span>
|<span data-ttu-id="c4088-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4088-121">Header</span></span>|<span data-ttu-id="c4088-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c4088-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c4088-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c4088-123">Authorization</span></span>|<span data-ttu-id="c4088-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c4088-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c4088-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c4088-125">Accept</span></span>|<span data-ttu-id="c4088-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c4088-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c4088-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c4088-127">Request body</span></span>
<span data-ttu-id="c4088-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-128">In the request body, supply a JSON representation for the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>

<span data-ttu-id="c4088-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-129">The following table shows the properties that are required when you create the [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span></span>

|<span data-ttu-id="c4088-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c4088-130">Property</span></span>|<span data-ttu-id="c4088-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4088-131">Type</span></span>|<span data-ttu-id="c4088-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4088-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c4088-133">id</span><span class="sxs-lookup"><span data-stu-id="c4088-133">id</span></span>|<span data-ttu-id="c4088-134">String</span><span class="sxs-lookup"><span data-stu-id="c4088-134">String</span></span>|<span data-ttu-id="c4088-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c4088-135">Key of the entity.</span></span> <span data-ttu-id="c4088-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-137">displayName</span><span class="sxs-lookup"><span data-stu-id="c4088-137">displayName</span></span>|<span data-ttu-id="c4088-138">String</span><span class="sxs-lookup"><span data-stu-id="c4088-138">String</span></span>|<span data-ttu-id="c4088-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="c4088-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="c4088-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-141">descripción</span><span class="sxs-lookup"><span data-stu-id="c4088-141">description</span></span>|<span data-ttu-id="c4088-142">String</span><span class="sxs-lookup"><span data-stu-id="c4088-142">String</span></span>|<span data-ttu-id="c4088-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-143">The description of the app.</span></span> <span data-ttu-id="c4088-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-145">publicador</span><span class="sxs-lookup"><span data-stu-id="c4088-145">publisher</span></span>|<span data-ttu-id="c4088-146">String</span><span class="sxs-lookup"><span data-stu-id="c4088-146">String</span></span>|<span data-ttu-id="c4088-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-147">The publisher of the app.</span></span> <span data-ttu-id="c4088-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="c4088-149">largeIcon</span></span>|[<span data-ttu-id="c4088-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="c4088-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="c4088-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="c4088-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="c4088-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c4088-153">createdDateTime</span></span>|<span data-ttu-id="c4088-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c4088-154">DateTimeOffset</span></span>|<span data-ttu-id="c4088-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-155">The date and time the app was created.</span></span> <span data-ttu-id="c4088-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c4088-157">lastModifiedDateTime</span></span>|<span data-ttu-id="c4088-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c4088-158">DateTimeOffset</span></span>|<span data-ttu-id="c4088-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-159">The date and time the app was last modified.</span></span> <span data-ttu-id="c4088-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="c4088-161">isFeatured</span></span>|<span data-ttu-id="c4088-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="c4088-162">Boolean</span></span>|<span data-ttu-id="c4088-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="c4088-164">privacyInformationUrl</span></span>|<span data-ttu-id="c4088-165">String</span><span class="sxs-lookup"><span data-stu-id="c4088-165">String</span></span>|<span data-ttu-id="c4088-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="c4088-166">The privacy statement Url.</span></span> <span data-ttu-id="c4088-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="c4088-168">informationUrl</span></span>|<span data-ttu-id="c4088-169">String</span><span class="sxs-lookup"><span data-stu-id="c4088-169">String</span></span>|<span data-ttu-id="c4088-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4088-170">The more information Url.</span></span> <span data-ttu-id="c4088-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-172">owner</span><span class="sxs-lookup"><span data-stu-id="c4088-172">owner</span></span>|<span data-ttu-id="c4088-173">String</span><span class="sxs-lookup"><span data-stu-id="c4088-173">String</span></span>|<span data-ttu-id="c4088-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-174">The owner of the app.</span></span> <span data-ttu-id="c4088-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-176">developer</span><span class="sxs-lookup"><span data-stu-id="c4088-176">developer</span></span>|<span data-ttu-id="c4088-177">String</span><span class="sxs-lookup"><span data-stu-id="c4088-177">String</span></span>|<span data-ttu-id="c4088-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-178">The developer of the app.</span></span> <span data-ttu-id="c4088-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-180">notas</span><span class="sxs-lookup"><span data-stu-id="c4088-180">notes</span></span>|<span data-ttu-id="c4088-181">String</span><span class="sxs-lookup"><span data-stu-id="c4088-181">String</span></span>|<span data-ttu-id="c4088-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-182">Notes for the app.</span></span> <span data-ttu-id="c4088-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="c4088-184">uploadState</span></span>|<span data-ttu-id="c4088-185">Int32</span><span class="sxs-lookup"><span data-stu-id="c4088-185">Int32</span></span>|<span data-ttu-id="c4088-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="c4088-186">The upload state.</span></span> <span data-ttu-id="c4088-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c4088-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="c4088-188">publishingState</span></span>|[<span data-ttu-id="c4088-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="c4088-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="c4088-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-190">The publishing state for the app.</span></span> <span data-ttu-id="c4088-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="c4088-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="c4088-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="c4088-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="c4088-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="c4088-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="c4088-194">appAvailability</span></span>|[<span data-ttu-id="c4088-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="c4088-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="c4088-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-196">The Application's availability.</span></span> <span data-ttu-id="c4088-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="c4088-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="c4088-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="c4088-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="c4088-199">versión</span><span class="sxs-lookup"><span data-stu-id="c4088-199">version</span></span>|<span data-ttu-id="c4088-200">String</span><span class="sxs-lookup"><span data-stu-id="c4088-200">String</span></span>|<span data-ttu-id="c4088-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-201">The Application's version.</span></span> <span data-ttu-id="c4088-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="c4088-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="c4088-203">bundleId</span><span class="sxs-lookup"><span data-stu-id="c4088-203">bundleId</span></span>|<span data-ttu-id="c4088-204">String</span><span class="sxs-lookup"><span data-stu-id="c4088-204">String</span></span>|<span data-ttu-id="c4088-205">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-205">The app's Bundle ID.</span></span>|
|<span data-ttu-id="c4088-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="c4088-206">appStoreUrl</span></span>|<span data-ttu-id="c4088-207">String</span><span class="sxs-lookup"><span data-stu-id="c4088-207">String</span></span>|<span data-ttu-id="c4088-208">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="c4088-208">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="c4088-209">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="c4088-209">applicableDeviceType</span></span>|[<span data-ttu-id="c4088-210">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="c4088-210">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="c4088-211">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4088-211">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="c4088-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c4088-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="c4088-213">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c4088-213">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="c4088-214">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="c4088-214">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="c4088-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4088-215">Response</span></span>
<span data-ttu-id="c4088-216">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4088-216">If successful, this method returns a `200 OK` response code and an updated [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c4088-217">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4088-217">Example</span></span>
### <a name="request"></a><span data-ttu-id="c4088-218">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c4088-218">Request</span></span>
<span data-ttu-id="c4088-219">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4088-219">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1113

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

### <a name="response"></a><span data-ttu-id="c4088-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4088-220">Response</span></span>
<span data-ttu-id="c4088-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c4088-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1278

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
  "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
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





