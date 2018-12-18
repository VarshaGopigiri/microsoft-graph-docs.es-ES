---
title: Actualizar androidForWorkAppConfigurationSchema
description: Actualice las propiedades de un objeto androidForWorkAppConfigurationSchema.
author: tfitzmac
ms.openlocfilehash: ba4050ce741e1fdcfd3158e7f9e9d9e47f422882
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333904"
---
# <a name="update-androidforworkappconfigurationschema"></a><span data-ttu-id="ba66b-103">Actualizar androidForWorkAppConfigurationSchema</span><span class="sxs-lookup"><span data-stu-id="ba66b-103">Update androidForWorkAppConfigurationSchema</span></span>

> <span data-ttu-id="ba66b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ba66b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ba66b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ba66b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ba66b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ba66b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ba66b-107">Actualice las propiedades de un objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="ba66b-107">Update the properties of a [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ba66b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba66b-108">Prerequisites</span></span>
<span data-ttu-id="ba66b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba66b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba66b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba66b-111">Permission type</span></span>|<span data-ttu-id="ba66b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba66b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ba66b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba66b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ba66b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba66b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ba66b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba66b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ba66b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba66b-116">Not supported.</span></span>|
|<span data-ttu-id="ba66b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba66b-117">Application</span></span>|<span data-ttu-id="ba66b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba66b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ba66b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba66b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkAppConfigurationSchemas/{androidForWorkAppConfigurationSchemaId}
```

## <a name="request-headers"></a><span data-ttu-id="ba66b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba66b-120">Request headers</span></span>
|<span data-ttu-id="ba66b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba66b-121">Header</span></span>|<span data-ttu-id="ba66b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ba66b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ba66b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ba66b-123">Authorization</span></span>|<span data-ttu-id="ba66b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ba66b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ba66b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ba66b-125">Accept</span></span>|<span data-ttu-id="ba66b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ba66b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ba66b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba66b-127">Request body</span></span>
<span data-ttu-id="ba66b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="ba66b-128">In the request body, supply a JSON representation for the [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) object.</span></span>

<span data-ttu-id="ba66b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="ba66b-129">The following table shows the properties that are required when you create the [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).</span></span>

|<span data-ttu-id="ba66b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ba66b-130">Property</span></span>|<span data-ttu-id="ba66b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba66b-131">Type</span></span>|<span data-ttu-id="ba66b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba66b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ba66b-133">id</span><span class="sxs-lookup"><span data-stu-id="ba66b-133">id</span></span>|<span data-ttu-id="ba66b-134">String</span><span class="sxs-lookup"><span data-stu-id="ba66b-134">String</span></span>|<span data-ttu-id="ba66b-135">Clave de la entidad a la que corresponde el esquema del nombre del paquete Android para la aplicación</span><span class="sxs-lookup"><span data-stu-id="ba66b-135">Key of the entity the Android package name for the application the schema corresponds to</span></span>|
|<span data-ttu-id="ba66b-136">exampleJson</span><span class="sxs-lookup"><span data-stu-id="ba66b-136">exampleJson</span></span>|<span data-ttu-id="ba66b-137">Binario</span><span class="sxs-lookup"><span data-stu-id="ba66b-137">Binary</span></span>|<span data-ttu-id="ba66b-138">Matriz de bytes codificada UTF8 que contiene la cadena JSON de ejemplo conforme a este esquema que muestra cómo configurar los ajustes de esta aplicación</span><span class="sxs-lookup"><span data-stu-id="ba66b-138">UTF8 encoded byte array containing example JSON string conforming to this schema that demonstrates how to set the configuration for this app</span></span>|
|<span data-ttu-id="ba66b-139">schemaItems</span><span class="sxs-lookup"><span data-stu-id="ba66b-139">schemaItems</span></span>|<span data-ttu-id="ba66b-140">Colección [androidForWorkAppConfigurationSchemaItem](../resources/intune-androidforwork-androidforworkappconfigurationschemaitem.md)</span><span class="sxs-lookup"><span data-stu-id="ba66b-140">[androidForWorkAppConfigurationSchemaItem](../resources/intune-androidforwork-androidforworkappconfigurationschemaitem.md) collection</span></span>|<span data-ttu-id="ba66b-141">Colección de elementos donde cada uno representa una opción de configuración con nombre en el esquema</span><span class="sxs-lookup"><span data-stu-id="ba66b-141">Collection of items each representing a named configuration option in the schema</span></span>|



## <a name="response"></a><span data-ttu-id="ba66b-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba66b-142">Response</span></span>
<span data-ttu-id="ba66b-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba66b-143">If successful, this method returns a `200 OK` response code and an updated [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ba66b-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba66b-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="ba66b-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba66b-145">Request</span></span>
<span data-ttu-id="ba66b-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba66b-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/androidForWorkAppConfigurationSchemas/{androidForWorkAppConfigurationSchemaId}
Content-type: application/json
Content-length: 720

{
  "exampleJson": "ZXhhbXBsZUpzb24=",
  "schemaItems": [
    {
      "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem",
      "schemaItemKey": "Schema Item Key value",
      "displayName": "Display Name value",
      "description": "Description value",
      "defaultBoolValue": true,
      "defaultIntValue": 15,
      "defaultStringValue": "Default String Value value",
      "defaultStringArrayValue": [
        "Default String Array Value value"
      ],
      "dataType": "integer",
      "selections": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ]
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="ba66b-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba66b-147">Response</span></span>
<span data-ttu-id="ba66b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba66b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 844

{
  "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchema",
  "id": "c1230dc6-0dc6-c123-c60d-23c1c60d23c1",
  "exampleJson": "ZXhhbXBsZUpzb24=",
  "schemaItems": [
    {
      "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem",
      "schemaItemKey": "Schema Item Key value",
      "displayName": "Display Name value",
      "description": "Description value",
      "defaultBoolValue": true,
      "defaultIntValue": 15,
      "defaultStringValue": "Default String Value value",
      "defaultStringArrayValue": [
        "Default String Array Value value"
      ],
      "dataType": "integer",
      "selections": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ]
    }
  ]
}
```





