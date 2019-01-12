---
title: Enumerar managedAppRegistrations
description: Enumere las propiedades y las relaciones de los objetos managedAppRegistration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a6a0a8f7d16a3946d0ccecb674b534906e73ce8f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951407"
---
# <a name="list-managedappregistrations"></a><span data-ttu-id="51711-103">Enumerar managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="51711-103">List managedAppRegistrations</span></span>

> <span data-ttu-id="51711-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51711-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51711-105">Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="51711-105">List properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51711-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51711-106">Prerequisites</span></span>
<span data-ttu-id="51711-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51711-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51711-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51711-109">Permission type</span></span>|<span data-ttu-id="51711-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51711-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51711-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51711-111">Delegated (work or school account)</span></span>|<span data-ttu-id="51711-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="51711-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="51711-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51711-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51711-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51711-114">Not supported.</span></span>|
|<span data-ttu-id="51711-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51711-115">Application</span></span>|<span data-ttu-id="51711-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51711-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51711-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51711-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="51711-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51711-118">Request headers</span></span>
|<span data-ttu-id="51711-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51711-119">Header</span></span>|<span data-ttu-id="51711-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51711-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51711-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="51711-121">Authorization</span></span>|<span data-ttu-id="51711-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51711-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51711-123">Accept</span><span class="sxs-lookup"><span data-stu-id="51711-123">Accept</span></span>|<span data-ttu-id="51711-124">application/json</span><span class="sxs-lookup"><span data-stu-id="51711-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51711-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51711-125">Request body</span></span>
<span data-ttu-id="51711-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="51711-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="51711-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51711-127">Response</span></span>
<span data-ttu-id="51711-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51711-128">If successful, this method returns a `200 OK` response code and a collection of [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51711-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51711-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="51711-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51711-130">Request</span></span>
<span data-ttu-id="51711-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51711-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="51711-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51711-132">Response</span></span>
<span data-ttu-id="51711-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51711-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 806

{
  "value": [
    {
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
  ]
}
```



