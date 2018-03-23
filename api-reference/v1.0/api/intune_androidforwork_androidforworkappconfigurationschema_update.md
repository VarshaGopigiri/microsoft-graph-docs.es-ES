# <a name="update-androidforworkappconfigurationschema"></a><span data-ttu-id="2e061-101">Actualizar androidForWorkAppConfigurationSchema</span><span class="sxs-lookup"><span data-stu-id="2e061-101">Update androidForWorkAppConfigurationSchema</span></span>

> <span data-ttu-id="2e061-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2e061-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2e061-103">Actualice las propiedades de un objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="2e061-103">Update the properties of a [calendar](../resources/intune_androidforwork_androidforworkappconfigurationschema.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2e061-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2e061-104">Prerequisites</span></span>
<span data-ttu-id="2e061-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2e061-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2e061-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e061-107">Permission type</span></span>|<span data-ttu-id="2e061-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e061-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2e061-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e061-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2e061-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e061-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2e061-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e061-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2e061-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e061-112">Not supported.</span></span>|
|<span data-ttu-id="2e061-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e061-113">Application</span></span>|<span data-ttu-id="2e061-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e061-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2e061-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e061-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkAppConfigurationSchemas/{androidForWorkAppConfigurationSchemaId}
```

## <a name="request-headers"></a><span data-ttu-id="2e061-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e061-116">Request headers</span></span>
|<span data-ttu-id="2e061-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e061-117">Header</span></span>|<span data-ttu-id="2e061-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2e061-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2e061-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="2e061-119">Authorization</span></span>|<span data-ttu-id="2e061-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2e061-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="2e061-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2e061-121">Accept</span></span>|<span data-ttu-id="2e061-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2e061-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2e061-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e061-123">Request body</span></span>
<span data-ttu-id="2e061-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="2e061-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_androidforwork_androidforworkappconfigurationschema.md) object.</span></span>

<span data-ttu-id="2e061-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="2e061-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="2e061-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2e061-126">Property</span></span>|<span data-ttu-id="2e061-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e061-127">Type</span></span>|<span data-ttu-id="2e061-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e061-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2e061-129">id</span><span class="sxs-lookup"><span data-stu-id="2e061-129">id</span></span>|<span data-ttu-id="2e061-130">String</span><span class="sxs-lookup"><span data-stu-id="2e061-130">String</span></span>|<span data-ttu-id="2e061-131">Clave de la entidad a la que corresponde el esquema del nombre del paquete Android para la aplicación</span><span class="sxs-lookup"><span data-stu-id="2e061-131">Key of the entity the Android package name for the application the schema corresponds to</span></span>|
|<span data-ttu-id="2e061-132">exampleJson</span><span class="sxs-lookup"><span data-stu-id="2e061-132">exampleJson</span></span>|<span data-ttu-id="2e061-133">Binario</span><span class="sxs-lookup"><span data-stu-id="2e061-133">Binary</span></span>|<span data-ttu-id="2e061-134">Matriz de bytes codificada UTF8 que contiene la cadena JSON de ejemplo conforme a este esquema que muestra cómo configurar los ajustes de esta aplicación</span><span class="sxs-lookup"><span data-stu-id="2e061-134">UTF8 encoded byte array containing example JSON string conforming to this schema that demonstrates how to set the configuration for this app</span></span>|
|<span data-ttu-id="2e061-135">schemaItems</span><span class="sxs-lookup"><span data-stu-id="2e061-135">schemaItems</span></span>|<span data-ttu-id="2e061-136">Colección [androidForWorkAppConfigurationSchemaItem](../resources/intune_androidforwork_androidforworkappconfigurationschemaitem.md)</span><span class="sxs-lookup"><span data-stu-id="2e061-136">[androidForWorkAppConfigurationSchemaItem](../resources/intune_androidforwork_androidforworkappconfigurationschemaitem.md) collection</span></span>|<span data-ttu-id="2e061-137">Colección de elementos donde cada uno representa una opción de configuración con nombre en el esquema</span><span class="sxs-lookup"><span data-stu-id="2e061-137">Collection of items each representing a named configuration option in the schema</span></span>|



## <a name="response"></a><span data-ttu-id="2e061-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e061-138">Response</span></span>
<span data-ttu-id="2e061-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e061-139">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_androidforwork_androidforworkappconfigurationschema.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e061-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e061-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="2e061-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e061-141">Request</span></span>
<span data-ttu-id="2e061-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e061-142">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/androidForWorkAppConfigurationSchemas/{androidForWorkAppConfigurationSchemaId}
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

### <a name="response"></a><span data-ttu-id="2e061-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e061-143">Response</span></span>
<span data-ttu-id="2e061-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2e061-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



