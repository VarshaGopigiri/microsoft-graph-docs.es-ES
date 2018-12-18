---
title: Crear managedIOSLobApp
description: Crear un objeto managedIOSLobApp.
author: tfitzmac
ms.openlocfilehash: 2ba9cfd96f59c1d444e0890224fe5d169493a9e7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323747"
---
# <a name="create-managedioslobapp"></a><span data-ttu-id="33f69-103">Crear managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="33f69-103">Create managedIOSLobApp</span></span>

> <span data-ttu-id="33f69-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="33f69-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="33f69-105">Crear un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-105">Create a new [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="33f69-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="33f69-106">Prerequisites</span></span>
<span data-ttu-id="33f69-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33f69-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="33f69-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33f69-109">Permission type</span></span>|<span data-ttu-id="33f69-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33f69-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="33f69-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33f69-111">Delegated (work or school account)</span></span>|<span data-ttu-id="33f69-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="33f69-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="33f69-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33f69-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="33f69-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33f69-114">Not supported.</span></span>|
|<span data-ttu-id="33f69-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33f69-115">Application</span></span>|<span data-ttu-id="33f69-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33f69-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="33f69-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33f69-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="33f69-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="33f69-118">Request headers</span></span>
|<span data-ttu-id="33f69-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33f69-119">Header</span></span>|<span data-ttu-id="33f69-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33f69-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="33f69-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="33f69-121">Authorization</span></span>|<span data-ttu-id="33f69-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="33f69-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="33f69-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="33f69-123">Accept</span></span>|<span data-ttu-id="33f69-124">application/json</span><span class="sxs-lookup"><span data-stu-id="33f69-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="33f69-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33f69-125">Request body</span></span>
<span data-ttu-id="33f69-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="33f69-126">In the request body, supply a JSON representation for the managedIOSLobApp object.</span></span>

<span data-ttu-id="33f69-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="33f69-127">The following table shows the properties that are required when you create the managedIOSLobApp.</span></span>

|<span data-ttu-id="33f69-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33f69-128">Property</span></span>|<span data-ttu-id="33f69-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="33f69-129">Type</span></span>|<span data-ttu-id="33f69-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="33f69-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="33f69-131">id</span><span class="sxs-lookup"><span data-stu-id="33f69-131">id</span></span>|<span data-ttu-id="33f69-132">String</span><span class="sxs-lookup"><span data-stu-id="33f69-132">String</span></span>|<span data-ttu-id="33f69-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="33f69-133">Key of the entity.</span></span> <span data-ttu-id="33f69-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-135">displayName</span><span class="sxs-lookup"><span data-stu-id="33f69-135">displayName</span></span>|<span data-ttu-id="33f69-136">String</span><span class="sxs-lookup"><span data-stu-id="33f69-136">String</span></span>|<span data-ttu-id="33f69-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="33f69-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="33f69-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-139">descripción</span><span class="sxs-lookup"><span data-stu-id="33f69-139">description</span></span>|<span data-ttu-id="33f69-140">String</span><span class="sxs-lookup"><span data-stu-id="33f69-140">String</span></span>|<span data-ttu-id="33f69-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-141">The description of the app.</span></span> <span data-ttu-id="33f69-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-143">publicador</span><span class="sxs-lookup"><span data-stu-id="33f69-143">publisher</span></span>|<span data-ttu-id="33f69-144">String</span><span class="sxs-lookup"><span data-stu-id="33f69-144">String</span></span>|<span data-ttu-id="33f69-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-145">The publisher of the app.</span></span> <span data-ttu-id="33f69-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="33f69-147">largeIcon</span></span>|[<span data-ttu-id="33f69-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="33f69-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="33f69-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="33f69-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="33f69-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="33f69-151">createdDateTime</span></span>|<span data-ttu-id="33f69-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="33f69-152">DateTimeOffset</span></span>|<span data-ttu-id="33f69-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-153">The date and time the app was created.</span></span> <span data-ttu-id="33f69-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="33f69-155">lastModifiedDateTime</span></span>|<span data-ttu-id="33f69-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="33f69-156">DateTimeOffset</span></span>|<span data-ttu-id="33f69-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-157">The date and time the app was last modified.</span></span> <span data-ttu-id="33f69-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="33f69-159">isFeatured</span></span>|<span data-ttu-id="33f69-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="33f69-160">Boolean</span></span>|<span data-ttu-id="33f69-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="33f69-162">privacyInformationUrl</span></span>|<span data-ttu-id="33f69-163">String</span><span class="sxs-lookup"><span data-stu-id="33f69-163">String</span></span>|<span data-ttu-id="33f69-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="33f69-164">The privacy statement Url.</span></span> <span data-ttu-id="33f69-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="33f69-166">informationUrl</span></span>|<span data-ttu-id="33f69-167">String</span><span class="sxs-lookup"><span data-stu-id="33f69-167">String</span></span>|<span data-ttu-id="33f69-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="33f69-168">The more information Url.</span></span> <span data-ttu-id="33f69-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-170">owner</span><span class="sxs-lookup"><span data-stu-id="33f69-170">owner</span></span>|<span data-ttu-id="33f69-171">String</span><span class="sxs-lookup"><span data-stu-id="33f69-171">String</span></span>|<span data-ttu-id="33f69-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-172">The owner of the app.</span></span> <span data-ttu-id="33f69-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-174">developer</span><span class="sxs-lookup"><span data-stu-id="33f69-174">developer</span></span>|<span data-ttu-id="33f69-175">String</span><span class="sxs-lookup"><span data-stu-id="33f69-175">String</span></span>|<span data-ttu-id="33f69-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-176">The developer of the app.</span></span> <span data-ttu-id="33f69-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-178">notas</span><span class="sxs-lookup"><span data-stu-id="33f69-178">notes</span></span>|<span data-ttu-id="33f69-179">String</span><span class="sxs-lookup"><span data-stu-id="33f69-179">String</span></span>|<span data-ttu-id="33f69-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-180">Notes for the app.</span></span> <span data-ttu-id="33f69-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="33f69-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="33f69-182">publishingState</span></span>|[<span data-ttu-id="33f69-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="33f69-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="33f69-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-184">The publishing state for the app.</span></span> <span data-ttu-id="33f69-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="33f69-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="33f69-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="33f69-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="33f69-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="33f69-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="33f69-188">appAvailability</span></span>|[<span data-ttu-id="33f69-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="33f69-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="33f69-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-190">The Application's availability.</span></span> <span data-ttu-id="33f69-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="33f69-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="33f69-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="33f69-193">versión</span><span class="sxs-lookup"><span data-stu-id="33f69-193">version</span></span>|<span data-ttu-id="33f69-194">String</span><span class="sxs-lookup"><span data-stu-id="33f69-194">String</span></span>|<span data-ttu-id="33f69-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-195">The Application's version.</span></span> <span data-ttu-id="33f69-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="33f69-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="33f69-197">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="33f69-197">committedContentVersion</span></span>|<span data-ttu-id="33f69-198">String</span><span class="sxs-lookup"><span data-stu-id="33f69-198">String</span></span>|<span data-ttu-id="33f69-199">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="33f69-199">The internal committed content version.</span></span> <span data-ttu-id="33f69-200">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-200">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="33f69-201">fileName</span><span class="sxs-lookup"><span data-stu-id="33f69-201">fileName</span></span>|<span data-ttu-id="33f69-202">String</span><span class="sxs-lookup"><span data-stu-id="33f69-202">String</span></span>|<span data-ttu-id="33f69-203">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="33f69-203">The name of the main Lob application file.</span></span> <span data-ttu-id="33f69-204">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-204">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="33f69-205">size</span><span class="sxs-lookup"><span data-stu-id="33f69-205">size</span></span>|<span data-ttu-id="33f69-206">Int64</span><span class="sxs-lookup"><span data-stu-id="33f69-206">Int64</span></span>|<span data-ttu-id="33f69-207">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="33f69-207">The total size, including all uploaded files.</span></span> <span data-ttu-id="33f69-208">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="33f69-208">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="33f69-209">bundleId</span><span class="sxs-lookup"><span data-stu-id="33f69-209">bundleId</span></span>|<span data-ttu-id="33f69-210">String</span><span class="sxs-lookup"><span data-stu-id="33f69-210">String</span></span>|<span data-ttu-id="33f69-211">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="33f69-211">The Identity Name.</span></span>|
|<span data-ttu-id="33f69-212">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="33f69-212">applicableDeviceType</span></span>|[<span data-ttu-id="33f69-213">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="33f69-213">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="33f69-214">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="33f69-214">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="33f69-215">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="33f69-215">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="33f69-216">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="33f69-216">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="33f69-217">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="33f69-217">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="33f69-218">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="33f69-218">expirationDateTime</span></span>|<span data-ttu-id="33f69-219">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="33f69-219">DateTimeOffset</span></span>|<span data-ttu-id="33f69-220">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="33f69-220">The expiration time.</span></span>|
|<span data-ttu-id="33f69-221">versionNumber</span><span class="sxs-lookup"><span data-stu-id="33f69-221">versionNumber</span></span>|<span data-ttu-id="33f69-222">String</span><span class="sxs-lookup"><span data-stu-id="33f69-222">String</span></span>|<span data-ttu-id="33f69-223">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="33f69-223">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="33f69-224">buildNumber</span><span class="sxs-lookup"><span data-stu-id="33f69-224">buildNumber</span></span>|<span data-ttu-id="33f69-225">String</span><span class="sxs-lookup"><span data-stu-id="33f69-225">String</span></span>|<span data-ttu-id="33f69-226">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="33f69-226">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="33f69-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33f69-227">Response</span></span>
<span data-ttu-id="33f69-228">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33f69-228">If successful, this method returns a `201 Created` response code and a [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="33f69-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33f69-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="33f69-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33f69-230">Request</span></span>
<span data-ttu-id="33f69-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33f69-231">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1287

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
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
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
  "buildNumber": "Build Number value"
}
```

### <a name="response"></a><span data-ttu-id="33f69-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33f69-232">Response</span></span>
<span data-ttu-id="33f69-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="33f69-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1459

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
  "buildNumber": "Build Number value"
}
```



