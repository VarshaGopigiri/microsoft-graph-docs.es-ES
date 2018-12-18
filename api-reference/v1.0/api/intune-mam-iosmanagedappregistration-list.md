---
title: Enumerar iosManagedAppRegistrations
description: Enumere las propiedades y las relaciones de los objetos iosManagedAppRegistration.
author: tfitzmac
ms.openlocfilehash: 9247548a2075e5567b1ae44487ab266b3fa1d05e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311819"
---
# <a name="list-iosmanagedappregistrations"></a><span data-ttu-id="a5330-103">Enumerar iosManagedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="a5330-103">List iosManagedAppRegistrations</span></span>

> <span data-ttu-id="a5330-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a5330-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a5330-105">Enumere las propiedades y las relaciones de los objetos [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a5330-105">List properties and relationships of the [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a5330-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a5330-106">Prerequisites</span></span>
<span data-ttu-id="a5330-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5330-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5330-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5330-109">Permission type</span></span>|<span data-ttu-id="a5330-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5330-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a5330-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5330-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a5330-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="a5330-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="a5330-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5330-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a5330-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5330-114">Not supported.</span></span>|
|<span data-ttu-id="a5330-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5330-115">Application</span></span>|<span data-ttu-id="a5330-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5330-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a5330-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5330-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="a5330-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5330-118">Request headers</span></span>
|<span data-ttu-id="a5330-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5330-119">Header</span></span>|<span data-ttu-id="a5330-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a5330-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a5330-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a5330-121">Authorization</span></span>|<span data-ttu-id="a5330-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a5330-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a5330-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a5330-123">Accept</span></span>|<span data-ttu-id="a5330-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a5330-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5330-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5330-125">Request body</span></span>
<span data-ttu-id="a5330-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a5330-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a5330-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5330-127">Response</span></span>
<span data-ttu-id="a5330-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5330-128">If successful, this method returns a `200 OK` response code and a collection of [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5330-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5330-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="a5330-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5330-130">Request</span></span>
<span data-ttu-id="a5330-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5330-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="a5330-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5330-132">Response</span></span>
<span data-ttu-id="a5330-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5330-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 852

{
  "value": [
    {
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
  ]
}
```



