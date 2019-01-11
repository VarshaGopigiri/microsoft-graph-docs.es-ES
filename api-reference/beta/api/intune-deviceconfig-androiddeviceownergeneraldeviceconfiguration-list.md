---
title: Lista androidDeviceOwnerGeneralDeviceConfigurations
description: Propiedades de la lista y relaciones de los objetos androidDeviceOwnerGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c45dac2aea007b2c9b54828376d8ae0b519fd736
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838573"
---
# <a name="list-androiddeviceownergeneraldeviceconfigurations"></a><span data-ttu-id="f1fdb-103">Lista androidDeviceOwnerGeneralDeviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="f1fdb-103">List androidDeviceOwnerGeneralDeviceConfigurations</span></span>

> <span data-ttu-id="f1fdb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f1fdb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f1fdb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f1fdb-107">Propiedades de la lista y relaciones de los objetos [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fdb-107">List properties and relationships of the [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f1fdb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f1fdb-108">Prerequisites</span></span>
<span data-ttu-id="f1fdb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1fdb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f1fdb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1fdb-111">Permission type</span></span>|<span data-ttu-id="f1fdb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1fdb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f1fdb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1fdb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f1fdb-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f1fdb-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f1fdb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1fdb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f1fdb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-116">Not supported.</span></span>|
|<span data-ttu-id="f1fdb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1fdb-117">Application</span></span>|<span data-ttu-id="f1fdb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f1fdb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1fdb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f1fdb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1fdb-120">Request headers</span></span>
|<span data-ttu-id="f1fdb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1fdb-121">Header</span></span>|<span data-ttu-id="f1fdb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f1fdb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f1fdb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f1fdb-123">Authorization</span></span>|<span data-ttu-id="f1fdb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f1fdb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f1fdb-125">Accept</span></span>|<span data-ttu-id="f1fdb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f1fdb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f1fdb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1fdb-127">Request body</span></span>
<span data-ttu-id="f1fdb-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f1fdb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1fdb-129">Response</span></span>
<span data-ttu-id="f1fdb-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-130">If successful, this method returns a `200 OK` response code and a collection of [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1fdb-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1fdb-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f1fdb-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1fdb-132">Request</span></span>
<span data-ttu-id="f1fdb-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="f1fdb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1fdb-134">Response</span></span>
<span data-ttu-id="f1fdb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1fdb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2549

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidDeviceOwnerGeneralDeviceConfiguration",
      "id": "edad943d-943d-edad-3d94-aded3d94aded",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "accountsBlockModification": true,
      "appsAllowInstallFromUnknownSources": true,
      "appsAutoUpdatePolicy": "userChoice",
      "appsDefaultPermissionPolicy": "prompt",
      "bluetoothBlockConfiguration": true,
      "bluetoothBlockContactSharing": true,
      "cameraBlocked": true,
      "cellularBlockWiFiTethering": true,
      "dataRoamingBlocked": true,
      "dateTimeConfigurationBlocked": true,
      "factoryResetDeviceAdministratorEmails": [
        "Factory Reset Device Administrator Emails value"
      ],
      "factoryResetBlocked": true,
      "kioskModeApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "microphoneForceMute": true,
      "networkEscapeHatchAllowed": true,
      "nfcBlockOutgoingBeam": true,
      "passwordBlockKeyguard": true,
      "passwordExpirationDays": 6,
      "passwordMinimumLength": 5,
      "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
      "passwordPreviousPasswordCountToBlock": 4,
      "passwordRequiredType": "required",
      "passwordSignInFailureCountBeforeFactoryReset": 12,
      "safeBootBlocked": true,
      "screenCaptureBlocked": true,
      "securityAllowDebuggingFeatures": true,
      "securityRequireVerifyApps": true,
      "statusBarBlocked": true,
      "stayOnModes": [
        "ac"
      ],
      "storageAllowUsb": true,
      "storageBlockExternalMedia": true,
      "storageBlockUsbFileTransfer": true,
      "systemUpdateWindowStartMinutesAfterMidnight": 11,
      "systemUpdateWindowEndMinutesAfterMidnight": 9,
      "systemUpdateInstallType": "postpone",
      "usersBlockAdd": true,
      "usersBlockRemove": true,
      "volumeBlockAdjustment": true,
      "wifiBlockEditConfigurations": true,
      "wifiBlockEditPolicyDefinedConfigurations": true
    }
  ]
}
```





