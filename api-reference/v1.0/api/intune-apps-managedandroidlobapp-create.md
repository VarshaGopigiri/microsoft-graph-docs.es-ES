---
title: Crear managedAndroidLobApp
description: Cree un objeto managedAndroidLobApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7200015c9937d604da5dfd39c74a0a556c172cbf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922756"
---
# <a name="create-managedandroidlobapp"></a><span data-ttu-id="d2bd0-103">Crear managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="d2bd0-103">Create managedAndroidLobApp</span></span>

> <span data-ttu-id="d2bd0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2bd0-105">Cree un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-105">Create a new [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2bd0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2bd0-106">Prerequisites</span></span>
<span data-ttu-id="d2bd0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2bd0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2bd0-109">Permission type</span></span>|<span data-ttu-id="d2bd0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2bd0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2bd0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2bd0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d2bd0-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2bd0-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d2bd0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2bd0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2bd0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-114">Not supported.</span></span>|
|<span data-ttu-id="d2bd0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2bd0-115">Application</span></span>|<span data-ttu-id="d2bd0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2bd0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2bd0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="d2bd0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2bd0-118">Request headers</span></span>
|<span data-ttu-id="d2bd0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2bd0-119">Header</span></span>|<span data-ttu-id="d2bd0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d2bd0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2bd0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2bd0-121">Authorization</span></span>|<span data-ttu-id="d2bd0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2bd0-123">Accept</span><span class="sxs-lookup"><span data-stu-id="d2bd0-123">Accept</span></span>|<span data-ttu-id="d2bd0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d2bd0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2bd0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2bd0-125">Request body</span></span>
<span data-ttu-id="d2bd0-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAndroidLobApp.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-126">In the request body, supply a JSON representation for the managedAndroidLobApp object.</span></span>

<span data-ttu-id="d2bd0-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAndroidLobApp.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-127">The following table shows the properties that are required when you create the managedAndroidLobApp.</span></span>

|<span data-ttu-id="d2bd0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2bd0-128">Property</span></span>|<span data-ttu-id="d2bd0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2bd0-129">Type</span></span>|<span data-ttu-id="d2bd0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2bd0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2bd0-131">id</span><span class="sxs-lookup"><span data-stu-id="d2bd0-131">id</span></span>|<span data-ttu-id="d2bd0-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-132">String</span></span>|<span data-ttu-id="d2bd0-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-133">Key of the entity.</span></span> <span data-ttu-id="d2bd0-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-135">displayName</span><span class="sxs-lookup"><span data-stu-id="d2bd0-135">displayName</span></span>|<span data-ttu-id="d2bd0-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-136">String</span></span>|<span data-ttu-id="d2bd0-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="d2bd0-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-139">descripción</span><span class="sxs-lookup"><span data-stu-id="d2bd0-139">description</span></span>|<span data-ttu-id="d2bd0-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-140">String</span></span>|<span data-ttu-id="d2bd0-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-141">The description of the app.</span></span> <span data-ttu-id="d2bd0-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-143">publicador</span><span class="sxs-lookup"><span data-stu-id="d2bd0-143">publisher</span></span>|<span data-ttu-id="d2bd0-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-144">String</span></span>|<span data-ttu-id="d2bd0-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-145">The publisher of the app.</span></span> <span data-ttu-id="d2bd0-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="d2bd0-147">largeIcon</span></span>|[<span data-ttu-id="d2bd0-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="d2bd0-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="d2bd0-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="d2bd0-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d2bd0-151">createdDateTime</span></span>|<span data-ttu-id="d2bd0-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2bd0-152">DateTimeOffset</span></span>|<span data-ttu-id="d2bd0-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-153">The date and time the app was created.</span></span> <span data-ttu-id="d2bd0-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d2bd0-155">lastModifiedDateTime</span></span>|<span data-ttu-id="d2bd0-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2bd0-156">DateTimeOffset</span></span>|<span data-ttu-id="d2bd0-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-157">The date and time the app was last modified.</span></span> <span data-ttu-id="d2bd0-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="d2bd0-159">isFeatured</span></span>|<span data-ttu-id="d2bd0-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="d2bd0-160">Boolean</span></span>|<span data-ttu-id="d2bd0-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="d2bd0-162">privacyInformationUrl</span></span>|<span data-ttu-id="d2bd0-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-163">String</span></span>|<span data-ttu-id="d2bd0-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-164">The privacy statement Url.</span></span> <span data-ttu-id="d2bd0-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="d2bd0-166">informationUrl</span></span>|<span data-ttu-id="d2bd0-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-167">String</span></span>|<span data-ttu-id="d2bd0-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-168">The more information Url.</span></span> <span data-ttu-id="d2bd0-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-170">owner</span><span class="sxs-lookup"><span data-stu-id="d2bd0-170">owner</span></span>|<span data-ttu-id="d2bd0-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-171">String</span></span>|<span data-ttu-id="d2bd0-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-172">The owner of the app.</span></span> <span data-ttu-id="d2bd0-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-174">developer</span><span class="sxs-lookup"><span data-stu-id="d2bd0-174">developer</span></span>|<span data-ttu-id="d2bd0-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-175">String</span></span>|<span data-ttu-id="d2bd0-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-176">The developer of the app.</span></span> <span data-ttu-id="d2bd0-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-178">notas</span><span class="sxs-lookup"><span data-stu-id="d2bd0-178">notes</span></span>|<span data-ttu-id="d2bd0-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-179">String</span></span>|<span data-ttu-id="d2bd0-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-180">Notes for the app.</span></span> <span data-ttu-id="d2bd0-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2bd0-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="d2bd0-182">publishingState</span></span>|[<span data-ttu-id="d2bd0-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="d2bd0-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="d2bd0-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-184">The publishing state for the app.</span></span> <span data-ttu-id="d2bd0-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="d2bd0-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="d2bd0-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="d2bd0-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="d2bd0-188">appAvailability</span></span>|[<span data-ttu-id="d2bd0-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="d2bd0-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="d2bd0-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-190">The Application's availability.</span></span> <span data-ttu-id="d2bd0-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="d2bd0-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="d2bd0-193">versión</span><span class="sxs-lookup"><span data-stu-id="d2bd0-193">version</span></span>|<span data-ttu-id="d2bd0-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-194">String</span></span>|<span data-ttu-id="d2bd0-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-195">The Application's version.</span></span> <span data-ttu-id="d2bd0-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="d2bd0-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="d2bd0-197">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="d2bd0-197">committedContentVersion</span></span>|<span data-ttu-id="d2bd0-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-198">String</span></span>|<span data-ttu-id="d2bd0-199">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-199">The internal committed content version.</span></span> <span data-ttu-id="d2bd0-200">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-200">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="d2bd0-201">fileName</span><span class="sxs-lookup"><span data-stu-id="d2bd0-201">fileName</span></span>|<span data-ttu-id="d2bd0-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-202">String</span></span>|<span data-ttu-id="d2bd0-203">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-203">The name of the main Lob application file.</span></span> <span data-ttu-id="d2bd0-204">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-204">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="d2bd0-205">size</span><span class="sxs-lookup"><span data-stu-id="d2bd0-205">size</span></span>|<span data-ttu-id="d2bd0-206">Int64</span><span class="sxs-lookup"><span data-stu-id="d2bd0-206">Int64</span></span>|<span data-ttu-id="d2bd0-207">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-207">The total size, including all uploaded files.</span></span> <span data-ttu-id="d2bd0-208">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2bd0-208">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="d2bd0-209">packageId</span><span class="sxs-lookup"><span data-stu-id="d2bd0-209">packageId</span></span>|<span data-ttu-id="d2bd0-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-210">String</span></span>|<span data-ttu-id="d2bd0-211">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-211">The package identifier.</span></span>|
|<span data-ttu-id="d2bd0-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d2bd0-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="d2bd0-213">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d2bd0-213">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="d2bd0-214">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-214">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="d2bd0-215">versionName</span><span class="sxs-lookup"><span data-stu-id="d2bd0-215">versionName</span></span>|<span data-ttu-id="d2bd0-216">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-216">String</span></span>|<span data-ttu-id="d2bd0-217">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-217">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="d2bd0-218">versionCode</span><span class="sxs-lookup"><span data-stu-id="d2bd0-218">versionCode</span></span>|<span data-ttu-id="d2bd0-219">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2bd0-219">String</span></span>|<span data-ttu-id="d2bd0-220">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-220">The version code of managed Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="d2bd0-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2bd0-221">Response</span></span>
<span data-ttu-id="d2bd0-222">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-222">If successful, this method returns a `201 Created` response code and a [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2bd0-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2bd0-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2bd0-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2bd0-224">Request</span></span>
<span data-ttu-id="d2bd0-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-225">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
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

### <a name="response"></a><span data-ttu-id="d2bd0-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2bd0-226">Response</span></span>
<span data-ttu-id="d2bd0-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2bd0-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



