---
title: Crear windows10SecureAssessmentConfiguration
description: Crear un objeto windows10SecureAssessmentConfiguration.
ms.openlocfilehash: 48c58c785740307ffaa42ca2e21c23270422e684
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029805"
---
# <a name="create-windows10secureassessmentconfiguration"></a><span data-ttu-id="a8906-103">Crear windows10SecureAssessmentConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8906-103">Create windows10SecureAssessmentConfiguration</span></span>

> <span data-ttu-id="a8906-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a8906-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a8906-105">Crear un objeto [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a8906-105">Create a new [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a8906-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a8906-106">Prerequisites</span></span>
<span data-ttu-id="a8906-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a8906-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a8906-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8906-109">Permission type</span></span>|<span data-ttu-id="a8906-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8906-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a8906-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8906-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a8906-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a8906-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a8906-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8906-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a8906-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8906-114">Not supported.</span></span>|
|<span data-ttu-id="a8906-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8906-115">Application</span></span>|<span data-ttu-id="a8906-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8906-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a8906-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8906-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a8906-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8906-118">Request headers</span></span>
|<span data-ttu-id="a8906-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8906-119">Header</span></span>|<span data-ttu-id="a8906-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a8906-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a8906-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a8906-121">Authorization</span></span>|<span data-ttu-id="a8906-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a8906-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a8906-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a8906-123">Accept</span></span>|<span data-ttu-id="a8906-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a8906-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a8906-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a8906-125">Request body</span></span>
<span data-ttu-id="a8906-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10SecureAssessmentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a8906-126">In the request body, supply a JSON representation for the windows10SecureAssessmentConfiguration object.</span></span>

<span data-ttu-id="a8906-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10SecureAssessmentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a8906-127">The following table shows the properties that are required when you create the windows10SecureAssessmentConfiguration.</span></span>

|<span data-ttu-id="a8906-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8906-128">Property</span></span>|<span data-ttu-id="a8906-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8906-129">Type</span></span>|<span data-ttu-id="a8906-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8906-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a8906-131">id</span><span class="sxs-lookup"><span data-stu-id="a8906-131">id</span></span>|<span data-ttu-id="a8906-132">String</span><span class="sxs-lookup"><span data-stu-id="a8906-132">String</span></span>|<span data-ttu-id="a8906-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a8906-133">Key of the entity.</span></span> <span data-ttu-id="a8906-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a8906-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a8906-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a8906-135">lastModifiedDateTime</span></span>|<span data-ttu-id="a8906-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a8906-136">DateTimeOffset</span></span>|<span data-ttu-id="a8906-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a8906-137">DateTime the object was last modified.</span></span> <span data-ttu-id="a8906-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a8906-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a8906-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a8906-139">createdDateTime</span></span>|<span data-ttu-id="a8906-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a8906-140">DateTimeOffset</span></span>|<span data-ttu-id="a8906-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a8906-141">DateTime the object was created.</span></span> <span data-ttu-id="a8906-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a8906-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a8906-143">descripción</span><span class="sxs-lookup"><span data-stu-id="a8906-143">description</span></span>|<span data-ttu-id="a8906-144">String</span><span class="sxs-lookup"><span data-stu-id="a8906-144">String</span></span>|<span data-ttu-id="a8906-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8906-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a8906-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a8906-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a8906-147">displayName</span><span class="sxs-lookup"><span data-stu-id="a8906-147">displayName</span></span>|<span data-ttu-id="a8906-148">String</span><span class="sxs-lookup"><span data-stu-id="a8906-148">String</span></span>|<span data-ttu-id="a8906-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8906-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a8906-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a8906-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a8906-151">version</span><span class="sxs-lookup"><span data-stu-id="a8906-151">version</span></span>|<span data-ttu-id="a8906-152">Int32</span><span class="sxs-lookup"><span data-stu-id="a8906-152">Int32</span></span>|<span data-ttu-id="a8906-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8906-153">Version of the device configuration.</span></span> <span data-ttu-id="a8906-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a8906-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a8906-155">launchUri</span><span class="sxs-lookup"><span data-stu-id="a8906-155">launchUri</span></span>|<span data-ttu-id="a8906-156">String</span><span class="sxs-lookup"><span data-stu-id="a8906-156">String</span></span>|<span data-ttu-id="a8906-157">Vínculo de dirección URL a una evaluación que se carga automáticamente al iniciar el explorador de evaluaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="a8906-157">Url link to an assessment that's automatically loaded when the secure assessment browser is launched.</span></span> <span data-ttu-id="a8906-158">Tiene que ser una dirección URL válida (http\[s\]://msdn.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a8906-158">It has to be a valid Url (http\[s\]://msdn.microsoft.com/).</span></span>|
|<span data-ttu-id="a8906-159">configurationAccount</span><span class="sxs-lookup"><span data-stu-id="a8906-159">configurationAccount</span></span>|<span data-ttu-id="a8906-160">String</span><span class="sxs-lookup"><span data-stu-id="a8906-160">String</span></span>|<span data-ttu-id="a8906-161">Cuenta usada al configurar el dispositivo Windows para realizar la prueba.</span><span class="sxs-lookup"><span data-stu-id="a8906-161">The account used to configure the Windows device for taking the test.</span></span> <span data-ttu-id="a8906-162">El usuario puede ser una cuenta de dominio (dominio\usuario), una cuenta de AAD (nombredeusuario@espacioempresarial.com) o una cuenta local (nombredeusuario).</span><span class="sxs-lookup"><span data-stu-id="a8906-162">The user can be a domain account (domain\user), an AAD account (username@tenant.com) or a local account (username).</span></span>|
|<span data-ttu-id="a8906-163">allowPrinting</span><span class="sxs-lookup"><span data-stu-id="a8906-163">allowPrinting</span></span>|<span data-ttu-id="a8906-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="a8906-164">Boolean</span></span>|<span data-ttu-id="a8906-165">Indica si se va a permitir que la aplicación imprima durante la prueba.</span><span class="sxs-lookup"><span data-stu-id="a8906-165">Indicates whether or not to allow the app from printing during the test.</span></span>|
|<span data-ttu-id="a8906-166">allowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="a8906-166">allowScreenCapture</span></span>|<span data-ttu-id="a8906-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="a8906-167">Boolean</span></span>|<span data-ttu-id="a8906-168">Indica si se va a permitir la funcionalidad de captura de pantalla durante una prueba.</span><span class="sxs-lookup"><span data-stu-id="a8906-168">Indicates whether or not to allow screen capture capability during a test.</span></span>|
|<span data-ttu-id="a8906-169">allowTextSuggestion</span><span class="sxs-lookup"><span data-stu-id="a8906-169">allowTextSuggestion</span></span>|<span data-ttu-id="a8906-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="a8906-170">Boolean</span></span>|<span data-ttu-id="a8906-171">Indica si se van a permitir las sugerencias de texto durante la prueba.</span><span class="sxs-lookup"><span data-stu-id="a8906-171">Indicates whether or not to allow text suggestions during the test.</span></span>|



## <a name="response"></a><span data-ttu-id="a8906-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8906-172">Response</span></span>
<span data-ttu-id="a8906-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8906-173">If successful, this method returns a `201 Created` response code and a [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a8906-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8906-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="a8906-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8906-175">Request</span></span>
<span data-ttu-id="a8906-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8906-176">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 359

{
  "@odata.type": "#microsoft.graph.windows10SecureAssessmentConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "launchUri": "Launch Uri value",
  "configurationAccount": "Configuration Account value",
  "allowPrinting": true,
  "allowScreenCapture": true,
  "allowTextSuggestion": true
}
```

### <a name="response"></a><span data-ttu-id="a8906-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8906-177">Response</span></span>
<span data-ttu-id="a8906-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a8906-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 531

{
  "@odata.type": "#microsoft.graph.windows10SecureAssessmentConfiguration",
  "id": "f60d71be-71be-f60d-be71-0df6be710df6",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "launchUri": "Launch Uri value",
  "configurationAccount": "Configuration Account value",
  "allowPrinting": true,
  "allowScreenCapture": true,
  "allowTextSuggestion": true
}
```


