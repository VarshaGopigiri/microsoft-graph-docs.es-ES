---
title: Obtener managedAppRegistration
description: Lea las propiedades y las relaciones del objeto managedAppRegistration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bdb92c9d70ab69508126630fd6430319f4027a27
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877584"
---
# <a name="get-managedappregistration"></a><span data-ttu-id="66efa-103">Obtener managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="66efa-103">Get managedAppRegistration</span></span>

> <span data-ttu-id="66efa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66efa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66efa-105">Lea las propiedades y las relaciones del objeto [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="66efa-105">Read properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="66efa-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="66efa-106">Prerequisites</span></span>
<span data-ttu-id="66efa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66efa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="66efa-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66efa-109">Permission type</span></span>|<span data-ttu-id="66efa-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66efa-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="66efa-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66efa-111">Delegated (work or school account)</span></span>|<span data-ttu-id="66efa-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="66efa-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="66efa-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66efa-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="66efa-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66efa-114">Not supported.</span></span>|
|<span data-ttu-id="66efa-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66efa-115">Application</span></span>|<span data-ttu-id="66efa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66efa-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="66efa-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66efa-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="66efa-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="66efa-118">Optional query parameters</span></span>
<span data-ttu-id="66efa-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66efa-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="66efa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66efa-120">Request headers</span></span>
|<span data-ttu-id="66efa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66efa-121">Header</span></span>|<span data-ttu-id="66efa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="66efa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="66efa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="66efa-123">Authorization</span></span>|<span data-ttu-id="66efa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="66efa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="66efa-125">Accept</span><span class="sxs-lookup"><span data-stu-id="66efa-125">Accept</span></span>|<span data-ttu-id="66efa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="66efa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="66efa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66efa-127">Request body</span></span>
<span data-ttu-id="66efa-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="66efa-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="66efa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66efa-129">Response</span></span>
<span data-ttu-id="66efa-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppRegistration](../resources/intune-mam-managedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66efa-130">If successful, this method returns a `200 OK` response code and [managedAppRegistration](../resources/intune-mam-managedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66efa-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66efa-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="66efa-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66efa-132">Request</span></span>
<span data-ttu-id="66efa-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66efa-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

### <a name="response"></a><span data-ttu-id="66efa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66efa-134">Response</span></span>
<span data-ttu-id="66efa-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66efa-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 756

{
  "value": {
    "@odata.type": "#microsoft.graph.managedAppRegistration",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
    "applicationVersion": "Application Version value",
    "managementSdkVersion": "Management Sdk Version value",
    "platformVersion": "Platform Version value",
    "deviceType": "Device Type value",
    "deviceTag": "Device Tag value",
    "deviceName": "Device Name value",
    "flaggedReasons": [
      "rootedDevice"
    ],
    "userId": "User Id value",
    "appIdentifier": {
      "@odata.type": "microsoft.graph.mobileAppIdentifier"
    },
    "id": "5496aa60-aa60-5496-60aa-965460aa9654",
    "version": "Version value"
  }
}
```



