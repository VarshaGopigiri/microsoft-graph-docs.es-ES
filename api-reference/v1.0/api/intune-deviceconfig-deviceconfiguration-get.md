---
title: Obtener deviceConfiguration
description: Lea las propiedades y las relaciones del objeto deviceConfiguration.
ms.openlocfilehash: 104d50de7e409f41e97cb144ea2f52d746fb1c8c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031557"
---
# <a name="get-deviceconfiguration"></a><span data-ttu-id="a5bd3-103">Obtener deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5bd3-103">Get deviceConfiguration</span></span>

> <span data-ttu-id="a5bd3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a5bd3-105">Lea las propiedades y las relaciones del objeto [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a5bd3-105">Read properties and relationships of the [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a5bd3-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a5bd3-106">Prerequisites</span></span>
<span data-ttu-id="a5bd3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5bd3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5bd3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5bd3-109">Permission type</span></span>|<span data-ttu-id="a5bd3-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5bd3-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a5bd3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5bd3-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a5bd3-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a5bd3-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a5bd3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5bd3-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a5bd3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-114">Not supported.</span></span>|
|<span data-ttu-id="a5bd3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5bd3-115">Application</span></span>|<span data-ttu-id="a5bd3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a5bd3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5bd3-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a5bd3-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a5bd3-118">Optional query parameters</span></span>
<span data-ttu-id="a5bd3-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a5bd3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5bd3-120">Request headers</span></span>
|<span data-ttu-id="a5bd3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5bd3-121">Header</span></span>|<span data-ttu-id="a5bd3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a5bd3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a5bd3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5bd3-123">Authorization</span></span>|<span data-ttu-id="a5bd3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a5bd3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a5bd3-125">Accept</span></span>|<span data-ttu-id="a5bd3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a5bd3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5bd3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5bd3-127">Request body</span></span>
<span data-ttu-id="a5bd3-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a5bd3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5bd3-129">Response</span></span>
<span data-ttu-id="a5bd3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-130">If successful, this method returns a `200 OK` response code and [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5bd3-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5bd3-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a5bd3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5bd3-132">Request</span></span>
<span data-ttu-id="a5bd3-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="a5bd3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5bd3-134">Response</span></span>
<span data-ttu-id="a5bd3-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 362

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfiguration",
    "id": "34977265-7265-3497-6572-973465729734",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7
  }
}
```


