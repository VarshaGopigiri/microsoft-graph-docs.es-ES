---
title: Enumerar androidManagedAppRegistrations
description: Enumere las propiedades y las relaciones de los objetos androidManagedAppRegistration.
author: tfitzmac
ms.openlocfilehash: e6fb7364e9b3dbef0fff3ca0e779d2740316f6f3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343375"
---
# <a name="list-androidmanagedappregistrations"></a><span data-ttu-id="c061a-103">Enumerar androidManagedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="c061a-103">List androidManagedAppRegistrations</span></span>

> <span data-ttu-id="c061a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c061a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c061a-105">Enumere las propiedades y las relaciones de los objetos [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="c061a-105">List properties and relationships of the [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c061a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c061a-106">Prerequisites</span></span>
<span data-ttu-id="c061a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c061a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c061a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c061a-109">Permission type</span></span>|<span data-ttu-id="c061a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c061a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c061a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c061a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c061a-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="c061a-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="c061a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c061a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c061a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c061a-114">Not supported.</span></span>|
|<span data-ttu-id="c061a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c061a-115">Application</span></span>|<span data-ttu-id="c061a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c061a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c061a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c061a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="c061a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c061a-118">Request headers</span></span>
|<span data-ttu-id="c061a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c061a-119">Header</span></span>|<span data-ttu-id="c061a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c061a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c061a-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c061a-121">Authorization</span></span>|<span data-ttu-id="c061a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c061a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c061a-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c061a-123">Accept</span></span>|<span data-ttu-id="c061a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c061a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c061a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c061a-125">Request body</span></span>
<span data-ttu-id="c061a-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c061a-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c061a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c061a-127">Response</span></span>
<span data-ttu-id="c061a-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c061a-128">If successful, this method returns a `200 OK` response code and a collection of [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c061a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c061a-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="c061a-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c061a-130">Request</span></span>
<span data-ttu-id="c061a-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c061a-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="c061a-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c061a-132">Response</span></span>
<span data-ttu-id="c061a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c061a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 862

{
  "value": [
    {
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
  ]
}
```



