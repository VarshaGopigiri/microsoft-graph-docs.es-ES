---
title: Lista androidWorkProfileGeneralDeviceConfigurations
description: Propiedades de la lista y relaciones de los objetos androidWorkProfileGeneralDeviceConfiguration.
author: tfitzmac
ms.openlocfilehash: aa1ee9daf168cc9c74e736e38705a957c09ef49b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334142"
---
# <a name="list-androidworkprofilegeneraldeviceconfigurations"></a><span data-ttu-id="71b03-103">Lista androidWorkProfileGeneralDeviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="71b03-103">List androidWorkProfileGeneralDeviceConfigurations</span></span>

> <span data-ttu-id="71b03-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71b03-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71b03-105">Propiedades de la lista y relaciones de los objetos [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="71b03-105">List properties and relationships of the [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71b03-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71b03-106">Prerequisites</span></span>
<span data-ttu-id="71b03-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71b03-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71b03-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71b03-109">Permission type</span></span>|<span data-ttu-id="71b03-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71b03-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71b03-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71b03-111">Delegated (work or school account)</span></span>|<span data-ttu-id="71b03-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="71b03-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="71b03-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71b03-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71b03-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71b03-114">Not supported.</span></span>|
|<span data-ttu-id="71b03-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71b03-115">Application</span></span>|<span data-ttu-id="71b03-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71b03-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71b03-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71b03-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="71b03-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71b03-118">Request headers</span></span>
|<span data-ttu-id="71b03-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71b03-119">Header</span></span>|<span data-ttu-id="71b03-120">Valor</span><span class="sxs-lookup"><span data-stu-id="71b03-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71b03-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="71b03-121">Authorization</span></span>|<span data-ttu-id="71b03-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71b03-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71b03-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="71b03-123">Accept</span></span>|<span data-ttu-id="71b03-124">application/json</span><span class="sxs-lookup"><span data-stu-id="71b03-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71b03-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71b03-125">Request body</span></span>
<span data-ttu-id="71b03-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71b03-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71b03-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71b03-127">Response</span></span>
<span data-ttu-id="71b03-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71b03-128">If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71b03-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71b03-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="71b03-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71b03-130">Request</span></span>
<span data-ttu-id="71b03-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71b03-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="71b03-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71b03-132">Response</span></span>
<span data-ttu-id="71b03-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71b03-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2200

{
  "value": [
    {
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
  ]
}
```



