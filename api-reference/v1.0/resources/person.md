# <a name="person-resource-type"></a><span data-ttu-id="6194e-101">Tipo de recurso person</span><span class="sxs-lookup"><span data-stu-id="6194e-101">person resource type</span></span>

<span data-ttu-id="6194e-p101">Una agregación de información sobre un contacto de correo electrónico, contactos y redes sociales. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype).</span><span class="sxs-lookup"><span data-stu-id="6194e-p101">An aggregation of information about a person from across mail, contacts, and social networks. People can be local contacts, contacts from social networking or your organization's directory, and people from recent communications (such as email and Skype).</span></span>

## <a name="methods"></a><span data-ttu-id="6194e-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="6194e-104">Methods</span></span>

| <span data-ttu-id="6194e-105">Método</span><span class="sxs-lookup"><span data-stu-id="6194e-105">Method</span></span> | <span data-ttu-id="6194e-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6194e-106">Return Type</span></span> | <span data-ttu-id="6194e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6194e-107">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="6194e-108">List people</span><span class="sxs-lookup"><span data-stu-id="6194e-108">List people</span></span>](../api/user_list_people.md) | <span data-ttu-id="6194e-109">**person**</span><span class="sxs-lookup"><span data-stu-id="6194e-109">**person**</span></span> |<span data-ttu-id="6194e-110">Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="6194e-110">Get a collection of person objects ordered by their relevance to the [user](../resources/user.md).</span></span>|

## <a name="properties"></a><span data-ttu-id="6194e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6194e-111">Properties</span></span>

| <span data-ttu-id="6194e-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6194e-112">Property</span></span> | <span data-ttu-id="6194e-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="6194e-113">Type</span></span> | <span data-ttu-id="6194e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6194e-114">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="6194e-115">birthday</span><span class="sxs-lookup"><span data-stu-id="6194e-115">birthday</span></span>|<span data-ttu-id="6194e-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-116">String</span></span>|<span data-ttu-id="6194e-117">Cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-117">The person's birthday.</span></span>|
|<span data-ttu-id="6194e-118">companyName</span><span class="sxs-lookup"><span data-stu-id="6194e-118">companyName</span></span>|<span data-ttu-id="6194e-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-119">String</span></span>|<span data-ttu-id="6194e-120">Nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-120">The name of the person's company.</span></span>|
|<span data-ttu-id="6194e-121">department</span><span class="sxs-lookup"><span data-stu-id="6194e-121">department</span></span>|<span data-ttu-id="6194e-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-122">String</span></span>|<span data-ttu-id="6194e-123">Departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-123">The person's department.</span></span>|
|<span data-ttu-id="6194e-124">displayName</span><span class="sxs-lookup"><span data-stu-id="6194e-124">displayName</span></span>|<span data-ttu-id="6194e-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-125">String</span></span>|<span data-ttu-id="6194e-126">Nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-126">The person's display name.</span></span>|
|<span data-ttu-id="6194e-127">scoredEmailAddresses</span><span class="sxs-lookup"><span data-stu-id="6194e-127">scoredEmailAddresses</span></span>|<span data-ttu-id="6194e-128">Colección [scoredEmailAddress](scoredemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="6194e-128">[scoredEmailAddress](scoredemailaddress.md) collection</span></span>|<span data-ttu-id="6194e-129">Direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-129">The person's email addresses.</span></span>|
|<span data-ttu-id="6194e-130">givenName</span><span class="sxs-lookup"><span data-stu-id="6194e-130">givenName</span></span>|<span data-ttu-id="6194e-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-131">String</span></span>|<span data-ttu-id="6194e-132">Nombre propio del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-132">The person's given name.</span></span>|
|<span data-ttu-id="6194e-133">id</span><span class="sxs-lookup"><span data-stu-id="6194e-133">id</span></span>|<span data-ttu-id="6194e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-134">String</span></span>|<span data-ttu-id="6194e-p102">Identificador único del contacto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6194e-p102">The person's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="6194e-137">imAddress</span><span class="sxs-lookup"><span data-stu-id="6194e-137">imAddress</span></span>|<span data-ttu-id="6194e-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-138">String</span></span>|<span data-ttu-id="6194e-p103">Dirección del protocolo de inicio de sesión (SIP) de voz sobre IP (VOIP) del servicio de mensajería instantánea correspondiente al usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6194e-p103">The instant message voice over IP (VOIP) session initiation protocol (SIP) address for the user. Read-only.</span></span>|
|<span data-ttu-id="6194e-141">isFavorite</span><span class="sxs-lookup"><span data-stu-id="6194e-141">isFavorite</span></span>|<span data-ttu-id="6194e-142">Booleano</span><span class="sxs-lookup"><span data-stu-id="6194e-142">Boolean</span></span>|<span data-ttu-id="6194e-143">`true` si el usuario ha marcado este contacto como favorito.</span><span class="sxs-lookup"><span data-stu-id="6194e-143">`true` if the user has flagged this person as a favorite.</span></span>|
|<span data-ttu-id="6194e-144">jobTitle</span><span class="sxs-lookup"><span data-stu-id="6194e-144">jobTitle</span></span>|<span data-ttu-id="6194e-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-145">String</span></span>|<span data-ttu-id="6194e-146">Puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-146">The person's job title.</span></span>|
|<span data-ttu-id="6194e-147">officeLocation</span><span class="sxs-lookup"><span data-stu-id="6194e-147">officeLocation</span></span>|<span data-ttu-id="6194e-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-148">String</span></span>|<span data-ttu-id="6194e-149">Ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-149">The location of the person's office.</span></span>|
|<span data-ttu-id="6194e-150">personNotes</span><span class="sxs-lookup"><span data-stu-id="6194e-150">personNotes</span></span>|<span data-ttu-id="6194e-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-151">String</span></span>|<span data-ttu-id="6194e-152">Notas de forma libre que el usuario ha tomado sobre este contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-152">Free-form notes that the user has taken about this person.</span></span>|
|<span data-ttu-id="6194e-153">personType</span><span class="sxs-lookup"><span data-stu-id="6194e-153">personType</span></span>|[<span data-ttu-id="6194e-154">personType</span><span class="sxs-lookup"><span data-stu-id="6194e-154">personType</span></span>](persontype.md) |<span data-ttu-id="6194e-155">El tipo de contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-155">The type of person.</span></span>|
|<span data-ttu-id="6194e-156">phones</span><span class="sxs-lookup"><span data-stu-id="6194e-156">phones</span></span>|<span data-ttu-id="6194e-157">Colección [phone](phone.md)</span><span class="sxs-lookup"><span data-stu-id="6194e-157">[phone](phone.md) collection</span></span>|<span data-ttu-id="6194e-158">Número de teléfono del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-158">The person's phone numbers.</span></span>|
|<span data-ttu-id="6194e-159">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="6194e-159">postalAddresses</span></span>|<span data-ttu-id="6194e-160">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="6194e-160">[location](location.md) collection</span></span>|<span data-ttu-id="6194e-161">Direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-161">The person's addresses.</span></span>|
|<span data-ttu-id="6194e-162">profession</span><span class="sxs-lookup"><span data-stu-id="6194e-162">profession</span></span>|<span data-ttu-id="6194e-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-163">String</span></span>|<span data-ttu-id="6194e-164">Profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-164">The person's profession.</span></span>|
|<span data-ttu-id="6194e-165">surname</span><span class="sxs-lookup"><span data-stu-id="6194e-165">surname</span></span>|<span data-ttu-id="6194e-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-166">String</span></span>|<span data-ttu-id="6194e-167">Apellido del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-167">The person's surname.</span></span>|
|<span data-ttu-id="6194e-168">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6194e-168">userPrincipalName</span></span>|<span data-ttu-id="6194e-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-169">String</span></span>|<span data-ttu-id="6194e-p104">Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](http://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.</span><span class="sxs-lookup"><span data-stu-id="6194e-p104">The user principal name (UPN) of the person. The UPN is an Internet-style login name for the person based on the Internet standard [RFC 822](http://www.ietf.org/rfc/rfc0822.txt). By convention, this should map to the person's email name. The general format is alias@domain.</span></span>|
|<span data-ttu-id="6194e-174">websites</span><span class="sxs-lookup"><span data-stu-id="6194e-174">websites</span></span>|<span data-ttu-id="6194e-175">Colección [website](website.md)</span><span class="sxs-lookup"><span data-stu-id="6194e-175">[website](website.md) collection</span></span>|<span data-ttu-id="6194e-176">Sitios web del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-176">The person's websites.</span></span>|
|<span data-ttu-id="6194e-177">yomiCompany</span><span class="sxs-lookup"><span data-stu-id="6194e-177">yomiCompany</span></span>|<span data-ttu-id="6194e-178">Cadena</span><span class="sxs-lookup"><span data-stu-id="6194e-178">String</span></span>|<span data-ttu-id="6194e-179">Nombre fonético japonés de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="6194e-179">The phonetic Japanese name of the person's company.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6194e-180">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6194e-180">Relationships</span></span>

<span data-ttu-id="6194e-181">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6194e-181">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6194e-182">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6194e-182">JSON representation</span></span>

<span data-ttu-id="6194e-183">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6194e-183">The following is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.person"
}-->

```json
{
  "birthday": "string",
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "scoredEmailAddresses": [{"@odata.type": "microsoft.graph.scoredEmailAddress"}],
  "givenName": "string",
  "id": "string (identifier)",
  "imAddress": "string",
  "isFavorite": true,
  "jobTitle": "string",
  "officeLocation": "string",
  "personNotes": "string",
  "personType": {"@odata.type": "microsoft.graph.personType"},
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.location"}],
  "profession": "string",
  "surname": "string",
  "userPrincipalName": "string",
  "websites": [{"@odata.type": "microsoft.graph.website"}],
  "yomiCompany": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "person resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
