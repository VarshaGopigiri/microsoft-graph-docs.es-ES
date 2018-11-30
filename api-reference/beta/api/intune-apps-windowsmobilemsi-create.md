---
title: Crear windowsMobileMSI
description: Crear un objeto windowsMobileMSI.
ms.openlocfilehash: b3826eeaa01a0d3f4b55f9927cf1bd305907253e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088134"
---
# <a name="create-windowsmobilemsi"></a><span data-ttu-id="b60a7-103">Crear windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="b60a7-103">Create windowsMobileMSI</span></span>

> <span data-ttu-id="b60a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b60a7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b60a7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b60a7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b60a7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b60a7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b60a7-107">Crear un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-107">Create a new [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b60a7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b60a7-108">Prerequisites</span></span>
<span data-ttu-id="b60a7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b60a7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b60a7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b60a7-111">Permission type</span></span>|<span data-ttu-id="b60a7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b60a7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b60a7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b60a7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b60a7-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b60a7-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b60a7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b60a7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b60a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b60a7-116">Not supported.</span></span>|
|<span data-ttu-id="b60a7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b60a7-117">Application</span></span>|<span data-ttu-id="b60a7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b60a7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b60a7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b60a7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="b60a7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b60a7-120">Request headers</span></span>
|<span data-ttu-id="b60a7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b60a7-121">Header</span></span>|<span data-ttu-id="b60a7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b60a7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b60a7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b60a7-123">Authorization</span></span>|<span data-ttu-id="b60a7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b60a7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b60a7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b60a7-125">Accept</span></span>|<span data-ttu-id="b60a7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b60a7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b60a7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b60a7-127">Request body</span></span>
<span data-ttu-id="b60a7-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="b60a7-128">In the request body, supply a JSON representation for the windowsMobileMSI object.</span></span>

<span data-ttu-id="b60a7-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="b60a7-129">The following table shows the properties that are required when you create the windowsMobileMSI.</span></span>

|<span data-ttu-id="b60a7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b60a7-130">Property</span></span>|<span data-ttu-id="b60a7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b60a7-131">Type</span></span>|<span data-ttu-id="b60a7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b60a7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b60a7-133">id</span><span class="sxs-lookup"><span data-stu-id="b60a7-133">id</span></span>|<span data-ttu-id="b60a7-134">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-134">String</span></span>|<span data-ttu-id="b60a7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b60a7-135">Key of the entity.</span></span> <span data-ttu-id="b60a7-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-137">displayName</span><span class="sxs-lookup"><span data-stu-id="b60a7-137">displayName</span></span>|<span data-ttu-id="b60a7-138">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-138">String</span></span>|<span data-ttu-id="b60a7-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="b60a7-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="b60a7-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-141">descripción</span><span class="sxs-lookup"><span data-stu-id="b60a7-141">description</span></span>|<span data-ttu-id="b60a7-142">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-142">String</span></span>|<span data-ttu-id="b60a7-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-143">The description of the app.</span></span> <span data-ttu-id="b60a7-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-145">publicador</span><span class="sxs-lookup"><span data-stu-id="b60a7-145">publisher</span></span>|<span data-ttu-id="b60a7-146">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-146">String</span></span>|<span data-ttu-id="b60a7-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-147">The publisher of the app.</span></span> <span data-ttu-id="b60a7-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="b60a7-149">largeIcon</span></span>|[<span data-ttu-id="b60a7-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="b60a7-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="b60a7-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="b60a7-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="b60a7-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b60a7-153">createdDateTime</span></span>|<span data-ttu-id="b60a7-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b60a7-154">DateTimeOffset</span></span>|<span data-ttu-id="b60a7-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-155">The date and time the app was created.</span></span> <span data-ttu-id="b60a7-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b60a7-157">lastModifiedDateTime</span></span>|<span data-ttu-id="b60a7-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b60a7-158">DateTimeOffset</span></span>|<span data-ttu-id="b60a7-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-159">The date and time the app was last modified.</span></span> <span data-ttu-id="b60a7-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="b60a7-161">isFeatured</span></span>|<span data-ttu-id="b60a7-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="b60a7-162">Boolean</span></span>|<span data-ttu-id="b60a7-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="b60a7-164">privacyInformationUrl</span></span>|<span data-ttu-id="b60a7-165">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-165">String</span></span>|<span data-ttu-id="b60a7-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="b60a7-166">The privacy statement Url.</span></span> <span data-ttu-id="b60a7-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="b60a7-168">informationUrl</span></span>|<span data-ttu-id="b60a7-169">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-169">String</span></span>|<span data-ttu-id="b60a7-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b60a7-170">The more information Url.</span></span> <span data-ttu-id="b60a7-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-172">owner</span><span class="sxs-lookup"><span data-stu-id="b60a7-172">owner</span></span>|<span data-ttu-id="b60a7-173">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-173">String</span></span>|<span data-ttu-id="b60a7-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-174">The owner of the app.</span></span> <span data-ttu-id="b60a7-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-176">developer</span><span class="sxs-lookup"><span data-stu-id="b60a7-176">developer</span></span>|<span data-ttu-id="b60a7-177">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-177">String</span></span>|<span data-ttu-id="b60a7-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-178">The developer of the app.</span></span> <span data-ttu-id="b60a7-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-180">notas</span><span class="sxs-lookup"><span data-stu-id="b60a7-180">notes</span></span>|<span data-ttu-id="b60a7-181">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-181">String</span></span>|<span data-ttu-id="b60a7-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-182">Notes for the app.</span></span> <span data-ttu-id="b60a7-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="b60a7-184">uploadState</span></span>|<span data-ttu-id="b60a7-185">Int32</span><span class="sxs-lookup"><span data-stu-id="b60a7-185">Int32</span></span>|<span data-ttu-id="b60a7-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="b60a7-186">The upload state.</span></span> <span data-ttu-id="b60a7-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b60a7-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="b60a7-188">publishingState</span></span>|[<span data-ttu-id="b60a7-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="b60a7-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="b60a7-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-190">The publishing state for the app.</span></span> <span data-ttu-id="b60a7-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="b60a7-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="b60a7-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="b60a7-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="b60a7-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="b60a7-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="b60a7-194">committedContentVersion</span></span>|<span data-ttu-id="b60a7-195">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-195">String</span></span>|<span data-ttu-id="b60a7-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="b60a7-196">The internal committed content version.</span></span> <span data-ttu-id="b60a7-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="b60a7-198">fileName</span><span class="sxs-lookup"><span data-stu-id="b60a7-198">fileName</span></span>|<span data-ttu-id="b60a7-199">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-199">String</span></span>|<span data-ttu-id="b60a7-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="b60a7-200">The name of the main Lob application file.</span></span> <span data-ttu-id="b60a7-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="b60a7-202">size</span><span class="sxs-lookup"><span data-stu-id="b60a7-202">size</span></span>|<span data-ttu-id="b60a7-203">Int64</span><span class="sxs-lookup"><span data-stu-id="b60a7-203">Int64</span></span>|<span data-ttu-id="b60a7-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="b60a7-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="b60a7-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="b60a7-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="b60a7-206">commandLine</span><span class="sxs-lookup"><span data-stu-id="b60a7-206">commandLine</span></span>|<span data-ttu-id="b60a7-207">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-207">String</span></span>|<span data-ttu-id="b60a7-208">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b60a7-208">The command line.</span></span>|
|<span data-ttu-id="b60a7-209">productCode</span><span class="sxs-lookup"><span data-stu-id="b60a7-209">productCode</span></span>|<span data-ttu-id="b60a7-210">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-210">String</span></span>|<span data-ttu-id="b60a7-211">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="b60a7-211">The product code.</span></span>|
|<span data-ttu-id="b60a7-212">productVersion</span><span class="sxs-lookup"><span data-stu-id="b60a7-212">productVersion</span></span>|<span data-ttu-id="b60a7-213">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-213">String</span></span>|<span data-ttu-id="b60a7-214">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="b60a7-214">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="b60a7-215">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="b60a7-215">ignoreVersionDetection</span></span>|<span data-ttu-id="b60a7-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="b60a7-216">Boolean</span></span>|<span data-ttu-id="b60a7-217">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b60a7-217">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="b60a7-218">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="b60a7-218">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|
|<span data-ttu-id="b60a7-219">identityVersion</span><span class="sxs-lookup"><span data-stu-id="b60a7-219">identityVersion</span></span>|<span data-ttu-id="b60a7-220">String</span><span class="sxs-lookup"><span data-stu-id="b60a7-220">String</span></span>|<span data-ttu-id="b60a7-221">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="b60a7-221">The identity version.</span></span>|
|<span data-ttu-id="b60a7-222">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="b60a7-222">useDeviceContext</span></span>|<span data-ttu-id="b60a7-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="b60a7-223">Boolean</span></span>|<span data-ttu-id="b60a7-224">Indica si se debe instalar un archivo MSI de modo dual en el contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b60a7-224">Indicates whether to install a dual-mode MSI in the device context.</span></span> <span data-ttu-id="b60a7-225">Si es true, se instalará la aplicación para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b60a7-225">If true, app will be installed for all users.</span></span> <span data-ttu-id="b60a7-226">Si es false, la aplicación será instalados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b60a7-226">If false, app will be installed per-user.</span></span> <span data-ttu-id="b60a7-227">Si es nulo, el servicio utilizará contexto de instalación del paquete MSI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b60a7-227">If null, service will use the MSI package's default install context.</span></span> <span data-ttu-id="b60a7-228">En el caso de MSI de modo dual, este valor predeterminado será por usuario.</span><span class="sxs-lookup"><span data-stu-id="b60a7-228">In case of dual-mode MSI, this default will be per-user.</span></span>  <span data-ttu-id="b60a7-229">No se puede establecer para las aplicaciones de modo que no sean de dual.</span><span class="sxs-lookup"><span data-stu-id="b60a7-229">Cannot be set for non-dual-mode apps.</span></span>  <span data-ttu-id="b60a7-230">No se puede cambiar después de la creación inicial de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b60a7-230">Cannot be changed after initial creation of the application.</span></span>|



## <a name="response"></a><span data-ttu-id="b60a7-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b60a7-231">Response</span></span>
<span data-ttu-id="b60a7-232">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b60a7-232">If successful, this method returns a `201 Created` response code and a [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b60a7-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b60a7-233">Example</span></span>
### <a name="request"></a><span data-ttu-id="b60a7-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b60a7-234">Request</span></span>
<span data-ttu-id="b60a7-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b60a7-235">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1018

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
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

### <a name="response"></a><span data-ttu-id="b60a7-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b60a7-236">Response</span></span>
<span data-ttu-id="b60a7-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b60a7-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




