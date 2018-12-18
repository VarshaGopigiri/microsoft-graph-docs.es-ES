---
title: Lista depOnboardingSettings
description: Propiedades de la lista y relaciones de los objetos depOnboardingSetting.
author: tfitzmac
ms.openlocfilehash: 6e3a84246f20b6939e156172f77c76a9baac18b7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305582"
---
# <a name="list-deponboardingsettings"></a><span data-ttu-id="18680-103">Lista depOnboardingSettings</span><span class="sxs-lookup"><span data-stu-id="18680-103">List depOnboardingSettings</span></span>

> <span data-ttu-id="18680-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18680-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18680-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18680-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="18680-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="18680-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="18680-107">Propiedades de la lista y relaciones de los objetos [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="18680-107">List properties and relationships of the [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="18680-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="18680-108">Prerequisites</span></span>
<span data-ttu-id="18680-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18680-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18680-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18680-111">Permission type</span></span>|<span data-ttu-id="18680-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18680-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="18680-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18680-113">Delegated (work or school account)</span></span>|<span data-ttu-id="18680-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="18680-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="18680-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18680-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="18680-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18680-116">Not supported.</span></span>|
|<span data-ttu-id="18680-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18680-117">Application</span></span>|<span data-ttu-id="18680-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18680-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="18680-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18680-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings
```

## <a name="request-headers"></a><span data-ttu-id="18680-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18680-120">Request headers</span></span>
|<span data-ttu-id="18680-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18680-121">Header</span></span>|<span data-ttu-id="18680-122">Valor</span><span class="sxs-lookup"><span data-stu-id="18680-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="18680-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="18680-123">Authorization</span></span>|<span data-ttu-id="18680-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="18680-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="18680-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="18680-125">Accept</span></span>|<span data-ttu-id="18680-126">application/json</span><span class="sxs-lookup"><span data-stu-id="18680-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="18680-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18680-127">Request body</span></span>
<span data-ttu-id="18680-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="18680-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="18680-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18680-129">Response</span></span>
<span data-ttu-id="18680-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18680-130">If successful, this method returns a `200 OK` response code and a collection of [depOnboardingSetting](../resources/intune-enrollment-deponboardingsetting.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18680-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18680-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="18680-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18680-132">Request</span></span>
<span data-ttu-id="18680-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18680-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings
```

### <a name="response"></a><span data-ttu-id="18680-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18680-134">Response</span></span>
<span data-ttu-id="18680-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18680-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





