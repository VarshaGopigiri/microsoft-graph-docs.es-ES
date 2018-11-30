---
title: Obtener windows81GeneralConfiguration
description: Lea las propiedades y las relaciones del objeto windows81GeneralConfiguration.
ms.openlocfilehash: cc64f6ac791648b02558c7ce30e21b78841fac0e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031290"
---
# <a name="get-windows81generalconfiguration"></a><span data-ttu-id="f723e-103">Obtener windows81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="f723e-103">Get windows81GeneralConfiguration</span></span>

> <span data-ttu-id="f723e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f723e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f723e-105">Lea las propiedades y las relaciones del objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f723e-105">Read properties and relationships of the [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f723e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f723e-106">Prerequisites</span></span>
<span data-ttu-id="f723e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f723e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f723e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f723e-109">Permission type</span></span>|<span data-ttu-id="f723e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f723e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f723e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f723e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f723e-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f723e-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f723e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f723e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f723e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f723e-114">Not supported.</span></span>|
|<span data-ttu-id="f723e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f723e-115">Application</span></span>|<span data-ttu-id="f723e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f723e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f723e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f723e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f723e-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f723e-118">Optional query parameters</span></span>
<span data-ttu-id="f723e-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f723e-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f723e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f723e-120">Request headers</span></span>
|<span data-ttu-id="f723e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f723e-121">Header</span></span>|<span data-ttu-id="f723e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f723e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f723e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f723e-123">Authorization</span></span>|<span data-ttu-id="f723e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f723e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f723e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f723e-125">Accept</span></span>|<span data-ttu-id="f723e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f723e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f723e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f723e-127">Request body</span></span>
<span data-ttu-id="f723e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f723e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f723e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f723e-129">Response</span></span>
<span data-ttu-id="f723e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f723e-130">If successful, this method returns a `200 OK` response code and [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f723e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f723e-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f723e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f723e-132">Request</span></span>
<span data-ttu-id="f723e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f723e-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="f723e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f723e-134">Response</span></span>
<span data-ttu-id="f723e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f723e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1964

{
  "value": {
    "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
    "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "accountsBlockAddingNonMicrosoftAccountEmail": true,
    "applyOnlyToWindows81": true,
    "browserBlockAutofill": true,
    "browserBlockAutomaticDetectionOfIntranetSites": true,
    "browserBlockEnterpriseModeAccess": true,
    "browserBlockJavaScript": true,
    "browserBlockPlugins": true,
    "browserBlockPopups": true,
    "browserBlockSendingDoNotTrackHeader": true,
    "browserBlockSingleWordEntryOnIntranetSites": true,
    "browserRequireSmartScreen": true,
    "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
    "browserInternetSecurityLevel": "medium",
    "browserIntranetSecurityLevel": "low",
    "browserLoggingReportLocation": "Browser Logging Report Location value",
    "browserRequireHighSecurityForRestrictedSites": true,
    "browserRequireFirewall": true,
    "browserRequireFraudWarning": true,
    "browserTrustedSitesSecurityLevel": "low",
    "cellularBlockDataRoaming": true,
    "diagnosticsBlockDataSubmission": true,
    "passwordBlockPicturePasswordAndPin": true,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
    "passwordMinimumCharacterSetCount": 0,
    "passwordPreviousPasswordBlockCount": 2,
    "passwordRequiredType": "alphanumeric",
    "passwordSignInFailureCountBeforeFactoryReset": 12,
    "storageRequireDeviceEncryption": true,
    "updatesRequireAutomaticUpdates": true,
    "userAccountControlSettings": "alwaysNotify",
    "workFoldersUrl": "https://example.com/workFoldersUrl/"
  }
}
```


