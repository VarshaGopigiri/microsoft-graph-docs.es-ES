---
title: Actualizar windowsMobileMSI
description: Actualice las propiedades de un objeto windowsMobileMSI.
author: tfitzmac
ms.openlocfilehash: 859d32fbf053ba22c0bd59afe8ad24d6b05c84a1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310748"
---
# <a name="update-windowsmobilemsi"></a><span data-ttu-id="81fe0-103">Actualizar windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="81fe0-103">Update windowsMobileMSI</span></span>

> <span data-ttu-id="81fe0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="81fe0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="81fe0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="81fe0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="81fe0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="81fe0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="81fe0-107">Actualice las propiedades de un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-107">Update the properties of a [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="81fe0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="81fe0-108">Prerequisites</span></span>
<span data-ttu-id="81fe0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="81fe0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="81fe0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="81fe0-111">Permission type</span></span>|<span data-ttu-id="81fe0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="81fe0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="81fe0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="81fe0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="81fe0-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="81fe0-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="81fe0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="81fe0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="81fe0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="81fe0-116">Not supported.</span></span>|
|<span data-ttu-id="81fe0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="81fe0-117">Application</span></span>|<span data-ttu-id="81fe0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="81fe0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="81fe0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="81fe0-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="81fe0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="81fe0-120">Request headers</span></span>
|<span data-ttu-id="81fe0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81fe0-121">Header</span></span>|<span data-ttu-id="81fe0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="81fe0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="81fe0-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="81fe0-123">Authorization</span></span>|<span data-ttu-id="81fe0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="81fe0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="81fe0-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="81fe0-125">Accept</span></span>|<span data-ttu-id="81fe0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="81fe0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="81fe0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="81fe0-127">Request body</span></span>
<span data-ttu-id="81fe0-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-128">In the request body, supply a JSON representation for the [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>

<span data-ttu-id="81fe0-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-129">The following table shows the properties that are required when you create the [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span></span>

|<span data-ttu-id="81fe0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="81fe0-130">Property</span></span>|<span data-ttu-id="81fe0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="81fe0-131">Type</span></span>|<span data-ttu-id="81fe0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="81fe0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="81fe0-133">id</span><span class="sxs-lookup"><span data-stu-id="81fe0-133">id</span></span>|<span data-ttu-id="81fe0-134">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-134">String</span></span>|<span data-ttu-id="81fe0-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="81fe0-135">Key of the entity.</span></span> <span data-ttu-id="81fe0-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-137">displayName</span><span class="sxs-lookup"><span data-stu-id="81fe0-137">displayName</span></span>|<span data-ttu-id="81fe0-138">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-138">String</span></span>|<span data-ttu-id="81fe0-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="81fe0-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="81fe0-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-141">descripción</span><span class="sxs-lookup"><span data-stu-id="81fe0-141">description</span></span>|<span data-ttu-id="81fe0-142">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-142">String</span></span>|<span data-ttu-id="81fe0-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-143">The description of the app.</span></span> <span data-ttu-id="81fe0-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-145">publicador</span><span class="sxs-lookup"><span data-stu-id="81fe0-145">publisher</span></span>|<span data-ttu-id="81fe0-146">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-146">String</span></span>|<span data-ttu-id="81fe0-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-147">The publisher of the app.</span></span> <span data-ttu-id="81fe0-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="81fe0-149">largeIcon</span></span>|[<span data-ttu-id="81fe0-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="81fe0-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="81fe0-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="81fe0-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="81fe0-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="81fe0-153">createdDateTime</span></span>|<span data-ttu-id="81fe0-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="81fe0-154">DateTimeOffset</span></span>|<span data-ttu-id="81fe0-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-155">The date and time the app was created.</span></span> <span data-ttu-id="81fe0-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="81fe0-157">lastModifiedDateTime</span></span>|<span data-ttu-id="81fe0-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="81fe0-158">DateTimeOffset</span></span>|<span data-ttu-id="81fe0-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-159">The date and time the app was last modified.</span></span> <span data-ttu-id="81fe0-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="81fe0-161">isFeatured</span></span>|<span data-ttu-id="81fe0-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="81fe0-162">Boolean</span></span>|<span data-ttu-id="81fe0-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="81fe0-164">privacyInformationUrl</span></span>|<span data-ttu-id="81fe0-165">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-165">String</span></span>|<span data-ttu-id="81fe0-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="81fe0-166">The privacy statement Url.</span></span> <span data-ttu-id="81fe0-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="81fe0-168">informationUrl</span></span>|<span data-ttu-id="81fe0-169">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-169">String</span></span>|<span data-ttu-id="81fe0-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="81fe0-170">The more information Url.</span></span> <span data-ttu-id="81fe0-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-172">owner</span><span class="sxs-lookup"><span data-stu-id="81fe0-172">owner</span></span>|<span data-ttu-id="81fe0-173">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-173">String</span></span>|<span data-ttu-id="81fe0-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-174">The owner of the app.</span></span> <span data-ttu-id="81fe0-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-176">developer</span><span class="sxs-lookup"><span data-stu-id="81fe0-176">developer</span></span>|<span data-ttu-id="81fe0-177">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-177">String</span></span>|<span data-ttu-id="81fe0-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-178">The developer of the app.</span></span> <span data-ttu-id="81fe0-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-180">notas</span><span class="sxs-lookup"><span data-stu-id="81fe0-180">notes</span></span>|<span data-ttu-id="81fe0-181">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-181">String</span></span>|<span data-ttu-id="81fe0-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-182">Notes for the app.</span></span> <span data-ttu-id="81fe0-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="81fe0-184">uploadState</span></span>|<span data-ttu-id="81fe0-185">Int32</span><span class="sxs-lookup"><span data-stu-id="81fe0-185">Int32</span></span>|<span data-ttu-id="81fe0-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="81fe0-186">The upload state.</span></span> <span data-ttu-id="81fe0-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="81fe0-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="81fe0-188">publishingState</span></span>|[<span data-ttu-id="81fe0-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="81fe0-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="81fe0-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-190">The publishing state for the app.</span></span> <span data-ttu-id="81fe0-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="81fe0-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="81fe0-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="81fe0-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="81fe0-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="81fe0-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="81fe0-194">committedContentVersion</span></span>|<span data-ttu-id="81fe0-195">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-195">String</span></span>|<span data-ttu-id="81fe0-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="81fe0-196">The internal committed content version.</span></span> <span data-ttu-id="81fe0-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="81fe0-198">fileName</span><span class="sxs-lookup"><span data-stu-id="81fe0-198">fileName</span></span>|<span data-ttu-id="81fe0-199">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-199">String</span></span>|<span data-ttu-id="81fe0-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="81fe0-200">The name of the main Lob application file.</span></span> <span data-ttu-id="81fe0-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="81fe0-202">size</span><span class="sxs-lookup"><span data-stu-id="81fe0-202">size</span></span>|<span data-ttu-id="81fe0-203">Int64</span><span class="sxs-lookup"><span data-stu-id="81fe0-203">Int64</span></span>|<span data-ttu-id="81fe0-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="81fe0-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="81fe0-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="81fe0-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="81fe0-206">commandLine</span><span class="sxs-lookup"><span data-stu-id="81fe0-206">commandLine</span></span>|<span data-ttu-id="81fe0-207">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-207">String</span></span>|<span data-ttu-id="81fe0-208">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="81fe0-208">The command line.</span></span>|
|<span data-ttu-id="81fe0-209">productCode</span><span class="sxs-lookup"><span data-stu-id="81fe0-209">productCode</span></span>|<span data-ttu-id="81fe0-210">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-210">String</span></span>|<span data-ttu-id="81fe0-211">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="81fe0-211">The product code.</span></span>|
|<span data-ttu-id="81fe0-212">productVersion</span><span class="sxs-lookup"><span data-stu-id="81fe0-212">productVersion</span></span>|<span data-ttu-id="81fe0-213">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-213">String</span></span>|<span data-ttu-id="81fe0-214">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="81fe0-214">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="81fe0-215">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="81fe0-215">ignoreVersionDetection</span></span>|<span data-ttu-id="81fe0-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="81fe0-216">Boolean</span></span>|<span data-ttu-id="81fe0-217">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81fe0-217">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="81fe0-218">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="81fe0-218">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|
|<span data-ttu-id="81fe0-219">identityVersion</span><span class="sxs-lookup"><span data-stu-id="81fe0-219">identityVersion</span></span>|<span data-ttu-id="81fe0-220">String</span><span class="sxs-lookup"><span data-stu-id="81fe0-220">String</span></span>|<span data-ttu-id="81fe0-221">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="81fe0-221">The identity version.</span></span>|
|<span data-ttu-id="81fe0-222">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="81fe0-222">useDeviceContext</span></span>|<span data-ttu-id="81fe0-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="81fe0-223">Boolean</span></span>|<span data-ttu-id="81fe0-224">Indica si se debe instalar un archivo MSI de modo dual en el contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81fe0-224">Indicates whether to install a dual-mode MSI in the device context.</span></span> <span data-ttu-id="81fe0-225">Si es true, se instalará la aplicación para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="81fe0-225">If true, app will be installed for all users.</span></span> <span data-ttu-id="81fe0-226">Si es false, la aplicación será instalados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="81fe0-226">If false, app will be installed per-user.</span></span> <span data-ttu-id="81fe0-227">Si es nulo, el servicio utilizará contexto de instalación del paquete MSI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81fe0-227">If null, service will use the MSI package's default install context.</span></span> <span data-ttu-id="81fe0-228">En el caso de MSI de modo dual, este valor predeterminado será por usuario.</span><span class="sxs-lookup"><span data-stu-id="81fe0-228">In case of dual-mode MSI, this default will be per-user.</span></span>  <span data-ttu-id="81fe0-229">No se puede establecer para las aplicaciones de modo que no sean de dual.</span><span class="sxs-lookup"><span data-stu-id="81fe0-229">Cannot be set for non-dual-mode apps.</span></span>  <span data-ttu-id="81fe0-230">No se puede cambiar después de la creación inicial de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81fe0-230">Cannot be changed after initial creation of the application.</span></span>|



## <a name="response"></a><span data-ttu-id="81fe0-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81fe0-231">Response</span></span>
<span data-ttu-id="81fe0-232">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81fe0-232">If successful, this method returns a `200 OK` response code and an updated [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="81fe0-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="81fe0-233">Example</span></span>
### <a name="request"></a><span data-ttu-id="81fe0-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="81fe0-234">Request</span></span>
<span data-ttu-id="81fe0-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="81fe0-235">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 963

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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true,
  "identityVersion": "Identity Version value",
  "useDeviceContext": true
}
```

### <a name="response"></a><span data-ttu-id="81fe0-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81fe0-236">Response</span></span>
<span data-ttu-id="81fe0-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="81fe0-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1126

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
  "id": "aa453e5d-3e5d-aa45-5d3e-45aa5d3e45aa",
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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true,
  "identityVersion": "Identity Version value",
  "useDeviceContext": true
}
```





