# <a name="hostsecuritystate-resource-type"></a><span data-ttu-id="f356c-101">Tipo de recurso hostSecurityState</span><span class="sxs-lookup"><span data-stu-id="f356c-101">hostSecurityState resource type</span></span>

<span data-ttu-id="f356c-102">Contiene información de estado acerca del host (incluidos los dispositivos, equipos, etc.).</span><span class="sxs-lookup"><span data-stu-id="f356c-102">Contains stateful information about the host (including devices, computers, and so on).</span></span>

## <a name="properties"></a><span data-ttu-id="f356c-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f356c-103">Properties</span></span>

| <span data-ttu-id="f356c-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f356c-104">Property</span></span>   | <span data-ttu-id="f356c-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="f356c-105">Type</span></span>|<span data-ttu-id="f356c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f356c-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f356c-107">fqdn</span><span class="sxs-lookup"><span data-stu-id="f356c-107">FQDN</span></span>|<span data-ttu-id="f356c-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="f356c-108">String</span></span>|<span data-ttu-id="f356c-109">Nombre de dominio completo del host (por ejemplo, `machine.company.com`).</span><span class="sxs-lookup"><span data-stu-id="f356c-109">Host FQDN (Fully Qualified Domain Name) (for example, `machine.company.com`).</span></span>|
|<span data-ttu-id="f356c-110">isAzureAadJoined</span><span class="sxs-lookup"><span data-stu-id="f356c-110">isAzureAadJoined</span></span>|<span data-ttu-id="f356c-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="f356c-111">Boolean</span></span>|<span data-ttu-id="f356c-112">True si el host es el dominio unido a los servicios de dominio de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f356c-112">True if the host is domain joined to Azure Active Directory Domain Services.</span></span>|
|<span data-ttu-id="f356c-113">isAzureAadRegistered</span><span class="sxs-lookup"><span data-stu-id="f356c-113">isAzureAadRegistered</span></span>|<span data-ttu-id="f356c-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="f356c-114">Boolean</span></span>|<span data-ttu-id="f356c-115">True si el host se ha registrado con el registro de dispositivos de Azure Active Directory (dispositivos BYOD, es decir, no administrados por completo por la empresa).</span><span class="sxs-lookup"><span data-stu-id="f356c-115">True if the host registered with Azure Active Directory Device Registration (BYOD devices - that is, not fully managed by enterprise).</span></span>|
|<span data-ttu-id="f356c-116">isHybridAzureDomainJoined</span><span class="sxs-lookup"><span data-stu-id="f356c-116">isHybridAzureDomainJoined</span></span>|<span data-ttu-id="f356c-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="f356c-117">Boolean</span></span>|<span data-ttu-id="f356c-118">True si el host se ha unido a un dominio local de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f356c-118">True if the host is domain joined to an on-premises Active Directory domain.</span></span>|
|<span data-ttu-id="f356c-119">netBiosName</span><span class="sxs-lookup"><span data-stu-id="f356c-119">netBiosName</span></span>|<span data-ttu-id="f356c-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="f356c-120">String</span></span>|<span data-ttu-id="f356c-121">El nombre de host local, sin el nombre de dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="f356c-121">The local host name, without the DNS domain name.</span></span>|
|<span data-ttu-id="f356c-122">os</span><span class="sxs-lookup"><span data-stu-id="f356c-122">OS</span></span>|<span data-ttu-id="f356c-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="f356c-123">String</span></span>|<span data-ttu-id="f356c-124">Sistema operativo del host.</span><span class="sxs-lookup"><span data-stu-id="f356c-124">Host Operating System.</span></span> <span data-ttu-id="f356c-125">(Por ejemplo, Windows10, Mac OS, RHEL, etcetera.).</span><span class="sxs-lookup"><span data-stu-id="f356c-125">(For example, Windows10, MacOS, RHEL, etc.).</span></span>|
|<span data-ttu-id="f356c-126">privateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f356c-126">privateIpAddress</span></span>|<span data-ttu-id="f356c-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="f356c-127">String</span></span>|<span data-ttu-id="f356c-128">Dirección de IPv4 o IPv6 (no enrutable) privada (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.</span><span class="sxs-lookup"><span data-stu-id="f356c-128">Private (not routable) IPv4 or IPv6 address (see [RFC 1918](https://tools.ietf.org/html/rfc1918)) at the time of the alert.</span></span>|
|<span data-ttu-id="f356c-129">publicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f356c-129">publicIpAddress</span></span>|<span data-ttu-id="f356c-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f356c-130">String</span></span>|<span data-ttu-id="f356c-131">Dirección IPv4 o IPv6 enrutable públicamente (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.</span><span class="sxs-lookup"><span data-stu-id="f356c-131">Publicly routable IPv4 or IPv6 address (see [RFC 1918](https://tools.ietf.org/html/rfc1918)) at time of the alert.</span></span>|
|<span data-ttu-id="f356c-132">riskScore</span><span class="sxs-lookup"><span data-stu-id="f356c-132">riskScore</span></span>|<span data-ttu-id="f356c-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="f356c-133">String</span></span>|<span data-ttu-id="f356c-134">Puntuación de riesgo calculado/generado por el proveedor del host.</span><span class="sxs-lookup"><span data-stu-id="f356c-134">Provider-generated/calculated risk score of the host.</span></span>  <span data-ttu-id="f356c-135">Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="f356c-135">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f356c-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f356c-136">JSON representation</span></span>

<span data-ttu-id="f356c-137">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f356c-137">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityState"
}-->

```json
{
  "fqdn": "String",
  "isAzureAadJoined": true,
  "isAzureAadRegistered": true,
  "isHybridAzureDomainJoined": true,
  "netBiosName": "String",
  "os": "String",
  "privateIpAddress": "String",
  "publicIpAddress": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hostSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
