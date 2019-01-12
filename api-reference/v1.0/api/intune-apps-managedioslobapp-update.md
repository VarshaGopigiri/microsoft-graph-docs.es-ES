---
title: Actualizar managedIOSLobApp
description: Actualice las propiedades de un objeto managedIOSLobApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 209c9be20b3fd1b6a3c96161e4f36b49215d28b8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971441"
---
# <a name="update-managedioslobapp"></a><span data-ttu-id="d2f58-103">Actualizar managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="d2f58-103">Update managedIOSLobApp</span></span>

> <span data-ttu-id="d2f58-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2f58-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2f58-105">Actualice las propiedades de un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-105">Update the properties of a [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2f58-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2f58-106">Prerequisites</span></span>
<span data-ttu-id="d2f58-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2f58-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2f58-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2f58-109">Permission type</span></span>|<span data-ttu-id="d2f58-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2f58-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2f58-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2f58-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d2f58-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2f58-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d2f58-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2f58-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2f58-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2f58-114">Not supported.</span></span>|
|<span data-ttu-id="d2f58-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2f58-115">Application</span></span>|<span data-ttu-id="d2f58-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2f58-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2f58-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2f58-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="d2f58-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2f58-118">Request headers</span></span>
|<span data-ttu-id="d2f58-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2f58-119">Header</span></span>|<span data-ttu-id="d2f58-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d2f58-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2f58-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2f58-121">Authorization</span></span>|<span data-ttu-id="d2f58-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2f58-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2f58-123">Accept</span><span class="sxs-lookup"><span data-stu-id="d2f58-123">Accept</span></span>|<span data-ttu-id="d2f58-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d2f58-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2f58-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2f58-125">Request body</span></span>
<span data-ttu-id="d2f58-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-126">In the request body, supply a JSON representation for the [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object.</span></span>

<span data-ttu-id="d2f58-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-127">The following table shows the properties that are required when you create the [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md).</span></span>

|<span data-ttu-id="d2f58-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2f58-128">Property</span></span>|<span data-ttu-id="d2f58-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2f58-129">Type</span></span>|<span data-ttu-id="d2f58-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2f58-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2f58-131">id</span><span class="sxs-lookup"><span data-stu-id="d2f58-131">id</span></span>|<span data-ttu-id="d2f58-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-132">String</span></span>|<span data-ttu-id="d2f58-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d2f58-133">Key of the entity.</span></span> <span data-ttu-id="d2f58-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-135">displayName</span><span class="sxs-lookup"><span data-stu-id="d2f58-135">displayName</span></span>|<span data-ttu-id="d2f58-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-136">String</span></span>|<span data-ttu-id="d2f58-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="d2f58-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="d2f58-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-139">descripción</span><span class="sxs-lookup"><span data-stu-id="d2f58-139">description</span></span>|<span data-ttu-id="d2f58-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-140">String</span></span>|<span data-ttu-id="d2f58-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-141">The description of the app.</span></span> <span data-ttu-id="d2f58-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-143">publicador</span><span class="sxs-lookup"><span data-stu-id="d2f58-143">publisher</span></span>|<span data-ttu-id="d2f58-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-144">String</span></span>|<span data-ttu-id="d2f58-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-145">The publisher of the app.</span></span> <span data-ttu-id="d2f58-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="d2f58-147">largeIcon</span></span>|[<span data-ttu-id="d2f58-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="d2f58-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="d2f58-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="d2f58-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="d2f58-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d2f58-151">createdDateTime</span></span>|<span data-ttu-id="d2f58-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2f58-152">DateTimeOffset</span></span>|<span data-ttu-id="d2f58-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-153">The date and time the app was created.</span></span> <span data-ttu-id="d2f58-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d2f58-155">lastModifiedDateTime</span></span>|<span data-ttu-id="d2f58-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2f58-156">DateTimeOffset</span></span>|<span data-ttu-id="d2f58-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-157">The date and time the app was last modified.</span></span> <span data-ttu-id="d2f58-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="d2f58-159">isFeatured</span></span>|<span data-ttu-id="d2f58-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="d2f58-160">Boolean</span></span>|<span data-ttu-id="d2f58-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="d2f58-162">privacyInformationUrl</span></span>|<span data-ttu-id="d2f58-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-163">String</span></span>|<span data-ttu-id="d2f58-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="d2f58-164">The privacy statement Url.</span></span> <span data-ttu-id="d2f58-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="d2f58-166">informationUrl</span></span>|<span data-ttu-id="d2f58-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-167">String</span></span>|<span data-ttu-id="d2f58-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d2f58-168">The more information Url.</span></span> <span data-ttu-id="d2f58-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-170">owner</span><span class="sxs-lookup"><span data-stu-id="d2f58-170">owner</span></span>|<span data-ttu-id="d2f58-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-171">String</span></span>|<span data-ttu-id="d2f58-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-172">The owner of the app.</span></span> <span data-ttu-id="d2f58-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-174">developer</span><span class="sxs-lookup"><span data-stu-id="d2f58-174">developer</span></span>|<span data-ttu-id="d2f58-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-175">String</span></span>|<span data-ttu-id="d2f58-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-176">The developer of the app.</span></span> <span data-ttu-id="d2f58-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-178">notas</span><span class="sxs-lookup"><span data-stu-id="d2f58-178">notes</span></span>|<span data-ttu-id="d2f58-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-179">String</span></span>|<span data-ttu-id="d2f58-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-180">Notes for the app.</span></span> <span data-ttu-id="d2f58-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="d2f58-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="d2f58-182">publishingState</span></span>|[<span data-ttu-id="d2f58-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="d2f58-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="d2f58-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-184">The publishing state for the app.</span></span> <span data-ttu-id="d2f58-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="d2f58-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="d2f58-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="d2f58-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="d2f58-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="d2f58-188">appAvailability</span><span class="sxs-lookup"><span data-stu-id="d2f58-188">appAvailability</span></span>|[<span data-ttu-id="d2f58-189">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="d2f58-189">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="d2f58-190">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-190">The Application's availability.</span></span> <span data-ttu-id="d2f58-191">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-191">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="d2f58-192">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="d2f58-192">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="d2f58-193">versión</span><span class="sxs-lookup"><span data-stu-id="d2f58-193">version</span></span>|<span data-ttu-id="d2f58-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-194">String</span></span>|<span data-ttu-id="d2f58-195">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-195">The Application's version.</span></span> <span data-ttu-id="d2f58-196">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="d2f58-196">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="d2f58-197">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="d2f58-197">committedContentVersion</span></span>|<span data-ttu-id="d2f58-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-198">String</span></span>|<span data-ttu-id="d2f58-199">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="d2f58-199">The internal committed content version.</span></span> <span data-ttu-id="d2f58-200">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-200">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="d2f58-201">fileName</span><span class="sxs-lookup"><span data-stu-id="d2f58-201">fileName</span></span>|<span data-ttu-id="d2f58-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-202">String</span></span>|<span data-ttu-id="d2f58-203">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="d2f58-203">The name of the main Lob application file.</span></span> <span data-ttu-id="d2f58-204">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-204">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="d2f58-205">size</span><span class="sxs-lookup"><span data-stu-id="d2f58-205">size</span></span>|<span data-ttu-id="d2f58-206">Int64</span><span class="sxs-lookup"><span data-stu-id="d2f58-206">Int64</span></span>|<span data-ttu-id="d2f58-207">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="d2f58-207">The total size, including all uploaded files.</span></span> <span data-ttu-id="d2f58-208">Heredado de [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d2f58-208">Inherited from [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="d2f58-209">bundleId</span><span class="sxs-lookup"><span data-stu-id="d2f58-209">bundleId</span></span>|<span data-ttu-id="d2f58-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-210">String</span></span>|<span data-ttu-id="d2f58-211">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="d2f58-211">The Identity Name.</span></span>|
|<span data-ttu-id="d2f58-212">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="d2f58-212">applicableDeviceType</span></span>|[<span data-ttu-id="d2f58-213">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="d2f58-213">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="d2f58-214">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2f58-214">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="d2f58-215">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d2f58-215">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="d2f58-216">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d2f58-216">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="d2f58-217">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="d2f58-217">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="d2f58-218">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d2f58-218">expirationDateTime</span></span>|<span data-ttu-id="d2f58-219">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2f58-219">DateTimeOffset</span></span>|<span data-ttu-id="d2f58-220">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="d2f58-220">The expiration time.</span></span>|
|<span data-ttu-id="d2f58-221">versionNumber</span><span class="sxs-lookup"><span data-stu-id="d2f58-221">versionNumber</span></span>|<span data-ttu-id="d2f58-222">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-222">String</span></span>|<span data-ttu-id="d2f58-223">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="d2f58-223">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="d2f58-224">buildNumber</span><span class="sxs-lookup"><span data-stu-id="d2f58-224">buildNumber</span></span>|<span data-ttu-id="d2f58-225">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2f58-225">String</span></span>|<span data-ttu-id="d2f58-226">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="d2f58-226">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="d2f58-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2f58-227">Response</span></span>
<span data-ttu-id="d2f58-228">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2f58-228">If successful, this method returns a `200 OK` response code and an updated [managedIOSLobApp](../resources/intune-apps-managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2f58-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2f58-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2f58-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2f58-230">Request</span></span>
<span data-ttu-id="d2f58-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2f58-231">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
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

### <a name="response"></a><span data-ttu-id="d2f58-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2f58-232">Response</span></span>
<span data-ttu-id="d2f58-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2f58-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



