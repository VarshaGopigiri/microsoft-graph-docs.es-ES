---
title: Obtener androidCustomConfiguration
description: Lea las propiedades y las relaciones del objeto androidCustomConfiguration.
author: tfitzmac
ms.openlocfilehash: 79f2cafe9ad01b7e58ee3cbc798929662d506307
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313177"
---
# <a name="get-androidcustomconfiguration"></a><span data-ttu-id="138cf-103">Obtener androidCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="138cf-103">Get androidCustomConfiguration</span></span>

> <span data-ttu-id="138cf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="138cf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="138cf-105">Lea las propiedades y las relaciones del objeto [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="138cf-105">Read properties and relationships of the [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="138cf-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="138cf-106">Prerequisites</span></span>
<span data-ttu-id="138cf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="138cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="138cf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="138cf-109">Permission type</span></span>|<span data-ttu-id="138cf-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="138cf-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="138cf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="138cf-111">Delegated (work or school account)</span></span>|<span data-ttu-id="138cf-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="138cf-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="138cf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="138cf-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="138cf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="138cf-114">Not supported.</span></span>|
|<span data-ttu-id="138cf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="138cf-115">Application</span></span>|<span data-ttu-id="138cf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="138cf-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="138cf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="138cf-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="138cf-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="138cf-118">Optional query parameters</span></span>
<span data-ttu-id="138cf-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="138cf-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="138cf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="138cf-120">Request headers</span></span>
|<span data-ttu-id="138cf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="138cf-121">Header</span></span>|<span data-ttu-id="138cf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="138cf-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="138cf-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="138cf-123">Authorization</span></span>|<span data-ttu-id="138cf-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="138cf-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="138cf-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="138cf-125">Accept</span></span>|<span data-ttu-id="138cf-126">application/json</span><span class="sxs-lookup"><span data-stu-id="138cf-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="138cf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="138cf-127">Request body</span></span>
<span data-ttu-id="138cf-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="138cf-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="138cf-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="138cf-129">Response</span></span>
<span data-ttu-id="138cf-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="138cf-130">If successful, this method returns a `200 OK` response code and [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="138cf-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="138cf-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="138cf-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="138cf-132">Request</span></span>
<span data-ttu-id="138cf-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="138cf-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="138cf-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="138cf-134">Response</span></span>
<span data-ttu-id="138cf-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="138cf-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 625

{
  "value": {
    "@odata.type": "#microsoft.graph.androidCustomConfiguration",
    "id": "619b5e6d-5e6d-619b-6d5e-9b616d5e9b61",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "omaSettings": [
      {
        "@odata.type": "microsoft.graph.omaSettingInteger",
        "displayName": "Display Name value",
        "description": "Description value",
        "omaUri": "Oma Uri value",
        "value": 5
      }
    ]
  }
}
```



