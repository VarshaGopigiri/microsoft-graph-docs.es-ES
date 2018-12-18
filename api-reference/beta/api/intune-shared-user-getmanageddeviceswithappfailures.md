---
title: getManagedDevicesWithAppFailures (función)
description: Recupera la lista de dispositivos con aplicaciones con errores
author: tfitzmac
ms.openlocfilehash: 147ee26644c3e2c425f70434516e13b03407891b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352958"
---
# <a name="getmanageddeviceswithappfailures-function"></a><span data-ttu-id="40fe1-103">getManagedDevicesWithAppFailures (función)</span><span class="sxs-lookup"><span data-stu-id="40fe1-103">getManagedDevicesWithAppFailures function</span></span>

> <span data-ttu-id="40fe1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="40fe1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="40fe1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="40fe1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="40fe1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40fe1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40fe1-107">Recupera la lista de dispositivos con aplicaciones con errores</span><span class="sxs-lookup"><span data-stu-id="40fe1-107">Retrieves the list of devices with failed apps</span></span>
## <a name="prerequisites"></a><span data-ttu-id="40fe1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="40fe1-108">Prerequisites</span></span>
<span data-ttu-id="40fe1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="40fe1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="40fe1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40fe1-111">Permission type</span></span>|<span data-ttu-id="40fe1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40fe1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="40fe1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40fe1-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="40fe1-114">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="40fe1-114">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="40fe1-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="40fe1-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="40fe1-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40fe1-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="40fe1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40fe1-117">Not supported.</span></span>|
|<span data-ttu-id="40fe1-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40fe1-118">Application</span></span>|<span data-ttu-id="40fe1-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40fe1-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="40fe1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40fe1-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedDevicesWithAppFailures
```

## <a name="request-headers"></a><span data-ttu-id="40fe1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="40fe1-121">Request headers</span></span>
|<span data-ttu-id="40fe1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40fe1-122">Header</span></span>|<span data-ttu-id="40fe1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="40fe1-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="40fe1-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="40fe1-124">Authorization</span></span>|<span data-ttu-id="40fe1-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="40fe1-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="40fe1-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="40fe1-126">Accept</span></span>|<span data-ttu-id="40fe1-127">application/json</span><span class="sxs-lookup"><span data-stu-id="40fe1-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="40fe1-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40fe1-128">Request body</span></span>
<span data-ttu-id="40fe1-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="40fe1-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="40fe1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40fe1-130">Response</span></span>
<span data-ttu-id="40fe1-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40fe1-131">If successful, this function returns a `200 OK` response code and a String collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="40fe1-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40fe1-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="40fe1-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="40fe1-133">Request</span></span>
<span data-ttu-id="40fe1-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40fe1-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/getManagedDevicesWithAppFailures
```

### <a name="response"></a><span data-ttu-id="40fe1-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40fe1-135">Response</span></span>
<span data-ttu-id="40fe1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="40fe1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 74

{
  "value": [
    "Get Managed Devices With App Failures value"
  ]
}
```





