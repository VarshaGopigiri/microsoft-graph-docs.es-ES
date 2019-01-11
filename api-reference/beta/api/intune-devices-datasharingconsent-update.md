---
title: Actualizar dataSharingConsent
description: Actualizar las propiedades de un objeto dataSharingConsent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8e2486b6d1900369bae17853be399eccb4fe8740
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816439"
---
# <a name="update-datasharingconsent"></a><span data-ttu-id="5163c-103">Actualizar dataSharingConsent</span><span class="sxs-lookup"><span data-stu-id="5163c-103">Update dataSharingConsent</span></span>

> <span data-ttu-id="5163c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5163c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5163c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5163c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5163c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5163c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5163c-107">Actualizar las propiedades de un objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .</span><span class="sxs-lookup"><span data-stu-id="5163c-107">Update the properties of a [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5163c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5163c-108">Prerequisites</span></span>
<span data-ttu-id="5163c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5163c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5163c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5163c-111">Permission type</span></span>|<span data-ttu-id="5163c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5163c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5163c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5163c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5163c-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5163c-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="5163c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5163c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5163c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5163c-116">Not supported.</span></span>|
|<span data-ttu-id="5163c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5163c-117">Application</span></span>|<span data-ttu-id="5163c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5163c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5163c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5163c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/dataSharingConsents/{dataSharingConsentId}
```

## <a name="request-headers"></a><span data-ttu-id="5163c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5163c-120">Request headers</span></span>
|<span data-ttu-id="5163c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5163c-121">Header</span></span>|<span data-ttu-id="5163c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5163c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5163c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5163c-123">Authorization</span></span>|<span data-ttu-id="5163c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5163c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5163c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5163c-125">Accept</span></span>|<span data-ttu-id="5163c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5163c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5163c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5163c-127">Request body</span></span>
<span data-ttu-id="5163c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .</span><span class="sxs-lookup"><span data-stu-id="5163c-128">In the request body, supply a JSON representation for the [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) object.</span></span>

<span data-ttu-id="5163c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [dataSharingConsent](../resources/intune-devices-datasharingconsent.md).</span><span class="sxs-lookup"><span data-stu-id="5163c-129">The following table shows the properties that are required when you create the [dataSharingConsent](../resources/intune-devices-datasharingconsent.md).</span></span>

|<span data-ttu-id="5163c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5163c-130">Property</span></span>|<span data-ttu-id="5163c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5163c-131">Type</span></span>|<span data-ttu-id="5163c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5163c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5163c-133">id</span><span class="sxs-lookup"><span data-stu-id="5163c-133">id</span></span>|<span data-ttu-id="5163c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5163c-134">String</span></span>|<span data-ttu-id="5163c-135">El consentimiento de uso compartido de datos Id.</span><span class="sxs-lookup"><span data-stu-id="5163c-135">The data sharing consent Id</span></span>|
|<span data-ttu-id="5163c-136">nombreDescriptivoDeServicio</span><span class="sxs-lookup"><span data-stu-id="5163c-136">serviceDisplayName</span></span>|<span data-ttu-id="5163c-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="5163c-137">String</span></span>|<span data-ttu-id="5163c-138">El nombre para mostrar del flujo de trabajo del servicio</span><span class="sxs-lookup"><span data-stu-id="5163c-138">The display name of the service work flow</span></span>|
|<span data-ttu-id="5163c-139">termsUrl</span><span class="sxs-lookup"><span data-stu-id="5163c-139">termsUrl</span></span>|<span data-ttu-id="5163c-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="5163c-140">String</span></span>|<span data-ttu-id="5163c-141">El TermsUrl para los datos de uso compartido de consentimiento</span><span class="sxs-lookup"><span data-stu-id="5163c-141">The TermsUrl for the data sharing consent</span></span>|
|<span data-ttu-id="5163c-142">concedido</span><span class="sxs-lookup"><span data-stu-id="5163c-142">granted</span></span>|<span data-ttu-id="5163c-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="5163c-143">Boolean</span></span>|<span data-ttu-id="5163c-144">El estado de concedidos para los datos de uso compartido de consentimiento</span><span class="sxs-lookup"><span data-stu-id="5163c-144">The granted state for the data sharing consent</span></span>|
|<span data-ttu-id="5163c-145">grantDateTime</span><span class="sxs-lookup"><span data-stu-id="5163c-145">grantDateTime</span></span>|<span data-ttu-id="5163c-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5163c-146">DateTimeOffset</span></span>|<span data-ttu-id="5163c-147">Esta cuenta se le conceden el consentimiento de tiempo</span><span class="sxs-lookup"><span data-stu-id="5163c-147">The time consent was granted for this account</span></span>|
|<span data-ttu-id="5163c-148">grantedByUpn</span><span class="sxs-lookup"><span data-stu-id="5163c-148">grantedByUpn</span></span>|<span data-ttu-id="5163c-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="5163c-149">String</span></span>|<span data-ttu-id="5163c-150">El Upn del usuario que concederse el consentimiento para esta cuenta</span><span class="sxs-lookup"><span data-stu-id="5163c-150">The Upn of the user that granted consent for this account</span></span>|
|<span data-ttu-id="5163c-151">grantedByUserId</span><span class="sxs-lookup"><span data-stu-id="5163c-151">grantedByUserId</span></span>|<span data-ttu-id="5163c-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="5163c-152">String</span></span>|<span data-ttu-id="5163c-153">El identificador de usuario del usuario que concederse el consentimiento para esta cuenta</span><span class="sxs-lookup"><span data-stu-id="5163c-153">The UserId of the user that granted consent for this account</span></span>|



## <a name="response"></a><span data-ttu-id="5163c-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5163c-154">Response</span></span>
<span data-ttu-id="5163c-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5163c-155">If successful, this method returns a `200 OK` response code and an updated [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5163c-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5163c-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="5163c-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5163c-157">Request</span></span>
<span data-ttu-id="5163c-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5163c-158">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/dataSharingConsents/{dataSharingConsentId}
Content-type: application/json
Content-length: 276

{
  "serviceDisplayName": "Service Display Name value",
  "termsUrl": "https://example.com/termsUrl/",
  "granted": true,
  "grantDateTime": "2016-12-31T23:59:55.7154191-08:00",
  "grantedByUpn": "Granted By Upn value",
  "grantedByUserId": "Granted By User Id value"
}
```

### <a name="response"></a><span data-ttu-id="5163c-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5163c-159">Response</span></span>
<span data-ttu-id="5163c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5163c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 382

{
  "@odata.type": "#microsoft.graph.dataSharingConsent",
  "id": "333387f7-87f7-3333-f787-3333f7873333",
  "serviceDisplayName": "Service Display Name value",
  "termsUrl": "https://example.com/termsUrl/",
  "granted": true,
  "grantDateTime": "2016-12-31T23:59:55.7154191-08:00",
  "grantedByUpn": "Granted By Upn value",
  "grantedByUserId": "Granted By User Id value"
}
```





