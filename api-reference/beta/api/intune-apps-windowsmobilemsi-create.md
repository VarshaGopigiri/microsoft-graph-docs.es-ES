---
title: Crear windowsMobileMSI
description: Crear un objeto windowsMobileMSI.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 731c869152d8b47f123f84f6640b5212f4b11185
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860147"
---
# <a name="create-windowsmobilemsi"></a><span data-ttu-id="9f86d-103">Crear windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="9f86d-103">Create windowsMobileMSI</span></span>

> <span data-ttu-id="9f86d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9f86d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9f86d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9f86d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9f86d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f86d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f86d-107">Crear un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-107">Create a new [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9f86d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f86d-108">Prerequisites</span></span>
<span data-ttu-id="9f86d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f86d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9f86d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f86d-111">Permission type</span></span>|<span data-ttu-id="9f86d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f86d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9f86d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f86d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9f86d-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9f86d-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9f86d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f86d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9f86d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f86d-116">Not supported.</span></span>|
|<span data-ttu-id="9f86d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f86d-117">Application</span></span>|<span data-ttu-id="9f86d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f86d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9f86d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f86d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="9f86d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f86d-120">Request headers</span></span>
|<span data-ttu-id="9f86d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f86d-121">Header</span></span>|<span data-ttu-id="9f86d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9f86d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9f86d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9f86d-123">Authorization</span></span>|<span data-ttu-id="9f86d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9f86d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9f86d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9f86d-125">Accept</span></span>|<span data-ttu-id="9f86d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9f86d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9f86d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f86d-127">Request body</span></span>
<span data-ttu-id="9f86d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="9f86d-128">In the request body, supply a JSON representation for the windowsMobileMSI object.</span></span>

<span data-ttu-id="9f86d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="9f86d-129">The following table shows the properties that are required when you create the windowsMobileMSI.</span></span>

|<span data-ttu-id="9f86d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f86d-130">Property</span></span>|<span data-ttu-id="9f86d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f86d-131">Type</span></span>|<span data-ttu-id="9f86d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f86d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f86d-133">id</span><span class="sxs-lookup"><span data-stu-id="9f86d-133">id</span></span>|<span data-ttu-id="9f86d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-134">String</span></span>|<span data-ttu-id="9f86d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9f86d-135">Key of the entity.</span></span> <span data-ttu-id="9f86d-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-137">displayName</span><span class="sxs-lookup"><span data-stu-id="9f86d-137">displayName</span></span>|<span data-ttu-id="9f86d-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-138">String</span></span>|<span data-ttu-id="9f86d-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="9f86d-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="9f86d-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-141">descripción</span><span class="sxs-lookup"><span data-stu-id="9f86d-141">description</span></span>|<span data-ttu-id="9f86d-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-142">String</span></span>|<span data-ttu-id="9f86d-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-143">The description of the app.</span></span> <span data-ttu-id="9f86d-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-145">publicador</span><span class="sxs-lookup"><span data-stu-id="9f86d-145">publisher</span></span>|<span data-ttu-id="9f86d-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-146">String</span></span>|<span data-ttu-id="9f86d-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-147">The publisher of the app.</span></span> <span data-ttu-id="9f86d-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="9f86d-149">largeIcon</span></span>|[<span data-ttu-id="9f86d-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="9f86d-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="9f86d-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="9f86d-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="9f86d-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9f86d-153">createdDateTime</span></span>|<span data-ttu-id="9f86d-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f86d-154">DateTimeOffset</span></span>|<span data-ttu-id="9f86d-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-155">The date and time the app was created.</span></span> <span data-ttu-id="9f86d-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9f86d-157">lastModifiedDateTime</span></span>|<span data-ttu-id="9f86d-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f86d-158">DateTimeOffset</span></span>|<span data-ttu-id="9f86d-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-159">The date and time the app was last modified.</span></span> <span data-ttu-id="9f86d-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="9f86d-161">isFeatured</span></span>|<span data-ttu-id="9f86d-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f86d-162">Boolean</span></span>|<span data-ttu-id="9f86d-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="9f86d-164">privacyInformationUrl</span></span>|<span data-ttu-id="9f86d-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-165">String</span></span>|<span data-ttu-id="9f86d-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="9f86d-166">The privacy statement Url.</span></span> <span data-ttu-id="9f86d-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="9f86d-168">informationUrl</span></span>|<span data-ttu-id="9f86d-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-169">String</span></span>|<span data-ttu-id="9f86d-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9f86d-170">The more information Url.</span></span> <span data-ttu-id="9f86d-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-172">owner</span><span class="sxs-lookup"><span data-stu-id="9f86d-172">owner</span></span>|<span data-ttu-id="9f86d-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-173">String</span></span>|<span data-ttu-id="9f86d-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-174">The owner of the app.</span></span> <span data-ttu-id="9f86d-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-176">developer</span><span class="sxs-lookup"><span data-stu-id="9f86d-176">developer</span></span>|<span data-ttu-id="9f86d-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-177">String</span></span>|<span data-ttu-id="9f86d-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-178">The developer of the app.</span></span> <span data-ttu-id="9f86d-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-180">notas</span><span class="sxs-lookup"><span data-stu-id="9f86d-180">notes</span></span>|<span data-ttu-id="9f86d-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-181">String</span></span>|<span data-ttu-id="9f86d-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-182">Notes for the app.</span></span> <span data-ttu-id="9f86d-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="9f86d-184">uploadState</span></span>|<span data-ttu-id="9f86d-185">Int32</span><span class="sxs-lookup"><span data-stu-id="9f86d-185">Int32</span></span>|<span data-ttu-id="9f86d-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="9f86d-186">The upload state.</span></span> <span data-ttu-id="9f86d-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9f86d-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="9f86d-188">publishingState</span></span>|[<span data-ttu-id="9f86d-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="9f86d-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="9f86d-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-190">The publishing state for the app.</span></span> <span data-ttu-id="9f86d-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="9f86d-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="9f86d-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="9f86d-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="9f86d-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="9f86d-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="9f86d-194">committedContentVersion</span></span>|<span data-ttu-id="9f86d-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-195">String</span></span>|<span data-ttu-id="9f86d-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="9f86d-196">The internal committed content version.</span></span> <span data-ttu-id="9f86d-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="9f86d-198">fileName</span><span class="sxs-lookup"><span data-stu-id="9f86d-198">fileName</span></span>|<span data-ttu-id="9f86d-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-199">String</span></span>|<span data-ttu-id="9f86d-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="9f86d-200">The name of the main Lob application file.</span></span> <span data-ttu-id="9f86d-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="9f86d-202">size</span><span class="sxs-lookup"><span data-stu-id="9f86d-202">size</span></span>|<span data-ttu-id="9f86d-203">Int64</span><span class="sxs-lookup"><span data-stu-id="9f86d-203">Int64</span></span>|<span data-ttu-id="9f86d-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="9f86d-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="9f86d-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f86d-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="9f86d-206">commandLine</span><span class="sxs-lookup"><span data-stu-id="9f86d-206">commandLine</span></span>|<span data-ttu-id="9f86d-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-207">String</span></span>|<span data-ttu-id="9f86d-208">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="9f86d-208">The command line.</span></span>|
|<span data-ttu-id="9f86d-209">productCode</span><span class="sxs-lookup"><span data-stu-id="9f86d-209">productCode</span></span>|<span data-ttu-id="9f86d-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-210">String</span></span>|<span data-ttu-id="9f86d-211">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="9f86d-211">The product code.</span></span>|
|<span data-ttu-id="9f86d-212">productVersion</span><span class="sxs-lookup"><span data-stu-id="9f86d-212">productVersion</span></span>|<span data-ttu-id="9f86d-213">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-213">String</span></span>|<span data-ttu-id="9f86d-214">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="9f86d-214">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="9f86d-215">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="9f86d-215">ignoreVersionDetection</span></span>|<span data-ttu-id="9f86d-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f86d-216">Boolean</span></span>|<span data-ttu-id="9f86d-217">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f86d-217">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="9f86d-218">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="9f86d-218">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|
|<span data-ttu-id="9f86d-219">identityVersion</span><span class="sxs-lookup"><span data-stu-id="9f86d-219">identityVersion</span></span>|<span data-ttu-id="9f86d-220">Cadena</span><span class="sxs-lookup"><span data-stu-id="9f86d-220">String</span></span>|<span data-ttu-id="9f86d-221">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="9f86d-221">The identity version.</span></span>|
|<span data-ttu-id="9f86d-222">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="9f86d-222">useDeviceContext</span></span>|<span data-ttu-id="9f86d-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f86d-223">Boolean</span></span>|<span data-ttu-id="9f86d-224">Indica si se debe instalar un archivo MSI de modo dual en el contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f86d-224">Indicates whether to install a dual-mode MSI in the device context.</span></span> <span data-ttu-id="9f86d-225">Si es true, se instalará la aplicación para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9f86d-225">If true, app will be installed for all users.</span></span> <span data-ttu-id="9f86d-226">Si es false, la aplicación será instalados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9f86d-226">If false, app will be installed per-user.</span></span> <span data-ttu-id="9f86d-227">Si es nulo, el servicio utilizará contexto de instalación del paquete MSI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9f86d-227">If null, service will use the MSI package's default install context.</span></span> <span data-ttu-id="9f86d-228">En el caso de MSI de modo dual, este valor predeterminado será por usuario.</span><span class="sxs-lookup"><span data-stu-id="9f86d-228">In case of dual-mode MSI, this default will be per-user.</span></span>  <span data-ttu-id="9f86d-229">No se puede establecer para las aplicaciones de modo que no sean de dual.</span><span class="sxs-lookup"><span data-stu-id="9f86d-229">Cannot be set for non-dual-mode apps.</span></span>  <span data-ttu-id="9f86d-230">No se puede cambiar después de la creación inicial de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f86d-230">Cannot be changed after initial creation of the application.</span></span>|



## <a name="response"></a><span data-ttu-id="9f86d-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f86d-231">Response</span></span>
<span data-ttu-id="9f86d-232">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f86d-232">If successful, this method returns a `201 Created` response code and a [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f86d-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f86d-233">Example</span></span>
### <a name="request"></a><span data-ttu-id="9f86d-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f86d-234">Request</span></span>
<span data-ttu-id="9f86d-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f86d-235">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9f86d-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f86d-236">Response</span></span>
<span data-ttu-id="9f86d-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f86d-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





