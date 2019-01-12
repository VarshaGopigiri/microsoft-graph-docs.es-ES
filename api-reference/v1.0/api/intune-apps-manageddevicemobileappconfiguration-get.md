---
title: Obtener managedDeviceMobileAppConfiguration
description: Lea las propiedades y las relaciones del objeto managedDeviceMobileAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 767bc15de14e38f353150e34e338210ca35c1593
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921888"
---
# <a name="get-manageddevicemobileappconfiguration"></a><span data-ttu-id="30423-103">Obtener managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="30423-103">Get managedDeviceMobileAppConfiguration</span></span>

> <span data-ttu-id="30423-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30423-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30423-105">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="30423-105">Read properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="30423-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30423-106">Prerequisites</span></span>
<span data-ttu-id="30423-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30423-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30423-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30423-109">Permission type</span></span>|<span data-ttu-id="30423-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30423-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="30423-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30423-111">Delegated (work or school account)</span></span>|<span data-ttu-id="30423-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="30423-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="30423-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30423-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="30423-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30423-114">Not supported.</span></span>|
|<span data-ttu-id="30423-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30423-115">Application</span></span>|<span data-ttu-id="30423-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30423-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="30423-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30423-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="30423-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="30423-118">Optional query parameters</span></span>
<span data-ttu-id="30423-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30423-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="30423-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30423-120">Request headers</span></span>
|<span data-ttu-id="30423-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30423-121">Header</span></span>|<span data-ttu-id="30423-122">Valor</span><span class="sxs-lookup"><span data-stu-id="30423-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="30423-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="30423-123">Authorization</span></span>|<span data-ttu-id="30423-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="30423-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="30423-125">Accept</span><span class="sxs-lookup"><span data-stu-id="30423-125">Accept</span></span>|<span data-ttu-id="30423-126">application/json</span><span class="sxs-lookup"><span data-stu-id="30423-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="30423-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30423-127">Request body</span></span>
<span data-ttu-id="30423-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="30423-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="30423-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30423-129">Response</span></span>
<span data-ttu-id="30423-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30423-130">If successful, this method returns a `200 OK` response code and [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30423-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30423-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="30423-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30423-132">Request</span></span>
<span data-ttu-id="30423-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30423-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

### <a name="response"></a><span data-ttu-id="30423-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30423-134">Response</span></span>
<span data-ttu-id="30423-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30423-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 451

{
  "value": {
    "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
    "id": "c60e7591-7591-c60e-9175-0ec691750ec6",
    "targetedMobileApps": [
      "Targeted Mobile Apps value"
    ],
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7
  }
}
```



