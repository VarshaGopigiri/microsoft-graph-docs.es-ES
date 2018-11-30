---
title: Actualizar deviceManagementExchangeConnector
description: Actualice las propiedades de un objeto deviceManagementExchangeConnector.
ms.openlocfilehash: ed63339a390a5fcba377236de8ddfe6c9b57bd5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030410"
---
# <a name="update-devicemanagementexchangeconnector"></a><span data-ttu-id="e7df8-103">Actualizar deviceManagementExchangeConnector</span><span class="sxs-lookup"><span data-stu-id="e7df8-103">Update deviceManagementExchangeConnector</span></span>

> <span data-ttu-id="e7df8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7df8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7df8-105">Actualice las propiedades de un objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="e7df8-105">Update the properties of a [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7df8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7df8-106">Prerequisites</span></span>
<span data-ttu-id="e7df8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7df8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7df8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7df8-109">Permission type</span></span>|<span data-ttu-id="e7df8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7df8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7df8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7df8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e7df8-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7df8-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e7df8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7df8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7df8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7df8-114">Not supported.</span></span>|
|<span data-ttu-id="e7df8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7df8-115">Application</span></span>|<span data-ttu-id="e7df8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7df8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7df8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7df8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="e7df8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7df8-118">Request headers</span></span>
|<span data-ttu-id="e7df8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7df8-119">Header</span></span>|<span data-ttu-id="e7df8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e7df8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7df8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e7df8-121">Authorization</span></span>|<span data-ttu-id="e7df8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e7df8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e7df8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e7df8-123">Accept</span></span>|<span data-ttu-id="e7df8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e7df8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7df8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7df8-125">Request body</span></span>
<span data-ttu-id="e7df8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="e7df8-126">In the request body, supply a JSON representation for the [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object.</span></span>

<span data-ttu-id="e7df8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="e7df8-127">The following table shows the properties that are required when you create the [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span></span>

|<span data-ttu-id="e7df8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7df8-128">Property</span></span>|<span data-ttu-id="e7df8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7df8-129">Type</span></span>|<span data-ttu-id="e7df8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7df8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7df8-131">id</span><span class="sxs-lookup"><span data-stu-id="e7df8-131">id</span></span>|<span data-ttu-id="e7df8-132">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-132">String</span></span>|<span data-ttu-id="e7df8-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e7df8-133">Not yet documented</span></span>|
|<span data-ttu-id="e7df8-134">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e7df8-134">lastSyncDateTime</span></span>|<span data-ttu-id="e7df8-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e7df8-135">DateTimeOffset</span></span>|<span data-ttu-id="e7df8-136">Última hora de sincronización para Exchange Connector</span><span class="sxs-lookup"><span data-stu-id="e7df8-136">Last sync time for the Exchange Connector</span></span>|
|<span data-ttu-id="e7df8-137">status</span><span class="sxs-lookup"><span data-stu-id="e7df8-137">status</span></span>|[<span data-ttu-id="e7df8-138">deviceManagementExchangeConnectorStatus</span><span class="sxs-lookup"><span data-stu-id="e7df8-138">deviceManagementExchangeConnectorStatus</span></span>](../resources/intune-onboarding-devicemanagementexchangeconnectorstatus.md)|<span data-ttu-id="e7df8-139">Estado del conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7df8-139">Exchange Connector Status.</span></span> <span data-ttu-id="e7df8-140">Los valores posibles son: `none`, `connectionPending`, `connected` y `disconnected`.</span><span class="sxs-lookup"><span data-stu-id="e7df8-140">Possible values are: `none`, `connectionPending`, `connected`, `disconnected`.</span></span>|
|<span data-ttu-id="e7df8-141">primarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e7df8-141">primarySmtpAddress</span></span>|<span data-ttu-id="e7df8-142">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-142">String</span></span>|<span data-ttu-id="e7df8-143">Dirección de correo electrónico que se usó para configurar el Exchange Connector de Service To Service.</span><span class="sxs-lookup"><span data-stu-id="e7df8-143">Email address used to configure the Service To Service Exchange Connector.</span></span>|
|<span data-ttu-id="e7df8-144">serverName</span><span class="sxs-lookup"><span data-stu-id="e7df8-144">serverName</span></span>|<span data-ttu-id="e7df8-145">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-145">String</span></span>|<span data-ttu-id="e7df8-146">El nombre del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7df8-146">The name of the Exchange server.</span></span>|
|<span data-ttu-id="e7df8-147">connectorServerName</span><span class="sxs-lookup"><span data-stu-id="e7df8-147">connectorServerName</span></span>|<span data-ttu-id="e7df8-148">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-148">String</span></span>|<span data-ttu-id="e7df8-149">El nombre del servidor que hospeda el Exchange Connector.</span><span class="sxs-lookup"><span data-stu-id="e7df8-149">The name of the server hosting the Exchange Connector.</span></span>|
|<span data-ttu-id="e7df8-150">exchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="e7df8-150">exchangeConnectorType</span></span>|[<span data-ttu-id="e7df8-151">deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="e7df8-151">deviceManagementExchangeConnectorType</span></span>](../resources/intune-onboarding-devicemanagementexchangeconnectortype.md)|<span data-ttu-id="e7df8-152">El tipo de Exchange Connector configurado.</span><span class="sxs-lookup"><span data-stu-id="e7df8-152">The type of Exchange Connector Configured.</span></span> <span data-ttu-id="e7df8-153">Los valores posibles son: `onPremises`, `hosted`, `serviceToService` y `dedicated`.</span><span class="sxs-lookup"><span data-stu-id="e7df8-153">Possible values are: `onPremises`, `hosted`, `serviceToService`, `dedicated`.</span></span>|
|<span data-ttu-id="e7df8-154">version</span><span class="sxs-lookup"><span data-stu-id="e7df8-154">version</span></span>|<span data-ttu-id="e7df8-155">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-155">String</span></span>|<span data-ttu-id="e7df8-156">La versión del ExchangeConnectorAgent</span><span class="sxs-lookup"><span data-stu-id="e7df8-156">The version of the ExchangeConnectorAgent</span></span>|
|<span data-ttu-id="e7df8-157">exchangeAlias</span><span class="sxs-lookup"><span data-stu-id="e7df8-157">exchangeAlias</span></span>|<span data-ttu-id="e7df8-158">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-158">String</span></span>|<span data-ttu-id="e7df8-159">Un alias asignado al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="e7df8-159">An alias assigned to the Exchange server</span></span>|
|<span data-ttu-id="e7df8-160">exchangeOrganization</span><span class="sxs-lookup"><span data-stu-id="e7df8-160">exchangeOrganization</span></span>|<span data-ttu-id="e7df8-161">String</span><span class="sxs-lookup"><span data-stu-id="e7df8-161">String</span></span>|<span data-ttu-id="e7df8-162">Organización de Exchange al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="e7df8-162">Exchange Organization to the Exchange server</span></span>|



## <a name="response"></a><span data-ttu-id="e7df8-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7df8-163">Response</span></span>
<span data-ttu-id="e7df8-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7df8-164">If successful, this method returns a `200 OK` response code and an updated [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e7df8-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7df8-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7df8-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7df8-166">Request</span></span>
<span data-ttu-id="e7df8-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7df8-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
Content-type: application/json
Content-length: 490

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
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

### <a name="response"></a><span data-ttu-id="e7df8-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7df8-168">Response</span></span>
<span data-ttu-id="e7df8-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7df8-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



