---
title: Enumerar windows10EnterpriseModernAppManagementConfigurations
description: Enumere las propiedades y las relaciones de los objetos windows10EnterpriseModernAppManagementConfiguration.
ms.openlocfilehash: 0b6e2e155d9d5dbc0c1bfa3cfc95153580873f40
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030614"
---
# <a name="list-windows10enterprisemodernappmanagementconfigurations"></a><span data-ttu-id="9c03f-103">Enumerar windows10EnterpriseModernAppManagementConfigurations</span><span class="sxs-lookup"><span data-stu-id="9c03f-103">List windows10EnterpriseModernAppManagementConfigurations</span></span>

> <span data-ttu-id="9c03f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9c03f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9c03f-105">Enumere las propiedades y las relaciones de los objetos [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9c03f-105">List properties and relationships of the [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9c03f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9c03f-106">Prerequisites</span></span>
<span data-ttu-id="9c03f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9c03f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9c03f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c03f-109">Permission type</span></span>|<span data-ttu-id="9c03f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c03f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9c03f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c03f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9c03f-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9c03f-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9c03f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c03f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9c03f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c03f-114">Not supported.</span></span>|
|<span data-ttu-id="9c03f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c03f-115">Application</span></span>|<span data-ttu-id="9c03f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c03f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9c03f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c03f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9c03f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c03f-118">Request headers</span></span>
|<span data-ttu-id="9c03f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c03f-119">Header</span></span>|<span data-ttu-id="9c03f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9c03f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9c03f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9c03f-121">Authorization</span></span>|<span data-ttu-id="9c03f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9c03f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9c03f-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9c03f-123">Accept</span></span>|<span data-ttu-id="9c03f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9c03f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9c03f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c03f-125">Request body</span></span>
<span data-ttu-id="9c03f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9c03f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9c03f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c03f-127">Response</span></span>
<span data-ttu-id="9c03f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c03f-128">If successful, this method returns a `200 OK` response code and a collection of [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9c03f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c03f-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="9c03f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c03f-130">Request</span></span>
<span data-ttu-id="9c03f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c03f-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="9c03f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c03f-132">Response</span></span>
<span data-ttu-id="9c03f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c03f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 459

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows10EnterpriseModernAppManagementConfiguration",
      "id": "d6577687-7687-d657-8776-57d6877657d6",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "uninstallBuiltInApps": true
    }
  ]
}
```



