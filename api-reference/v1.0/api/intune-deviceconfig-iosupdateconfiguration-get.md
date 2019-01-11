---
title: Obtener iosUpdateConfiguration
description: Lea las propiedades y las relaciones del objeto iosUpdateConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 08828e976831d70823de930405e15b489ed3d241
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829202"
---
# <a name="get-iosupdateconfiguration"></a><span data-ttu-id="bd218-103">Obtener iosUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd218-103">Get iosUpdateConfiguration</span></span>

> <span data-ttu-id="bd218-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bd218-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bd218-105">Lea las propiedades y las relaciones del objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="bd218-105">Read properties and relationships of the [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bd218-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bd218-106">Prerequisites</span></span>
<span data-ttu-id="bd218-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd218-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bd218-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd218-109">Permission type</span></span>|<span data-ttu-id="bd218-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd218-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bd218-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd218-111">Delegated (work or school account)</span></span>|<span data-ttu-id="bd218-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="bd218-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="bd218-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd218-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bd218-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd218-114">Not supported.</span></span>|
|<span data-ttu-id="bd218-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd218-115">Application</span></span>|<span data-ttu-id="bd218-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd218-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bd218-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd218-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bd218-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bd218-118">Optional query parameters</span></span>
<span data-ttu-id="bd218-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd218-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bd218-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd218-120">Request headers</span></span>
|<span data-ttu-id="bd218-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd218-121">Header</span></span>|<span data-ttu-id="bd218-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bd218-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bd218-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bd218-123">Authorization</span></span>|<span data-ttu-id="bd218-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bd218-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bd218-125">Accept</span><span class="sxs-lookup"><span data-stu-id="bd218-125">Accept</span></span>|<span data-ttu-id="bd218-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bd218-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bd218-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd218-127">Request body</span></span>
<span data-ttu-id="bd218-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd218-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd218-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd218-129">Response</span></span>
<span data-ttu-id="bd218-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd218-130">If successful, this method returns a `200 OK` response code and [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bd218-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd218-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="bd218-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd218-132">Request</span></span>
<span data-ttu-id="bd218-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd218-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="bd218-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd218-134">Response</span></span>
<span data-ttu-id="bd218-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd218-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 542

{
  "value": {
    "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
    "id": "321aef09-ef09-321a-09ef-1a3209ef1a32",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "activeHoursStart": "12:00:05.5020000",
    "activeHoursEnd": "11:59:00.8990000",
    "scheduledInstallDays": [
      "monday"
    ],
    "utcTimeOffsetInMinutes": 6
  }
}
```



