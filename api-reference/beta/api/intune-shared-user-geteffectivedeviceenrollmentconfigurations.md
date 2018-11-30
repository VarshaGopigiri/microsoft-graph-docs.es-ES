---
title: getEffectiveDeviceEnrollmentConfigurations (función)
description: Todavía no documentado
ms.openlocfilehash: dffde709d57d9cb138bb163da66f6ec24e6a2d5d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090844"
---
# <a name="geteffectivedeviceenrollmentconfigurations-function"></a><span data-ttu-id="a81c7-103">getEffectiveDeviceEnrollmentConfigurations (función)</span><span class="sxs-lookup"><span data-stu-id="a81c7-103">getEffectiveDeviceEnrollmentConfigurations function</span></span>

> <span data-ttu-id="a81c7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a81c7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a81c7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a81c7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a81c7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a81c7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a81c7-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a81c7-107">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a81c7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a81c7-108">Prerequisites</span></span>

<span data-ttu-id="a81c7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a81c7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a81c7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a81c7-111">Permission type</span></span>|<span data-ttu-id="a81c7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a81c7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a81c7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a81c7-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="a81c7-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="a81c7-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="a81c7-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a81c7-115">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="a81c7-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a81c7-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a81c7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a81c7-117">Not supported.</span></span>|
|<span data-ttu-id="a81c7-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a81c7-118">Application</span></span>|<span data-ttu-id="a81c7-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a81c7-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a81c7-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a81c7-120">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getEffectiveDeviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a81c7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a81c7-121">Request headers</span></span>

|<span data-ttu-id="a81c7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a81c7-122">Header</span></span>|<span data-ttu-id="a81c7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a81c7-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a81c7-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a81c7-124">Authorization</span></span>|<span data-ttu-id="a81c7-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a81c7-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a81c7-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a81c7-126">Accept</span></span>|<span data-ttu-id="a81c7-127">application/json</span><span class="sxs-lookup"><span data-stu-id="a81c7-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a81c7-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a81c7-128">Request body</span></span>

<span data-ttu-id="a81c7-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a81c7-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a81c7-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a81c7-130">Response</span></span>

<span data-ttu-id="a81c7-131">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y una colección de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a81c7-131">If successful, this function returns a `200 OK` response code and a [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a81c7-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a81c7-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="a81c7-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a81c7-133">Request</span></span>

<span data-ttu-id="a81c7-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a81c7-134">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users/{usersId}/getEffectiveDeviceEnrollmentConfigurations
```

### <a name="response"></a><span data-ttu-id="a81c7-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a81c7-135">Response</span></span>

<span data-ttu-id="a81c7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a81c7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 422

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceEnrollmentConfiguration",
      "id": "df13d8b9-d8b9-df13-b9d8-13dfb9d813df",
      "displayName": "Display Name value",
      "description": "Description value",
      "priority": 8,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "version": 7
    }
  ]
}
```


