---
title: Crear windows10EnrollmentCompletionPageConfiguration
description: Crear un nuevo objeto windows10EnrollmentCompletionPageConfiguration.
ms.openlocfilehash: db276cefec8a764b2ad2ddcade93bae7a518f264
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083710"
---
# <a name="create-windows10enrollmentcompletionpageconfiguration"></a><span data-ttu-id="9736b-103">Crear windows10EnrollmentCompletionPageConfiguration</span><span class="sxs-lookup"><span data-stu-id="9736b-103">Create windows10EnrollmentCompletionPageConfiguration</span></span>

> <span data-ttu-id="9736b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9736b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9736b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9736b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9736b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9736b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9736b-107">Crear un nuevo objeto [windows10EnrollmentCompletionPageConfiguration](../resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="9736b-107">Create a new [windows10EnrollmentCompletionPageConfiguration](../resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9736b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9736b-108">Prerequisites</span></span>
<span data-ttu-id="9736b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9736b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9736b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9736b-111">Permission type</span></span>|<span data-ttu-id="9736b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9736b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9736b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9736b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9736b-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9736b-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="9736b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9736b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9736b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9736b-116">Not supported.</span></span>|
|<span data-ttu-id="9736b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9736b-117">Application</span></span>|<span data-ttu-id="9736b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9736b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9736b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9736b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9736b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9736b-120">Request headers</span></span>
|<span data-ttu-id="9736b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9736b-121">Header</span></span>|<span data-ttu-id="9736b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9736b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9736b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9736b-123">Authorization</span></span>|<span data-ttu-id="9736b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9736b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9736b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9736b-125">Accept</span></span>|<span data-ttu-id="9736b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9736b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9736b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9736b-127">Request body</span></span>
<span data-ttu-id="9736b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windows10EnrollmentCompletionPageConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9736b-128">In the request body, supply a JSON representation for the windows10EnrollmentCompletionPageConfiguration object.</span></span>

<span data-ttu-id="9736b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windows10EnrollmentCompletionPageConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9736b-129">The following table shows the properties that are required when you create the windows10EnrollmentCompletionPageConfiguration.</span></span>

|<span data-ttu-id="9736b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9736b-130">Property</span></span>|<span data-ttu-id="9736b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9736b-131">Type</span></span>|<span data-ttu-id="9736b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9736b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9736b-133">id</span><span class="sxs-lookup"><span data-stu-id="9736b-133">id</span></span>|<span data-ttu-id="9736b-134">String</span><span class="sxs-lookup"><span data-stu-id="9736b-134">String</span></span>|<span data-ttu-id="9736b-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-136">displayName</span><span class="sxs-lookup"><span data-stu-id="9736b-136">displayName</span></span>|<span data-ttu-id="9736b-137">String</span><span class="sxs-lookup"><span data-stu-id="9736b-137">String</span></span>|<span data-ttu-id="9736b-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-139">descripción</span><span class="sxs-lookup"><span data-stu-id="9736b-139">description</span></span>|<span data-ttu-id="9736b-140">String</span><span class="sxs-lookup"><span data-stu-id="9736b-140">String</span></span>|<span data-ttu-id="9736b-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="9736b-142">priority</span></span>|<span data-ttu-id="9736b-143">Int32</span><span class="sxs-lookup"><span data-stu-id="9736b-143">Int32</span></span>|<span data-ttu-id="9736b-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9736b-145">createdDateTime</span></span>|<span data-ttu-id="9736b-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9736b-146">DateTimeOffset</span></span>|<span data-ttu-id="9736b-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9736b-148">lastModifiedDateTime</span></span>|<span data-ttu-id="9736b-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9736b-149">DateTimeOffset</span></span>|<span data-ttu-id="9736b-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-151">version</span><span class="sxs-lookup"><span data-stu-id="9736b-151">version</span></span>|<span data-ttu-id="9736b-152">Int32</span><span class="sxs-lookup"><span data-stu-id="9736b-152">Int32</span></span>|<span data-ttu-id="9736b-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9736b-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9736b-154">showInstallationProgress</span><span class="sxs-lookup"><span data-stu-id="9736b-154">showInstallationProgress</span></span>|<span data-ttu-id="9736b-155">Booleano</span><span class="sxs-lookup"><span data-stu-id="9736b-155">Boolean</span></span>|<span data-ttu-id="9736b-156">Mostrar u ocultar el progreso de la instalación para el usuario</span><span class="sxs-lookup"><span data-stu-id="9736b-156">Show or hide installation progress to user</span></span>|
|<span data-ttu-id="9736b-157">blockDeviceSetupRetryByUser</span><span class="sxs-lookup"><span data-stu-id="9736b-157">blockDeviceSetupRetryByUser</span></span>|<span data-ttu-id="9736b-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="9736b-158">Boolean</span></span>|<span data-ttu-id="9736b-159">Permitir al usuario que vuelva a intentar la instalación en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="9736b-159">Allow the user to retry the setup on installation failure</span></span>|
|<span data-ttu-id="9736b-160">allowDeviceResetOnInstallFailure</span><span class="sxs-lookup"><span data-stu-id="9736b-160">allowDeviceResetOnInstallFailure</span></span>|<span data-ttu-id="9736b-161">Booleano</span><span class="sxs-lookup"><span data-stu-id="9736b-161">Boolean</span></span>|<span data-ttu-id="9736b-162">Permitir o bloquear el dispositivo restablecer en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="9736b-162">Allow or block device reset on installation failure</span></span>|
|<span data-ttu-id="9736b-163">allowLogCollectionOnInstallFailure</span><span class="sxs-lookup"><span data-stu-id="9736b-163">allowLogCollectionOnInstallFailure</span></span>|<span data-ttu-id="9736b-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="9736b-164">Boolean</span></span>|<span data-ttu-id="9736b-165">Permitir o bloquear registro colección en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="9736b-165">Allow or block log collection on installation failure</span></span>|
|<span data-ttu-id="9736b-166">customErrorMessage</span><span class="sxs-lookup"><span data-stu-id="9736b-166">customErrorMessage</span></span>|<span data-ttu-id="9736b-167">String</span><span class="sxs-lookup"><span data-stu-id="9736b-167">String</span></span>|<span data-ttu-id="9736b-168">Establecer el mensaje de error personalizado para mostrar al producirse un error de instalación</span><span class="sxs-lookup"><span data-stu-id="9736b-168">Set custom error message to show upon installation failure</span></span>|
|<span data-ttu-id="9736b-169">installProgressTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9736b-169">installProgressTimeoutInMinutes</span></span>|<span data-ttu-id="9736b-170">Int32</span><span class="sxs-lookup"><span data-stu-id="9736b-170">Int32</span></span>|<span data-ttu-id="9736b-171">Establecer tiempo de espera de progreso de la instalación en minutos</span><span class="sxs-lookup"><span data-stu-id="9736b-171">Set installation progress timeout in minutes</span></span>|
|<span data-ttu-id="9736b-172">allowDeviceUseOnInstallFailure</span><span class="sxs-lookup"><span data-stu-id="9736b-172">allowDeviceUseOnInstallFailure</span></span>|<span data-ttu-id="9736b-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="9736b-173">Boolean</span></span>|<span data-ttu-id="9736b-174">Permitir que el usuario continuar utilizando el dispositivo en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="9736b-174">Allow the user to continue using the device on installation failure</span></span>|
|<span data-ttu-id="9736b-175">selectedMobileAppIds</span><span class="sxs-lookup"><span data-stu-id="9736b-175">selectedMobileAppIds</span></span>|<span data-ttu-id="9736b-176">Colección String</span><span class="sxs-lookup"><span data-stu-id="9736b-176">String collection</span></span>|<span data-ttu-id="9736b-177">Aplicaciones seleccionadas para realizar un seguimiento del estado de la instalación</span><span class="sxs-lookup"><span data-stu-id="9736b-177">Selected applications to track the installation status</span></span>|



## <a name="response"></a><span data-ttu-id="9736b-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9736b-178">Response</span></span>
<span data-ttu-id="9736b-179">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windows10EnrollmentCompletionPageConfiguration](../resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9736b-179">If successful, this method returns a `201 Created` response code and a [windows10EnrollmentCompletionPageConfiguration](../resources/intune-onboarding-windows10enrollmentcompletionpageconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9736b-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9736b-180">Example</span></span>
### <a name="request"></a><span data-ttu-id="9736b-181">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9736b-181">Request</span></span>
<span data-ttu-id="9736b-182">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9736b-182">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 647

{
  "@odata.type": "#microsoft.graph.windows10EnrollmentCompletionPageConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "showInstallationProgress": true,
  "blockDeviceSetupRetryByUser": true,
  "allowDeviceResetOnInstallFailure": true,
  "allowLogCollectionOnInstallFailure": true,
  "customErrorMessage": "Custom Error Message value",
  "installProgressTimeoutInMinutes": 15,
  "allowDeviceUseOnInstallFailure": true,
  "selectedMobileAppIds": [
    "Selected Mobile App Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="9736b-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9736b-183">Response</span></span>
<span data-ttu-id="9736b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9736b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 755

{
  "@odata.type": "#microsoft.graph.windows10EnrollmentCompletionPageConfiguration",
  "id": "77bf8248-8248-77bf-4882-bf774882bf77",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "showInstallationProgress": true,
  "blockDeviceSetupRetryByUser": true,
  "allowDeviceResetOnInstallFailure": true,
  "allowLogCollectionOnInstallFailure": true,
  "customErrorMessage": "Custom Error Message value",
  "installProgressTimeoutInMinutes": 15,
  "allowDeviceUseOnInstallFailure": true,
  "selectedMobileAppIds": [
    "Selected Mobile App Ids value"
  ]
}
```




