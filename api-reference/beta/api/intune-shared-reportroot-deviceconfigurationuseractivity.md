---
title: Función deviceConfigurationUserActivity
description: Metadatos para el informe de actividad de usuario de configuración de dispositivo
ms.openlocfilehash: d103f439048dd8c34173169c37541b6bfb9eeadf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089420"
---
# <a name="deviceconfigurationuseractivity-function"></a><span data-ttu-id="33ad5-103">Función deviceConfigurationUserActivity</span><span class="sxs-lookup"><span data-stu-id="33ad5-103">deviceConfigurationUserActivity function</span></span>

> <span data-ttu-id="33ad5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="33ad5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="33ad5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="33ad5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="33ad5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="33ad5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="33ad5-107">Metadatos para el informe de actividad de usuario de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="33ad5-107">Metadata for the device configuration user activity report</span></span>
## <a name="prerequisites"></a><span data-ttu-id="33ad5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="33ad5-108">Prerequisites</span></span>
<span data-ttu-id="33ad5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33ad5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="33ad5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33ad5-111">Permission type</span></span>|<span data-ttu-id="33ad5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33ad5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="33ad5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33ad5-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="33ad5-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="33ad5-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="33ad5-115">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="33ad5-115">DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="33ad5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33ad5-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="33ad5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33ad5-117">Not supported.</span></span>|
|<span data-ttu-id="33ad5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33ad5-118">Application</span></span>|<span data-ttu-id="33ad5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33ad5-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="33ad5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33ad5-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/deviceConfigurationUserActivity
```

## <a name="request-headers"></a><span data-ttu-id="33ad5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="33ad5-121">Request headers</span></span>
|<span data-ttu-id="33ad5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33ad5-122">Header</span></span>|<span data-ttu-id="33ad5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="33ad5-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="33ad5-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="33ad5-124">Authorization</span></span>|<span data-ttu-id="33ad5-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="33ad5-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="33ad5-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="33ad5-126">Accept</span></span>|<span data-ttu-id="33ad5-127">application/json</span><span class="sxs-lookup"><span data-stu-id="33ad5-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="33ad5-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33ad5-128">Request body</span></span>
<span data-ttu-id="33ad5-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="33ad5-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="33ad5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33ad5-130">Response</span></span>
<span data-ttu-id="33ad5-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33ad5-131">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="33ad5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33ad5-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="33ad5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33ad5-133">Request</span></span>
<span data-ttu-id="33ad5-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33ad5-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/deviceConfigurationUserActivity
```

### <a name="response"></a><span data-ttu-id="33ad5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33ad5-135">Response</span></span>
<span data-ttu-id="33ad5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="33ad5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 123

{
  "value": {
    "@odata.type": "microsoft.graph.report",
    "content": "<Unknown Primitive Type Edm.Stream>"
  }
}
```


