---
title: Crear windowsPhone81AppX
description: Crear un nuevo objeto windowsPhone81AppX.
ms.openlocfilehash: 13c2e2b0484b5760973a67dbb980bdf829c7ba32
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088485"
---
# <a name="create-windowsphone81appx"></a><span data-ttu-id="2564a-103">Crear windowsPhone81AppX</span><span class="sxs-lookup"><span data-stu-id="2564a-103">Create windowsPhone81AppX</span></span>

> <span data-ttu-id="2564a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2564a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2564a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2564a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2564a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2564a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2564a-107">Crear un nuevo objeto [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) .</span><span class="sxs-lookup"><span data-stu-id="2564a-107">Create a new [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2564a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2564a-108">Prerequisites</span></span>
<span data-ttu-id="2564a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2564a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2564a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2564a-111">Permission type</span></span>|<span data-ttu-id="2564a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2564a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2564a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2564a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2564a-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2564a-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2564a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2564a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2564a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2564a-116">Not supported.</span></span>|
|<span data-ttu-id="2564a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2564a-117">Application</span></span>|<span data-ttu-id="2564a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2564a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2564a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2564a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="2564a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2564a-120">Request headers</span></span>
|<span data-ttu-id="2564a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2564a-121">Header</span></span>|<span data-ttu-id="2564a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2564a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2564a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2564a-123">Authorization</span></span>|<span data-ttu-id="2564a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2564a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2564a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2564a-125">Accept</span></span>|<span data-ttu-id="2564a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2564a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2564a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2564a-127">Request body</span></span>
<span data-ttu-id="2564a-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsPhone81AppX.</span><span class="sxs-lookup"><span data-stu-id="2564a-128">In the request body, supply a JSON representation for the windowsPhone81AppX object.</span></span>

<span data-ttu-id="2564a-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsPhone81AppX.</span><span class="sxs-lookup"><span data-stu-id="2564a-129">The following table shows the properties that are required when you create the windowsPhone81AppX.</span></span>

|<span data-ttu-id="2564a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2564a-130">Property</span></span>|<span data-ttu-id="2564a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2564a-131">Type</span></span>|<span data-ttu-id="2564a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2564a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2564a-133">id</span><span class="sxs-lookup"><span data-stu-id="2564a-133">id</span></span>|<span data-ttu-id="2564a-134">String</span><span class="sxs-lookup"><span data-stu-id="2564a-134">String</span></span>|<span data-ttu-id="2564a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2564a-135">Key of the entity.</span></span> <span data-ttu-id="2564a-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-137">displayName</span><span class="sxs-lookup"><span data-stu-id="2564a-137">displayName</span></span>|<span data-ttu-id="2564a-138">String</span><span class="sxs-lookup"><span data-stu-id="2564a-138">String</span></span>|<span data-ttu-id="2564a-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="2564a-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="2564a-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-141">descripción</span><span class="sxs-lookup"><span data-stu-id="2564a-141">description</span></span>|<span data-ttu-id="2564a-142">String</span><span class="sxs-lookup"><span data-stu-id="2564a-142">String</span></span>|<span data-ttu-id="2564a-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-143">The description of the app.</span></span> <span data-ttu-id="2564a-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-145">publicador</span><span class="sxs-lookup"><span data-stu-id="2564a-145">publisher</span></span>|<span data-ttu-id="2564a-146">String</span><span class="sxs-lookup"><span data-stu-id="2564a-146">String</span></span>|<span data-ttu-id="2564a-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-147">The publisher of the app.</span></span> <span data-ttu-id="2564a-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="2564a-149">largeIcon</span></span>|[<span data-ttu-id="2564a-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="2564a-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="2564a-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="2564a-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="2564a-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2564a-153">createdDateTime</span></span>|<span data-ttu-id="2564a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2564a-154">DateTimeOffset</span></span>|<span data-ttu-id="2564a-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-155">The date and time the app was created.</span></span> <span data-ttu-id="2564a-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2564a-157">lastModifiedDateTime</span></span>|<span data-ttu-id="2564a-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2564a-158">DateTimeOffset</span></span>|<span data-ttu-id="2564a-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-159">The date and time the app was last modified.</span></span> <span data-ttu-id="2564a-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="2564a-161">isFeatured</span></span>|<span data-ttu-id="2564a-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="2564a-162">Boolean</span></span>|<span data-ttu-id="2564a-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="2564a-164">privacyInformationUrl</span></span>|<span data-ttu-id="2564a-165">String</span><span class="sxs-lookup"><span data-stu-id="2564a-165">String</span></span>|<span data-ttu-id="2564a-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="2564a-166">The privacy statement Url.</span></span> <span data-ttu-id="2564a-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="2564a-168">informationUrl</span></span>|<span data-ttu-id="2564a-169">String</span><span class="sxs-lookup"><span data-stu-id="2564a-169">String</span></span>|<span data-ttu-id="2564a-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2564a-170">The more information Url.</span></span> <span data-ttu-id="2564a-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-172">owner</span><span class="sxs-lookup"><span data-stu-id="2564a-172">owner</span></span>|<span data-ttu-id="2564a-173">String</span><span class="sxs-lookup"><span data-stu-id="2564a-173">String</span></span>|<span data-ttu-id="2564a-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-174">The owner of the app.</span></span> <span data-ttu-id="2564a-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-176">developer</span><span class="sxs-lookup"><span data-stu-id="2564a-176">developer</span></span>|<span data-ttu-id="2564a-177">String</span><span class="sxs-lookup"><span data-stu-id="2564a-177">String</span></span>|<span data-ttu-id="2564a-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-178">The developer of the app.</span></span> <span data-ttu-id="2564a-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-180">notas</span><span class="sxs-lookup"><span data-stu-id="2564a-180">notes</span></span>|<span data-ttu-id="2564a-181">String</span><span class="sxs-lookup"><span data-stu-id="2564a-181">String</span></span>|<span data-ttu-id="2564a-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-182">Notes for the app.</span></span> <span data-ttu-id="2564a-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="2564a-184">uploadState</span></span>|<span data-ttu-id="2564a-185">Int32</span><span class="sxs-lookup"><span data-stu-id="2564a-185">Int32</span></span>|<span data-ttu-id="2564a-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="2564a-186">The upload state.</span></span> <span data-ttu-id="2564a-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2564a-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="2564a-188">publishingState</span></span>|[<span data-ttu-id="2564a-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="2564a-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="2564a-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-190">The publishing state for the app.</span></span> <span data-ttu-id="2564a-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="2564a-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="2564a-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="2564a-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="2564a-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="2564a-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="2564a-194">committedContentVersion</span></span>|<span data-ttu-id="2564a-195">String</span><span class="sxs-lookup"><span data-stu-id="2564a-195">String</span></span>|<span data-ttu-id="2564a-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="2564a-196">The internal committed content version.</span></span> <span data-ttu-id="2564a-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2564a-198">fileName</span><span class="sxs-lookup"><span data-stu-id="2564a-198">fileName</span></span>|<span data-ttu-id="2564a-199">String</span><span class="sxs-lookup"><span data-stu-id="2564a-199">String</span></span>|<span data-ttu-id="2564a-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="2564a-200">The name of the main Lob application file.</span></span> <span data-ttu-id="2564a-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2564a-202">size</span><span class="sxs-lookup"><span data-stu-id="2564a-202">size</span></span>|<span data-ttu-id="2564a-203">Int64</span><span class="sxs-lookup"><span data-stu-id="2564a-203">Int64</span></span>|<span data-ttu-id="2564a-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="2564a-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="2564a-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2564a-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2564a-206">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="2564a-206">applicableArchitectures</span></span>|[<span data-ttu-id="2564a-207">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="2564a-207">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="2564a-208">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2564a-208">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="2564a-209">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="2564a-209">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="2564a-210">identityName</span><span class="sxs-lookup"><span data-stu-id="2564a-210">identityName</span></span>|<span data-ttu-id="2564a-211">String</span><span class="sxs-lookup"><span data-stu-id="2564a-211">String</span></span>|<span data-ttu-id="2564a-212">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="2564a-212">The Identity Name.</span></span>|
|<span data-ttu-id="2564a-213">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="2564a-213">identityPublisherHash</span></span>|<span data-ttu-id="2564a-214">String</span><span class="sxs-lookup"><span data-stu-id="2564a-214">String</span></span>|<span data-ttu-id="2564a-215">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="2564a-215">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="2564a-216">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="2564a-216">identityResourceIdentifier</span></span>|<span data-ttu-id="2564a-217">String</span><span class="sxs-lookup"><span data-stu-id="2564a-217">String</span></span>|<span data-ttu-id="2564a-218">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="2564a-218">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="2564a-219">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2564a-219">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="2564a-220">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2564a-220">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="2564a-221">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="2564a-221">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="2564a-222">phoneProductIdentifier</span><span class="sxs-lookup"><span data-stu-id="2564a-222">phoneProductIdentifier</span></span>|<span data-ttu-id="2564a-223">String</span><span class="sxs-lookup"><span data-stu-id="2564a-223">String</span></span>|<span data-ttu-id="2564a-224">El identificador de producto del teléfono.</span><span class="sxs-lookup"><span data-stu-id="2564a-224">The Phone Product Identifier.</span></span>|
|<span data-ttu-id="2564a-225">phonePublisherId</span><span class="sxs-lookup"><span data-stu-id="2564a-225">phonePublisherId</span></span>|<span data-ttu-id="2564a-226">String</span><span class="sxs-lookup"><span data-stu-id="2564a-226">String</span></span>|<span data-ttu-id="2564a-227">El identificador de Publisher de teléfono.</span><span class="sxs-lookup"><span data-stu-id="2564a-227">The Phone Publisher Id.</span></span>|
|<span data-ttu-id="2564a-228">identityVersion</span><span class="sxs-lookup"><span data-stu-id="2564a-228">identityVersion</span></span>|<span data-ttu-id="2564a-229">String</span><span class="sxs-lookup"><span data-stu-id="2564a-229">String</span></span>|<span data-ttu-id="2564a-230">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="2564a-230">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="2564a-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2564a-231">Response</span></span>
<span data-ttu-id="2564a-232">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2564a-232">If successful, this method returns a `201 Created` response code and a [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2564a-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2564a-233">Example</span></span>
### <a name="request"></a><span data-ttu-id="2564a-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2564a-234">Request</span></span>
<span data-ttu-id="2564a-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2564a-235">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1419

{
  "@odata.type": "#microsoft.graph.windowsPhone81AppX",
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
  "applicableArchitectures": "x86",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
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
  "phoneProductIdentifier": "Phone Product Identifier value",
  "phonePublisherId": "Phone Publisher Id value",
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="2564a-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2564a-236">Response</span></span>
<span data-ttu-id="2564a-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2564a-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1527

{
  "@odata.type": "#microsoft.graph.windowsPhone81AppX",
  "id": "4ff27f80-7f80-4ff2-807f-f24f807ff24f",
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
  "applicableArchitectures": "x86",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
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
  "phoneProductIdentifier": "Phone Product Identifier value",
  "phonePublisherId": "Phone Publisher Id value",
  "identityVersion": "Identity Version value"
}
```




