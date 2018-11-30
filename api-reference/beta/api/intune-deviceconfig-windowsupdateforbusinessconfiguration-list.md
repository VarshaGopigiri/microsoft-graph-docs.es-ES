---
title: Enumerar windowsUpdateForBusinessConfigurations
description: Enumere las propiedades y las relaciones de los objetos windowsUpdateForBusinessConfiguration.
ms.openlocfilehash: 2709109ae523033f38a8e125e3b769051a67a832
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089412"
---
# <a name="list-windowsupdateforbusinessconfigurations"></a><span data-ttu-id="ce18e-103">Enumerar windowsUpdateForBusinessConfigurations</span><span class="sxs-lookup"><span data-stu-id="ce18e-103">List windowsUpdateForBusinessConfigurations</span></span>

> <span data-ttu-id="ce18e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce18e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce18e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce18e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ce18e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce18e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce18e-107">Enumere las propiedades y las relaciones de los objetos [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce18e-107">List properties and relationships of the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ce18e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ce18e-108">Prerequisites</span></span>
<span data-ttu-id="ce18e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce18e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce18e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce18e-111">Permission type</span></span>|<span data-ttu-id="ce18e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce18e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ce18e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce18e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ce18e-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="ce18e-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="ce18e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce18e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ce18e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce18e-116">Not supported.</span></span>|
|<span data-ttu-id="ce18e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce18e-117">Application</span></span>|<span data-ttu-id="ce18e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce18e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ce18e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce18e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="ce18e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce18e-120">Request headers</span></span>
|<span data-ttu-id="ce18e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce18e-121">Header</span></span>|<span data-ttu-id="ce18e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ce18e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ce18e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce18e-123">Authorization</span></span>|<span data-ttu-id="ce18e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ce18e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ce18e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ce18e-125">Accept</span></span>|<span data-ttu-id="ce18e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ce18e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce18e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce18e-127">Request body</span></span>
<span data-ttu-id="ce18e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ce18e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ce18e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce18e-129">Response</span></span>
<span data-ttu-id="ce18e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce18e-130">If successful, this method returns a `200 OK` response code and a collection of [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ce18e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce18e-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ce18e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce18e-132">Request</span></span>
<span data-ttu-id="ce18e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce18e-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="ce18e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce18e-134">Response</span></span>
<span data-ttu-id="ce18e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce18e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2176

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
      "id": "4928dd6a-dd6a-4928-6add-28496add2849",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "deliveryOptimizationMode": "httpOnly",
      "prereleaseFeatures": "settingsOnly",
      "automaticUpdateMode": "notifyDownload",
      "microsoftUpdateServiceAllowed": true,
      "driversExcluded": true,
      "installationSchedule": {
        "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
        "scheduledInstallDay": "everyday",
        "scheduledInstallTime": "11:59:31.3170000"
      },
      "qualityUpdatesDeferralPeriodInDays": 2,
      "featureUpdatesDeferralPeriodInDays": 2,
      "qualityUpdatesPaused": true,
      "featureUpdatesPaused": true,
      "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
      "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
      "businessReadyUpdatesOnly": "all",
      "skipChecksBeforeRestart": true,
      "updateWeeks": "firstWeek",
      "qualityUpdatesPauseStartDateTime": "Quality Updates Pause Start Date Time value",
      "featureUpdatesPauseStartDateTime": "Feature Updates Pause Start Date Time value",
      "featureUpdatesRollbackWindowInDays": 2,
      "qualityUpdatesWillBeRolledBack": true,
      "featureUpdatesWillBeRolledBack": true,
      "qualityUpdatesRollbackStartDateTime": "2016-12-31T23:57:01.05526-08:00",
      "featureUpdatesRollbackStartDateTime": "2017-01-01T00:03:21.6080517-08:00",
      "engagedRestartDeadlineInDays": 12,
      "engagedRestartSnoozeScheduleInDays": 2,
      "engagedRestartTransitionScheduleInDays": 6,
      "autoRestartNotificationDismissal": "automatic",
      "scheduleRestartWarningInHours": 13,
      "scheduleImminentRestartWarningInMinutes": 7
    }
  ]
}
```





