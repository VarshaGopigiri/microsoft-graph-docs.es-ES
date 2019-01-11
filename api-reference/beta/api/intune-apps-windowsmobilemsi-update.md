---
title: Actualizar windowsMobileMSI
description: Actualice las propiedades de un objeto windowsMobileMSI.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6632343b7a85b6f3444908b6dc3699d11bf4673a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894582"
---
# <a name="update-windowsmobilemsi"></a><span data-ttu-id="f0811-103">Actualizar windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="f0811-103">Update windowsMobileMSI</span></span>

> <span data-ttu-id="f0811-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0811-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0811-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0811-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f0811-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f0811-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f0811-107">Actualice las propiedades de un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-107">Update the properties of a [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f0811-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f0811-108">Prerequisites</span></span>
<span data-ttu-id="f0811-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f0811-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f0811-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0811-111">Permission type</span></span>|<span data-ttu-id="f0811-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0811-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f0811-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0811-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f0811-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0811-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f0811-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0811-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f0811-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0811-116">Not supported.</span></span>|
|<span data-ttu-id="f0811-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0811-117">Application</span></span>|<span data-ttu-id="f0811-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0811-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f0811-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0811-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="f0811-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0811-120">Request headers</span></span>
|<span data-ttu-id="f0811-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0811-121">Header</span></span>|<span data-ttu-id="f0811-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f0811-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f0811-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f0811-123">Authorization</span></span>|<span data-ttu-id="f0811-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f0811-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f0811-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f0811-125">Accept</span></span>|<span data-ttu-id="f0811-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f0811-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f0811-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0811-127">Request body</span></span>
<span data-ttu-id="f0811-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-128">In the request body, supply a JSON representation for the [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>

<span data-ttu-id="f0811-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-129">The following table shows the properties that are required when you create the [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span></span>

|<span data-ttu-id="f0811-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f0811-130">Property</span></span>|<span data-ttu-id="f0811-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0811-131">Type</span></span>|<span data-ttu-id="f0811-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0811-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f0811-133">id</span><span class="sxs-lookup"><span data-stu-id="f0811-133">id</span></span>|<span data-ttu-id="f0811-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-134">String</span></span>|<span data-ttu-id="f0811-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f0811-135">Key of the entity.</span></span> <span data-ttu-id="f0811-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-137">displayName</span><span class="sxs-lookup"><span data-stu-id="f0811-137">displayName</span></span>|<span data-ttu-id="f0811-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-138">String</span></span>|<span data-ttu-id="f0811-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="f0811-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="f0811-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-141">descripción</span><span class="sxs-lookup"><span data-stu-id="f0811-141">description</span></span>|<span data-ttu-id="f0811-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-142">String</span></span>|<span data-ttu-id="f0811-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-143">The description of the app.</span></span> <span data-ttu-id="f0811-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-145">publicador</span><span class="sxs-lookup"><span data-stu-id="f0811-145">publisher</span></span>|<span data-ttu-id="f0811-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-146">String</span></span>|<span data-ttu-id="f0811-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-147">The publisher of the app.</span></span> <span data-ttu-id="f0811-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="f0811-149">largeIcon</span></span>|[<span data-ttu-id="f0811-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="f0811-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="f0811-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="f0811-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="f0811-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f0811-153">createdDateTime</span></span>|<span data-ttu-id="f0811-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f0811-154">DateTimeOffset</span></span>|<span data-ttu-id="f0811-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-155">The date and time the app was created.</span></span> <span data-ttu-id="f0811-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f0811-157">lastModifiedDateTime</span></span>|<span data-ttu-id="f0811-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f0811-158">DateTimeOffset</span></span>|<span data-ttu-id="f0811-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-159">The date and time the app was last modified.</span></span> <span data-ttu-id="f0811-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="f0811-161">isFeatured</span></span>|<span data-ttu-id="f0811-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="f0811-162">Boolean</span></span>|<span data-ttu-id="f0811-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="f0811-164">privacyInformationUrl</span></span>|<span data-ttu-id="f0811-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-165">String</span></span>|<span data-ttu-id="f0811-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f0811-166">The privacy statement Url.</span></span> <span data-ttu-id="f0811-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="f0811-168">informationUrl</span></span>|<span data-ttu-id="f0811-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-169">String</span></span>|<span data-ttu-id="f0811-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f0811-170">The more information Url.</span></span> <span data-ttu-id="f0811-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-172">owner</span><span class="sxs-lookup"><span data-stu-id="f0811-172">owner</span></span>|<span data-ttu-id="f0811-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-173">String</span></span>|<span data-ttu-id="f0811-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-174">The owner of the app.</span></span> <span data-ttu-id="f0811-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-176">developer</span><span class="sxs-lookup"><span data-stu-id="f0811-176">developer</span></span>|<span data-ttu-id="f0811-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-177">String</span></span>|<span data-ttu-id="f0811-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-178">The developer of the app.</span></span> <span data-ttu-id="f0811-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-180">notas</span><span class="sxs-lookup"><span data-stu-id="f0811-180">notes</span></span>|<span data-ttu-id="f0811-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-181">String</span></span>|<span data-ttu-id="f0811-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-182">Notes for the app.</span></span> <span data-ttu-id="f0811-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="f0811-184">uploadState</span></span>|<span data-ttu-id="f0811-185">Int32</span><span class="sxs-lookup"><span data-stu-id="f0811-185">Int32</span></span>|<span data-ttu-id="f0811-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="f0811-186">The upload state.</span></span> <span data-ttu-id="f0811-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f0811-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="f0811-188">publishingState</span></span>|[<span data-ttu-id="f0811-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="f0811-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="f0811-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-190">The publishing state for the app.</span></span> <span data-ttu-id="f0811-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="f0811-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="f0811-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="f0811-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="f0811-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="f0811-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="f0811-194">committedContentVersion</span></span>|<span data-ttu-id="f0811-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-195">String</span></span>|<span data-ttu-id="f0811-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="f0811-196">The internal committed content version.</span></span> <span data-ttu-id="f0811-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="f0811-198">fileName</span><span class="sxs-lookup"><span data-stu-id="f0811-198">fileName</span></span>|<span data-ttu-id="f0811-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-199">String</span></span>|<span data-ttu-id="f0811-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="f0811-200">The name of the main Lob application file.</span></span> <span data-ttu-id="f0811-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="f0811-202">size</span><span class="sxs-lookup"><span data-stu-id="f0811-202">size</span></span>|<span data-ttu-id="f0811-203">Int64</span><span class="sxs-lookup"><span data-stu-id="f0811-203">Int64</span></span>|<span data-ttu-id="f0811-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="f0811-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="f0811-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0811-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="f0811-206">commandLine</span><span class="sxs-lookup"><span data-stu-id="f0811-206">commandLine</span></span>|<span data-ttu-id="f0811-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-207">String</span></span>|<span data-ttu-id="f0811-208">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f0811-208">The command line.</span></span>|
|<span data-ttu-id="f0811-209">productCode</span><span class="sxs-lookup"><span data-stu-id="f0811-209">productCode</span></span>|<span data-ttu-id="f0811-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-210">String</span></span>|<span data-ttu-id="f0811-211">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="f0811-211">The product code.</span></span>|
|<span data-ttu-id="f0811-212">productVersion</span><span class="sxs-lookup"><span data-stu-id="f0811-212">productVersion</span></span>|<span data-ttu-id="f0811-213">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-213">String</span></span>|<span data-ttu-id="f0811-214">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="f0811-214">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="f0811-215">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="f0811-215">ignoreVersionDetection</span></span>|<span data-ttu-id="f0811-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="f0811-216">Boolean</span></span>|<span data-ttu-id="f0811-217">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0811-217">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="f0811-218">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="f0811-218">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|
|<span data-ttu-id="f0811-219">identityVersion</span><span class="sxs-lookup"><span data-stu-id="f0811-219">identityVersion</span></span>|<span data-ttu-id="f0811-220">Cadena</span><span class="sxs-lookup"><span data-stu-id="f0811-220">String</span></span>|<span data-ttu-id="f0811-221">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="f0811-221">The identity version.</span></span>|
|<span data-ttu-id="f0811-222">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="f0811-222">useDeviceContext</span></span>|<span data-ttu-id="f0811-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="f0811-223">Boolean</span></span>|<span data-ttu-id="f0811-224">Indica si se debe instalar un archivo MSI de modo dual en el contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0811-224">Indicates whether to install a dual-mode MSI in the device context.</span></span> <span data-ttu-id="f0811-225">Si es true, se instalará la aplicación para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f0811-225">If true, app will be installed for all users.</span></span> <span data-ttu-id="f0811-226">Si es false, la aplicación será instalados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f0811-226">If false, app will be installed per-user.</span></span> <span data-ttu-id="f0811-227">Si es nulo, el servicio utilizará contexto de instalación del paquete MSI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f0811-227">If null, service will use the MSI package's default install context.</span></span> <span data-ttu-id="f0811-228">En el caso de MSI de modo dual, este valor predeterminado será por usuario.</span><span class="sxs-lookup"><span data-stu-id="f0811-228">In case of dual-mode MSI, this default will be per-user.</span></span>  <span data-ttu-id="f0811-229">No se puede establecer para las aplicaciones de modo que no sean de dual.</span><span class="sxs-lookup"><span data-stu-id="f0811-229">Cannot be set for non-dual-mode apps.</span></span>  <span data-ttu-id="f0811-230">No se puede cambiar después de la creación inicial de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0811-230">Cannot be changed after initial creation of the application.</span></span>|



## <a name="response"></a><span data-ttu-id="f0811-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0811-231">Response</span></span>
<span data-ttu-id="f0811-232">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0811-232">If successful, this method returns a `200 OK` response code and an updated [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0811-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0811-233">Example</span></span>
### <a name="request"></a><span data-ttu-id="f0811-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0811-234">Request</span></span>
<span data-ttu-id="f0811-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0811-235">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f0811-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0811-236">Response</span></span>
<span data-ttu-id="f0811-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f0811-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





