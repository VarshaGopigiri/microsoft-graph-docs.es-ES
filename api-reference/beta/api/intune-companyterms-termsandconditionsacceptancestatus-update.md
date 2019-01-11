---
title: Actualizar termsAndConditionsAcceptanceStatus
description: Actualice las propiedades de un objeto termsAndConditionsAcceptanceStatus.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 886910cfe2ac0b1bcf6ad1fcbd0a76a79c515aba
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858439"
---
# <a name="update-termsandconditionsacceptancestatus"></a><span data-ttu-id="0a17a-103">Actualizar termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="0a17a-103">Update termsAndConditionsAcceptanceStatus</span></span>

> <span data-ttu-id="0a17a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0a17a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0a17a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0a17a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0a17a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0a17a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a17a-107">Actualice las propiedades de un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="0a17a-107">Update the properties of a [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a17a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0a17a-108">Prerequisites</span></span>
<span data-ttu-id="0a17a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0a17a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0a17a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a17a-111">Permission type</span></span>|<span data-ttu-id="0a17a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a17a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0a17a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a17a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0a17a-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a17a-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="0a17a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a17a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0a17a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a17a-116">Not supported.</span></span>|
|<span data-ttu-id="0a17a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a17a-117">Application</span></span>|<span data-ttu-id="0a17a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a17a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0a17a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a17a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="0a17a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a17a-120">Request headers</span></span>
|<span data-ttu-id="0a17a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a17a-121">Header</span></span>|<span data-ttu-id="0a17a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0a17a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0a17a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0a17a-123">Authorization</span></span>|<span data-ttu-id="0a17a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0a17a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0a17a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0a17a-125">Accept</span></span>|<span data-ttu-id="0a17a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0a17a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a17a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a17a-127">Request body</span></span>
<span data-ttu-id="0a17a-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="0a17a-128">In the request body, supply a JSON representation for the [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>

<span data-ttu-id="0a17a-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="0a17a-129">The following table shows the properties that are required when you create the [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span></span>

|<span data-ttu-id="0a17a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a17a-130">Property</span></span>|<span data-ttu-id="0a17a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a17a-131">Type</span></span>|<span data-ttu-id="0a17a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a17a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0a17a-133">id</span><span class="sxs-lookup"><span data-stu-id="0a17a-133">id</span></span>|<span data-ttu-id="0a17a-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="0a17a-134">String</span></span>|<span data-ttu-id="0a17a-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0a17a-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="0a17a-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="0a17a-136">userDisplayName</span></span>|<span data-ttu-id="0a17a-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="0a17a-137">String</span></span>|<span data-ttu-id="0a17a-138">Nombre para mostrar del usuario cuya aceptación representa la entidad.</span><span class="sxs-lookup"><span data-stu-id="0a17a-138">Display name of the user whose acceptance the entity represents.</span></span>|
|<span data-ttu-id="0a17a-139">acceptedVersion</span><span class="sxs-lookup"><span data-stu-id="0a17a-139">acceptedVersion</span></span>|<span data-ttu-id="0a17a-140">Int32</span><span class="sxs-lookup"><span data-stu-id="0a17a-140">Int32</span></span>|<span data-ttu-id="0a17a-141">Número de versión más reciente de los TyC aceptados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0a17a-141">Most recent version number of the T&C accepted by the user.</span></span>|
|<span data-ttu-id="0a17a-142">acceptedDateTime</span><span class="sxs-lookup"><span data-stu-id="0a17a-142">acceptedDateTime</span></span>|<span data-ttu-id="0a17a-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a17a-143">DateTimeOffset</span></span>|<span data-ttu-id="0a17a-144">Fecha y hora en la que el usuario aceptó los términos por última vez.</span><span class="sxs-lookup"><span data-stu-id="0a17a-144">DateTime when the terms were last accepted by the user.</span></span>|



## <a name="response"></a><span data-ttu-id="0a17a-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a17a-145">Response</span></span>
<span data-ttu-id="0a17a-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a17a-146">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a17a-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a17a-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="0a17a-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a17a-148">Request</span></span>
<span data-ttu-id="0a17a-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a17a-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
Content-type: application/json
Content-length: 138

{
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```

### <a name="response"></a><span data-ttu-id="0a17a-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a17a-150">Response</span></span>
<span data-ttu-id="0a17a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a17a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





