---
title: Obtener userAppInstallStatus
description: Leer las propiedades y las relaciones del objeto userAppInstallStatus.
ms.openlocfilehash: 98716dddb7ad6a649d8e847fa13c5a4eff1f39f4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089302"
---
# <a name="get-userappinstallstatus"></a><span data-ttu-id="5205d-103">Obtener userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="5205d-103">Get userAppInstallStatus</span></span>

> <span data-ttu-id="5205d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5205d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5205d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5205d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5205d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5205d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5205d-107">Leer las propiedades y las relaciones del objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5205d-107">Read properties and relationships of the [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5205d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5205d-108">Prerequisites</span></span>
<span data-ttu-id="5205d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5205d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5205d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5205d-111">Permission type</span></span>|<span data-ttu-id="5205d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5205d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5205d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5205d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5205d-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="5205d-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="5205d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5205d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5205d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5205d-116">Not supported.</span></span>|
|<span data-ttu-id="5205d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5205d-117">Application</span></span>|<span data-ttu-id="5205d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5205d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5205d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5205d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="5205d-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5205d-120">Optional query parameters</span></span>
<span data-ttu-id="5205d-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5205d-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="5205d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5205d-122">Request headers</span></span>
|<span data-ttu-id="5205d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5205d-123">Header</span></span>|<span data-ttu-id="5205d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5205d-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5205d-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="5205d-125">Authorization</span></span>|<span data-ttu-id="5205d-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5205d-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5205d-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5205d-127">Accept</span></span>|<span data-ttu-id="5205d-128">application/json</span><span class="sxs-lookup"><span data-stu-id="5205d-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5205d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5205d-129">Request body</span></span>
<span data-ttu-id="5205d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5205d-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5205d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5205d-131">Response</span></span>
<span data-ttu-id="5205d-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5205d-132">If successful, this method returns a `200 OK` response code and [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5205d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5205d-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="5205d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5205d-134">Request</span></span>
<span data-ttu-id="5205d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5205d-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}
```

### <a name="response"></a><span data-ttu-id="5205d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5205d-136">Response</span></span>
<span data-ttu-id="5205d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5205d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 321

{
  "value": {
    "@odata.type": "#microsoft.graph.userAppInstallStatus",
    "id": "14959a2a-9a2a-1495-2a9a-95142a9a9514",
    "userName": "User Name value",
    "userPrincipalName": "User Principal Name value",
    "installedDeviceCount": 4,
    "failedDeviceCount": 1,
    "notInstalledDeviceCount": 7
  }
}
```





