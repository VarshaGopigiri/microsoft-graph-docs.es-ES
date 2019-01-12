---
title: Obtener editionUpgradeConfiguration
description: Lea las propiedades y las relaciones del objeto editionUpgradeConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8701fc9420d4e659ddd138cae37ff4eb66483032
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953816"
---
# <a name="get-editionupgradeconfiguration"></a><span data-ttu-id="17f05-103">Obtener editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="17f05-103">Get editionUpgradeConfiguration</span></span>

> <span data-ttu-id="17f05-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17f05-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17f05-105">Lea las propiedades y las relaciones del objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="17f05-105">Read properties and relationships of the [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="17f05-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="17f05-106">Prerequisites</span></span>
<span data-ttu-id="17f05-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17f05-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17f05-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17f05-109">Permission type</span></span>|<span data-ttu-id="17f05-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17f05-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="17f05-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17f05-111">Delegated (work or school account)</span></span>|<span data-ttu-id="17f05-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="17f05-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="17f05-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17f05-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="17f05-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17f05-114">Not supported.</span></span>|
|<span data-ttu-id="17f05-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17f05-115">Application</span></span>|<span data-ttu-id="17f05-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17f05-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="17f05-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17f05-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="17f05-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="17f05-118">Optional query parameters</span></span>
<span data-ttu-id="17f05-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17f05-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="17f05-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17f05-120">Request headers</span></span>
|<span data-ttu-id="17f05-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17f05-121">Header</span></span>|<span data-ttu-id="17f05-122">Valor</span><span class="sxs-lookup"><span data-stu-id="17f05-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="17f05-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="17f05-123">Authorization</span></span>|<span data-ttu-id="17f05-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="17f05-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="17f05-125">Accept</span><span class="sxs-lookup"><span data-stu-id="17f05-125">Accept</span></span>|<span data-ttu-id="17f05-126">application/json</span><span class="sxs-lookup"><span data-stu-id="17f05-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="17f05-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17f05-127">Request body</span></span>
<span data-ttu-id="17f05-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17f05-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17f05-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17f05-129">Response</span></span>
<span data-ttu-id="17f05-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17f05-130">If successful, this method returns a `200 OK` response code and [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17f05-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17f05-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="17f05-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17f05-132">Request</span></span>
<span data-ttu-id="17f05-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17f05-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="17f05-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17f05-134">Response</span></span>
<span data-ttu-id="17f05-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17f05-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 524

{
  "value": {
    "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
    "id": "f39fc471-c471-f39f-71c4-9ff371c49ff3",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "licenseType": "licenseFile",
    "targetEdition": "windows10EnterpriseN",
    "license": "License value",
    "productKey": "Product Key value"
  }
}
```



