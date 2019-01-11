---
title: Enumerar managedAppStatusRaws
description: Enumere las propiedades y las relaciones de los objetos managedAppStatusRaw.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7dd30f4731042307f543bde7420795b95bc496bd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828801"
---
# <a name="list-managedappstatusraws"></a><span data-ttu-id="0d2e0-103">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="0d2e0-103">List managedAppStatusRaws</span></span>

> <span data-ttu-id="0d2e0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0d2e0-105">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="0d2e0-105">List properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0d2e0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0d2e0-106">Prerequisites</span></span>
<span data-ttu-id="0d2e0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0d2e0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0d2e0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0d2e0-109">Permission type</span></span>|<span data-ttu-id="0d2e0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0d2e0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0d2e0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0d2e0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0d2e0-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="0d2e0-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="0d2e0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0d2e0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0d2e0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-114">Not supported.</span></span>|
|<span data-ttu-id="0d2e0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0d2e0-115">Application</span></span>|<span data-ttu-id="0d2e0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0d2e0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0d2e0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppStatuses
```

## <a name="request-headers"></a><span data-ttu-id="0d2e0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d2e0-118">Request headers</span></span>
|<span data-ttu-id="0d2e0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d2e0-119">Header</span></span>|<span data-ttu-id="0d2e0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0d2e0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0d2e0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="0d2e0-121">Authorization</span></span>|<span data-ttu-id="0d2e0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0d2e0-123">Accept</span><span class="sxs-lookup"><span data-stu-id="0d2e0-123">Accept</span></span>|<span data-ttu-id="0d2e0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0d2e0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0d2e0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0d2e0-125">Request body</span></span>
<span data-ttu-id="0d2e0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0d2e0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d2e0-127">Response</span></span>
<span data-ttu-id="0d2e0-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-128">If successful, this method returns a `200 OK` response code and a collection of [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0d2e0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d2e0-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="0d2e0-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d2e0-130">Request</span></span>
<span data-ttu-id="0d2e0-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppStatuses
```

### <a name="response"></a><span data-ttu-id="0d2e0-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d2e0-132">Response</span></span>
<span data-ttu-id="0d2e0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 307

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppStatusRaw",
      "displayName": "Display Name value",
      "id": "80847581-7581-8084-8175-848081758480",
      "version": "Version value",
      "content": {
        "@odata.type": "microsoft.graph.Json"
      }
    }
  ]
}
```



