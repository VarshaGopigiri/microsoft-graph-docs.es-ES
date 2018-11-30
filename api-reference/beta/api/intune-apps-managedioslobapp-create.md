---
title: Crear managedIOSLobApp
description: Crear un objeto managedIOSLobApp.
ms.openlocfilehash: 8e5e4bf9e4d713ce973394eaedfc626114ebc6da
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083012"
---
# <a name="create-managedioslobapp"></a><span data-ttu-id="804a7-103">Crear managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="804a7-103">Create managedIOSLobApp</span></span>

> <span data-ttu-id="804a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="804a7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="804a7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="804a7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="804a7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="804a7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="804a7-107">Crear un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-107">Create a new [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="804a7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="804a7-108">Prerequisites</span></span>
<span data-ttu-id="804a7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="804a7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="804a7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="804a7-111">Permission type</span></span>|<span data-ttu-id="804a7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="804a7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="804a7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="804a7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="804a7-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="804a7-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="804a7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="804a7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="804a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="804a7-116">Not supported.</span></span>|
|<span data-ttu-id="804a7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="804a7-117">Application</span></span>|<span data-ttu-id="804a7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="804a7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="804a7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="804a7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="804a7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="804a7-120">Request headers</span></span>
|<span data-ttu-id="804a7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="804a7-121">Header</span></span>|<span data-ttu-id="804a7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="804a7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="804a7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="804a7-123">Authorization</span></span>|<span data-ttu-id="804a7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="804a7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="804a7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="804a7-125">Accept</span></span>|<span data-ttu-id="804a7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="804a7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="804a7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="804a7-127">Request body</span></span>
<span data-ttu-id="804a7-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="804a7-128">In the request body, supply a JSON representation for the managedIOSLobApp object.</span></span>

<span data-ttu-id="804a7-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="804a7-129">The following table shows the properties that are required when you create the managedIOSLobApp.</span></span>

|<span data-ttu-id="804a7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="804a7-130">Property</span></span>|<span data-ttu-id="804a7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="804a7-131">Type</span></span>|<span data-ttu-id="804a7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="804a7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="804a7-133">id</span><span class="sxs-lookup"><span data-stu-id="804a7-133">id</span></span>|<span data-ttu-id="804a7-134">String</span><span class="sxs-lookup"><span data-stu-id="804a7-134">String</span></span>|<span data-ttu-id="804a7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="804a7-135">Key of the entity.</span></span> <span data-ttu-id="804a7-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-137">displayName</span><span class="sxs-lookup"><span data-stu-id="804a7-137">displayName</span></span>|<span data-ttu-id="804a7-138">String</span><span class="sxs-lookup"><span data-stu-id="804a7-138">String</span></span>|<span data-ttu-id="804a7-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="804a7-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="804a7-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-141">descripción</span><span class="sxs-lookup"><span data-stu-id="804a7-141">description</span></span>|<span data-ttu-id="804a7-142">String</span><span class="sxs-lookup"><span data-stu-id="804a7-142">String</span></span>|<span data-ttu-id="804a7-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-143">The description of the app.</span></span> <span data-ttu-id="804a7-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-145">publicador</span><span class="sxs-lookup"><span data-stu-id="804a7-145">publisher</span></span>|<span data-ttu-id="804a7-146">String</span><span class="sxs-lookup"><span data-stu-id="804a7-146">String</span></span>|<span data-ttu-id="804a7-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-147">The publisher of the app.</span></span> <span data-ttu-id="804a7-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="804a7-149">largeIcon</span></span>|[<span data-ttu-id="804a7-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="804a7-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="804a7-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="804a7-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="804a7-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="804a7-153">createdDateTime</span></span>|<span data-ttu-id="804a7-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="804a7-154">DateTimeOffset</span></span>|<span data-ttu-id="804a7-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-155">The date and time the app was created.</span></span> <span data-ttu-id="804a7-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="804a7-157">lastModifiedDateTime</span></span>|<span data-ttu-id="804a7-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="804a7-158">DateTimeOffset</span></span>|<span data-ttu-id="804a7-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-159">The date and time the app was last modified.</span></span> <span data-ttu-id="804a7-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="804a7-161">isFeatured</span></span>|<span data-ttu-id="804a7-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="804a7-162">Boolean</span></span>|<span data-ttu-id="804a7-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="804a7-164">privacyInformationUrl</span></span>|<span data-ttu-id="804a7-165">String</span><span class="sxs-lookup"><span data-stu-id="804a7-165">String</span></span>|<span data-ttu-id="804a7-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="804a7-166">The privacy statement Url.</span></span> <span data-ttu-id="804a7-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="804a7-168">informationUrl</span></span>|<span data-ttu-id="804a7-169">String</span><span class="sxs-lookup"><span data-stu-id="804a7-169">String</span></span>|<span data-ttu-id="804a7-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="804a7-170">The more information Url.</span></span> <span data-ttu-id="804a7-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-172">owner</span><span class="sxs-lookup"><span data-stu-id="804a7-172">owner</span></span>|<span data-ttu-id="804a7-173">String</span><span class="sxs-lookup"><span data-stu-id="804a7-173">String</span></span>|<span data-ttu-id="804a7-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-174">The owner of the app.</span></span> <span data-ttu-id="804a7-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-176">developer</span><span class="sxs-lookup"><span data-stu-id="804a7-176">developer</span></span>|<span data-ttu-id="804a7-177">String</span><span class="sxs-lookup"><span data-stu-id="804a7-177">String</span></span>|<span data-ttu-id="804a7-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-178">The developer of the app.</span></span> <span data-ttu-id="804a7-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-180">notas</span><span class="sxs-lookup"><span data-stu-id="804a7-180">notes</span></span>|<span data-ttu-id="804a7-181">String</span><span class="sxs-lookup"><span data-stu-id="804a7-181">String</span></span>|<span data-ttu-id="804a7-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-182">Notes for the app.</span></span> <span data-ttu-id="804a7-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="804a7-184">uploadState</span></span>|<span data-ttu-id="804a7-185">Int32</span><span class="sxs-lookup"><span data-stu-id="804a7-185">Int32</span></span>|<span data-ttu-id="804a7-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="804a7-186">The upload state.</span></span> <span data-ttu-id="804a7-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="804a7-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="804a7-188">publishingState</span></span>|[<span data-ttu-id="804a7-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="804a7-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="804a7-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-190">The publishing state for the app.</span></span> <span data-ttu-id="804a7-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="804a7-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="804a7-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="804a7-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="804a7-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="804a7-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="804a7-194">appAvailability</span></span>|[<span data-ttu-id="804a7-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="804a7-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="804a7-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-196">The Application's availability.</span></span> <span data-ttu-id="804a7-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="804a7-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="804a7-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="804a7-199">versión</span><span class="sxs-lookup"><span data-stu-id="804a7-199">version</span></span>|<span data-ttu-id="804a7-200">String</span><span class="sxs-lookup"><span data-stu-id="804a7-200">String</span></span>|<span data-ttu-id="804a7-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-201">The Application's version.</span></span> <span data-ttu-id="804a7-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="804a7-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="804a7-203">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="804a7-203">committedContentVersion</span></span>|<span data-ttu-id="804a7-204">String</span><span class="sxs-lookup"><span data-stu-id="804a7-204">String</span></span>|<span data-ttu-id="804a7-205">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="804a7-205">The internal committed content version.</span></span> <span data-ttu-id="804a7-206">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-206">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="804a7-207">fileName</span><span class="sxs-lookup"><span data-stu-id="804a7-207">fileName</span></span>|<span data-ttu-id="804a7-208">String</span><span class="sxs-lookup"><span data-stu-id="804a7-208">String</span></span>|<span data-ttu-id="804a7-209">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="804a7-209">The name of the main Lob application file.</span></span> <span data-ttu-id="804a7-210">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-210">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="804a7-211">size</span><span class="sxs-lookup"><span data-stu-id="804a7-211">size</span></span>|<span data-ttu-id="804a7-212">Int64</span><span class="sxs-lookup"><span data-stu-id="804a7-212">Int64</span></span>|<span data-ttu-id="804a7-213">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="804a7-213">The total size, including all uploaded files.</span></span> <span data-ttu-id="804a7-214">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="804a7-214">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="804a7-215">bundleId</span><span class="sxs-lookup"><span data-stu-id="804a7-215">bundleId</span></span>|<span data-ttu-id="804a7-216">String</span><span class="sxs-lookup"><span data-stu-id="804a7-216">String</span></span>|<span data-ttu-id="804a7-217">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="804a7-217">The Identity Name.</span></span>|
|<span data-ttu-id="804a7-218">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="804a7-218">applicableDeviceType</span></span>|[<span data-ttu-id="804a7-219">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="804a7-219">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="804a7-220">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="804a7-220">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="804a7-221">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="804a7-221">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="804a7-222">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="804a7-222">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="804a7-223">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="804a7-223">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="804a7-224">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="804a7-224">expirationDateTime</span></span>|<span data-ttu-id="804a7-225">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="804a7-225">DateTimeOffset</span></span>|<span data-ttu-id="804a7-226">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="804a7-226">The expiration time.</span></span>|
|<span data-ttu-id="804a7-227">versionNumber</span><span class="sxs-lookup"><span data-stu-id="804a7-227">versionNumber</span></span>|<span data-ttu-id="804a7-228">String</span><span class="sxs-lookup"><span data-stu-id="804a7-228">String</span></span>|<span data-ttu-id="804a7-229">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="804a7-229">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="804a7-230">buildNumber</span><span class="sxs-lookup"><span data-stu-id="804a7-230">buildNumber</span></span>|<span data-ttu-id="804a7-231">String</span><span class="sxs-lookup"><span data-stu-id="804a7-231">String</span></span>|<span data-ttu-id="804a7-232">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="804a7-232">The build number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="804a7-233">identityVersion</span><span class="sxs-lookup"><span data-stu-id="804a7-233">identityVersion</span></span>|<span data-ttu-id="804a7-234">String</span><span class="sxs-lookup"><span data-stu-id="804a7-234">String</span></span>|<span data-ttu-id="804a7-235">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="804a7-235">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="804a7-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="804a7-236">Response</span></span>
<span data-ttu-id="804a7-237">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="804a7-237">If successful, this method returns a `201 Created` response code and a [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="804a7-238">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="804a7-238">Example</span></span>
### <a name="request"></a><span data-ttu-id="804a7-239">Solicitud</span><span class="sxs-lookup"><span data-stu-id="804a7-239">Request</span></span>
<span data-ttu-id="804a7-240">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="804a7-240">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1421

{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "bundleId": "Bundle Id value",
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
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value",
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="804a7-241">Respuesta</span><span class="sxs-lookup"><span data-stu-id="804a7-241">Response</span></span>
<span data-ttu-id="804a7-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="804a7-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1529

{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
  "id": "8f59792d-792d-8f59-2d79-598f2d79598f",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "bundleId": "Bundle Id value",
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
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value",
  "identityVersion": "Identity Version value"
}
```




