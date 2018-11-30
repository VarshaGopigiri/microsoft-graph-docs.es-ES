---
title: Actualizar ndesConnector
description: Actualizar las propiedades de un objeto ndesConnector.
ms.openlocfilehash: 963d27b89cb8c8731eb466475f65b36257f56b45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085104"
---
# <a name="update-ndesconnector"></a><span data-ttu-id="3a00b-103">Actualizar ndesConnector</span><span class="sxs-lookup"><span data-stu-id="3a00b-103">Update ndesConnector</span></span>

> <span data-ttu-id="3a00b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a00b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a00b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a00b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3a00b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a00b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a00b-107">Actualizar las propiedades de un objeto [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) .</span><span class="sxs-lookup"><span data-stu-id="3a00b-107">Update the properties of a [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3a00b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a00b-108">Prerequisites</span></span>
<span data-ttu-id="3a00b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3a00b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3a00b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a00b-111">Permission type</span></span>|<span data-ttu-id="3a00b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a00b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3a00b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a00b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3a00b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a00b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="3a00b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a00b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3a00b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a00b-116">Not supported.</span></span>|
|<span data-ttu-id="3a00b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a00b-117">Application</span></span>|<span data-ttu-id="3a00b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a00b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3a00b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a00b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/ndesConnectors/{ndesConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="3a00b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a00b-120">Request headers</span></span>
|<span data-ttu-id="3a00b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a00b-121">Header</span></span>|<span data-ttu-id="3a00b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3a00b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3a00b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a00b-123">Authorization</span></span>|<span data-ttu-id="3a00b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3a00b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3a00b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3a00b-125">Accept</span></span>|<span data-ttu-id="3a00b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3a00b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3a00b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a00b-127">Request body</span></span>
<span data-ttu-id="3a00b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) .</span><span class="sxs-lookup"><span data-stu-id="3a00b-128">In the request body, supply a JSON representation for the [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) object.</span></span>

<span data-ttu-id="3a00b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md).</span><span class="sxs-lookup"><span data-stu-id="3a00b-129">The following table shows the properties that are required when you create the [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md).</span></span>

|<span data-ttu-id="3a00b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a00b-130">Property</span></span>|<span data-ttu-id="3a00b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a00b-131">Type</span></span>|<span data-ttu-id="3a00b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a00b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a00b-133">id</span><span class="sxs-lookup"><span data-stu-id="3a00b-133">id</span></span>|<span data-ttu-id="3a00b-134">String</span><span class="sxs-lookup"><span data-stu-id="3a00b-134">String</span></span>|<span data-ttu-id="3a00b-135">La clave del conector NDES.</span><span class="sxs-lookup"><span data-stu-id="3a00b-135">The key of the NDES Connector.</span></span>|
|<span data-ttu-id="3a00b-136">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="3a00b-136">lastConnectionDateTime</span></span>|<span data-ttu-id="3a00b-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3a00b-137">DateTimeOffset</span></span>|<span data-ttu-id="3a00b-138">Última hora de conexión para el conector Ndes</span><span class="sxs-lookup"><span data-stu-id="3a00b-138">Last connection time for the Ndes Connector</span></span>|
|<span data-ttu-id="3a00b-139">estado</span><span class="sxs-lookup"><span data-stu-id="3a00b-139">state</span></span>|[<span data-ttu-id="3a00b-140">ndesConnectorState</span><span class="sxs-lookup"><span data-stu-id="3a00b-140">ndesConnectorState</span></span>](../resources/intune-deviceconfig-ndesconnectorstate.md)|<span data-ttu-id="3a00b-141">Estado de conector NDES.</span><span class="sxs-lookup"><span data-stu-id="3a00b-141">Ndes Connector Status.</span></span> <span data-ttu-id="3a00b-142">Los valores posibles son: `none`, `active` y `inactive`.</span><span class="sxs-lookup"><span data-stu-id="3a00b-142">Possible values are: `none`, `active`, `inactive`.</span></span>|
|<span data-ttu-id="3a00b-143">displayName</span><span class="sxs-lookup"><span data-stu-id="3a00b-143">displayName</span></span>|<span data-ttu-id="3a00b-144">String</span><span class="sxs-lookup"><span data-stu-id="3a00b-144">String</span></span>|<span data-ttu-id="3a00b-145">El nombre descriptivo del conector Ndes.</span><span class="sxs-lookup"><span data-stu-id="3a00b-145">The friendly name of the Ndes Connector.</span></span>|



## <a name="response"></a><span data-ttu-id="3a00b-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a00b-146">Response</span></span>
<span data-ttu-id="3a00b-147">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a00b-147">If successful, this method returns a `200 OK` response code and an updated [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a00b-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a00b-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="3a00b-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a00b-149">Request</span></span>
<span data-ttu-id="3a00b-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a00b-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/ndesConnectors/{ndesConnectorId}
Content-type: application/json
Content-length: 131

{
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00",
  "state": "active",
  "displayName": "Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="3a00b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a00b-151">Response</span></span>
<span data-ttu-id="3a00b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a00b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 232

{
  "@odata.type": "#microsoft.graph.ndesConnector",
  "id": "e71fa706-a706-e71f-06a7-1fe706a71fe7",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00",
  "state": "active",
  "displayName": "Display Name value"
}
```





