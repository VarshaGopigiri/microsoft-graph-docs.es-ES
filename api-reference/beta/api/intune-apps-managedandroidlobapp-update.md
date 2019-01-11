---
title: Actualizar managedAndroidLobApp
description: Actualice las propiedades de un objeto managedAndroidLobApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 48700cdc4c54acd760f775bd8d3beab36b798197
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809183"
---
# <a name="update-managedandroidlobapp"></a><span data-ttu-id="3f8b6-103">Actualizar managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="3f8b6-103">Update managedAndroidLobApp</span></span>

> <span data-ttu-id="3f8b6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f8b6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3f8b6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3f8b6-107">Actualice las propiedades de un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-107">Update the properties of a [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3f8b6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3f8b6-108">Prerequisites</span></span>
<span data-ttu-id="3f8b6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f8b6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f8b6-111">Permission type</span></span>|<span data-ttu-id="3f8b6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f8b6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3f8b6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f8b6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3f8b6-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f8b6-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3f8b6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f8b6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3f8b6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-116">Not supported.</span></span>|
|<span data-ttu-id="3f8b6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f8b6-117">Application</span></span>|<span data-ttu-id="3f8b6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3f8b6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f8b6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="3f8b6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f8b6-120">Request headers</span></span>
|<span data-ttu-id="3f8b6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f8b6-121">Header</span></span>|<span data-ttu-id="3f8b6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3f8b6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3f8b6-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3f8b6-123">Authorization</span></span>|<span data-ttu-id="3f8b6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3f8b6-125">Accept</span><span class="sxs-lookup"><span data-stu-id="3f8b6-125">Accept</span></span>|<span data-ttu-id="3f8b6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3f8b6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f8b6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f8b6-127">Request body</span></span>
<span data-ttu-id="3f8b6-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-128">In the request body, supply a JSON representation for the [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object.</span></span>

<span data-ttu-id="3f8b6-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-129">The following table shows the properties that are required when you create the [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md).</span></span>

|<span data-ttu-id="3f8b6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f8b6-130">Property</span></span>|<span data-ttu-id="3f8b6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f8b6-131">Type</span></span>|<span data-ttu-id="3f8b6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f8b6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3f8b6-133">id</span><span class="sxs-lookup"><span data-stu-id="3f8b6-133">id</span></span>|<span data-ttu-id="3f8b6-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-134">String</span></span>|<span data-ttu-id="3f8b6-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-135">Key of the entity.</span></span> <span data-ttu-id="3f8b6-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-137">displayName</span><span class="sxs-lookup"><span data-stu-id="3f8b6-137">displayName</span></span>|<span data-ttu-id="3f8b6-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-138">String</span></span>|<span data-ttu-id="3f8b6-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="3f8b6-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-141">descripción</span><span class="sxs-lookup"><span data-stu-id="3f8b6-141">description</span></span>|<span data-ttu-id="3f8b6-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-142">String</span></span>|<span data-ttu-id="3f8b6-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-143">The description of the app.</span></span> <span data-ttu-id="3f8b6-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-145">publicador</span><span class="sxs-lookup"><span data-stu-id="3f8b6-145">publisher</span></span>|<span data-ttu-id="3f8b6-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-146">String</span></span>|<span data-ttu-id="3f8b6-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-147">The publisher of the app.</span></span> <span data-ttu-id="3f8b6-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="3f8b6-149">largeIcon</span></span>|[<span data-ttu-id="3f8b6-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="3f8b6-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="3f8b6-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="3f8b6-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3f8b6-153">createdDateTime</span></span>|<span data-ttu-id="3f8b6-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3f8b6-154">DateTimeOffset</span></span>|<span data-ttu-id="3f8b6-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-155">The date and time the app was created.</span></span> <span data-ttu-id="3f8b6-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3f8b6-157">lastModifiedDateTime</span></span>|<span data-ttu-id="3f8b6-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3f8b6-158">DateTimeOffset</span></span>|<span data-ttu-id="3f8b6-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-159">The date and time the app was last modified.</span></span> <span data-ttu-id="3f8b6-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="3f8b6-161">isFeatured</span></span>|<span data-ttu-id="3f8b6-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="3f8b6-162">Boolean</span></span>|<span data-ttu-id="3f8b6-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="3f8b6-164">privacyInformationUrl</span></span>|<span data-ttu-id="3f8b6-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-165">String</span></span>|<span data-ttu-id="3f8b6-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-166">The privacy statement Url.</span></span> <span data-ttu-id="3f8b6-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="3f8b6-168">informationUrl</span></span>|<span data-ttu-id="3f8b6-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-169">String</span></span>|<span data-ttu-id="3f8b6-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-170">The more information Url.</span></span> <span data-ttu-id="3f8b6-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-172">owner</span><span class="sxs-lookup"><span data-stu-id="3f8b6-172">owner</span></span>|<span data-ttu-id="3f8b6-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-173">String</span></span>|<span data-ttu-id="3f8b6-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-174">The owner of the app.</span></span> <span data-ttu-id="3f8b6-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-176">developer</span><span class="sxs-lookup"><span data-stu-id="3f8b6-176">developer</span></span>|<span data-ttu-id="3f8b6-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-177">String</span></span>|<span data-ttu-id="3f8b6-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-178">The developer of the app.</span></span> <span data-ttu-id="3f8b6-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-180">notas</span><span class="sxs-lookup"><span data-stu-id="3f8b6-180">notes</span></span>|<span data-ttu-id="3f8b6-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-181">String</span></span>|<span data-ttu-id="3f8b6-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-182">Notes for the app.</span></span> <span data-ttu-id="3f8b6-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="3f8b6-184">uploadState</span></span>|<span data-ttu-id="3f8b6-185">Int32</span><span class="sxs-lookup"><span data-stu-id="3f8b6-185">Int32</span></span>|<span data-ttu-id="3f8b6-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-186">The upload state.</span></span> <span data-ttu-id="3f8b6-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="3f8b6-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="3f8b6-188">publishingState</span></span>|[<span data-ttu-id="3f8b6-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="3f8b6-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="3f8b6-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-190">The publishing state for the app.</span></span> <span data-ttu-id="3f8b6-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="3f8b6-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="3f8b6-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="3f8b6-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="3f8b6-194">appAvailability</span></span>|[<span data-ttu-id="3f8b6-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="3f8b6-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="3f8b6-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-196">The Application's availability.</span></span> <span data-ttu-id="3f8b6-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="3f8b6-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="3f8b6-199">versión</span><span class="sxs-lookup"><span data-stu-id="3f8b6-199">version</span></span>|<span data-ttu-id="3f8b6-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-200">String</span></span>|<span data-ttu-id="3f8b6-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-201">The Application's version.</span></span> <span data-ttu-id="3f8b6-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="3f8b6-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="3f8b6-203">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="3f8b6-203">committedContentVersion</span></span>|<span data-ttu-id="3f8b6-204">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-204">String</span></span>|<span data-ttu-id="3f8b6-205">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-205">The internal committed content version.</span></span> <span data-ttu-id="3f8b6-206">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-206">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="3f8b6-207">fileName</span><span class="sxs-lookup"><span data-stu-id="3f8b6-207">fileName</span></span>|<span data-ttu-id="3f8b6-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-208">String</span></span>|<span data-ttu-id="3f8b6-209">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-209">The name of the main Lob application file.</span></span> <span data-ttu-id="3f8b6-210">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-210">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="3f8b6-211">size</span><span class="sxs-lookup"><span data-stu-id="3f8b6-211">size</span></span>|<span data-ttu-id="3f8b6-212">Int64</span><span class="sxs-lookup"><span data-stu-id="3f8b6-212">Int64</span></span>|<span data-ttu-id="3f8b6-213">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-213">The total size, including all uploaded files.</span></span> <span data-ttu-id="3f8b6-214">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3f8b6-214">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="3f8b6-215">packageId</span><span class="sxs-lookup"><span data-stu-id="3f8b6-215">packageId</span></span>|<span data-ttu-id="3f8b6-216">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-216">String</span></span>|<span data-ttu-id="3f8b6-217">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-217">The package identifier.</span></span>|
|<span data-ttu-id="3f8b6-218">identityName</span><span class="sxs-lookup"><span data-stu-id="3f8b6-218">identityName</span></span>|<span data-ttu-id="3f8b6-219">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-219">String</span></span>|<span data-ttu-id="3f8b6-220">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-220">The Identity Name.</span></span>|
|<span data-ttu-id="3f8b6-221">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3f8b6-221">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="3f8b6-222">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3f8b6-222">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="3f8b6-223">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-223">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="3f8b6-224">versionName</span><span class="sxs-lookup"><span data-stu-id="3f8b6-224">versionName</span></span>|<span data-ttu-id="3f8b6-225">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-225">String</span></span>|<span data-ttu-id="3f8b6-226">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-226">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="3f8b6-227">versionCode</span><span class="sxs-lookup"><span data-stu-id="3f8b6-227">versionCode</span></span>|<span data-ttu-id="3f8b6-228">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-228">String</span></span>|<span data-ttu-id="3f8b6-229">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-229">The version code of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="3f8b6-230">identityVersion</span><span class="sxs-lookup"><span data-stu-id="3f8b6-230">identityVersion</span></span>|<span data-ttu-id="3f8b6-231">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f8b6-231">String</span></span>|<span data-ttu-id="3f8b6-232">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-232">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="3f8b6-233">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f8b6-233">Response</span></span>
<span data-ttu-id="3f8b6-234">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-234">If successful, this method returns a `200 OK` response code and an updated [managedAndroidLobApp](../resources/intune-apps-managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f8b6-235">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f8b6-235">Example</span></span>
### <a name="request"></a><span data-ttu-id="3f8b6-236">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f8b6-236">Request</span></span>
<span data-ttu-id="3f8b6-237">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-237">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1384

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
  "packageId": "Package Id value",
  "identityName": "Identity Name value",
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
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value",
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="3f8b6-238">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f8b6-238">Response</span></span>
<span data-ttu-id="3f8b6-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1551

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
  "uploadState": 11,
  "publishingState": "processing",
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "packageId": "Package Id value",
  "identityName": "Identity Name value",
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
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value",
  "identityVersion": "Identity Version value"
}
```





