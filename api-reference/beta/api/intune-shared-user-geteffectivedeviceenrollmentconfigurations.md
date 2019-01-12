---
title: getEffectiveDeviceEnrollmentConfigurations (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 90b997c438f2fd313bc25f08e624f8a22acd22d1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933634"
---
# <a name="geteffectivedeviceenrollmentconfigurations-function"></a><span data-ttu-id="0070e-103">getEffectiveDeviceEnrollmentConfigurations (función)</span><span class="sxs-lookup"><span data-stu-id="0070e-103">getEffectiveDeviceEnrollmentConfigurations function</span></span>

> <span data-ttu-id="0070e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0070e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0070e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0070e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0070e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0070e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0070e-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0070e-107">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0070e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0070e-108">Prerequisites</span></span>

<span data-ttu-id="0070e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0070e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0070e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0070e-111">Permission type</span></span>|<span data-ttu-id="0070e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0070e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0070e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0070e-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="0070e-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="0070e-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="0070e-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0070e-115">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="0070e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0070e-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0070e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0070e-117">Not supported.</span></span>|
|<span data-ttu-id="0070e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0070e-118">Application</span></span>|<span data-ttu-id="0070e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0070e-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0070e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0070e-120">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getEffectiveDeviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="0070e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0070e-121">Request headers</span></span>

|<span data-ttu-id="0070e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0070e-122">Header</span></span>|<span data-ttu-id="0070e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0070e-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0070e-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="0070e-124">Authorization</span></span>|<span data-ttu-id="0070e-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0070e-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0070e-126">Accept</span><span class="sxs-lookup"><span data-stu-id="0070e-126">Accept</span></span>|<span data-ttu-id="0070e-127">application/json</span><span class="sxs-lookup"><span data-stu-id="0070e-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0070e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0070e-128">Request body</span></span>

<span data-ttu-id="0070e-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0070e-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0070e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0070e-130">Response</span></span>

<span data-ttu-id="0070e-131">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y una colección de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0070e-131">If successful, this function returns a `200 OK` response code and a [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0070e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0070e-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="0070e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0070e-133">Request</span></span>

<span data-ttu-id="0070e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0070e-134">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users/{usersId}/getEffectiveDeviceEnrollmentConfigurations
```

### <a name="response"></a><span data-ttu-id="0070e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0070e-135">Response</span></span>

<span data-ttu-id="0070e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0070e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



