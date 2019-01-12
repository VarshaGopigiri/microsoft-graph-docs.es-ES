---
title: Crear telecomExpenseManagementPartner
description: Cree un objeto telecomExpenseManagementPartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ca3a94da0c908bec0af44075dcb15b6fa4f007a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984804"
---
# <a name="create-telecomexpensemanagementpartner"></a><span data-ttu-id="c6ec1-103">Crear telecomExpenseManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c6ec1-103">Create telecomExpenseManagementPartner</span></span>

> <span data-ttu-id="c6ec1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c6ec1-105">Cree un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="c6ec1-105">Create a new [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c6ec1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c6ec1-106">Prerequisites</span></span>
<span data-ttu-id="c6ec1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6ec1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c6ec1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6ec1-109">Permission type</span></span>|<span data-ttu-id="c6ec1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6ec1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c6ec1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6ec1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c6ec1-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6ec1-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="c6ec1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6ec1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c6ec1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-114">Not supported.</span></span>|
|<span data-ttu-id="c6ec1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6ec1-115">Application</span></span>|<span data-ttu-id="c6ec1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c6ec1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6ec1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/telecomExpenseManagementPartners
```

## <a name="request-headers"></a><span data-ttu-id="c6ec1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ec1-118">Request headers</span></span>
|<span data-ttu-id="c6ec1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6ec1-119">Header</span></span>|<span data-ttu-id="c6ec1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c6ec1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c6ec1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c6ec1-121">Authorization</span></span>|<span data-ttu-id="c6ec1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c6ec1-123">Accept</span><span class="sxs-lookup"><span data-stu-id="c6ec1-123">Accept</span></span>|<span data-ttu-id="c6ec1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c6ec1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c6ec1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ec1-125">Request body</span></span>
<span data-ttu-id="c6ec1-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto telecomExpenseManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-126">In the request body, supply a JSON representation for the telecomExpenseManagementPartner object.</span></span>

<span data-ttu-id="c6ec1-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto telecomExpenseManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-127">The following table shows the properties that are required when you create the telecomExpenseManagementPartner.</span></span>

|<span data-ttu-id="c6ec1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6ec1-128">Property</span></span>|<span data-ttu-id="c6ec1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6ec1-129">Type</span></span>|<span data-ttu-id="c6ec1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6ec1-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c6ec1-131">id</span><span class="sxs-lookup"><span data-stu-id="c6ec1-131">id</span></span>|<span data-ttu-id="c6ec1-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="c6ec1-132">String</span></span>|<span data-ttu-id="c6ec1-133">Identificador único del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-133">Unique identifier of the TEM partner.</span></span>|
|<span data-ttu-id="c6ec1-134">displayName</span><span class="sxs-lookup"><span data-stu-id="c6ec1-134">displayName</span></span>|<span data-ttu-id="c6ec1-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="c6ec1-135">String</span></span>|<span data-ttu-id="c6ec1-136">Nombre para mostrar del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-136">Display name of the TEM partner.</span></span>|
|<span data-ttu-id="c6ec1-137">url</span><span class="sxs-lookup"><span data-stu-id="c6ec1-137">url</span></span>|<span data-ttu-id="c6ec1-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="c6ec1-138">String</span></span>|<span data-ttu-id="c6ec1-139">Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-139">URL of the TEM partner's administrative control panel, where an administrator can configure their TEM service.</span></span>|
|<span data-ttu-id="c6ec1-140">appAuthorized</span><span class="sxs-lookup"><span data-stu-id="c6ec1-140">appAuthorized</span></span>|<span data-ttu-id="c6ec1-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="c6ec1-141">Boolean</span></span>|<span data-ttu-id="c6ec1-142">Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-142">Whether the partner's AAD app has been authorized to access Intune.</span></span>|
|<span data-ttu-id="c6ec1-143">enabled</span><span class="sxs-lookup"><span data-stu-id="c6ec1-143">enabled</span></span>|<span data-ttu-id="c6ec1-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="c6ec1-144">Boolean</span></span>|<span data-ttu-id="c6ec1-145">Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-145">Whether Intune's connection to the TEM service is currently enabled or disabled.</span></span>|
|<span data-ttu-id="c6ec1-146">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="c6ec1-146">lastConnectionDateTime</span></span>|<span data-ttu-id="c6ec1-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c6ec1-147">DateTimeOffset</span></span>|<span data-ttu-id="c6ec1-148">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-148">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="c6ec1-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ec1-149">Response</span></span>
<span data-ttu-id="c6ec1-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-150">If successful, this method returns a `201 Created` response code and a [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6ec1-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6ec1-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="c6ec1-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ec1-152">Request</span></span>
<span data-ttu-id="c6ec1-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-153">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners
Content-type: application/json
Content-length: 248

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="c6ec1-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ec1-154">Response</span></span>
<span data-ttu-id="c6ec1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 297

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```



