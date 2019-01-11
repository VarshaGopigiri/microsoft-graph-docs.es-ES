---
title: Actualizar deviceManagementExchangeConnector
description: Actualice las propiedades de un objeto deviceManagementExchangeConnector.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5bb6a490f5f192a673a050f9c4711fd4981665d3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865999"
---
# <a name="update-devicemanagementexchangeconnector"></a><span data-ttu-id="224c9-103">Actualizar deviceManagementExchangeConnector</span><span class="sxs-lookup"><span data-stu-id="224c9-103">Update deviceManagementExchangeConnector</span></span>

> <span data-ttu-id="224c9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="224c9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="224c9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="224c9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="224c9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="224c9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="224c9-107">Actualice las propiedades de un objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="224c9-107">Update the properties of a [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="224c9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="224c9-108">Prerequisites</span></span>
<span data-ttu-id="224c9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="224c9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="224c9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="224c9-111">Permission type</span></span>|<span data-ttu-id="224c9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="224c9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="224c9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="224c9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="224c9-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="224c9-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="224c9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="224c9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="224c9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="224c9-116">Not supported.</span></span>|
|<span data-ttu-id="224c9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="224c9-117">Application</span></span>|<span data-ttu-id="224c9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="224c9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="224c9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="224c9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="224c9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="224c9-120">Request headers</span></span>
|<span data-ttu-id="224c9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="224c9-121">Header</span></span>|<span data-ttu-id="224c9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="224c9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="224c9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="224c9-123">Authorization</span></span>|<span data-ttu-id="224c9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="224c9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="224c9-125">Accept</span><span class="sxs-lookup"><span data-stu-id="224c9-125">Accept</span></span>|<span data-ttu-id="224c9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="224c9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="224c9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="224c9-127">Request body</span></span>
<span data-ttu-id="224c9-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="224c9-128">In the request body, supply a JSON representation for the [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object.</span></span>

<span data-ttu-id="224c9-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="224c9-129">The following table shows the properties that are required when you create the [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span></span>

|<span data-ttu-id="224c9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="224c9-130">Property</span></span>|<span data-ttu-id="224c9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="224c9-131">Type</span></span>|<span data-ttu-id="224c9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="224c9-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="224c9-133">id</span><span class="sxs-lookup"><span data-stu-id="224c9-133">id</span></span>|<span data-ttu-id="224c9-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="224c9-134">String</span></span>|<span data-ttu-id="224c9-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="224c9-135">Not yet documented</span></span>|
|<span data-ttu-id="224c9-136">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="224c9-136">lastSyncDateTime</span></span>|<span data-ttu-id="224c9-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="224c9-137">DateTimeOffset</span></span>|<span data-ttu-id="224c9-138">Última hora de sincronización para Exchange Connector</span><span class="sxs-lookup"><span data-stu-id="224c9-138">Last sync time for the Exchange Connector</span></span>|
|<span data-ttu-id="224c9-139">status</span><span class="sxs-lookup"><span data-stu-id="224c9-139">status</span></span>|[<span data-ttu-id="224c9-140">deviceManagementExchangeConnectorStatus</span><span class="sxs-lookup"><span data-stu-id="224c9-140">deviceManagementExchangeConnectorStatus</span></span>](../resources/intune-onboarding-devicemanagementexchangeconnectorstatus.md)|<span data-ttu-id="224c9-141">Estado del conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="224c9-141">Exchange Connector Status.</span></span> <span data-ttu-id="224c9-142">Los valores posibles son: `none`, `connectionPending`, `connected` y `disconnected`.</span><span class="sxs-lookup"><span data-stu-id="224c9-142">Possible values are: `none`, `connectionPending`, `connected`, `disconnected`.</span></span>|
|<span data-ttu-id="224c9-143">primarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="224c9-143">primarySmtpAddress</span></span>|<span data-ttu-id="224c9-144">String</span><span class="sxs-lookup"><span data-stu-id="224c9-144">String</span></span>|<span data-ttu-id="224c9-145">Dirección de correo electrónico que se usó para configurar el Exchange Connector de Service To Service.</span><span class="sxs-lookup"><span data-stu-id="224c9-145">Email address used to configure the Service To Service Exchange Connector.</span></span>|
|<span data-ttu-id="224c9-146">serverName</span><span class="sxs-lookup"><span data-stu-id="224c9-146">serverName</span></span>|<span data-ttu-id="224c9-147">String</span><span class="sxs-lookup"><span data-stu-id="224c9-147">String</span></span>|<span data-ttu-id="224c9-148">El nombre del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="224c9-148">The name of the Exchange server.</span></span>|
|<span data-ttu-id="224c9-149">connectorServerName</span><span class="sxs-lookup"><span data-stu-id="224c9-149">connectorServerName</span></span>|<span data-ttu-id="224c9-150">String</span><span class="sxs-lookup"><span data-stu-id="224c9-150">String</span></span>|<span data-ttu-id="224c9-151">El nombre del servidor que hospeda el Exchange Connector.</span><span class="sxs-lookup"><span data-stu-id="224c9-151">The name of the server hosting the Exchange Connector.</span></span>|
|<span data-ttu-id="224c9-152">exchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="224c9-152">exchangeConnectorType</span></span>|[<span data-ttu-id="224c9-153">deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="224c9-153">deviceManagementExchangeConnectorType</span></span>](../resources/intune-onboarding-devicemanagementexchangeconnectortype.md)|<span data-ttu-id="224c9-154">El tipo de Exchange Connector configurado.</span><span class="sxs-lookup"><span data-stu-id="224c9-154">The type of Exchange Connector Configured.</span></span> <span data-ttu-id="224c9-155">Los valores posibles son: `onPremises`, `hosted`, `serviceToService` y `dedicated`.</span><span class="sxs-lookup"><span data-stu-id="224c9-155">Possible values are: `onPremises`, `hosted`, `serviceToService`, `dedicated`.</span></span>|
|<span data-ttu-id="224c9-156">version</span><span class="sxs-lookup"><span data-stu-id="224c9-156">version</span></span>|<span data-ttu-id="224c9-157">String</span><span class="sxs-lookup"><span data-stu-id="224c9-157">String</span></span>|<span data-ttu-id="224c9-158">La versión del ExchangeConnectorAgent</span><span class="sxs-lookup"><span data-stu-id="224c9-158">The version of the ExchangeConnectorAgent</span></span>|
|<span data-ttu-id="224c9-159">exchangeAlias</span><span class="sxs-lookup"><span data-stu-id="224c9-159">exchangeAlias</span></span>|<span data-ttu-id="224c9-160">String</span><span class="sxs-lookup"><span data-stu-id="224c9-160">String</span></span>|<span data-ttu-id="224c9-161">Un alias asignado al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="224c9-161">An alias assigned to the Exchange server</span></span>|
|<span data-ttu-id="224c9-162">exchangeOrganization</span><span class="sxs-lookup"><span data-stu-id="224c9-162">exchangeOrganization</span></span>|<span data-ttu-id="224c9-163">String</span><span class="sxs-lookup"><span data-stu-id="224c9-163">String</span></span>|<span data-ttu-id="224c9-164">Organización de Exchange al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="224c9-164">Exchange Organization to the Exchange server</span></span>|



## <a name="response"></a><span data-ttu-id="224c9-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="224c9-165">Response</span></span>
<span data-ttu-id="224c9-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="224c9-166">If successful, this method returns a `200 OK` response code and an updated [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="224c9-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="224c9-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="224c9-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="224c9-168">Request</span></span>
<span data-ttu-id="224c9-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="224c9-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
Content-type: application/json
Content-length: 418

{
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "status": "connectionPending",
  "primarySmtpAddress": "Primary Smtp Address value",
  "serverName": "Server Name value",
  "connectorServerName": "Connector Server Name value",
  "exchangeConnectorType": "hosted",
  "version": "Version value",
  "exchangeAlias": "Exchange Alias value",
  "exchangeOrganization": "Exchange Organization value"
}
```

### <a name="response"></a><span data-ttu-id="224c9-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="224c9-170">Response</span></span>
<span data-ttu-id="224c9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="224c9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 539

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
  "id": "e11c1de8-1de8-e11c-e81d-1ce1e81d1ce1",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "status": "connectionPending",
  "primarySmtpAddress": "Primary Smtp Address value",
  "serverName": "Server Name value",
  "connectorServerName": "Connector Server Name value",
  "exchangeConnectorType": "hosted",
  "version": "Version value",
  "exchangeAlias": "Exchange Alias value",
  "exchangeOrganization": "Exchange Organization value"
}
```





