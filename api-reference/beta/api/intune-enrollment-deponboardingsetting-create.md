---
title: Crear depOnboardingSetting
description: Crear un nuevo objeto depOnboardingSetting.
ms.openlocfilehash: 612afd3111af00cc8fd9819017b272ce5a38fe4d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090482"
---
# <a name="create-deponboardingsetting"></a><span data-ttu-id="0133c-103">Crear depOnboardingSetting</span><span class="sxs-lookup"><span data-stu-id="0133c-103">Create depOnboardingSetting</span></span>

> <span data-ttu-id="0133c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0133c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0133c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0133c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0133c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0133c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0133c-107">Crear un nuevo objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="0133c-107">Create a new [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0133c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0133c-108">Prerequisites</span></span>
<span data-ttu-id="0133c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0133c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0133c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0133c-111">Permission type</span></span>|<span data-ttu-id="0133c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0133c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0133c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0133c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0133c-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0133c-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="0133c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0133c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0133c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0133c-116">Not supported.</span></span>|
|<span data-ttu-id="0133c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0133c-117">Application</span></span>|<span data-ttu-id="0133c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0133c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0133c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0133c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings
```

## <a name="request-headers"></a><span data-ttu-id="0133c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0133c-120">Request headers</span></span>
|<span data-ttu-id="0133c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0133c-121">Header</span></span>|<span data-ttu-id="0133c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0133c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0133c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0133c-123">Authorization</span></span>|<span data-ttu-id="0133c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0133c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0133c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0133c-125">Accept</span></span>|<span data-ttu-id="0133c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0133c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0133c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0133c-127">Request body</span></span>
<span data-ttu-id="0133c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto depOnboardingSetting.</span><span class="sxs-lookup"><span data-stu-id="0133c-128">In the request body, supply a JSON representation for the depOnboardingSetting object.</span></span>

<span data-ttu-id="0133c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el depOnboardingSetting.</span><span class="sxs-lookup"><span data-stu-id="0133c-129">The following table shows the properties that are required when you create the depOnboardingSetting.</span></span>

|<span data-ttu-id="0133c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0133c-130">Property</span></span>|<span data-ttu-id="0133c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0133c-131">Type</span></span>|<span data-ttu-id="0133c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0133c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0133c-133">id</span><span class="sxs-lookup"><span data-stu-id="0133c-133">id</span></span>|<span data-ttu-id="0133c-134">String</span><span class="sxs-lookup"><span data-stu-id="0133c-134">String</span></span>|<span data-ttu-id="0133c-135">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="0133c-135">UUID for the object</span></span>|
|<span data-ttu-id="0133c-136">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="0133c-136">appleIdentifier</span></span>|<span data-ttu-id="0133c-137">String</span><span class="sxs-lookup"><span data-stu-id="0133c-137">String</span></span>|<span data-ttu-id="0133c-138">El identificador de Apple se utiliza para obtener el token actual.</span><span class="sxs-lookup"><span data-stu-id="0133c-138">The Apple ID used to obtain the current token.</span></span>|
|<span data-ttu-id="0133c-139">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="0133c-139">tokenExpirationDateTime</span></span>|<span data-ttu-id="0133c-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0133c-140">DateTimeOffset</span></span>|<span data-ttu-id="0133c-141">Cuando caduca el token.</span><span class="sxs-lookup"><span data-stu-id="0133c-141">When the token will expire.</span></span>|
|<span data-ttu-id="0133c-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0133c-142">lastModifiedDateTime</span></span>|<span data-ttu-id="0133c-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0133c-143">DateTimeOffset</span></span>|<span data-ttu-id="0133c-144">Cuando el servicio fue onboarded.</span><span class="sxs-lookup"><span data-stu-id="0133c-144">When the service was onboarded.</span></span>|
|<span data-ttu-id="0133c-145">lastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="0133c-145">lastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="0133c-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0133c-146">DateTimeOffset</span></span>|<span data-ttu-id="0133c-147">Cuando el syned último servicio con Intune</span><span class="sxs-lookup"><span data-stu-id="0133c-147">When the service last syned with Intune</span></span>|
|<span data-ttu-id="0133c-148">lastSyncTriggeredDateTime</span><span class="sxs-lookup"><span data-stu-id="0133c-148">lastSyncTriggeredDateTime</span></span>|<span data-ttu-id="0133c-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0133c-149">DateTimeOffset</span></span>|<span data-ttu-id="0133c-150">Cuando Intune solicitada por última vez una sincronización.</span><span class="sxs-lookup"><span data-stu-id="0133c-150">When Intune last requested a sync.</span></span>|
|<span data-ttu-id="0133c-151">shareTokenWithSchoolDataSyncService</span><span class="sxs-lookup"><span data-stu-id="0133c-151">shareTokenWithSchoolDataSyncService</span></span>|<span data-ttu-id="0133c-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="0133c-152">Boolean</span></span>|<span data-ttu-id="0133c-153">Si el símbolo (token) de la característica Dep compartir está habilitada o no con el servicio de sincronización de datos de School.</span><span class="sxs-lookup"><span data-stu-id="0133c-153">Whether or not the Dep token sharing is enabled with the School Data Sync service.</span></span>|
|<span data-ttu-id="0133c-154">lastSyncErrorCode</span><span class="sxs-lookup"><span data-stu-id="0133c-154">lastSyncErrorCode</span></span>|<span data-ttu-id="0133c-155">Int32</span><span class="sxs-lookup"><span data-stu-id="0133c-155">Int32</span></span>|<span data-ttu-id="0133c-156">Código de error que informa Apple durante la última sincronización de la característica dep.</span><span class="sxs-lookup"><span data-stu-id="0133c-156">Error code reported by Apple during last dep sync.</span></span>|
|<span data-ttu-id="0133c-157">TokenType en</span><span class="sxs-lookup"><span data-stu-id="0133c-157">tokenType</span></span>|[<span data-ttu-id="0133c-158">depTokenType</span><span class="sxs-lookup"><span data-stu-id="0133c-158">depTokenType</span></span>](../resources/intune-enrollment-deptokentype.md)|<span data-ttu-id="0133c-159">Obtiene o establece el tipo de símbolo (token) de la característica Dep.</span><span class="sxs-lookup"><span data-stu-id="0133c-159">Gets or sets the Dep Token Type.</span></span> <span data-ttu-id="0133c-160">Los valores posibles son: `none`, `dep` y `appleSchoolManager`.</span><span class="sxs-lookup"><span data-stu-id="0133c-160">Possible values are: `none`, `dep`, `appleSchoolManager`.</span></span>|
|<span data-ttu-id="0133c-161">tokenName</span><span class="sxs-lookup"><span data-stu-id="0133c-161">tokenName</span></span>|<span data-ttu-id="0133c-162">String</span><span class="sxs-lookup"><span data-stu-id="0133c-162">String</span></span>|<span data-ttu-id="0133c-163">Nombre descriptivo para la característica Dep símbolo (token)</span><span class="sxs-lookup"><span data-stu-id="0133c-163">Friendly Name for Dep Token</span></span>|
|<span data-ttu-id="0133c-164">syncedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0133c-164">syncedDeviceCount</span></span>|<span data-ttu-id="0133c-165">Int32</span><span class="sxs-lookup"><span data-stu-id="0133c-165">Int32</span></span>|<span data-ttu-id="0133c-166">Obtiene sincronizado recuento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0133c-166">Gets synced device count</span></span>|
|<span data-ttu-id="0133c-167">defaultProfileDisplayName</span><span class="sxs-lookup"><span data-stu-id="0133c-167">defaultProfileDisplayName</span></span>|<span data-ttu-id="0133c-168">String</span><span class="sxs-lookup"><span data-stu-id="0133c-168">String</span></span>|<span data-ttu-id="0133c-169">Obtiene sincronizado recuento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0133c-169">Gets synced device count</span></span>|
|<span data-ttu-id="0133c-170">dataSharingConsentGranted</span><span class="sxs-lookup"><span data-stu-id="0133c-170">dataSharingConsentGranted</span></span>|<span data-ttu-id="0133c-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="0133c-171">Boolean</span></span>|<span data-ttu-id="0133c-172">Concede de consentimiento para uso compartido con Apple Dep servicio de datos</span><span class="sxs-lookup"><span data-stu-id="0133c-172">Consent granted for data sharing with Apple Dep Service</span></span>|



## <a name="response"></a><span data-ttu-id="0133c-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0133c-173">Response</span></span>
<span data-ttu-id="0133c-174">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0133c-174">If successful, this method returns a `201 Created` response code and a [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0133c-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0133c-175">Example</span></span>
### <a name="request"></a><span data-ttu-id="0133c-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0133c-176">Request</span></span>
<span data-ttu-id="0133c-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0133c-177">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings
Content-type: application/json
Content-length: 648

{
  "@odata.type": "#microsoft.graph.depOnboardingSetting",
  "appleIdentifier": "Apple Identifier value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastSuccessfulSyncDateTime": "2017-01-01T00:03:28.120883-08:00",
  "lastSyncTriggeredDateTime": "2017-01-01T00:00:02.0916369-08:00",
  "shareTokenWithSchoolDataSyncService": true,
  "lastSyncErrorCode": 1,
  "tokenType": "dep",
  "tokenName": "Token Name value",
  "syncedDeviceCount": 1,
  "defaultProfileDisplayName": "Default Profile Display Name value",
  "dataSharingConsentGranted": true
}
```

### <a name="response"></a><span data-ttu-id="0133c-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0133c-178">Response</span></span>
<span data-ttu-id="0133c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0133c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 697

{
  "@odata.type": "#microsoft.graph.depOnboardingSetting",
  "id": "40342229-2229-4034-2922-344029223440",
  "appleIdentifier": "Apple Identifier value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastSuccessfulSyncDateTime": "2017-01-01T00:03:28.120883-08:00",
  "lastSyncTriggeredDateTime": "2017-01-01T00:00:02.0916369-08:00",
  "shareTokenWithSchoolDataSyncService": true,
  "lastSyncErrorCode": 1,
  "tokenType": "dep",
  "tokenName": "Token Name value",
  "syncedDeviceCount": 1,
  "defaultProfileDisplayName": "Default Profile Display Name value",
  "dataSharingConsentGranted": true
}
```





