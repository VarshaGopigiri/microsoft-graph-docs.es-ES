---
title: Actualizar managedAndroidLobApp
description: Actualice las propiedades de un objeto managedAndroidLobApp.
ms.openlocfilehash: 8991efc1a3957100902a3801a284a17ee93c659a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030716"
---
# <a name="update-managedandroidlobapp"></a><span data-ttu-id="4b698-103">Actualizar managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="4b698-103">Update managedAndroidLobApp</span></span>

> <span data-ttu-id="4b698-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4b698-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4b698-105">Actualice las propiedades de un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-105">Update the properties of a [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4b698-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4b698-106">Prerequisites</span></span>
<span data-ttu-id="4b698-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4b698-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4b698-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4b698-109">Permission type</span></span>|<span data-ttu-id="4b698-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4b698-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4b698-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4b698-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4b698-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4b698-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4b698-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4b698-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4b698-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4b698-114">Not supported.</span></span>|
|<span data-ttu-id="4b698-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4b698-115">Application</span></span>|<span data-ttu-id="4b698-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4b698-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4b698-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4b698-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="4b698-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4b698-118">Request headers</span></span>
|<span data-ttu-id="4b698-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b698-119">Header</span></span>|<span data-ttu-id="4b698-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4b698-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4b698-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4b698-121">Authorization</span></span>|<span data-ttu-id="4b698-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4b698-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4b698-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4b698-123">Accept</span></span>|<span data-ttu-id="4b698-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4b698-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4b698-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4b698-125">Request body</span></span>
<span data-ttu-id="4b698-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-126">In the request body, supply a JSON representation for the [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>

<span data-ttu-id="4b698-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-127">The following table shows the properties that are required when you create the [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span></span>

|<span data-ttu-id="4b698-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b698-128">Property</span></span>|<span data-ttu-id="4b698-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b698-129">Type</span></span>|<span data-ttu-id="4b698-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b698-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4b698-131">id</span><span class="sxs-lookup"><span data-stu-id="4b698-131">id</span></span>|<span data-ttu-id="4b698-132">String</span><span class="sxs-lookup"><span data-stu-id="4b698-132">String</span></span>|<span data-ttu-id="4b698-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4b698-133">Key of the entity.</span></span> <span data-ttu-id="4b698-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-135">displayName</span><span class="sxs-lookup"><span data-stu-id="4b698-135">displayName</span></span>|<span data-ttu-id="4b698-136">String</span><span class="sxs-lookup"><span data-stu-id="4b698-136">String</span></span>|<span data-ttu-id="4b698-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="4b698-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="4b698-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-139">descripción</span><span class="sxs-lookup"><span data-stu-id="4b698-139">description</span></span>|<span data-ttu-id="4b698-140">String</span><span class="sxs-lookup"><span data-stu-id="4b698-140">String</span></span>|<span data-ttu-id="4b698-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-141">The description of the app.</span></span> <span data-ttu-id="4b698-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-143">publicador</span><span class="sxs-lookup"><span data-stu-id="4b698-143">publisher</span></span>|<span data-ttu-id="4b698-144">String</span><span class="sxs-lookup"><span data-stu-id="4b698-144">String</span></span>|<span data-ttu-id="4b698-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-145">The publisher of the app.</span></span> <span data-ttu-id="4b698-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="4b698-147">largeIcon</span></span>|[<span data-ttu-id="4b698-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4b698-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="4b698-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="4b698-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="4b698-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4b698-151">createdDateTime</span></span>|<span data-ttu-id="4b698-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b698-152">DateTimeOffset</span></span>|<span data-ttu-id="4b698-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-153">The date and time the app was created.</span></span> <span data-ttu-id="4b698-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4b698-155">lastModifiedDateTime</span></span>|<span data-ttu-id="4b698-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b698-156">DateTimeOffset</span></span>|<span data-ttu-id="4b698-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-157">The date and time the app was last modified.</span></span> <span data-ttu-id="4b698-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="4b698-159">isFeatured</span></span>|<span data-ttu-id="4b698-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="4b698-160">Boolean</span></span>|<span data-ttu-id="4b698-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="4b698-162">privacyInformationUrl</span></span>|<span data-ttu-id="4b698-163">String</span><span class="sxs-lookup"><span data-stu-id="4b698-163">String</span></span>|<span data-ttu-id="4b698-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="4b698-164">The privacy statement Url.</span></span> <span data-ttu-id="4b698-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="4b698-166">informationUrl</span></span>|<span data-ttu-id="4b698-167">String</span><span class="sxs-lookup"><span data-stu-id="4b698-167">String</span></span>|<span data-ttu-id="4b698-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4b698-168">The more information Url.</span></span> <span data-ttu-id="4b698-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-170">owner</span><span class="sxs-lookup"><span data-stu-id="4b698-170">owner</span></span>|<span data-ttu-id="4b698-171">String</span><span class="sxs-lookup"><span data-stu-id="4b698-171">String</span></span>|<span data-ttu-id="4b698-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-172">The owner of the app.</span></span> <span data-ttu-id="4b698-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-174">developer</span><span class="sxs-lookup"><span data-stu-id="4b698-174">developer</span></span>|<span data-ttu-id="4b698-175">String</span><span class="sxs-lookup"><span data-stu-id="4b698-175">String</span></span>|<span data-ttu-id="4b698-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-176">The developer of the app.</span></span> <span data-ttu-id="4b698-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-178">notas</span><span class="sxs-lookup"><span data-stu-id="4b698-178">notes</span></span>|<span data-ttu-id="4b698-179">String</span><span class="sxs-lookup"><span data-stu-id="4b698-179">String</span></span>|<span data-ttu-id="4b698-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-180">Notes for the app.</span></span> <span data-ttu-id="4b698-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4b698-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="4b698-182">publishingState</span></span>|[<span data-ttu-id="4b698-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="4b698-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="4b698-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-184">The publishing state for the app.</span></span> <span data-ttu-id="4b698-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="4b698-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="4b698-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="4b698-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="4b698-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="4b698-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="4b698-188">appAvailability</span></span>|[<span data-ttu-id="4b698-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="4b698-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="4b698-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-190">The Application's availability.</span></span> <span data-ttu-id="4b698-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="4b698-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="4b698-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="4b698-193">versión</span><span class="sxs-lookup"><span data-stu-id="4b698-193">version</span></span>|<span data-ttu-id="4b698-194">String</span><span class="sxs-lookup"><span data-stu-id="4b698-194">String</span></span>|<span data-ttu-id="4b698-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b698-195">The Application's version.</span></span> <span data-ttu-id="4b698-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="4b698-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="4b698-197">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="4b698-197">committedContentVersion</span></span>|<span data-ttu-id="4b698-198">String</span><span class="sxs-lookup"><span data-stu-id="4b698-198">String</span></span>|<span data-ttu-id="4b698-199">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="4b698-199">The internal committed content version.</span></span> <span data-ttu-id="4b698-200">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-200">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="4b698-201">fileName</span><span class="sxs-lookup"><span data-stu-id="4b698-201">fileName</span></span>|<span data-ttu-id="4b698-202">String</span><span class="sxs-lookup"><span data-stu-id="4b698-202">String</span></span>|<span data-ttu-id="4b698-203">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="4b698-203">The name of the main Lob application file.</span></span> <span data-ttu-id="4b698-204">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-204">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="4b698-205">size</span><span class="sxs-lookup"><span data-stu-id="4b698-205">size</span></span>|<span data-ttu-id="4b698-206">Int64</span><span class="sxs-lookup"><span data-stu-id="4b698-206">Int64</span></span>|<span data-ttu-id="4b698-207">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="4b698-207">The total size, including all uploaded files.</span></span> <span data-ttu-id="4b698-208">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b698-208">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="4b698-209">packageId</span><span class="sxs-lookup"><span data-stu-id="4b698-209">packageId</span></span>|<span data-ttu-id="4b698-210">String</span><span class="sxs-lookup"><span data-stu-id="4b698-210">String</span></span>|<span data-ttu-id="4b698-211">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="4b698-211">The package identifier.</span></span>|
|<span data-ttu-id="4b698-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4b698-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="4b698-213">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4b698-213">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="4b698-214">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="4b698-214">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="4b698-215">versionName</span><span class="sxs-lookup"><span data-stu-id="4b698-215">versionName</span></span>|<span data-ttu-id="4b698-216">String</span><span class="sxs-lookup"><span data-stu-id="4b698-216">String</span></span>|<span data-ttu-id="4b698-217">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="4b698-217">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="4b698-218">versionCode</span><span class="sxs-lookup"><span data-stu-id="4b698-218">versionCode</span></span>|<span data-ttu-id="4b698-219">String</span><span class="sxs-lookup"><span data-stu-id="4b698-219">String</span></span>|<span data-ttu-id="4b698-220">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="4b698-220">The version code of managed Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="4b698-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b698-221">Response</span></span>
<span data-ttu-id="4b698-222">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b698-222">If successful, this method returns a `200 OK` response code and an updated [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4b698-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b698-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="4b698-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4b698-224">Request</span></span>
<span data-ttu-id="4b698-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b698-225">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="4b698-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b698-226">Response</span></span>
<span data-ttu-id="4b698-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4b698-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



