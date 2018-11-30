---
title: Obtener iosMobileAppConfiguration
description: Lee las propiedades y las relaciones del objeto iosMobileAppConfiguration.
ms.openlocfilehash: a85f570caa82ad803bf6ed8163ebe798da5c3d2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031942"
---
# <a name="get-iosmobileappconfiguration"></a><span data-ttu-id="578c7-103">Obtener iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="578c7-103">Get iosMobileAppConfiguration</span></span>

> <span data-ttu-id="578c7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="578c7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="578c7-105">Lee las propiedades y las relaciones del objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="578c7-105">Read properties and relationships of the [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="578c7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="578c7-106">Prerequisites</span></span>
<span data-ttu-id="578c7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="578c7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="578c7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="578c7-109">Permission type</span></span>|<span data-ttu-id="578c7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="578c7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="578c7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="578c7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="578c7-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="578c7-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="578c7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="578c7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="578c7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="578c7-114">Not supported.</span></span>|
|<span data-ttu-id="578c7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="578c7-115">Application</span></span>|<span data-ttu-id="578c7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="578c7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="578c7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="578c7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="578c7-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="578c7-118">Optional query parameters</span></span>
<span data-ttu-id="578c7-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="578c7-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="578c7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="578c7-120">Request headers</span></span>
|<span data-ttu-id="578c7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="578c7-121">Header</span></span>|<span data-ttu-id="578c7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="578c7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="578c7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="578c7-123">Authorization</span></span>|<span data-ttu-id="578c7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="578c7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="578c7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="578c7-125">Accept</span></span>|<span data-ttu-id="578c7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="578c7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="578c7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="578c7-127">Request body</span></span>
<span data-ttu-id="578c7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="578c7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="578c7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="578c7-129">Response</span></span>
<span data-ttu-id="578c7-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="578c7-130">If successful, this method returns a `200 OK` response code and [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="578c7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="578c7-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="578c7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="578c7-132">Request</span></span>
<span data-ttu-id="578c7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="578c7-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

### <a name="response"></a><span data-ttu-id="578c7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="578c7-134">Response</span></span>
<span data-ttu-id="578c7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="578c7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 763

{
  "value": {
    "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
    "id": "b2c33191-3191-b2c3-9131-c3b29131c3b2",
    "targetedMobileApps": [
      "Targeted Mobile Apps value"
    ],
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "encodedSettingXml": "ZW5jb2RlZFNldHRpbmdYbWw=",
    "settings": [
      {
        "@odata.type": "microsoft.graph.appConfigurationSettingItem",
        "appConfigKey": "App Config Key value",
        "appConfigKeyType": "integerType",
        "appConfigKeyValue": "App Config Key Value value"
      }
    ]
  }
}
```



