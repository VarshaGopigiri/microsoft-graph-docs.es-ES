---
title: Actualizar managedAndroidLobApp
description: Actualice las propiedades de un objeto managedAndroidLobApp.
author: tfitzmac
ms.openlocfilehash: 7d121570b5d1a5de6529dcf5b163354849178366
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346266"
---
# <a name="update-managedandroidlobapp"></a><span data-ttu-id="eeadc-103">Actualizar managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="eeadc-103">Update managedAndroidLobApp</span></span>

> <span data-ttu-id="eeadc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eeadc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eeadc-105">Actualice las propiedades de un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-105">Update the properties of a [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eeadc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eeadc-106">Prerequisites</span></span>
<span data-ttu-id="eeadc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eeadc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eeadc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eeadc-109">Permission type</span></span>|<span data-ttu-id="eeadc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eeadc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eeadc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eeadc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="eeadc-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eeadc-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="eeadc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eeadc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eeadc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eeadc-114">Not supported.</span></span>|
|<span data-ttu-id="eeadc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eeadc-115">Application</span></span>|<span data-ttu-id="eeadc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eeadc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eeadc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eeadc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="eeadc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eeadc-118">Request headers</span></span>
|<span data-ttu-id="eeadc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eeadc-119">Header</span></span>|<span data-ttu-id="eeadc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eeadc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eeadc-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="eeadc-121">Authorization</span></span>|<span data-ttu-id="eeadc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eeadc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eeadc-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eeadc-123">Accept</span></span>|<span data-ttu-id="eeadc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="eeadc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eeadc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eeadc-125">Request body</span></span>
<span data-ttu-id="eeadc-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-126">In the request body, supply a JSON representation for the [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>

<span data-ttu-id="eeadc-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-127">The following table shows the properties that are required when you create the [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span></span>

|<span data-ttu-id="eeadc-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eeadc-128">Property</span></span>|<span data-ttu-id="eeadc-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="eeadc-129">Type</span></span>|<span data-ttu-id="eeadc-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeadc-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eeadc-131">id</span><span class="sxs-lookup"><span data-stu-id="eeadc-131">id</span></span>|<span data-ttu-id="eeadc-132">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-132">String</span></span>|<span data-ttu-id="eeadc-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="eeadc-133">Key of the entity.</span></span> <span data-ttu-id="eeadc-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-135">displayName</span><span class="sxs-lookup"><span data-stu-id="eeadc-135">displayName</span></span>|<span data-ttu-id="eeadc-136">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-136">String</span></span>|<span data-ttu-id="eeadc-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="eeadc-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="eeadc-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-139">descripción</span><span class="sxs-lookup"><span data-stu-id="eeadc-139">description</span></span>|<span data-ttu-id="eeadc-140">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-140">String</span></span>|<span data-ttu-id="eeadc-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-141">The description of the app.</span></span> <span data-ttu-id="eeadc-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-143">publicador</span><span class="sxs-lookup"><span data-stu-id="eeadc-143">publisher</span></span>|<span data-ttu-id="eeadc-144">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-144">String</span></span>|<span data-ttu-id="eeadc-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-145">The publisher of the app.</span></span> <span data-ttu-id="eeadc-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="eeadc-147">largeIcon</span></span>|[<span data-ttu-id="eeadc-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="eeadc-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="eeadc-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="eeadc-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="eeadc-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="eeadc-151">createdDateTime</span></span>|<span data-ttu-id="eeadc-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eeadc-152">DateTimeOffset</span></span>|<span data-ttu-id="eeadc-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-153">The date and time the app was created.</span></span> <span data-ttu-id="eeadc-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="eeadc-155">lastModifiedDateTime</span></span>|<span data-ttu-id="eeadc-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eeadc-156">DateTimeOffset</span></span>|<span data-ttu-id="eeadc-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-157">The date and time the app was last modified.</span></span> <span data-ttu-id="eeadc-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="eeadc-159">isFeatured</span></span>|<span data-ttu-id="eeadc-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="eeadc-160">Boolean</span></span>|<span data-ttu-id="eeadc-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="eeadc-162">privacyInformationUrl</span></span>|<span data-ttu-id="eeadc-163">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-163">String</span></span>|<span data-ttu-id="eeadc-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="eeadc-164">The privacy statement Url.</span></span> <span data-ttu-id="eeadc-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="eeadc-166">informationUrl</span></span>|<span data-ttu-id="eeadc-167">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-167">String</span></span>|<span data-ttu-id="eeadc-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="eeadc-168">The more information Url.</span></span> <span data-ttu-id="eeadc-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-170">owner</span><span class="sxs-lookup"><span data-stu-id="eeadc-170">owner</span></span>|<span data-ttu-id="eeadc-171">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-171">String</span></span>|<span data-ttu-id="eeadc-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-172">The owner of the app.</span></span> <span data-ttu-id="eeadc-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-174">developer</span><span class="sxs-lookup"><span data-stu-id="eeadc-174">developer</span></span>|<span data-ttu-id="eeadc-175">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-175">String</span></span>|<span data-ttu-id="eeadc-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-176">The developer of the app.</span></span> <span data-ttu-id="eeadc-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-178">notas</span><span class="sxs-lookup"><span data-stu-id="eeadc-178">notes</span></span>|<span data-ttu-id="eeadc-179">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-179">String</span></span>|<span data-ttu-id="eeadc-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-180">Notes for the app.</span></span> <span data-ttu-id="eeadc-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="eeadc-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="eeadc-182">publishingState</span></span>|[<span data-ttu-id="eeadc-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="eeadc-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="eeadc-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-184">The publishing state for the app.</span></span> <span data-ttu-id="eeadc-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="eeadc-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="eeadc-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="eeadc-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="eeadc-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="eeadc-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="eeadc-188">appAvailability</span></span>|[<span data-ttu-id="eeadc-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="eeadc-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="eeadc-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-190">The Application's availability.</span></span> <span data-ttu-id="eeadc-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="eeadc-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="eeadc-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="eeadc-193">versión</span><span class="sxs-lookup"><span data-stu-id="eeadc-193">version</span></span>|<span data-ttu-id="eeadc-194">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-194">String</span></span>|<span data-ttu-id="eeadc-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeadc-195">The Application's version.</span></span> <span data-ttu-id="eeadc-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="eeadc-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="eeadc-197">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="eeadc-197">committedContentVersion</span></span>|<span data-ttu-id="eeadc-198">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-198">String</span></span>|<span data-ttu-id="eeadc-199">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="eeadc-199">The internal committed content version.</span></span> <span data-ttu-id="eeadc-200">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-200">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="eeadc-201">fileName</span><span class="sxs-lookup"><span data-stu-id="eeadc-201">fileName</span></span>|<span data-ttu-id="eeadc-202">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-202">String</span></span>|<span data-ttu-id="eeadc-203">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="eeadc-203">The name of the main Lob application file.</span></span> <span data-ttu-id="eeadc-204">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-204">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="eeadc-205">size</span><span class="sxs-lookup"><span data-stu-id="eeadc-205">size</span></span>|<span data-ttu-id="eeadc-206">Int64</span><span class="sxs-lookup"><span data-stu-id="eeadc-206">Int64</span></span>|<span data-ttu-id="eeadc-207">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="eeadc-207">The total size, including all uploaded files.</span></span> <span data-ttu-id="eeadc-208">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="eeadc-208">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="eeadc-209">packageId</span><span class="sxs-lookup"><span data-stu-id="eeadc-209">packageId</span></span>|<span data-ttu-id="eeadc-210">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-210">String</span></span>|<span data-ttu-id="eeadc-211">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="eeadc-211">The package identifier.</span></span>|
|<span data-ttu-id="eeadc-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="eeadc-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="eeadc-213">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="eeadc-213">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="eeadc-214">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="eeadc-214">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="eeadc-215">versionName</span><span class="sxs-lookup"><span data-stu-id="eeadc-215">versionName</span></span>|<span data-ttu-id="eeadc-216">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-216">String</span></span>|<span data-ttu-id="eeadc-217">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="eeadc-217">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="eeadc-218">versionCode</span><span class="sxs-lookup"><span data-stu-id="eeadc-218">versionCode</span></span>|<span data-ttu-id="eeadc-219">String</span><span class="sxs-lookup"><span data-stu-id="eeadc-219">String</span></span>|<span data-ttu-id="eeadc-220">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="eeadc-220">The version code of managed Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="eeadc-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eeadc-221">Response</span></span>
<span data-ttu-id="eeadc-222">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eeadc-222">If successful, this method returns a `200 OK` response code and an updated [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eeadc-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eeadc-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="eeadc-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eeadc-224">Request</span></span>
<span data-ttu-id="eeadc-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eeadc-225">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1153

{
  "@odata.type": "#microsoft.graph.managedAndroidLobApp",
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
  "packageId": "Package Id value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```

### <a name="response"></a><span data-ttu-id="eeadc-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eeadc-226">Response</span></span>
<span data-ttu-id="eeadc-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eeadc-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1325

{
  "@odata.type": "#microsoft.graph.managedAndroidLobApp",
  "id": "802b7ed3-7ed3-802b-d37e-2b80d37e2b80",
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
  "packageId": "Package Id value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```



