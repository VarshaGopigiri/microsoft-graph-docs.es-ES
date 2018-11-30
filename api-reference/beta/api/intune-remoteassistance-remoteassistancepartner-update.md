---
title: Actualizar remoteAssistancePartner
description: Actualice las propiedades de un objeto remoteAssistancePartner.
ms.openlocfilehash: 62647e197d7c4666ce177fff6c2f1fb7dd1271af
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085637"
---
# <a name="update-remoteassistancepartner"></a><span data-ttu-id="f49ac-103">Actualizar remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="f49ac-103">Update remoteAssistancePartner</span></span>

> <span data-ttu-id="f49ac-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f49ac-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f49ac-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f49ac-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f49ac-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f49ac-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f49ac-107">Actualice las propiedades de un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="f49ac-107">Update the properties of a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f49ac-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f49ac-108">Prerequisites</span></span>
<span data-ttu-id="f49ac-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f49ac-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f49ac-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f49ac-111">Permission type</span></span>|<span data-ttu-id="f49ac-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f49ac-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f49ac-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f49ac-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f49ac-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f49ac-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f49ac-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f49ac-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f49ac-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f49ac-116">Not supported.</span></span>|
|<span data-ttu-id="f49ac-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f49ac-117">Application</span></span>|<span data-ttu-id="f49ac-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f49ac-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f49ac-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f49ac-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="f49ac-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f49ac-120">Request headers</span></span>
|<span data-ttu-id="f49ac-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f49ac-121">Header</span></span>|<span data-ttu-id="f49ac-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f49ac-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f49ac-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f49ac-123">Authorization</span></span>|<span data-ttu-id="f49ac-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f49ac-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f49ac-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f49ac-125">Accept</span></span>|<span data-ttu-id="f49ac-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f49ac-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f49ac-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f49ac-127">Request body</span></span>
<span data-ttu-id="f49ac-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="f49ac-128">In the request body, supply a JSON representation for the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>

<span data-ttu-id="f49ac-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="f49ac-129">The following table shows the properties that are required when you create the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span></span>

|<span data-ttu-id="f49ac-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f49ac-130">Property</span></span>|<span data-ttu-id="f49ac-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f49ac-131">Type</span></span>|<span data-ttu-id="f49ac-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f49ac-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f49ac-133">id</span><span class="sxs-lookup"><span data-stu-id="f49ac-133">id</span></span>|<span data-ttu-id="f49ac-134">String</span><span class="sxs-lookup"><span data-stu-id="f49ac-134">String</span></span>|<span data-ttu-id="f49ac-135">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="f49ac-135">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="f49ac-136">displayName</span><span class="sxs-lookup"><span data-stu-id="f49ac-136">displayName</span></span>|<span data-ttu-id="f49ac-137">String</span><span class="sxs-lookup"><span data-stu-id="f49ac-137">String</span></span>|<span data-ttu-id="f49ac-138">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="f49ac-138">Display name of the partner.</span></span>|
|<span data-ttu-id="f49ac-139">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="f49ac-139">onboardingUrl</span></span>|<span data-ttu-id="f49ac-140">String</span><span class="sxs-lookup"><span data-stu-id="f49ac-140">String</span></span>|<span data-ttu-id="f49ac-141">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="f49ac-141">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="f49ac-142">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="f49ac-142">onboardingStatus</span></span>|[<span data-ttu-id="f49ac-143">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="f49ac-143">remoteAssistanceOnboardingStatus</span></span>](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|<span data-ttu-id="f49ac-144">TBD.</span><span class="sxs-lookup"><span data-stu-id="f49ac-144">TBD.</span></span> <span data-ttu-id="f49ac-145">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="f49ac-145">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="f49ac-146">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="f49ac-146">lastConnectionDateTime</span></span>|<span data-ttu-id="f49ac-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f49ac-147">DateTimeOffset</span></span>|<span data-ttu-id="f49ac-148">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="f49ac-148">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="f49ac-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f49ac-149">Response</span></span>
<span data-ttu-id="f49ac-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f49ac-150">If successful, this method returns a `200 OK` response code and an updated [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f49ac-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f49ac-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="f49ac-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f49ac-152">Request</span></span>
<span data-ttu-id="f49ac-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f49ac-153">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
Content-type: application/json
Content-length: 204

{
  "displayName": "Display Name value",
  "onboardingUrl": "https://example.com/onboardingUrl/",
  "onboardingStatus": "onboarding",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="f49ac-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f49ac-154">Response</span></span>
<span data-ttu-id="f49ac-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f49ac-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 315

{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "id": "7443c8b9-c8b9-7443-b9c8-4374b9c84374",
  "displayName": "Display Name value",
  "onboardingUrl": "https://example.com/onboardingUrl/",
  "onboardingStatus": "onboarding",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```





