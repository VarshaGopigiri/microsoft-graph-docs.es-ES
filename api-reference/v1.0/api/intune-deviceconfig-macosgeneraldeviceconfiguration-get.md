---
title: Obtener macOSGeneralDeviceConfiguration
description: Lea las propiedades y las relaciones del objeto macOSGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c26f2f04a0c77ea4bb17ef160a573e40a5811b0a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823740"
---
# <a name="get-macosgeneraldeviceconfiguration"></a><span data-ttu-id="a7394-103">Obtener macOSGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7394-103">Get macOSGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="a7394-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7394-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7394-105">Lea las propiedades y las relaciones del objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a7394-105">Read properties and relationships of the [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a7394-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a7394-106">Prerequisites</span></span>
<span data-ttu-id="a7394-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7394-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7394-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7394-109">Permission type</span></span>|<span data-ttu-id="a7394-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7394-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a7394-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7394-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a7394-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7394-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a7394-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7394-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a7394-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7394-114">Not supported.</span></span>|
|<span data-ttu-id="a7394-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7394-115">Application</span></span>|<span data-ttu-id="a7394-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7394-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a7394-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7394-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a7394-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a7394-118">Optional query parameters</span></span>
<span data-ttu-id="a7394-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7394-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a7394-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7394-120">Request headers</span></span>
|<span data-ttu-id="a7394-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7394-121">Header</span></span>|<span data-ttu-id="a7394-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a7394-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a7394-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a7394-123">Authorization</span></span>|<span data-ttu-id="a7394-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a7394-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a7394-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a7394-125">Accept</span></span>|<span data-ttu-id="a7394-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a7394-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a7394-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7394-127">Request body</span></span>
<span data-ttu-id="a7394-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7394-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7394-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7394-129">Response</span></span>
<span data-ttu-id="a7394-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7394-130">If successful, this method returns a `200 OK` response code and [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7394-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7394-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a7394-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7394-132">Request</span></span>
<span data-ttu-id="a7394-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7394-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="a7394-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7394-134">Response</span></span>
<span data-ttu-id="a7394-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7394-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1155

{
  "value": {
    "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
    "id": "dc356aee-6aee-dc35-ee6a-35dcee6a35dc",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "compliantAppsList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "compliantAppListType": "appsInListCompliant",
    "emailInDomainSuffixes": [
      "Email In Domain Suffixes value"
    ],
    "passwordBlockSimple": true,
    "passwordExpirationDays": 6,
    "passwordMinimumCharacterSetCount": 0,
    "passwordMinimumLength": 5,
    "passwordMinutesOfInactivityBeforeLock": 5,
    "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
    "passwordPreviousPasswordBlockCount": 2,
    "passwordRequiredType": "alphanumeric",
    "passwordRequired": true
  }
}
```



