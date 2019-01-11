---
title: Obtener androidManagedAppRegistration
description: Lea las propiedades y las relaciones del objeto androidManagedAppRegistration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0d1d2bfc1f55ac90335cb9f37a03474a469b372f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809537"
---
# <a name="get-androidmanagedappregistration"></a><span data-ttu-id="ffdbd-103">Obtener androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="ffdbd-103">Get androidManagedAppRegistration</span></span>

> <span data-ttu-id="ffdbd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffdbd-105">Lea las propiedades y las relaciones del objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="ffdbd-105">Read properties and relationships of the [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ffdbd-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ffdbd-106">Prerequisites</span></span>
<span data-ttu-id="ffdbd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ffdbd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ffdbd-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ffdbd-109">Permission type</span></span>|<span data-ttu-id="ffdbd-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ffdbd-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ffdbd-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ffdbd-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ffdbd-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="ffdbd-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="ffdbd-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ffdbd-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ffdbd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-114">Not supported.</span></span>|
|<span data-ttu-id="ffdbd-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ffdbd-115">Application</span></span>|<span data-ttu-id="ffdbd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ffdbd-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdbd-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ffdbd-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ffdbd-118">Optional query parameters</span></span>
<span data-ttu-id="ffdbd-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ffdbd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ffdbd-120">Request headers</span></span>
|<span data-ttu-id="ffdbd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffdbd-121">Header</span></span>|<span data-ttu-id="ffdbd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ffdbd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ffdbd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ffdbd-123">Authorization</span></span>|<span data-ttu-id="ffdbd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ffdbd-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ffdbd-125">Accept</span></span>|<span data-ttu-id="ffdbd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ffdbd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ffdbd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ffdbd-127">Request body</span></span>
<span data-ttu-id="ffdbd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ffdbd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffdbd-129">Response</span></span>
<span data-ttu-id="ffdbd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-130">If successful, this method returns a `200 OK` response code and [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ffdbd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffdbd-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ffdbd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ffdbd-132">Request</span></span>
<span data-ttu-id="ffdbd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

### <a name="response"></a><span data-ttu-id="ffdbd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffdbd-134">Response</span></span>
<span data-ttu-id="ffdbd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ffdbd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 810

{
  "value": {
    "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
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
      "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
      "packageId": "Package Id value"
    },
    "id": "0e064997-4997-0e06-9749-060e9749060e",
    "version": "Version value"
  }
}
```



