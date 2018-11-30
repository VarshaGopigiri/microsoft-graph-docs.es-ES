---
title: Crear macOSLobApp
description: Crear un nuevo objeto macOSLobApp.
ms.openlocfilehash: 71f925bd2279365c0d3d73e4f63eca74bde46c86
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088076"
---
# <a name="create-macoslobapp"></a><span data-ttu-id="bb421-103">Crear macOSLobApp</span><span class="sxs-lookup"><span data-stu-id="bb421-103">Create macOSLobApp</span></span>

> <span data-ttu-id="bb421-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb421-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb421-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb421-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bb421-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bb421-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb421-107">Crear un nuevo objeto [macOSLobApp](../resources/intune-apps-macoslobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="bb421-107">Create a new [macOSLobApp](../resources/intune-apps-macoslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb421-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bb421-108">Prerequisites</span></span>
<span data-ttu-id="bb421-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb421-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb421-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb421-111">Permission type</span></span>|<span data-ttu-id="bb421-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb421-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb421-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb421-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bb421-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb421-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bb421-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb421-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb421-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb421-116">Not supported.</span></span>|
|<span data-ttu-id="bb421-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb421-117">Application</span></span>|<span data-ttu-id="bb421-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb421-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb421-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb421-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="bb421-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb421-120">Request headers</span></span>
|<span data-ttu-id="bb421-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb421-121">Header</span></span>|<span data-ttu-id="bb421-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bb421-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb421-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bb421-123">Authorization</span></span>|<span data-ttu-id="bb421-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bb421-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb421-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bb421-125">Accept</span></span>|<span data-ttu-id="bb421-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bb421-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb421-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb421-127">Request body</span></span>
<span data-ttu-id="bb421-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto macOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="bb421-128">In the request body, supply a JSON representation for the macOSLobApp object.</span></span>

<span data-ttu-id="bb421-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el macOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="bb421-129">The following table shows the properties that are required when you create the macOSLobApp.</span></span>

|<span data-ttu-id="bb421-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb421-130">Property</span></span>|<span data-ttu-id="bb421-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb421-131">Type</span></span>|<span data-ttu-id="bb421-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb421-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bb421-133">id</span><span class="sxs-lookup"><span data-stu-id="bb421-133">id</span></span>|<span data-ttu-id="bb421-134">String</span><span class="sxs-lookup"><span data-stu-id="bb421-134">String</span></span>|<span data-ttu-id="bb421-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bb421-135">Key of the entity.</span></span> <span data-ttu-id="bb421-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-137">displayName</span><span class="sxs-lookup"><span data-stu-id="bb421-137">displayName</span></span>|<span data-ttu-id="bb421-138">String</span><span class="sxs-lookup"><span data-stu-id="bb421-138">String</span></span>|<span data-ttu-id="bb421-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="bb421-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="bb421-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-141">descripción</span><span class="sxs-lookup"><span data-stu-id="bb421-141">description</span></span>|<span data-ttu-id="bb421-142">String</span><span class="sxs-lookup"><span data-stu-id="bb421-142">String</span></span>|<span data-ttu-id="bb421-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-143">The description of the app.</span></span> <span data-ttu-id="bb421-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-145">publicador</span><span class="sxs-lookup"><span data-stu-id="bb421-145">publisher</span></span>|<span data-ttu-id="bb421-146">String</span><span class="sxs-lookup"><span data-stu-id="bb421-146">String</span></span>|<span data-ttu-id="bb421-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-147">The publisher of the app.</span></span> <span data-ttu-id="bb421-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="bb421-149">largeIcon</span></span>|[<span data-ttu-id="bb421-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="bb421-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="bb421-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="bb421-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="bb421-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bb421-153">createdDateTime</span></span>|<span data-ttu-id="bb421-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb421-154">DateTimeOffset</span></span>|<span data-ttu-id="bb421-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-155">The date and time the app was created.</span></span> <span data-ttu-id="bb421-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bb421-157">lastModifiedDateTime</span></span>|<span data-ttu-id="bb421-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb421-158">DateTimeOffset</span></span>|<span data-ttu-id="bb421-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-159">The date and time the app was last modified.</span></span> <span data-ttu-id="bb421-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="bb421-161">isFeatured</span></span>|<span data-ttu-id="bb421-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="bb421-162">Boolean</span></span>|<span data-ttu-id="bb421-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="bb421-164">privacyInformationUrl</span></span>|<span data-ttu-id="bb421-165">String</span><span class="sxs-lookup"><span data-stu-id="bb421-165">String</span></span>|<span data-ttu-id="bb421-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="bb421-166">The privacy statement Url.</span></span> <span data-ttu-id="bb421-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="bb421-168">informationUrl</span></span>|<span data-ttu-id="bb421-169">String</span><span class="sxs-lookup"><span data-stu-id="bb421-169">String</span></span>|<span data-ttu-id="bb421-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="bb421-170">The more information Url.</span></span> <span data-ttu-id="bb421-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-172">owner</span><span class="sxs-lookup"><span data-stu-id="bb421-172">owner</span></span>|<span data-ttu-id="bb421-173">String</span><span class="sxs-lookup"><span data-stu-id="bb421-173">String</span></span>|<span data-ttu-id="bb421-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-174">The owner of the app.</span></span> <span data-ttu-id="bb421-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-176">developer</span><span class="sxs-lookup"><span data-stu-id="bb421-176">developer</span></span>|<span data-ttu-id="bb421-177">String</span><span class="sxs-lookup"><span data-stu-id="bb421-177">String</span></span>|<span data-ttu-id="bb421-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-178">The developer of the app.</span></span> <span data-ttu-id="bb421-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-180">notas</span><span class="sxs-lookup"><span data-stu-id="bb421-180">notes</span></span>|<span data-ttu-id="bb421-181">String</span><span class="sxs-lookup"><span data-stu-id="bb421-181">String</span></span>|<span data-ttu-id="bb421-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-182">Notes for the app.</span></span> <span data-ttu-id="bb421-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="bb421-184">uploadState</span></span>|<span data-ttu-id="bb421-185">Int32</span><span class="sxs-lookup"><span data-stu-id="bb421-185">Int32</span></span>|<span data-ttu-id="bb421-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="bb421-186">The upload state.</span></span> <span data-ttu-id="bb421-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="bb421-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="bb421-188">publishingState</span></span>|[<span data-ttu-id="bb421-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="bb421-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="bb421-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb421-190">The publishing state for the app.</span></span> <span data-ttu-id="bb421-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="bb421-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="bb421-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="bb421-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="bb421-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="bb421-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="bb421-194">committedContentVersion</span></span>|<span data-ttu-id="bb421-195">String</span><span class="sxs-lookup"><span data-stu-id="bb421-195">String</span></span>|<span data-ttu-id="bb421-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="bb421-196">The internal committed content version.</span></span> <span data-ttu-id="bb421-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="bb421-198">fileName</span><span class="sxs-lookup"><span data-stu-id="bb421-198">fileName</span></span>|<span data-ttu-id="bb421-199">String</span><span class="sxs-lookup"><span data-stu-id="bb421-199">String</span></span>|<span data-ttu-id="bb421-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="bb421-200">The name of the main Lob application file.</span></span> <span data-ttu-id="bb421-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="bb421-202">size</span><span class="sxs-lookup"><span data-stu-id="bb421-202">size</span></span>|<span data-ttu-id="bb421-203">Int64</span><span class="sxs-lookup"><span data-stu-id="bb421-203">Int64</span></span>|<span data-ttu-id="bb421-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="bb421-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="bb421-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="bb421-206">bundleId</span><span class="sxs-lookup"><span data-stu-id="bb421-206">bundleId</span></span>|<span data-ttu-id="bb421-207">String</span><span class="sxs-lookup"><span data-stu-id="bb421-207">String</span></span>|<span data-ttu-id="bb421-208">El identificador de paquete.</span><span class="sxs-lookup"><span data-stu-id="bb421-208">The bundle id.</span></span>|
|<span data-ttu-id="bb421-209">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bb421-209">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="bb421-210">macOSMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bb421-210">macOSMinimumOperatingSystem</span></span>](../resources/intune-apps-macosminimumoperatingsystem.md)|<span data-ttu-id="bb421-211">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="bb421-211">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="bb421-212">buildNumber</span><span class="sxs-lookup"><span data-stu-id="bb421-212">buildNumber</span></span>|<span data-ttu-id="bb421-213">String</span><span class="sxs-lookup"><span data-stu-id="bb421-213">String</span></span>|<span data-ttu-id="bb421-214">El número de compilación de línea de Mac OS de aplicación de negocio (LoB).</span><span class="sxs-lookup"><span data-stu-id="bb421-214">The build number of MacOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="bb421-215">versionNumber</span><span class="sxs-lookup"><span data-stu-id="bb421-215">versionNumber</span></span>|<span data-ttu-id="bb421-216">String</span><span class="sxs-lookup"><span data-stu-id="bb421-216">String</span></span>|<span data-ttu-id="bb421-217">El número de versión de línea de Mac OS de aplicación de negocio (LoB).</span><span class="sxs-lookup"><span data-stu-id="bb421-217">The version number of MacOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="bb421-218">childApps</span><span class="sxs-lookup"><span data-stu-id="bb421-218">childApps</span></span>|<span data-ttu-id="bb421-219">colección de [macOSLobChildApp](../resources/intune-apps-macoslobchildapp.md)</span><span class="sxs-lookup"><span data-stu-id="bb421-219">[macOSLobChildApp](../resources/intune-apps-macoslobchildapp.md) collection</span></span>|<span data-ttu-id="bb421-220">La lista de aplicaciones en este paquete de agrupación</span><span class="sxs-lookup"><span data-stu-id="bb421-220">The app list in this bundle package</span></span>|
|<span data-ttu-id="bb421-221">identityVersion</span><span class="sxs-lookup"><span data-stu-id="bb421-221">identityVersion</span></span>|<span data-ttu-id="bb421-222">String</span><span class="sxs-lookup"><span data-stu-id="bb421-222">String</span></span>|<span data-ttu-id="bb421-223">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="bb421-223">The identity version.</span></span>|
|<span data-ttu-id="bb421-224">md5HashChunkSize</span><span class="sxs-lookup"><span data-stu-id="bb421-224">md5HashChunkSize</span></span>|<span data-ttu-id="bb421-225">Int32</span><span class="sxs-lookup"><span data-stu-id="bb421-225">Int32</span></span>|<span data-ttu-id="bb421-226">El tamaño del fragmento de hash MD5</span><span class="sxs-lookup"><span data-stu-id="bb421-226">The chunk size for MD5 hash</span></span>|
|<span data-ttu-id="bb421-227">md5Hash</span><span class="sxs-lookup"><span data-stu-id="bb421-227">md5Hash</span></span>|<span data-ttu-id="bb421-228">Colección String</span><span class="sxs-lookup"><span data-stu-id="bb421-228">String collection</span></span>|<span data-ttu-id="bb421-229">Los códigos de hash MD5</span><span class="sxs-lookup"><span data-stu-id="bb421-229">The MD5 hash codes</span></span>|
|<span data-ttu-id="bb421-230">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="bb421-230">ignoreVersionDetection</span></span>|<span data-ttu-id="bb421-231">Booleano</span><span class="sxs-lookup"><span data-stu-id="bb421-231">Boolean</span></span>|<span data-ttu-id="bb421-232">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb421-232">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="bb421-233">Se debe establecer en true para Mac OS aplicaciones de línea de negocio (LoB) que usan una característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="bb421-233">Set this to true for macOS Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="bb421-234">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb421-234">Response</span></span>
<span data-ttu-id="bb421-235">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [macOSLobApp](../resources/intune-apps-macoslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb421-235">If successful, this method returns a `201 Created` response code and a [macOSLobApp](../resources/intune-apps-macoslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb421-236">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb421-236">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb421-237">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb421-237">Request</span></span>
<span data-ttu-id="bb421-238">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb421-238">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1526

{
  "@odata.type": "#microsoft.graph.macOSLobApp",
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
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.macOSMinimumOperatingSystem",
    "v10_7": true,
    "v10_8": true,
    "v10_9": true,
    "v10_10": true,
    "v10_11": true,
    "v10_12": true,
    "v10_13": true
  },
  "buildNumber": "Build Number value",
  "versionNumber": "Version Number value",
  "childApps": [
    {
      "@odata.type": "microsoft.graph.macOSLobChildApp",
      "bundleId": "Bundle Id value",
      "buildNumber": "Build Number value",
      "versionNumber": "Version Number value"
    }
  ],
  "identityVersion": "Identity Version value",
  "md5HashChunkSize": 0,
  "md5Hash": [
    "Md5Hash value"
  ],
  "ignoreVersionDetection": true
}
```

### <a name="response"></a><span data-ttu-id="bb421-239">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb421-239">Response</span></span>
<span data-ttu-id="bb421-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb421-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1634

{
  "@odata.type": "#microsoft.graph.macOSLobApp",
  "id": "7be9250a-250a-7be9-0a25-e97b0a25e97b",
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
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.macOSMinimumOperatingSystem",
    "v10_7": true,
    "v10_8": true,
    "v10_9": true,
    "v10_10": true,
    "v10_11": true,
    "v10_12": true,
    "v10_13": true
  },
  "buildNumber": "Build Number value",
  "versionNumber": "Version Number value",
  "childApps": [
    {
      "@odata.type": "microsoft.graph.macOSLobChildApp",
      "bundleId": "Bundle Id value",
      "buildNumber": "Build Number value",
      "versionNumber": "Version Number value"
    }
  ],
  "identityVersion": "Identity Version value",
  "md5HashChunkSize": 0,
  "md5Hash": [
    "Md5Hash value"
  ],
  "ignoreVersionDetection": true
}
```




