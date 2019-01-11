---
title: Lista windowsIdentityProtectionConfigurations
description: Propiedades de la lista y relaciones de los objetos windowsIdentityProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0bc4b871ea2b093867051a76b53d756126006e40
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877670"
---
# <a name="list-windowsidentityprotectionconfigurations"></a><span data-ttu-id="08074-103">Lista windowsIdentityProtectionConfigurations</span><span class="sxs-lookup"><span data-stu-id="08074-103">List windowsIdentityProtectionConfigurations</span></span>

> <span data-ttu-id="08074-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="08074-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="08074-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="08074-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="08074-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="08074-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="08074-107">Propiedades de la lista y relaciones de los objetos [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="08074-107">List properties and relationships of the [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="08074-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="08074-108">Prerequisites</span></span>
<span data-ttu-id="08074-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="08074-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="08074-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08074-111">Permission type</span></span>|<span data-ttu-id="08074-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08074-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="08074-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08074-113">Delegated (work or school account)</span></span>|<span data-ttu-id="08074-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="08074-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="08074-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08074-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="08074-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08074-116">Not supported.</span></span>|
|<span data-ttu-id="08074-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08074-117">Application</span></span>|<span data-ttu-id="08074-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08074-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="08074-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08074-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="08074-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08074-120">Request headers</span></span>
|<span data-ttu-id="08074-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08074-121">Header</span></span>|<span data-ttu-id="08074-122">Valor</span><span class="sxs-lookup"><span data-stu-id="08074-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="08074-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="08074-123">Authorization</span></span>|<span data-ttu-id="08074-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="08074-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="08074-125">Accept</span><span class="sxs-lookup"><span data-stu-id="08074-125">Accept</span></span>|<span data-ttu-id="08074-126">application/json</span><span class="sxs-lookup"><span data-stu-id="08074-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="08074-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08074-127">Request body</span></span>
<span data-ttu-id="08074-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="08074-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="08074-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08074-129">Response</span></span>
<span data-ttu-id="08074-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08074-130">If successful, this method returns a `200 OK` response code and a collection of [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08074-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08074-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="08074-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08074-132">Request</span></span>
<span data-ttu-id="08074-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08074-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="08074-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08074-134">Response</span></span>
<span data-ttu-id="08074-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08074-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1075

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsIdentityProtectionConfiguration",
      "id": "b2e64303-4303-b2e6-0343-e6b20343e6b2",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "enhancedAntiSpoofingForFacialFeaturesEnabled": true,
      "pinMinimumLength": 0,
      "pinMaximumLength": 0,
      "pinUppercaseCharactersUsage": "required",
      "pinLowercaseCharactersUsage": "required",
      "pinSpecialCharactersUsage": "required",
      "pinExpirationInDays": 3,
      "pinPreviousBlockCount": 5,
      "pinRecoveryEnabled": true,
      "securityDeviceRequired": true,
      "unlockWithBiometricsEnabled": true,
      "useCertificatesForOnPremisesAuthEnabled": true,
      "windowsHelloForBusinessBlocked": true
    }
  ]
}
```





