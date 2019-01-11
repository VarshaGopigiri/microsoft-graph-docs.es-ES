---
title: Actualizar managedIOSLobApp
description: Actualice las propiedades de un objeto managedIOSLobApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 353c4827070dd84112f8c646092b4e434394b3e9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825392"
---
# <a name="update-managedioslobapp"></a><span data-ttu-id="69d06-103">Actualizar managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="69d06-103">Update managedIOSLobApp</span></span>

> <span data-ttu-id="69d06-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="69d06-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="69d06-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="69d06-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="69d06-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="69d06-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="69d06-107">Actualice las propiedades de un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-107">Update the properties of a [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="69d06-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="69d06-108">Prerequisites</span></span>
<span data-ttu-id="69d06-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69d06-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69d06-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69d06-111">Permission type</span></span>|<span data-ttu-id="69d06-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69d06-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="69d06-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69d06-113">Delegated (work or school account)</span></span>|<span data-ttu-id="69d06-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69d06-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="69d06-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69d06-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="69d06-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69d06-116">Not supported.</span></span>|
|<span data-ttu-id="69d06-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69d06-117">Application</span></span>|<span data-ttu-id="69d06-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69d06-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="69d06-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69d06-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="69d06-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69d06-120">Request headers</span></span>
|<span data-ttu-id="69d06-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69d06-121">Header</span></span>|<span data-ttu-id="69d06-122">Valor</span><span class="sxs-lookup"><span data-stu-id="69d06-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="69d06-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="69d06-123">Authorization</span></span>|<span data-ttu-id="69d06-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="69d06-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="69d06-125">Accept</span><span class="sxs-lookup"><span data-stu-id="69d06-125">Accept</span></span>|<span data-ttu-id="69d06-126">application/json</span><span class="sxs-lookup"><span data-stu-id="69d06-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="69d06-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69d06-127">Request body</span></span>
<span data-ttu-id="69d06-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-128">In the request body, supply a JSON representation for the [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object.</span></span>

<span data-ttu-id="69d06-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-129">The following table shows the properties that are required when you create the [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span></span>

|<span data-ttu-id="69d06-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69d06-130">Property</span></span>|<span data-ttu-id="69d06-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="69d06-131">Type</span></span>|<span data-ttu-id="69d06-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="69d06-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="69d06-133">id</span><span class="sxs-lookup"><span data-stu-id="69d06-133">id</span></span>|<span data-ttu-id="69d06-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-134">String</span></span>|<span data-ttu-id="69d06-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="69d06-135">Key of the entity.</span></span> <span data-ttu-id="69d06-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-137">displayName</span><span class="sxs-lookup"><span data-stu-id="69d06-137">displayName</span></span>|<span data-ttu-id="69d06-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-138">String</span></span>|<span data-ttu-id="69d06-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="69d06-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="69d06-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-141">descripción</span><span class="sxs-lookup"><span data-stu-id="69d06-141">description</span></span>|<span data-ttu-id="69d06-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-142">String</span></span>|<span data-ttu-id="69d06-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-143">The description of the app.</span></span> <span data-ttu-id="69d06-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-145">publicador</span><span class="sxs-lookup"><span data-stu-id="69d06-145">publisher</span></span>|<span data-ttu-id="69d06-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-146">String</span></span>|<span data-ttu-id="69d06-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-147">The publisher of the app.</span></span> <span data-ttu-id="69d06-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="69d06-149">largeIcon</span></span>|[<span data-ttu-id="69d06-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="69d06-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="69d06-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="69d06-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="69d06-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="69d06-153">createdDateTime</span></span>|<span data-ttu-id="69d06-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69d06-154">DateTimeOffset</span></span>|<span data-ttu-id="69d06-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-155">The date and time the app was created.</span></span> <span data-ttu-id="69d06-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="69d06-157">lastModifiedDateTime</span></span>|<span data-ttu-id="69d06-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69d06-158">DateTimeOffset</span></span>|<span data-ttu-id="69d06-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-159">The date and time the app was last modified.</span></span> <span data-ttu-id="69d06-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="69d06-161">isFeatured</span></span>|<span data-ttu-id="69d06-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="69d06-162">Boolean</span></span>|<span data-ttu-id="69d06-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="69d06-164">privacyInformationUrl</span></span>|<span data-ttu-id="69d06-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-165">String</span></span>|<span data-ttu-id="69d06-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="69d06-166">The privacy statement Url.</span></span> <span data-ttu-id="69d06-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="69d06-168">informationUrl</span></span>|<span data-ttu-id="69d06-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-169">String</span></span>|<span data-ttu-id="69d06-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="69d06-170">The more information Url.</span></span> <span data-ttu-id="69d06-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-172">owner</span><span class="sxs-lookup"><span data-stu-id="69d06-172">owner</span></span>|<span data-ttu-id="69d06-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-173">String</span></span>|<span data-ttu-id="69d06-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-174">The owner of the app.</span></span> <span data-ttu-id="69d06-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-176">developer</span><span class="sxs-lookup"><span data-stu-id="69d06-176">developer</span></span>|<span data-ttu-id="69d06-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-177">String</span></span>|<span data-ttu-id="69d06-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-178">The developer of the app.</span></span> <span data-ttu-id="69d06-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-180">notas</span><span class="sxs-lookup"><span data-stu-id="69d06-180">notes</span></span>|<span data-ttu-id="69d06-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-181">String</span></span>|<span data-ttu-id="69d06-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-182">Notes for the app.</span></span> <span data-ttu-id="69d06-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="69d06-184">uploadState</span></span>|<span data-ttu-id="69d06-185">Int32</span><span class="sxs-lookup"><span data-stu-id="69d06-185">Int32</span></span>|<span data-ttu-id="69d06-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="69d06-186">The upload state.</span></span> <span data-ttu-id="69d06-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69d06-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="69d06-188">publishingState</span></span>|[<span data-ttu-id="69d06-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="69d06-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="69d06-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-190">The publishing state for the app.</span></span> <span data-ttu-id="69d06-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="69d06-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="69d06-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="69d06-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="69d06-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="69d06-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="69d06-194">appAvailability</span></span>|[<span data-ttu-id="69d06-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="69d06-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="69d06-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-196">The Application's availability.</span></span> <span data-ttu-id="69d06-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="69d06-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="69d06-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="69d06-199">versión</span><span class="sxs-lookup"><span data-stu-id="69d06-199">version</span></span>|<span data-ttu-id="69d06-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-200">String</span></span>|<span data-ttu-id="69d06-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-201">The Application's version.</span></span> <span data-ttu-id="69d06-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="69d06-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="69d06-203">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="69d06-203">committedContentVersion</span></span>|<span data-ttu-id="69d06-204">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-204">String</span></span>|<span data-ttu-id="69d06-205">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="69d06-205">The internal committed content version.</span></span> <span data-ttu-id="69d06-206">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-206">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="69d06-207">fileName</span><span class="sxs-lookup"><span data-stu-id="69d06-207">fileName</span></span>|<span data-ttu-id="69d06-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-208">String</span></span>|<span data-ttu-id="69d06-209">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="69d06-209">The name of the main Lob application file.</span></span> <span data-ttu-id="69d06-210">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-210">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="69d06-211">size</span><span class="sxs-lookup"><span data-stu-id="69d06-211">size</span></span>|<span data-ttu-id="69d06-212">Int64</span><span class="sxs-lookup"><span data-stu-id="69d06-212">Int64</span></span>|<span data-ttu-id="69d06-213">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="69d06-213">The total size, including all uploaded files.</span></span> <span data-ttu-id="69d06-214">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="69d06-214">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="69d06-215">bundleId</span><span class="sxs-lookup"><span data-stu-id="69d06-215">bundleId</span></span>|<span data-ttu-id="69d06-216">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-216">String</span></span>|<span data-ttu-id="69d06-217">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="69d06-217">The Identity Name.</span></span>|
|<span data-ttu-id="69d06-218">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="69d06-218">applicableDeviceType</span></span>|[<span data-ttu-id="69d06-219">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="69d06-219">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="69d06-220">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d06-220">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="69d06-221">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="69d06-221">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="69d06-222">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="69d06-222">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="69d06-223">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="69d06-223">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="69d06-224">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="69d06-224">expirationDateTime</span></span>|<span data-ttu-id="69d06-225">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69d06-225">DateTimeOffset</span></span>|<span data-ttu-id="69d06-226">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="69d06-226">The expiration time.</span></span>|
|<span data-ttu-id="69d06-227">versionNumber</span><span class="sxs-lookup"><span data-stu-id="69d06-227">versionNumber</span></span>|<span data-ttu-id="69d06-228">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-228">String</span></span>|<span data-ttu-id="69d06-229">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="69d06-229">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="69d06-230">buildNumber</span><span class="sxs-lookup"><span data-stu-id="69d06-230">buildNumber</span></span>|<span data-ttu-id="69d06-231">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-231">String</span></span>|<span data-ttu-id="69d06-232">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="69d06-232">The build number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="69d06-233">identityVersion</span><span class="sxs-lookup"><span data-stu-id="69d06-233">identityVersion</span></span>|<span data-ttu-id="69d06-234">Cadena</span><span class="sxs-lookup"><span data-stu-id="69d06-234">String</span></span>|<span data-ttu-id="69d06-235">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="69d06-235">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="69d06-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69d06-236">Response</span></span>
<span data-ttu-id="69d06-237">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69d06-237">If successful, this method returns a `200 OK` response code and an updated [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69d06-238">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69d06-238">Example</span></span>
### <a name="request"></a><span data-ttu-id="69d06-239">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69d06-239">Request</span></span>
<span data-ttu-id="69d06-240">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69d06-240">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1366

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

### <a name="response"></a><span data-ttu-id="69d06-241">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69d06-241">Response</span></span>
<span data-ttu-id="69d06-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69d06-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





