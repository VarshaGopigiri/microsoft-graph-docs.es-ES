---
title: Obtener androidWorkProfileGeneralDeviceConfiguration
description: Leer las propiedades y las relaciones del objeto androidWorkProfileGeneralDeviceConfiguration.
author: tfitzmac
ms.openlocfilehash: 61a8516a2f6dc5263c3976c0827f4acfd758831d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27300836"
---
# <a name="get-androidworkprofilegeneraldeviceconfiguration"></a><span data-ttu-id="74351-103">Obtener androidWorkProfileGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="74351-103">Get androidWorkProfileGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="74351-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74351-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74351-105">Leer las propiedades y las relaciones del objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="74351-105">Read properties and relationships of the [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74351-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74351-106">Prerequisites</span></span>
<span data-ttu-id="74351-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74351-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74351-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74351-109">Permission type</span></span>|<span data-ttu-id="74351-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74351-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74351-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74351-111">Delegated (work or school account)</span></span>|<span data-ttu-id="74351-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="74351-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="74351-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74351-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74351-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74351-114">Not supported.</span></span>|
|<span data-ttu-id="74351-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74351-115">Application</span></span>|<span data-ttu-id="74351-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74351-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74351-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74351-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="74351-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="74351-118">Optional query parameters</span></span>
<span data-ttu-id="74351-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74351-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="74351-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74351-120">Request headers</span></span>
|<span data-ttu-id="74351-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74351-121">Header</span></span>|<span data-ttu-id="74351-122">Valor</span><span class="sxs-lookup"><span data-stu-id="74351-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74351-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="74351-123">Authorization</span></span>|<span data-ttu-id="74351-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74351-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74351-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="74351-125">Accept</span></span>|<span data-ttu-id="74351-126">application/json</span><span class="sxs-lookup"><span data-stu-id="74351-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74351-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74351-127">Request body</span></span>
<span data-ttu-id="74351-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="74351-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74351-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74351-129">Response</span></span>
<span data-ttu-id="74351-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74351-130">If successful, this method returns a `200 OK` response code and [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74351-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74351-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="74351-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74351-132">Request</span></span>
<span data-ttu-id="74351-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74351-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="74351-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74351-134">Response</span></span>
<span data-ttu-id="74351-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74351-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2104

{
  "value": {
    "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
    "id": "6decda7e-da7e-6dec-7eda-ec6d7edaec6d",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "passwordBlockFingerprintUnlock": true,
    "passwordBlockTrustAgents": true,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
    "passwordPreviousPasswordBlockCount": 2,
    "passwordSignInFailureCountBeforeFactoryReset": 12,
    "passwordRequiredType": "lowSecurityBiometric",
    "workProfileDataSharingType": "preventAny",
    "workProfileBlockNotificationsWhileDeviceLocked": true,
    "workProfileBlockAddingAccounts": true,
    "workProfileBluetoothEnableContactSharing": true,
    "workProfileBlockScreenCapture": true,
    "workProfileBlockCrossProfileCallerId": true,
    "workProfileBlockCamera": true,
    "workProfileBlockCrossProfileContactsSearch": true,
    "workProfileBlockCrossProfileCopyPaste": true,
    "workProfileDefaultAppPermissionPolicy": "prompt",
    "workProfilePasswordBlockFingerprintUnlock": true,
    "workProfilePasswordBlockTrustAgents": true,
    "workProfilePasswordExpirationDays": 1,
    "workProfilePasswordMinimumLength": 0,
    "workProfilePasswordMinNumericCharacters": 7,
    "workProfilePasswordMinNonLetterCharacters": 9,
    "workProfilePasswordMinLetterCharacters": 6,
    "workProfilePasswordMinLowerCaseCharacters": 9,
    "workProfilePasswordMinUpperCaseCharacters": 9,
    "workProfilePasswordMinSymbolCharacters": 6,
    "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
    "workProfilePasswordPreviousPasswordBlockCount": 13,
    "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
    "workProfilePasswordRequiredType": "lowSecurityBiometric",
    "workProfileRequirePassword": true,
    "securityRequireVerifyApps": true
  }
}
```



