---
title: Lista depOnboardingSettings
description: Propiedades de la lista y relaciones de los objetos depOnboardingSetting.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 65c4dbfb50539e40404dc103817360c8fc259533
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812113"
---
# <a name="list-deponboardingsettings"></a><span data-ttu-id="1bd18-103">Lista depOnboardingSettings</span><span class="sxs-lookup"><span data-stu-id="1bd18-103">List depOnboardingSettings</span></span>

> <span data-ttu-id="1bd18-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1bd18-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1bd18-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1bd18-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1bd18-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1bd18-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1bd18-107">Propiedades de la lista y relaciones de los objetos [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd18-107">List properties and relationships of the [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1bd18-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1bd18-108">Prerequisites</span></span>
<span data-ttu-id="1bd18-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1bd18-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1bd18-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1bd18-111">Permission type</span></span>|<span data-ttu-id="1bd18-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1bd18-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1bd18-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1bd18-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1bd18-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="1bd18-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="1bd18-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1bd18-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1bd18-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1bd18-116">Not supported.</span></span>|
|<span data-ttu-id="1bd18-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1bd18-117">Application</span></span>|<span data-ttu-id="1bd18-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1bd18-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1bd18-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1bd18-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings
```

## <a name="request-headers"></a><span data-ttu-id="1bd18-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1bd18-120">Request headers</span></span>
|<span data-ttu-id="1bd18-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bd18-121">Header</span></span>|<span data-ttu-id="1bd18-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1bd18-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1bd18-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1bd18-123">Authorization</span></span>|<span data-ttu-id="1bd18-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1bd18-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1bd18-125">Accept</span><span class="sxs-lookup"><span data-stu-id="1bd18-125">Accept</span></span>|<span data-ttu-id="1bd18-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1bd18-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1bd18-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1bd18-127">Request body</span></span>
<span data-ttu-id="1bd18-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1bd18-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1bd18-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1bd18-129">Response</span></span>
<span data-ttu-id="1bd18-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1bd18-130">If successful, this method returns a `200 OK` response code and a collection of [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1bd18-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1bd18-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1bd18-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1bd18-132">Request</span></span>
<span data-ttu-id="1bd18-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1bd18-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings
```

### <a name="response"></a><span data-ttu-id="1bd18-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1bd18-134">Response</span></span>
<span data-ttu-id="1bd18-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1bd18-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 786

{
  "value": [
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
  ]
}
```





