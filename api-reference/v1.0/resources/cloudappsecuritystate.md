# <a name="cloudappsecuritystate-resource-type"></a><span data-ttu-id="dd8fc-101">Tipo de recurso cloudAppSecurityState</span><span class="sxs-lookup"><span data-stu-id="dd8fc-101">cloudAppSecurityState resource type</span></span>

<span data-ttu-id="dd8fc-102">Contiene información con estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).</span><span class="sxs-lookup"><span data-stu-id="dd8fc-102">Contains stateful information about the cloud application (destinationServiceName, destinationServiceIp).</span></span>

## <a name="properties"></a><span data-ttu-id="dd8fc-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd8fc-103">Properties</span></span>

| <span data-ttu-id="dd8fc-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd8fc-104">Property</span></span>     | <span data-ttu-id="dd8fc-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd8fc-105">Type</span></span>        | <span data-ttu-id="dd8fc-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd8fc-106">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="dd8fc-107">destinationServiceIp</span><span class="sxs-lookup"><span data-stu-id="dd8fc-107">destinationServiceIp</span></span>|<span data-ttu-id="dd8fc-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="dd8fc-108">String</span></span>|<span data-ttu-id="dd8fc-109">Dirección IP de destino de la conexión a la aplicación o servicio en la nube.</span><span class="sxs-lookup"><span data-stu-id="dd8fc-109">Destination IP Address of the connection to the cloud application/service.</span></span>|
|<span data-ttu-id="dd8fc-110">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="dd8fc-110">destinationServiceName</span></span>|<span data-ttu-id="dd8fc-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="dd8fc-111">String</span></span>|<span data-ttu-id="dd8fc-112">Nombre de aplicación o servicio en la nube (por ejemplo "Salesforce", "DropBox", etc.).</span><span class="sxs-lookup"><span data-stu-id="dd8fc-112">Cloud application/service name (for example "Salesforce", "DropBox", etc.).</span></span>|
|<span data-ttu-id="dd8fc-113">riskScore</span><span class="sxs-lookup"><span data-stu-id="dd8fc-113">riskScore</span></span>|<span data-ttu-id="dd8fc-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="dd8fc-114">String</span></span>|<span data-ttu-id="dd8fc-115">Puntuación de riesgo calculado/generado por el proveedor de la aplicación o servicio en la nube.</span><span class="sxs-lookup"><span data-stu-id="dd8fc-115">Provider-generated/calculated risk score of the Cloud Application/Service.</span></span> <span data-ttu-id="dd8fc-116">Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="dd8fc-116">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="dd8fc-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dd8fc-117">JSON representation</span></span>

<span data-ttu-id="dd8fc-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dd8fc-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.cloudAppSecurityState"
}-->

```json
{
  "destinationServiceIp": "String",
  "destinationServiceName": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "cloudAppSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->