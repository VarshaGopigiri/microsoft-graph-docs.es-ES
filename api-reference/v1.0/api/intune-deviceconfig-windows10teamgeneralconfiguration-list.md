---
title: Enumerar windows10TeamGeneralConfigurations
description: Enumere las propiedades y las relaciones de los objetos windows10TeamGeneralConfiguration.
ms.openlocfilehash: ad05a8c19337db5d49057b8dc7ff395297f66803
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032565"
---
# <a name="list-windows10teamgeneralconfigurations"></a><span data-ttu-id="8f240-103">Enumerar windows10TeamGeneralConfigurations</span><span class="sxs-lookup"><span data-stu-id="8f240-103">List windows10TeamGeneralConfigurations</span></span>

> <span data-ttu-id="8f240-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f240-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f240-105">Enumere las propiedades y las relaciones de los objetos [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8f240-105">List properties and relationships of the [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8f240-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8f240-106">Prerequisites</span></span>
<span data-ttu-id="8f240-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f240-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f240-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f240-109">Permission type</span></span>|<span data-ttu-id="8f240-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f240-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8f240-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f240-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8f240-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="8f240-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="8f240-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f240-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8f240-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f240-114">Not supported.</span></span>|
|<span data-ttu-id="8f240-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f240-115">Application</span></span>|<span data-ttu-id="8f240-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f240-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8f240-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f240-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="8f240-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f240-118">Request headers</span></span>
|<span data-ttu-id="8f240-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f240-119">Header</span></span>|<span data-ttu-id="8f240-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8f240-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8f240-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f240-121">Authorization</span></span>|<span data-ttu-id="8f240-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8f240-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8f240-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8f240-123">Accept</span></span>|<span data-ttu-id="8f240-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8f240-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f240-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f240-125">Request body</span></span>
<span data-ttu-id="8f240-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8f240-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8f240-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f240-127">Response</span></span>
<span data-ttu-id="8f240-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f240-128">If successful, this method returns a `200 OK` response code and a collection of [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f240-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f240-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="8f240-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f240-130">Request</span></span>
<span data-ttu-id="8f240-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f240-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="8f240-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f240-132">Response</span></span>
<span data-ttu-id="8f240-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f240-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1463

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
      "id": "0c94aa20-aa20-0c94-20aa-940c20aa940c",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "azureOperationalInsightsBlockTelemetry": true,
      "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
      "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
      "connectAppBlockAutoLaunch": true,
      "maintenanceWindowBlocked": true,
      "maintenanceWindowDurationInHours": 0,
      "maintenanceWindowStartTime": "11:59:09.3130000",
      "miracastChannel": "one",
      "miracastBlocked": true,
      "miracastRequirePin": true,
      "settingsBlockMyMeetingsAndFiles": true,
      "settingsBlockSessionResume": true,
      "settingsBlockSigninSuggestions": true,
      "settingsDefaultVolume": 5,
      "settingsScreenTimeoutInMinutes": 14,
      "settingsSessionTimeoutInMinutes": 15,
      "settingsSleepTimeoutInMinutes": 13,
      "welcomeScreenBlockAutomaticWakeUp": true,
      "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
      "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
    }
  ]
}
```



