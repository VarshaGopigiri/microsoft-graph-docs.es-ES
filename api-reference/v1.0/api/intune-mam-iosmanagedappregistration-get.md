---
title: Obtener iosManagedAppRegistration
description: Lea las propiedades y las relaciones del objeto iosManagedAppRegistration.
ms.openlocfilehash: 04220d7b707eedc877b66a7ad5652185d1efd464
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029681"
---
# <a name="get-iosmanagedappregistration"></a><span data-ttu-id="4ffa6-103">Obtener iosManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="4ffa6-103">Get iosManagedAppRegistration</span></span>

> <span data-ttu-id="4ffa6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4ffa6-105">Lea las propiedades y las relaciones del objeto [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4ffa6-105">Read properties and relationships of the [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4ffa6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4ffa6-106">Prerequisites</span></span>
<span data-ttu-id="4ffa6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4ffa6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4ffa6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4ffa6-109">Permission type</span></span>|<span data-ttu-id="4ffa6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4ffa6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4ffa6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4ffa6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4ffa6-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="4ffa6-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="4ffa6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4ffa6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4ffa6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-114">Not supported.</span></span>|
|<span data-ttu-id="4ffa6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4ffa6-115">Application</span></span>|<span data-ttu-id="4ffa6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4ffa6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ffa6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4ffa6-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4ffa6-118">Optional query parameters</span></span>
<span data-ttu-id="4ffa6-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4ffa6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4ffa6-120">Request headers</span></span>
|<span data-ttu-id="4ffa6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ffa6-121">Header</span></span>|<span data-ttu-id="4ffa6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4ffa6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4ffa6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4ffa6-123">Authorization</span></span>|<span data-ttu-id="4ffa6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4ffa6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4ffa6-125">Accept</span></span>|<span data-ttu-id="4ffa6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4ffa6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4ffa6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4ffa6-127">Request body</span></span>
<span data-ttu-id="4ffa6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4ffa6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ffa6-129">Response</span></span>
<span data-ttu-id="4ffa6-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-130">If successful, this method returns a `200 OK` response code and [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4ffa6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ffa6-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="4ffa6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4ffa6-132">Request</span></span>
<span data-ttu-id="4ffa6-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

### <a name="response"></a><span data-ttu-id="4ffa6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ffa6-134">Response</span></span>
<span data-ttu-id="4ffa6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4ffa6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 800

{
  "value": {
    "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
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
      "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
      "bundleId": "Bundle Id value"
    },
    "id": "47632c19-2c19-4763-192c-6347192c6347",
    "version": "Version value"
  }
}
```



