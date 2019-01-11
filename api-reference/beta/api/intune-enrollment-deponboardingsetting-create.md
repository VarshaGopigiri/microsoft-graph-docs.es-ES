---
title: Crear depOnboardingSetting
description: Crear un nuevo objeto depOnboardingSetting.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 89e46c715b5f888ae3c9f1fb02a0566da8485944
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854904"
---
# <a name="create-deponboardingsetting"></a><span data-ttu-id="77bf5-103">Crear depOnboardingSetting</span><span class="sxs-lookup"><span data-stu-id="77bf5-103">Create depOnboardingSetting</span></span>

> <span data-ttu-id="77bf5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77bf5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77bf5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77bf5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="77bf5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="77bf5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="77bf5-107">Crear un nuevo objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="77bf5-107">Create a new [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="77bf5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="77bf5-108">Prerequisites</span></span>
<span data-ttu-id="77bf5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77bf5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77bf5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77bf5-111">Permission type</span></span>|<span data-ttu-id="77bf5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77bf5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="77bf5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77bf5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="77bf5-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77bf5-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="77bf5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77bf5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="77bf5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77bf5-116">Not supported.</span></span>|
|<span data-ttu-id="77bf5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77bf5-117">Application</span></span>|<span data-ttu-id="77bf5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77bf5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="77bf5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77bf5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings
```

## <a name="request-headers"></a><span data-ttu-id="77bf5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77bf5-120">Request headers</span></span>
|<span data-ttu-id="77bf5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77bf5-121">Header</span></span>|<span data-ttu-id="77bf5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="77bf5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="77bf5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="77bf5-123">Authorization</span></span>|<span data-ttu-id="77bf5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="77bf5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="77bf5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="77bf5-125">Accept</span></span>|<span data-ttu-id="77bf5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="77bf5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="77bf5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77bf5-127">Request body</span></span>
<span data-ttu-id="77bf5-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto depOnboardingSetting.</span><span class="sxs-lookup"><span data-stu-id="77bf5-128">In the request body, supply a JSON representation for the depOnboardingSetting object.</span></span>

<span data-ttu-id="77bf5-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el depOnboardingSetting.</span><span class="sxs-lookup"><span data-stu-id="77bf5-129">The following table shows the properties that are required when you create the depOnboardingSetting.</span></span>

|<span data-ttu-id="77bf5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77bf5-130">Property</span></span>|<span data-ttu-id="77bf5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="77bf5-131">Type</span></span>|<span data-ttu-id="77bf5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="77bf5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="77bf5-133">id</span><span class="sxs-lookup"><span data-stu-id="77bf5-133">id</span></span>|<span data-ttu-id="77bf5-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="77bf5-134">String</span></span>|<span data-ttu-id="77bf5-135">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="77bf5-135">UUID for the object</span></span>|
|<span data-ttu-id="77bf5-136">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="77bf5-136">appleIdentifier</span></span>|<span data-ttu-id="77bf5-137">String</span><span class="sxs-lookup"><span data-stu-id="77bf5-137">String</span></span>|<span data-ttu-id="77bf5-138">El identificador de Apple se utiliza para obtener el token actual.</span><span class="sxs-lookup"><span data-stu-id="77bf5-138">The Apple ID used to obtain the current token.</span></span>|
|<span data-ttu-id="77bf5-139">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="77bf5-139">tokenExpirationDateTime</span></span>|<span data-ttu-id="77bf5-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77bf5-140">DateTimeOffset</span></span>|<span data-ttu-id="77bf5-141">Cuando caduca el token.</span><span class="sxs-lookup"><span data-stu-id="77bf5-141">When the token will expire.</span></span>|
|<span data-ttu-id="77bf5-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="77bf5-142">lastModifiedDateTime</span></span>|<span data-ttu-id="77bf5-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77bf5-143">DateTimeOffset</span></span>|<span data-ttu-id="77bf5-144">Cuando el servicio fue onboarded.</span><span class="sxs-lookup"><span data-stu-id="77bf5-144">When the service was onboarded.</span></span>|
|<span data-ttu-id="77bf5-145">lastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="77bf5-145">lastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="77bf5-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77bf5-146">DateTimeOffset</span></span>|<span data-ttu-id="77bf5-147">Cuando el syned último servicio con Intune</span><span class="sxs-lookup"><span data-stu-id="77bf5-147">When the service last syned with Intune</span></span>|
|<span data-ttu-id="77bf5-148">lastSyncTriggeredDateTime</span><span class="sxs-lookup"><span data-stu-id="77bf5-148">lastSyncTriggeredDateTime</span></span>|<span data-ttu-id="77bf5-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77bf5-149">DateTimeOffset</span></span>|<span data-ttu-id="77bf5-150">Cuando Intune solicitada por última vez una sincronización.</span><span class="sxs-lookup"><span data-stu-id="77bf5-150">When Intune last requested a sync.</span></span>|
|<span data-ttu-id="77bf5-151">shareTokenWithSchoolDataSyncService</span><span class="sxs-lookup"><span data-stu-id="77bf5-151">shareTokenWithSchoolDataSyncService</span></span>|<span data-ttu-id="77bf5-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="77bf5-152">Boolean</span></span>|<span data-ttu-id="77bf5-153">Si el símbolo (token) de la característica Dep compartir está habilitada o no con el servicio de sincronización de datos de School.</span><span class="sxs-lookup"><span data-stu-id="77bf5-153">Whether or not the Dep token sharing is enabled with the School Data Sync service.</span></span>|
|<span data-ttu-id="77bf5-154">lastSyncErrorCode</span><span class="sxs-lookup"><span data-stu-id="77bf5-154">lastSyncErrorCode</span></span>|<span data-ttu-id="77bf5-155">Int32</span><span class="sxs-lookup"><span data-stu-id="77bf5-155">Int32</span></span>|<span data-ttu-id="77bf5-156">Código de error que informa Apple durante la última sincronización de la característica dep.</span><span class="sxs-lookup"><span data-stu-id="77bf5-156">Error code reported by Apple during last dep sync.</span></span>|
|<span data-ttu-id="77bf5-157">TokenType en</span><span class="sxs-lookup"><span data-stu-id="77bf5-157">tokenType</span></span>|[<span data-ttu-id="77bf5-158">depTokenType</span><span class="sxs-lookup"><span data-stu-id="77bf5-158">depTokenType</span></span>](../resources/intune-enrollment-deptokentype.md)|<span data-ttu-id="77bf5-159">Obtiene o establece el tipo de símbolo (token) de la característica Dep.</span><span class="sxs-lookup"><span data-stu-id="77bf5-159">Gets or sets the Dep Token Type.</span></span> <span data-ttu-id="77bf5-160">Los valores posibles son: `none`, `dep` y `appleSchoolManager`.</span><span class="sxs-lookup"><span data-stu-id="77bf5-160">Possible values are: `none`, `dep`, `appleSchoolManager`.</span></span>|
|<span data-ttu-id="77bf5-161">tokenName</span><span class="sxs-lookup"><span data-stu-id="77bf5-161">tokenName</span></span>|<span data-ttu-id="77bf5-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="77bf5-162">String</span></span>|<span data-ttu-id="77bf5-163">Nombre descriptivo para la característica Dep símbolo (token)</span><span class="sxs-lookup"><span data-stu-id="77bf5-163">Friendly Name for Dep Token</span></span>|
|<span data-ttu-id="77bf5-164">syncedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="77bf5-164">syncedDeviceCount</span></span>|<span data-ttu-id="77bf5-165">Int32</span><span class="sxs-lookup"><span data-stu-id="77bf5-165">Int32</span></span>|<span data-ttu-id="77bf5-166">Obtiene sincronizado recuento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="77bf5-166">Gets synced device count</span></span>|
|<span data-ttu-id="77bf5-167">defaultProfileDisplayName</span><span class="sxs-lookup"><span data-stu-id="77bf5-167">defaultProfileDisplayName</span></span>|<span data-ttu-id="77bf5-168">Cadena</span><span class="sxs-lookup"><span data-stu-id="77bf5-168">String</span></span>|<span data-ttu-id="77bf5-169">Obtiene sincronizado recuento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="77bf5-169">Gets synced device count</span></span>|
|<span data-ttu-id="77bf5-170">dataSharingConsentGranted</span><span class="sxs-lookup"><span data-stu-id="77bf5-170">dataSharingConsentGranted</span></span>|<span data-ttu-id="77bf5-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="77bf5-171">Boolean</span></span>|<span data-ttu-id="77bf5-172">Concede de consentimiento para uso compartido con Apple Dep servicio de datos</span><span class="sxs-lookup"><span data-stu-id="77bf5-172">Consent granted for data sharing with Apple Dep Service</span></span>|



## <a name="response"></a><span data-ttu-id="77bf5-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77bf5-173">Response</span></span>
<span data-ttu-id="77bf5-174">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77bf5-174">If successful, this method returns a `201 Created` response code and a [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77bf5-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77bf5-175">Example</span></span>
### <a name="request"></a><span data-ttu-id="77bf5-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77bf5-176">Request</span></span>
<span data-ttu-id="77bf5-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77bf5-177">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="77bf5-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77bf5-178">Response</span></span>
<span data-ttu-id="77bf5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77bf5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





