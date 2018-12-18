---
title: Enumerar managedAppStatusRaws
description: Enumere las propiedades y las relaciones de los objetos managedAppStatusRaw.
author: tfitzmac
ms.openlocfilehash: 5be953f243ffc0c24d72387dbea11513d8d202cb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301669"
---
# <a name="list-managedappstatusraws"></a><span data-ttu-id="6c363-103">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="6c363-103">List managedAppStatusRaws</span></span>

> <span data-ttu-id="6c363-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6c363-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6c363-105">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="6c363-105">List properties and relationships of the [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6c363-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6c363-106">Prerequisites</span></span>
<span data-ttu-id="6c363-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6c363-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6c363-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c363-109">Permission type</span></span>|<span data-ttu-id="6c363-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c363-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6c363-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c363-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6c363-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="6c363-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="6c363-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c363-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6c363-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c363-114">Not supported.</span></span>|
|<span data-ttu-id="6c363-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c363-115">Application</span></span>|<span data-ttu-id="6c363-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c363-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6c363-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c363-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppStatuses
```

## <a name="request-headers"></a><span data-ttu-id="6c363-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c363-118">Request headers</span></span>
|<span data-ttu-id="6c363-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c363-119">Header</span></span>|<span data-ttu-id="6c363-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6c363-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6c363-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="6c363-121">Authorization</span></span>|<span data-ttu-id="6c363-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6c363-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6c363-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6c363-123">Accept</span></span>|<span data-ttu-id="6c363-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6c363-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6c363-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c363-125">Request body</span></span>
<span data-ttu-id="6c363-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6c363-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6c363-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c363-127">Response</span></span>
<span data-ttu-id="6c363-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c363-128">If successful, this method returns a `200 OK` response code and a collection of [managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6c363-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c363-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="6c363-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c363-130">Request</span></span>
<span data-ttu-id="6c363-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c363-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppStatuses
```

### <a name="response"></a><span data-ttu-id="6c363-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c363-132">Response</span></span>
<span data-ttu-id="6c363-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c363-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



