---
title: Actualizar iosLobApp
description: Actualice las propiedades de un objeto iosLobApp.
ms.openlocfilehash: 40289d7d714518ef70824ab78937c3ee09139c73
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088940"
---
# <a name="update-ioslobapp"></a><span data-ttu-id="e9e03-103">Actualizar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="e9e03-103">Update iosLobApp</span></span>

> <span data-ttu-id="e9e03-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9e03-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9e03-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9e03-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e9e03-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9e03-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9e03-107">Actualice las propiedades de un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-107">Update the properties of a [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9e03-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9e03-108">Prerequisites</span></span>
<span data-ttu-id="e9e03-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9e03-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9e03-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9e03-111">Permission type</span></span>|<span data-ttu-id="e9e03-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9e03-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e9e03-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9e03-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e9e03-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9e03-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e9e03-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9e03-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e9e03-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9e03-116">Not supported.</span></span>|
|<span data-ttu-id="e9e03-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9e03-117">Application</span></span>|<span data-ttu-id="e9e03-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9e03-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e9e03-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9e03-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="e9e03-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e03-120">Request headers</span></span>
|<span data-ttu-id="e9e03-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9e03-121">Header</span></span>|<span data-ttu-id="e9e03-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e9e03-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e9e03-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9e03-123">Authorization</span></span>|<span data-ttu-id="e9e03-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e9e03-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e9e03-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9e03-125">Accept</span></span>|<span data-ttu-id="e9e03-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e9e03-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9e03-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e03-127">Request body</span></span>
<span data-ttu-id="e9e03-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-128">In the request body, supply a JSON representation for the [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>

<span data-ttu-id="e9e03-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-129">The following table shows the properties that are required when you create the [iosLobApp](../resources/intune-apps-ioslobapp.md).</span></span>

|<span data-ttu-id="e9e03-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9e03-130">Property</span></span>|<span data-ttu-id="e9e03-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9e03-131">Type</span></span>|<span data-ttu-id="e9e03-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9e03-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9e03-133">id</span><span class="sxs-lookup"><span data-stu-id="e9e03-133">id</span></span>|<span data-ttu-id="e9e03-134">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-134">String</span></span>|<span data-ttu-id="e9e03-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e9e03-135">Key of the entity.</span></span> <span data-ttu-id="e9e03-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-137">displayName</span><span class="sxs-lookup"><span data-stu-id="e9e03-137">displayName</span></span>|<span data-ttu-id="e9e03-138">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-138">String</span></span>|<span data-ttu-id="e9e03-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e9e03-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e9e03-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-141">descripción</span><span class="sxs-lookup"><span data-stu-id="e9e03-141">description</span></span>|<span data-ttu-id="e9e03-142">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-142">String</span></span>|<span data-ttu-id="e9e03-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-143">The description of the app.</span></span> <span data-ttu-id="e9e03-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-145">publicador</span><span class="sxs-lookup"><span data-stu-id="e9e03-145">publisher</span></span>|<span data-ttu-id="e9e03-146">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-146">String</span></span>|<span data-ttu-id="e9e03-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-147">The publisher of the app.</span></span> <span data-ttu-id="e9e03-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e9e03-149">largeIcon</span></span>|[<span data-ttu-id="e9e03-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e9e03-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="e9e03-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e9e03-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e9e03-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e9e03-153">createdDateTime</span></span>|<span data-ttu-id="e9e03-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9e03-154">DateTimeOffset</span></span>|<span data-ttu-id="e9e03-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-155">The date and time the app was created.</span></span> <span data-ttu-id="e9e03-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e9e03-157">lastModifiedDateTime</span></span>|<span data-ttu-id="e9e03-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9e03-158">DateTimeOffset</span></span>|<span data-ttu-id="e9e03-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-159">The date and time the app was last modified.</span></span> <span data-ttu-id="e9e03-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e9e03-161">isFeatured</span></span>|<span data-ttu-id="e9e03-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9e03-162">Boolean</span></span>|<span data-ttu-id="e9e03-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e9e03-164">privacyInformationUrl</span></span>|<span data-ttu-id="e9e03-165">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-165">String</span></span>|<span data-ttu-id="e9e03-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e9e03-166">The privacy statement Url.</span></span> <span data-ttu-id="e9e03-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e9e03-168">informationUrl</span></span>|<span data-ttu-id="e9e03-169">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-169">String</span></span>|<span data-ttu-id="e9e03-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e9e03-170">The more information Url.</span></span> <span data-ttu-id="e9e03-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-172">owner</span><span class="sxs-lookup"><span data-stu-id="e9e03-172">owner</span></span>|<span data-ttu-id="e9e03-173">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-173">String</span></span>|<span data-ttu-id="e9e03-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-174">The owner of the app.</span></span> <span data-ttu-id="e9e03-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-176">developer</span><span class="sxs-lookup"><span data-stu-id="e9e03-176">developer</span></span>|<span data-ttu-id="e9e03-177">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-177">String</span></span>|<span data-ttu-id="e9e03-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-178">The developer of the app.</span></span> <span data-ttu-id="e9e03-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-180">notas</span><span class="sxs-lookup"><span data-stu-id="e9e03-180">notes</span></span>|<span data-ttu-id="e9e03-181">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-181">String</span></span>|<span data-ttu-id="e9e03-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-182">Notes for the app.</span></span> <span data-ttu-id="e9e03-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="e9e03-184">uploadState</span></span>|<span data-ttu-id="e9e03-185">Int32</span><span class="sxs-lookup"><span data-stu-id="e9e03-185">Int32</span></span>|<span data-ttu-id="e9e03-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="e9e03-186">The upload state.</span></span> <span data-ttu-id="e9e03-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9e03-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="e9e03-188">publishingState</span></span>|[<span data-ttu-id="e9e03-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="e9e03-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="e9e03-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-190">The publishing state for the app.</span></span> <span data-ttu-id="e9e03-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e9e03-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e9e03-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="e9e03-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e9e03-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="e9e03-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="e9e03-194">committedContentVersion</span></span>|<span data-ttu-id="e9e03-195">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-195">String</span></span>|<span data-ttu-id="e9e03-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="e9e03-196">The internal committed content version.</span></span> <span data-ttu-id="e9e03-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="e9e03-198">fileName</span><span class="sxs-lookup"><span data-stu-id="e9e03-198">fileName</span></span>|<span data-ttu-id="e9e03-199">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-199">String</span></span>|<span data-ttu-id="e9e03-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="e9e03-200">The name of the main Lob application file.</span></span> <span data-ttu-id="e9e03-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="e9e03-202">size</span><span class="sxs-lookup"><span data-stu-id="e9e03-202">size</span></span>|<span data-ttu-id="e9e03-203">Int64</span><span class="sxs-lookup"><span data-stu-id="e9e03-203">Int64</span></span>|<span data-ttu-id="e9e03-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="e9e03-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="e9e03-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9e03-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="e9e03-206">bundleId</span><span class="sxs-lookup"><span data-stu-id="e9e03-206">bundleId</span></span>|<span data-ttu-id="e9e03-207">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-207">String</span></span>|<span data-ttu-id="e9e03-208">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e9e03-208">The Identity Name.</span></span>|
|<span data-ttu-id="e9e03-209">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="e9e03-209">applicableDeviceType</span></span>|[<span data-ttu-id="e9e03-210">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="e9e03-210">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="e9e03-211">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e03-211">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="e9e03-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9e03-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="e9e03-213">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9e03-213">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="e9e03-214">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="e9e03-214">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="e9e03-215">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e9e03-215">expirationDateTime</span></span>|<span data-ttu-id="e9e03-216">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9e03-216">DateTimeOffset</span></span>|<span data-ttu-id="e9e03-217">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="e9e03-217">The expiration time.</span></span>|
|<span data-ttu-id="e9e03-218">versionNumber</span><span class="sxs-lookup"><span data-stu-id="e9e03-218">versionNumber</span></span>|<span data-ttu-id="e9e03-219">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-219">String</span></span>|<span data-ttu-id="e9e03-220">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="e9e03-220">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="e9e03-221">buildNumber</span><span class="sxs-lookup"><span data-stu-id="e9e03-221">buildNumber</span></span>|<span data-ttu-id="e9e03-222">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-222">String</span></span>|<span data-ttu-id="e9e03-223">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="e9e03-223">The build number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="e9e03-224">identityVersion</span><span class="sxs-lookup"><span data-stu-id="e9e03-224">identityVersion</span></span>|<span data-ttu-id="e9e03-225">String</span><span class="sxs-lookup"><span data-stu-id="e9e03-225">String</span></span>|<span data-ttu-id="e9e03-226">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e9e03-226">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="e9e03-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e03-227">Response</span></span>
<span data-ttu-id="e9e03-228">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e03-228">If successful, this method returns a `200 OK` response code and an updated [iosLobApp](../resources/intune-apps-ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9e03-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9e03-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="e9e03-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e03-230">Request</span></span>
<span data-ttu-id="e9e03-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9e03-231">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1295

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

### <a name="response"></a><span data-ttu-id="e9e03-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e03-232">Response</span></span>
<span data-ttu-id="e9e03-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9e03-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1451

{
  "@odata.type": "#microsoft.graph.iosLobApp",
  "id": "b34052ea-52ea-b340-ea52-40b3ea5240b3",
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




