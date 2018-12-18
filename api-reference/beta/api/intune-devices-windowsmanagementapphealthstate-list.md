---
title: Lista windowsManagementAppHealthStates
description: Propiedades de la lista y relaciones de los objetos windowsManagementAppHealthState.
author: tfitzmac
ms.openlocfilehash: 68f1c1b1c59d1a70590356b791fcbf1dc25fd6c5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362793"
---
# <a name="list-windowsmanagementapphealthstates"></a><span data-ttu-id="31057-103">Lista windowsManagementAppHealthStates</span><span class="sxs-lookup"><span data-stu-id="31057-103">List windowsManagementAppHealthStates</span></span>

> <span data-ttu-id="31057-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31057-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31057-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31057-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="31057-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31057-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31057-107">Propiedades de la lista y relaciones de los objetos [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .</span><span class="sxs-lookup"><span data-stu-id="31057-107">List properties and relationships of the [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="31057-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="31057-108">Prerequisites</span></span>
<span data-ttu-id="31057-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31057-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31057-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31057-111">Permission type</span></span>|<span data-ttu-id="31057-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31057-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="31057-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31057-113">Delegated (work or school account)</span></span>|<span data-ttu-id="31057-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="31057-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="31057-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31057-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="31057-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31057-116">Not supported.</span></span>|
|<span data-ttu-id="31057-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31057-117">Application</span></span>|<span data-ttu-id="31057-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31057-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="31057-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31057-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/windowsManagementApp/healthStates
```

## <a name="request-headers"></a><span data-ttu-id="31057-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31057-120">Request headers</span></span>
|<span data-ttu-id="31057-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31057-121">Header</span></span>|<span data-ttu-id="31057-122">Valor</span><span class="sxs-lookup"><span data-stu-id="31057-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="31057-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="31057-123">Authorization</span></span>|<span data-ttu-id="31057-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="31057-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="31057-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="31057-125">Accept</span></span>|<span data-ttu-id="31057-126">application/json</span><span class="sxs-lookup"><span data-stu-id="31057-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="31057-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31057-127">Request body</span></span>
<span data-ttu-id="31057-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="31057-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="31057-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31057-129">Response</span></span>
<span data-ttu-id="31057-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31057-130">If successful, this method returns a `200 OK` response code and a collection of [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31057-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31057-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="31057-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31057-132">Request</span></span>
<span data-ttu-id="31057-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31057-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp/healthStates
```

### <a name="response"></a><span data-ttu-id="31057-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31057-134">Response</span></span>
<span data-ttu-id="31057-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31057-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 410

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsManagementAppHealthState",
      "id": "5c7e50fb-50fb-5c7e-fb50-7e5cfb507e5c",
      "healthState": "healthy",
      "installedVersion": "Installed Version value",
      "lastCheckInDateTime": "2016-12-31T23:59:56.413532-08:00",
      "deviceName": "Device Name value",
      "deviceOSVersion": "Device OSVersion value"
    }
  ]
}
```





