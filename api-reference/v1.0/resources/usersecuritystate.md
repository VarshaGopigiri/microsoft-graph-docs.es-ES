# <a name="usersecuritystate-resource-type"></a><span data-ttu-id="d831b-101">Tipo de recurso userSecurityState</span><span class="sxs-lookup"><span data-stu-id="d831b-101">userSecurityState resource type</span></span>

<span data-ttu-id="d831b-102">Contiene información de estado acerca de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="d831b-102">Contains stateful information about the user account.</span></span>

## <a name="properties"></a><span data-ttu-id="d831b-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d831b-103">Properties</span></span>

| <span data-ttu-id="d831b-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d831b-104">Property</span></span>   | <span data-ttu-id="d831b-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="d831b-105">Type</span></span> |<span data-ttu-id="d831b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d831b-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d831b-107">aadUserId</span><span class="sxs-lookup"><span data-stu-id="d831b-107">aadUserId</span></span>|<span data-ttu-id="d831b-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-108">String</span></span>|<span data-ttu-id="d831b-109">Identificador de objeto de usuario (GUID) de AAD: representa la entidad de usuario física/multicuenta.</span><span class="sxs-lookup"><span data-stu-id="d831b-109">AAD User object identifier (GUID) - represents the physical/multi-account user entity.</span></span>|
|<span data-ttu-id="d831b-110">accountName</span><span class="sxs-lookup"><span data-stu-id="d831b-110">accountName</span></span>|<span data-ttu-id="d831b-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-111">String</span></span>|<span data-ttu-id="d831b-112">Nombre de cuenta de la cuenta de usuario (sin dominio de Active Directory o dominio DNS) - (también denominada `mailNickName`).</span><span class="sxs-lookup"><span data-stu-id="d831b-112">Account name of user account (without Active Directory domain or DNS domain) - (also called `mailNickName`).</span></span>|
|<span data-ttu-id="d831b-113">domainName</span><span class="sxs-lookup"><span data-stu-id="d831b-113">domainName</span></span>|<span data-ttu-id="d831b-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-114">String</span></span>|<span data-ttu-id="d831b-115">Dominio de NetBIOS o Active Directory de la cuenta de usuario (es decir, el formato dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d831b-115">NetBIOS/Active Directory domain of user account (that is, domain\account format).</span></span>|
|<span data-ttu-id="d831b-116">emailRole</span><span class="sxs-lookup"><span data-stu-id="d831b-116">emailRole</span></span>|<span data-ttu-id="d831b-117">emailRole</span><span class="sxs-lookup"><span data-stu-id="d831b-117">emailRole</span></span>|<span data-ttu-id="d831b-118">Para las alertas relacionadas con el correo electrónico: correo electrónico de una cuenta de usuario 'rol'.</span><span class="sxs-lookup"><span data-stu-id="d831b-118">For email-related alerts - user account's email 'role'.</span></span> <span data-ttu-id="d831b-119">Los valores posibles son: `unknown`, `sender` y `recipient`.</span><span class="sxs-lookup"><span data-stu-id="d831b-119">Possible values are: `unknown`, `sender`, `recipient`.</span></span>|
|<span data-ttu-id="d831b-120">isVpn</span><span class="sxs-lookup"><span data-stu-id="d831b-120">isVpn</span></span>|<span data-ttu-id="d831b-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="d831b-121">Boolean</span></span>|<span data-ttu-id="d831b-122">Indica si el usuario se ha conectado mediante una red privada virtual (VPN).</span><span class="sxs-lookup"><span data-stu-id="d831b-122">Indicates whether the user logged on through a VPN.</span></span>|
|<span data-ttu-id="d831b-123">logonDateTime</span><span class="sxs-lookup"><span data-stu-id="d831b-123">logonDateTime</span></span>|<span data-ttu-id="d831b-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d831b-124">DateTimeOffset</span></span>|<span data-ttu-id="d831b-125">Hora del inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d831b-125">Time at which the sign-in occurred.</span></span> <span data-ttu-id="d831b-126">El tipo de marca de hora representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="d831b-126">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="d831b-127">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="d831b-127">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="d831b-128">logonId</span><span class="sxs-lookup"><span data-stu-id="d831b-128">logonId</span></span>|<span data-ttu-id="d831b-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-129">String</span></span>|<span data-ttu-id="d831b-130">Id. de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d831b-130">User sign-in ID.</span></span>|
|<span data-ttu-id="d831b-131">logonIp</span><span class="sxs-lookup"><span data-stu-id="d831b-131">logonIp</span></span>|<span data-ttu-id="d831b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-132">String</span></span>|<span data-ttu-id="d831b-133">Dirección IP desde la que se ha originado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d831b-133">IP Address the sign-in request originated from.</span></span>|
|<span data-ttu-id="d831b-134">logonLocation</span><span class="sxs-lookup"><span data-stu-id="d831b-134">logonLocation</span></span>|<span data-ttu-id="d831b-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-135">String</span></span>|<span data-ttu-id="d831b-136">Ubicación (mediante asignación de dirección IP) asociada a un evento de inicio de sesión de usuario por parte de este usuario.</span><span class="sxs-lookup"><span data-stu-id="d831b-136">Location (by IP address mapping) associated with a user sign-in event by this user.</span></span>|
|<span data-ttu-id="d831b-137">logonType</span><span class="sxs-lookup"><span data-stu-id="d831b-137">logonType</span></span>|<span data-ttu-id="d831b-138">logonType</span><span class="sxs-lookup"><span data-stu-id="d831b-138">logonType</span></span>|<span data-ttu-id="d831b-139">Método de inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="d831b-139">Method of user sign in.</span></span> <span data-ttu-id="d831b-140">Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch` y `service`.</span><span class="sxs-lookup"><span data-stu-id="d831b-140">Possible values are: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span></span>|
|<span data-ttu-id="d831b-141">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="d831b-141">onPremisesSecurityIdentifier</span></span>|<span data-ttu-id="d831b-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-142">String</span></span>|<span data-ttu-id="d831b-143">Identificador de seguridad (SID) de Active Directory (local) del usuario.</span><span class="sxs-lookup"><span data-stu-id="d831b-143">Active Directory (on-premises) Security Identifier (SID) of the user.</span></span>|
|<span data-ttu-id="d831b-144">riskScore</span><span class="sxs-lookup"><span data-stu-id="d831b-144">riskScore</span></span>|<span data-ttu-id="d831b-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-145">String</span></span>|<span data-ttu-id="d831b-146">Puntuación de riesgo calculado/generado por el proveedor de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="d831b-146">Provider-generated/calculated risk score of the user account.</span></span> <span data-ttu-id="d831b-147">Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="d831b-147">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="d831b-148">userAccountType</span><span class="sxs-lookup"><span data-stu-id="d831b-148">userAccountType</span></span>|<span data-ttu-id="d831b-149">userAccountSecurityType</span><span class="sxs-lookup"><span data-stu-id="d831b-149">userAccountSecurityType</span></span>|<span data-ttu-id="d831b-150">Tipo de cuenta de usuario (pertenencia a grupo), por definición de Windows.</span><span class="sxs-lookup"><span data-stu-id="d831b-150">User account type (group membership), per Windows definition.</span></span> <span data-ttu-id="d831b-151">Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.</span><span class="sxs-lookup"><span data-stu-id="d831b-151">Possible values are: `unknown`, `standard`, `power`, `administrator`.</span></span>|
|<span data-ttu-id="d831b-152">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d831b-152">userPrincipalName</span></span>|<span data-ttu-id="d831b-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="d831b-153">String</span></span>|<span data-ttu-id="d831b-154">Nombre de inicio de sesión de usuario - formato de internet: (nombre de cuenta de usuario) @(nombre de dominio DNS de cuenta de usuario).</span><span class="sxs-lookup"><span data-stu-id="d831b-154">User sign-in name - internet format: (user account name)@(user account DNS domain name).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d831b-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d831b-155">JSON representation</span></span>

<span data-ttu-id="d831b-156">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d831b-156">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userSecurityState"
}-->

```json
{
  "aadUserId": "String",
  "accountName": "String",
  "domainName": "String",
  "emailRole": "@odata.type: microsoft.graph.emailRole",
  "isVpn": true,
  "logonDateTime": "String (timestamp)",
  "logonId": "String",
  "logonIp": "String",
  "logonLocation": "String",
  "logonType": "@odata.type: microsoft.graph.logonType",
  "onPremisesSecurityIdentifier": "String",
  "riskScore": "String",
  "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
