---
title: Actualizar termsAndConditionsAcceptanceStatus
description: Actualice las propiedades de un objeto termsAndConditionsAcceptanceStatus.
ms.openlocfilehash: 4078cc304e85b360b7156235105fc9a0e4949402
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029138"
---
# <a name="update-termsandconditionsacceptancestatus"></a><span data-ttu-id="dbf2f-103">Actualizar termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="dbf2f-103">Update termsAndConditionsAcceptanceStatus</span></span>

> <span data-ttu-id="dbf2f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dbf2f-105">Actualice las propiedades de un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="dbf2f-105">Update the properties of a [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dbf2f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbf2f-106">Prerequisites</span></span>
<span data-ttu-id="dbf2f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dbf2f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dbf2f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbf2f-109">Permission type</span></span>|<span data-ttu-id="dbf2f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbf2f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dbf2f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbf2f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dbf2f-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dbf2f-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="dbf2f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbf2f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dbf2f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-114">Not supported.</span></span>|
|<span data-ttu-id="dbf2f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbf2f-115">Application</span></span>|<span data-ttu-id="dbf2f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dbf2f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbf2f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="dbf2f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbf2f-118">Request headers</span></span>
|<span data-ttu-id="dbf2f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbf2f-119">Header</span></span>|<span data-ttu-id="dbf2f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf2f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dbf2f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="dbf2f-121">Authorization</span></span>|<span data-ttu-id="dbf2f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dbf2f-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dbf2f-123">Accept</span></span>|<span data-ttu-id="dbf2f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dbf2f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dbf2f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbf2f-125">Request body</span></span>
<span data-ttu-id="dbf2f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="dbf2f-126">In the request body, supply a JSON representation for the [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>

<span data-ttu-id="dbf2f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="dbf2f-127">The following table shows the properties that are required when you create the [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span></span>

|<span data-ttu-id="dbf2f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbf2f-128">Property</span></span>|<span data-ttu-id="dbf2f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbf2f-129">Type</span></span>|<span data-ttu-id="dbf2f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbf2f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dbf2f-131">id</span><span class="sxs-lookup"><span data-stu-id="dbf2f-131">id</span></span>|<span data-ttu-id="dbf2f-132">String</span><span class="sxs-lookup"><span data-stu-id="dbf2f-132">String</span></span>|<span data-ttu-id="dbf2f-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="dbf2f-134">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="dbf2f-134">userDisplayName</span></span>|<span data-ttu-id="dbf2f-135">String</span><span class="sxs-lookup"><span data-stu-id="dbf2f-135">String</span></span>|<span data-ttu-id="dbf2f-136">Nombre para mostrar del usuario cuya aceptación representa la entidad.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-136">Display name of the user whose acceptance the entity represents.</span></span>|
|<span data-ttu-id="dbf2f-137">acceptedVersion</span><span class="sxs-lookup"><span data-stu-id="dbf2f-137">acceptedVersion</span></span>|<span data-ttu-id="dbf2f-138">Int32</span><span class="sxs-lookup"><span data-stu-id="dbf2f-138">Int32</span></span>|<span data-ttu-id="dbf2f-139">Número de versión más reciente de los TyC aceptados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-139">Most recent version number of the T&C accepted by the user.</span></span>|
|<span data-ttu-id="dbf2f-140">acceptedDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf2f-140">acceptedDateTime</span></span>|<span data-ttu-id="dbf2f-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf2f-141">DateTimeOffset</span></span>|<span data-ttu-id="dbf2f-142">Fecha y hora en la que el usuario aceptó los términos por última vez.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-142">DateTime when the terms were last accepted by the user.</span></span>|



## <a name="response"></a><span data-ttu-id="dbf2f-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbf2f-143">Response</span></span>
<span data-ttu-id="dbf2f-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-144">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dbf2f-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbf2f-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="dbf2f-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbf2f-146">Request</span></span>
<span data-ttu-id="dbf2f-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```

### <a name="response"></a><span data-ttu-id="dbf2f-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbf2f-148">Response</span></span>
<span data-ttu-id="dbf2f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "a045ce1a-ce1a-a045-1ace-45a01ace45a0",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```



