---
title: Actualizar cartToClassAssociation
description: Actualizar las propiedades de un objeto cartToClassAssociation.
author: tfitzmac
ms.openlocfilehash: 43b272a5fa2871daebbf7cfeea890ba0b9e204e8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343019"
---
# <a name="update-carttoclassassociation"></a><span data-ttu-id="25a49-103">Actualizar cartToClassAssociation</span><span class="sxs-lookup"><span data-stu-id="25a49-103">Update cartToClassAssociation</span></span>

> <span data-ttu-id="25a49-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25a49-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25a49-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25a49-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="25a49-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25a49-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25a49-107">Actualizar las propiedades de un objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .</span><span class="sxs-lookup"><span data-stu-id="25a49-107">Update the properties of a [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="25a49-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25a49-108">Prerequisites</span></span>
<span data-ttu-id="25a49-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25a49-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25a49-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25a49-111">Permission type</span></span>|<span data-ttu-id="25a49-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25a49-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="25a49-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25a49-113">Delegated (work or school account)</span></span>|<span data-ttu-id="25a49-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25a49-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="25a49-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25a49-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="25a49-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25a49-116">Not supported.</span></span>|
|<span data-ttu-id="25a49-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25a49-117">Application</span></span>|<span data-ttu-id="25a49-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25a49-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="25a49-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25a49-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/cartToClassAssociations/{cartToClassAssociationId}
```

## <a name="request-headers"></a><span data-ttu-id="25a49-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25a49-120">Request headers</span></span>
|<span data-ttu-id="25a49-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25a49-121">Header</span></span>|<span data-ttu-id="25a49-122">Valor</span><span class="sxs-lookup"><span data-stu-id="25a49-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="25a49-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="25a49-123">Authorization</span></span>|<span data-ttu-id="25a49-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="25a49-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="25a49-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="25a49-125">Accept</span></span>|<span data-ttu-id="25a49-126">application/json</span><span class="sxs-lookup"><span data-stu-id="25a49-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="25a49-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25a49-127">Request body</span></span>
<span data-ttu-id="25a49-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .</span><span class="sxs-lookup"><span data-stu-id="25a49-128">In the request body, supply a JSON representation for the [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object.</span></span>

<span data-ttu-id="25a49-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md).</span><span class="sxs-lookup"><span data-stu-id="25a49-129">The following table shows the properties that are required when you create the [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md).</span></span>

|<span data-ttu-id="25a49-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25a49-130">Property</span></span>|<span data-ttu-id="25a49-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="25a49-131">Type</span></span>|<span data-ttu-id="25a49-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="25a49-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25a49-133">id</span><span class="sxs-lookup"><span data-stu-id="25a49-133">id</span></span>|<span data-ttu-id="25a49-134">String</span><span class="sxs-lookup"><span data-stu-id="25a49-134">String</span></span>|<span data-ttu-id="25a49-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="25a49-135">Key of the entity.</span></span>|
|<span data-ttu-id="25a49-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="25a49-136">createdDateTime</span></span>|<span data-ttu-id="25a49-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25a49-137">DateTimeOffset</span></span>|<span data-ttu-id="25a49-138">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="25a49-138">DateTime the object was created.</span></span>|
|<span data-ttu-id="25a49-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="25a49-139">lastModifiedDateTime</span></span>|<span data-ttu-id="25a49-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25a49-140">DateTimeOffset</span></span>|<span data-ttu-id="25a49-141">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="25a49-141">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="25a49-142">version</span><span class="sxs-lookup"><span data-stu-id="25a49-142">version</span></span>|<span data-ttu-id="25a49-143">Int32</span><span class="sxs-lookup"><span data-stu-id="25a49-143">Int32</span></span>|<span data-ttu-id="25a49-144">Versión de la CartToClassAssociation.</span><span class="sxs-lookup"><span data-stu-id="25a49-144">Version of the CartToClassAssociation.</span></span>|
|<span data-ttu-id="25a49-145">displayName</span><span class="sxs-lookup"><span data-stu-id="25a49-145">displayName</span></span>|<span data-ttu-id="25a49-146">String</span><span class="sxs-lookup"><span data-stu-id="25a49-146">String</span></span>|<span data-ttu-id="25a49-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25a49-147">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="25a49-148">descripción</span><span class="sxs-lookup"><span data-stu-id="25a49-148">description</span></span>|<span data-ttu-id="25a49-149">String</span><span class="sxs-lookup"><span data-stu-id="25a49-149">String</span></span>|<span data-ttu-id="25a49-150">Descripción de la CartToClassAssociation proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="25a49-150">Admin provided description of the CartToClassAssociation.</span></span>|
|<span data-ttu-id="25a49-151">deviceCartIds</span><span class="sxs-lookup"><span data-stu-id="25a49-151">deviceCartIds</span></span>|<span data-ttu-id="25a49-152">Colección String</span><span class="sxs-lookup"><span data-stu-id="25a49-152">String collection</span></span>|<span data-ttu-id="25a49-153">Identificadores de carros de dispositivo que se asociará con clases.</span><span class="sxs-lookup"><span data-stu-id="25a49-153">Identifiers of device carts to be associated with classes.</span></span>|
|<span data-ttu-id="25a49-154">classroomIds</span><span class="sxs-lookup"><span data-stu-id="25a49-154">classroomIds</span></span>|<span data-ttu-id="25a49-155">Colección String</span><span class="sxs-lookup"><span data-stu-id="25a49-155">String collection</span></span>|<span data-ttu-id="25a49-156">Identificadores de aulas que se asociará con carros de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25a49-156">Identifiers of classrooms to be associated with device carts.</span></span>|



## <a name="response"></a><span data-ttu-id="25a49-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25a49-157">Response</span></span>
<span data-ttu-id="25a49-158">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25a49-158">If successful, this method returns a `200 OK` response code and an updated [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25a49-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25a49-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="25a49-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25a49-160">Request</span></span>
<span data-ttu-id="25a49-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25a49-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/cartToClassAssociations/{cartToClassAssociationId}
Content-type: application/json
Content-length: 274

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "displayName": "Display Name value",
  "description": "Description value",
  "deviceCartIds": [
    "Device Cart Ids value"
  ],
  "classroomIds": [
    "Classroom Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="25a49-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25a49-162">Response</span></span>
<span data-ttu-id="25a49-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25a49-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 443

{
  "@odata.type": "#microsoft.graph.cartToClassAssociation",
  "id": "9bdc58dd-58dd-9bdc-dd58-dc9bdd58dc9b",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "displayName": "Display Name value",
  "description": "Description value",
  "deviceCartIds": [
    "Device Cart Ids value"
  ],
  "classroomIds": [
    "Classroom Ids value"
  ]
}
```





