---
title: Actualizar win32LobApp
description: Actualizar las propiedades de un objeto win32LobApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c2deac829d1aad6cf0b1a1f3ec4a2a91e7b07c6c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864935"
---
# <a name="update-win32lobapp"></a><span data-ttu-id="2ab69-103">Actualizar win32LobApp</span><span class="sxs-lookup"><span data-stu-id="2ab69-103">Update win32LobApp</span></span>

> <span data-ttu-id="2ab69-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ab69-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ab69-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ab69-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2ab69-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ab69-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ab69-107">Actualizar las propiedades de un objeto [win32LobApp](../resources/intune-apps-win32lobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="2ab69-107">Update the properties of a [win32LobApp](../resources/intune-apps-win32lobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2ab69-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2ab69-108">Prerequisites</span></span>
<span data-ttu-id="2ab69-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ab69-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2ab69-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ab69-111">Permission type</span></span>|<span data-ttu-id="2ab69-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ab69-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2ab69-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ab69-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2ab69-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ab69-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2ab69-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ab69-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2ab69-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ab69-116">Not supported.</span></span>|
|<span data-ttu-id="2ab69-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ab69-117">Application</span></span>|<span data-ttu-id="2ab69-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ab69-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2ab69-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ab69-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="2ab69-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ab69-120">Request headers</span></span>
|<span data-ttu-id="2ab69-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ab69-121">Header</span></span>|<span data-ttu-id="2ab69-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2ab69-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2ab69-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2ab69-123">Authorization</span></span>|<span data-ttu-id="2ab69-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2ab69-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2ab69-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2ab69-125">Accept</span></span>|<span data-ttu-id="2ab69-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2ab69-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2ab69-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ab69-127">Request body</span></span>
<span data-ttu-id="2ab69-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [win32LobApp](../resources/intune-apps-win32lobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="2ab69-128">In the request body, supply a JSON representation for the [win32LobApp](../resources/intune-apps-win32lobapp.md) object.</span></span>

<span data-ttu-id="2ab69-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [win32LobApp](../resources/intune-apps-win32lobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-129">The following table shows the properties that are required when you create the [win32LobApp](../resources/intune-apps-win32lobapp.md).</span></span>

|<span data-ttu-id="2ab69-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ab69-130">Property</span></span>|<span data-ttu-id="2ab69-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ab69-131">Type</span></span>|<span data-ttu-id="2ab69-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ab69-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ab69-133">id</span><span class="sxs-lookup"><span data-stu-id="2ab69-133">id</span></span>|<span data-ttu-id="2ab69-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-134">String</span></span>|<span data-ttu-id="2ab69-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2ab69-135">Key of the entity.</span></span> <span data-ttu-id="2ab69-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-137">displayName</span><span class="sxs-lookup"><span data-stu-id="2ab69-137">displayName</span></span>|<span data-ttu-id="2ab69-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-138">String</span></span>|<span data-ttu-id="2ab69-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="2ab69-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="2ab69-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-141">descripción</span><span class="sxs-lookup"><span data-stu-id="2ab69-141">description</span></span>|<span data-ttu-id="2ab69-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-142">String</span></span>|<span data-ttu-id="2ab69-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-143">The description of the app.</span></span> <span data-ttu-id="2ab69-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-145">publicador</span><span class="sxs-lookup"><span data-stu-id="2ab69-145">publisher</span></span>|<span data-ttu-id="2ab69-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-146">String</span></span>|<span data-ttu-id="2ab69-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-147">The publisher of the app.</span></span> <span data-ttu-id="2ab69-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="2ab69-149">largeIcon</span></span>|[<span data-ttu-id="2ab69-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="2ab69-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="2ab69-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="2ab69-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="2ab69-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2ab69-153">createdDateTime</span></span>|<span data-ttu-id="2ab69-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2ab69-154">DateTimeOffset</span></span>|<span data-ttu-id="2ab69-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-155">The date and time the app was created.</span></span> <span data-ttu-id="2ab69-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2ab69-157">lastModifiedDateTime</span></span>|<span data-ttu-id="2ab69-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2ab69-158">DateTimeOffset</span></span>|<span data-ttu-id="2ab69-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-159">The date and time the app was last modified.</span></span> <span data-ttu-id="2ab69-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="2ab69-161">isFeatured</span></span>|<span data-ttu-id="2ab69-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="2ab69-162">Boolean</span></span>|<span data-ttu-id="2ab69-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="2ab69-164">privacyInformationUrl</span></span>|<span data-ttu-id="2ab69-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-165">String</span></span>|<span data-ttu-id="2ab69-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="2ab69-166">The privacy statement Url.</span></span> <span data-ttu-id="2ab69-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="2ab69-168">informationUrl</span></span>|<span data-ttu-id="2ab69-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-169">String</span></span>|<span data-ttu-id="2ab69-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2ab69-170">The more information Url.</span></span> <span data-ttu-id="2ab69-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-172">owner</span><span class="sxs-lookup"><span data-stu-id="2ab69-172">owner</span></span>|<span data-ttu-id="2ab69-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-173">String</span></span>|<span data-ttu-id="2ab69-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-174">The owner of the app.</span></span> <span data-ttu-id="2ab69-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-176">developer</span><span class="sxs-lookup"><span data-stu-id="2ab69-176">developer</span></span>|<span data-ttu-id="2ab69-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-177">String</span></span>|<span data-ttu-id="2ab69-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-178">The developer of the app.</span></span> <span data-ttu-id="2ab69-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-180">notas</span><span class="sxs-lookup"><span data-stu-id="2ab69-180">notes</span></span>|<span data-ttu-id="2ab69-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-181">String</span></span>|<span data-ttu-id="2ab69-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-182">Notes for the app.</span></span> <span data-ttu-id="2ab69-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="2ab69-184">uploadState</span></span>|<span data-ttu-id="2ab69-185">Int32</span><span class="sxs-lookup"><span data-stu-id="2ab69-185">Int32</span></span>|<span data-ttu-id="2ab69-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="2ab69-186">The upload state.</span></span> <span data-ttu-id="2ab69-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2ab69-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="2ab69-188">publishingState</span></span>|[<span data-ttu-id="2ab69-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="2ab69-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="2ab69-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-190">The publishing state for the app.</span></span> <span data-ttu-id="2ab69-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="2ab69-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="2ab69-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="2ab69-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="2ab69-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="2ab69-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="2ab69-194">committedContentVersion</span></span>|<span data-ttu-id="2ab69-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-195">String</span></span>|<span data-ttu-id="2ab69-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="2ab69-196">The internal committed content version.</span></span> <span data-ttu-id="2ab69-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2ab69-198">fileName</span><span class="sxs-lookup"><span data-stu-id="2ab69-198">fileName</span></span>|<span data-ttu-id="2ab69-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-199">String</span></span>|<span data-ttu-id="2ab69-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="2ab69-200">The name of the main Lob application file.</span></span> <span data-ttu-id="2ab69-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2ab69-202">size</span><span class="sxs-lookup"><span data-stu-id="2ab69-202">size</span></span>|<span data-ttu-id="2ab69-203">Int64</span><span class="sxs-lookup"><span data-stu-id="2ab69-203">Int64</span></span>|<span data-ttu-id="2ab69-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="2ab69-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="2ab69-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2ab69-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2ab69-206">installCommandLine</span><span class="sxs-lookup"><span data-stu-id="2ab69-206">installCommandLine</span></span>|<span data-ttu-id="2ab69-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-207">String</span></span>|<span data-ttu-id="2ab69-208">La línea de comandos para instalar esta aplicación</span><span class="sxs-lookup"><span data-stu-id="2ab69-208">The command line to install this app</span></span>|
|<span data-ttu-id="2ab69-209">uninstallCommandLine</span><span class="sxs-lookup"><span data-stu-id="2ab69-209">uninstallCommandLine</span></span>|<span data-ttu-id="2ab69-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-210">String</span></span>|<span data-ttu-id="2ab69-211">La línea de comandos para desinstalar esta aplicación</span><span class="sxs-lookup"><span data-stu-id="2ab69-211">The command line to uninstall this app</span></span>|
|<span data-ttu-id="2ab69-212">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="2ab69-212">applicableArchitectures</span></span>|[<span data-ttu-id="2ab69-213">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="2ab69-213">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="2ab69-214">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-214">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="2ab69-215">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="2ab69-215">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="2ab69-216">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2ab69-216">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="2ab69-217">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2ab69-217">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="2ab69-218">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="2ab69-218">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="2ab69-219">minimumFreeDiskSpaceInMB</span><span class="sxs-lookup"><span data-stu-id="2ab69-219">minimumFreeDiskSpaceInMB</span></span>|<span data-ttu-id="2ab69-220">Int32</span><span class="sxs-lookup"><span data-stu-id="2ab69-220">Int32</span></span>|<span data-ttu-id="2ab69-221">El valor para el espacio libre en disco mínimo que se requiere para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-221">The value for the minimum free disk space which is required to install this app.</span></span>|
|<span data-ttu-id="2ab69-222">minimumMemoryInMB</span><span class="sxs-lookup"><span data-stu-id="2ab69-222">minimumMemoryInMB</span></span>|<span data-ttu-id="2ab69-223">Int32</span><span class="sxs-lookup"><span data-stu-id="2ab69-223">Int32</span></span>|<span data-ttu-id="2ab69-224">El valor de la memoria física mínimo que se requiere para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-224">The value for the minimum physical memory which is required to install this app.</span></span>|
|<span data-ttu-id="2ab69-225">minimumNumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="2ab69-225">minimumNumberOfProcessors</span></span>|<span data-ttu-id="2ab69-226">Int32</span><span class="sxs-lookup"><span data-stu-id="2ab69-226">Int32</span></span>|<span data-ttu-id="2ab69-227">El valor para el número mínimo de procesadores que se requiere para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-227">The value for the minimum number of processors which is required to install this app.</span></span>|
|<span data-ttu-id="2ab69-228">minimumCpuSpeedInMHz</span><span class="sxs-lookup"><span data-stu-id="2ab69-228">minimumCpuSpeedInMHz</span></span>|<span data-ttu-id="2ab69-229">Int32</span><span class="sxs-lookup"><span data-stu-id="2ab69-229">Int32</span></span>|<span data-ttu-id="2ab69-230">El valor de la velocidad de CPU mínimo que se requiere para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-230">The value for the minimum CPU speed which is required to install this app.</span></span>|
|<span data-ttu-id="2ab69-231">detectionRules</span><span class="sxs-lookup"><span data-stu-id="2ab69-231">detectionRules</span></span>|<span data-ttu-id="2ab69-232">colección de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="2ab69-232">[win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md) collection</span></span>|<span data-ttu-id="2ab69-233">Las reglas de detección para detectar la aplicación de línea de negocio (LoB) de Win32.</span><span class="sxs-lookup"><span data-stu-id="2ab69-233">The detection rules to detect Win32 Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="2ab69-234">installExperience</span><span class="sxs-lookup"><span data-stu-id="2ab69-234">installExperience</span></span>|[<span data-ttu-id="2ab69-235">win32LobAppInstallExperience</span><span class="sxs-lookup"><span data-stu-id="2ab69-235">win32LobAppInstallExperience</span></span>](../resources/intune-apps-win32lobappinstallexperience.md)|<span data-ttu-id="2ab69-236">La experiencia de instalación para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-236">The install experience for this app.</span></span>|
|<span data-ttu-id="2ab69-237">returnCodes</span><span class="sxs-lookup"><span data-stu-id="2ab69-237">returnCodes</span></span>|<span data-ttu-id="2ab69-238">colección de [win32LobAppReturnCode](../resources/intune-apps-win32lobappreturncode.md)</span><span class="sxs-lookup"><span data-stu-id="2ab69-238">[win32LobAppReturnCode](../resources/intune-apps-win32lobappreturncode.md) collection</span></span>|<span data-ttu-id="2ab69-239">Los códigos de retorno para registrar el comportamiento de la instalación.</span><span class="sxs-lookup"><span data-stu-id="2ab69-239">The return codes for post installation behavior.</span></span>|
|<span data-ttu-id="2ab69-240">msiInformation</span><span class="sxs-lookup"><span data-stu-id="2ab69-240">msiInformation</span></span>|[<span data-ttu-id="2ab69-241">win32LobAppMsiInformation</span><span class="sxs-lookup"><span data-stu-id="2ab69-241">win32LobAppMsiInformation</span></span>](../resources/intune-apps-win32lobappmsiinformation.md)|<span data-ttu-id="2ab69-242">Los detalles MSI si esta aplicación Win32 es una aplicación MSI.</span><span class="sxs-lookup"><span data-stu-id="2ab69-242">The MSI details if this Win32 app is an MSI app.</span></span>|
|<span data-ttu-id="2ab69-243">setupFilePath</span><span class="sxs-lookup"><span data-stu-id="2ab69-243">setupFilePath</span></span>|<span data-ttu-id="2ab69-244">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ab69-244">String</span></span>|<span data-ttu-id="2ab69-245">La ruta de acceso relativa del archivo del programa de instalación en el paquete de Win32LobApp cifrado.</span><span class="sxs-lookup"><span data-stu-id="2ab69-245">The relative path of the setup file in the encrypted Win32LobApp package.</span></span>|



## <a name="response"></a><span data-ttu-id="2ab69-246">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ab69-246">Response</span></span>
<span data-ttu-id="2ab69-247">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [win32LobApp](../resources/intune-apps-win32lobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ab69-247">If successful, this method returns a `200 OK` response code and an updated [win32LobApp](../resources/intune-apps-win32lobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2ab69-248">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ab69-248">Example</span></span>
### <a name="request"></a><span data-ttu-id="2ab69-249">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ab69-249">Request</span></span>
<span data-ttu-id="2ab69-250">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ab69-250">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 2214

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
  "installCommandLine": "Install Command Line value",
  "uninstallCommandLine": "Uninstall Command Line value",
  "applicableArchitectures": "x86",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "minimumFreeDiskSpaceInMB": 8,
  "minimumMemoryInMB": 1,
  "minimumNumberOfProcessors": 9,
  "minimumCpuSpeedInMHz": 4,
  "detectionRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryDetection",
      "check32BitOn64System": true,
      "keyPath": "Key Path value",
      "valueName": "Value Name value",
      "detectionType": "exists",
      "operator": "equal",
      "detectionValue": "Detection Value value"
    }
  ],
  "installExperience": {
    "@odata.type": "microsoft.graph.win32LobAppInstallExperience",
    "runAsAccount": "user"
  },
  "returnCodes": [
    {
      "@odata.type": "microsoft.graph.win32LobAppReturnCode",
      "returnCode": 10,
      "type": "success"
    }
  ],
  "msiInformation": {
    "@odata.type": "microsoft.graph.win32LobAppMsiInformation",
    "productCode": "Product Code value",
    "productVersion": "Product Version value",
    "upgradeCode": "Upgrade Code value",
    "requiresReboot": true,
    "packageType": "perUser"
  },
  "setupFilePath": "Setup File Path value"
}
```

### <a name="response"></a><span data-ttu-id="2ab69-251">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ab69-251">Response</span></span>
<span data-ttu-id="2ab69-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ab69-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2372

{
  "@odata.type": "#microsoft.graph.win32LobApp",
  "id": "9607b530-b530-9607-30b5-079630b50796",
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
  "installCommandLine": "Install Command Line value",
  "uninstallCommandLine": "Uninstall Command Line value",
  "applicableArchitectures": "x86",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "minimumFreeDiskSpaceInMB": 8,
  "minimumMemoryInMB": 1,
  "minimumNumberOfProcessors": 9,
  "minimumCpuSpeedInMHz": 4,
  "detectionRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryDetection",
      "check32BitOn64System": true,
      "keyPath": "Key Path value",
      "valueName": "Value Name value",
      "detectionType": "exists",
      "operator": "equal",
      "detectionValue": "Detection Value value"
    }
  ],
  "installExperience": {
    "@odata.type": "microsoft.graph.win32LobAppInstallExperience",
    "runAsAccount": "user"
  },
  "returnCodes": [
    {
      "@odata.type": "microsoft.graph.win32LobAppReturnCode",
      "returnCode": 10,
      "type": "success"
    }
  ],
  "msiInformation": {
    "@odata.type": "microsoft.graph.win32LobAppMsiInformation",
    "productCode": "Product Code value",
    "productVersion": "Product Version value",
    "upgradeCode": "Upgrade Code value",
    "requiresReboot": true,
    "packageType": "perUser"
  },
  "setupFilePath": "Setup File Path value"
}
```





