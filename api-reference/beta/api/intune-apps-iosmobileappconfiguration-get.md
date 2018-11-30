---
title: Obtener iosMobileAppConfiguration
description: Lee las propiedades y las relaciones del objeto iosMobileAppConfiguration.
ms.openlocfilehash: cbff1c1405d02aa21069ba7fa4c981d494d6ffb3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084034"
---
# <a name="get-iosmobileappconfiguration"></a><span data-ttu-id="7c230-103">Obtener iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c230-103">Get iosMobileAppConfiguration</span></span>

> <span data-ttu-id="7c230-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c230-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c230-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c230-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7c230-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7c230-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7c230-107">Lee las propiedades y las relaciones del objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7c230-107">Read properties and relationships of the [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7c230-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7c230-108">Prerequisites</span></span>
<span data-ttu-id="7c230-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7c230-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7c230-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7c230-111">Permission type</span></span>|<span data-ttu-id="7c230-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7c230-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7c230-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7c230-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7c230-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="7c230-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="7c230-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7c230-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7c230-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7c230-116">Not supported.</span></span>|
|<span data-ttu-id="7c230-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7c230-117">Application</span></span>|<span data-ttu-id="7c230-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7c230-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7c230-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c230-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="7c230-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7c230-120">Optional query parameters</span></span>
<span data-ttu-id="7c230-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c230-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7c230-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c230-122">Request headers</span></span>
|<span data-ttu-id="7c230-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c230-123">Header</span></span>|<span data-ttu-id="7c230-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7c230-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7c230-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="7c230-125">Authorization</span></span>|<span data-ttu-id="7c230-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7c230-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7c230-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7c230-127">Accept</span></span>|<span data-ttu-id="7c230-128">application/json</span><span class="sxs-lookup"><span data-stu-id="7c230-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7c230-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7c230-129">Request body</span></span>
<span data-ttu-id="7c230-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7c230-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7c230-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c230-131">Response</span></span>
<span data-ttu-id="7c230-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c230-132">If successful, this method returns a `200 OK` response code and [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7c230-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c230-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="7c230-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c230-134">Request</span></span>
<span data-ttu-id="7c230-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c230-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

### <a name="response"></a><span data-ttu-id="7c230-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c230-136">Response</span></span>
<span data-ttu-id="7c230-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c230-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 831

{
  "value": {
    "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
    "id": "b2c33191-3191-b2c3-9131-c3b29131c3b2",
    "targetedMobileApps": [
      "Targeted Mobile Apps value"
    ],
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
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





