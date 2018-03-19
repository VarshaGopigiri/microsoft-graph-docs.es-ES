# <a name="person-resource-type"></a><span data-ttu-id="00051-101">Tipo de recurso person</span><span class="sxs-lookup"><span data-stu-id="00051-101">person resource type</span></span>

<span data-ttu-id="00051-p101">Una agregación de información sobre un contacto de correo electrónico, contactos y redes sociales. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype).</span><span class="sxs-lookup"><span data-stu-id="00051-p101">An aggregation of information about a person from across mail, contacts, and social networks. People can be local contacts, contacts from social networking or your organization's directory, and people from recent communications (such as email and Skype).</span></span>

## <a name="methods"></a><span data-ttu-id="00051-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="00051-104">Methods</span></span>

| <span data-ttu-id="00051-105">Método</span><span class="sxs-lookup"><span data-stu-id="00051-105">Method</span></span>           | <span data-ttu-id="00051-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00051-106">Return Type</span></span>    |<span data-ttu-id="00051-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="00051-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="00051-108">List people</span><span class="sxs-lookup"><span data-stu-id="00051-108">List people</span></span>](../api/user_list_people.md) | <span data-ttu-id="00051-109">**person**</span><span class="sxs-lookup"><span data-stu-id="00051-109">**person**</span></span> |<span data-ttu-id="00051-110">Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="00051-110">Get a collection of person objects ordered by their relevance to the [user](../resources/user.md).</span></span>|
|[<span data-ttu-id="00051-111">Get person</span><span class="sxs-lookup"><span data-stu-id="00051-111">Get person</span></span>](../api/person_get.md) | <span data-ttu-id="00051-112">**person**</span><span class="sxs-lookup"><span data-stu-id="00051-112">**person**</span></span> |<span data-ttu-id="00051-113">Recupere las propiedades y las relaciones del objeto person.</span><span class="sxs-lookup"><span data-stu-id="00051-113">Get properties and relationships of a person object.</span></span>|

## <a name="properties"></a><span data-ttu-id="00051-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00051-114">Properties</span></span>
| <span data-ttu-id="00051-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00051-115">Property</span></span>     | <span data-ttu-id="00051-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="00051-116">Type</span></span>   |<span data-ttu-id="00051-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="00051-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="00051-118">birthday</span><span class="sxs-lookup"><span data-stu-id="00051-118">birthday</span></span>|<span data-ttu-id="00051-119">String</span><span class="sxs-lookup"><span data-stu-id="00051-119">String</span></span>|<span data-ttu-id="00051-120">Cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-120">The person's birthday.</span></span>|
|<span data-ttu-id="00051-121">companyName</span><span class="sxs-lookup"><span data-stu-id="00051-121">companyName</span></span>|<span data-ttu-id="00051-122">String</span><span class="sxs-lookup"><span data-stu-id="00051-122">String</span></span>|<span data-ttu-id="00051-123">Nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-123">The name of the person's company.</span></span>|
|<span data-ttu-id="00051-124">department</span><span class="sxs-lookup"><span data-stu-id="00051-124">department</span></span>|<span data-ttu-id="00051-125">String</span><span class="sxs-lookup"><span data-stu-id="00051-125">String</span></span>|<span data-ttu-id="00051-126">Departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-126">The person's department.</span></span>|
|<span data-ttu-id="00051-127">displayName</span><span class="sxs-lookup"><span data-stu-id="00051-127">displayName</span></span>|<span data-ttu-id="00051-128">String</span><span class="sxs-lookup"><span data-stu-id="00051-128">String</span></span>|<span data-ttu-id="00051-129">Nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-129">The person's display name.</span></span>|
|<span data-ttu-id="00051-130">scoredEmailAddresses</span><span class="sxs-lookup"><span data-stu-id="00051-130">scoredEmailAddresses</span></span>|<span data-ttu-id="00051-131">Colección [scoredEmailAddress](scoredemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="00051-131">[scoredEmailAddress](scoredemailaddress.md) collection</span></span>|<span data-ttu-id="00051-132">Direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-132">The person's email addresses.</span></span>|
|<span data-ttu-id="00051-133">givenName</span><span class="sxs-lookup"><span data-stu-id="00051-133">givenName</span></span>|<span data-ttu-id="00051-134">String</span><span class="sxs-lookup"><span data-stu-id="00051-134">String</span></span>|<span data-ttu-id="00051-135">Nombre propio del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-135">The person's given name.</span></span>|
|<span data-ttu-id="00051-136">id</span><span class="sxs-lookup"><span data-stu-id="00051-136">id</span></span>|<span data-ttu-id="00051-137">String</span><span class="sxs-lookup"><span data-stu-id="00051-137">String</span></span>|<span data-ttu-id="00051-p102">Identificador único del contacto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00051-p102">The person's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="00051-140">imAddress</span><span class="sxs-lookup"><span data-stu-id="00051-140">imAddress</span></span>|<span data-ttu-id="00051-141">String</span><span class="sxs-lookup"><span data-stu-id="00051-141">String</span></span>|<span data-ttu-id="00051-p103">Dirección del protocolo de inicio de sesión (SIP) de voz sobre IP (VOIP) del servicio de mensajería instantánea correspondiente al usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00051-p103">The instant message voice over IP (VOIP) session initiation protocol (SIP) address for the user. Read-only.</span></span>|
|<span data-ttu-id="00051-144">isFavorite</span><span class="sxs-lookup"><span data-stu-id="00051-144">isFavorite</span></span>|<span data-ttu-id="00051-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="00051-145">Boolean</span></span>|<span data-ttu-id="00051-146">`true` si el usuario ha marcado este contacto como favorito.</span><span class="sxs-lookup"><span data-stu-id="00051-146">`true` if the user has flagged this person as a favorite.</span></span>|
|<span data-ttu-id="00051-147">jobTitle</span><span class="sxs-lookup"><span data-stu-id="00051-147">jobTitle</span></span>|<span data-ttu-id="00051-148">String</span><span class="sxs-lookup"><span data-stu-id="00051-148">String</span></span>|<span data-ttu-id="00051-149">Puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-149">The person's job title.</span></span>|
|<span data-ttu-id="00051-150">officeLocation</span><span class="sxs-lookup"><span data-stu-id="00051-150">officeLocation</span></span>|<span data-ttu-id="00051-151">String</span><span class="sxs-lookup"><span data-stu-id="00051-151">String</span></span>|<span data-ttu-id="00051-152">Ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-152">The location of the person's office.</span></span>|
|<span data-ttu-id="00051-153">personNotes</span><span class="sxs-lookup"><span data-stu-id="00051-153">personNotes</span></span>|<span data-ttu-id="00051-154">String</span><span class="sxs-lookup"><span data-stu-id="00051-154">String</span></span>|<span data-ttu-id="00051-155">Notas de forma libre que el usuario ha tomado sobre este contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-155">Free-form notes that the the user has taken about this person.</span></span>|
|<span data-ttu-id="00051-156">personType</span><span class="sxs-lookup"><span data-stu-id="00051-156">personType</span></span>|<span data-ttu-id="00051-157">Colección [personType](persontype.md)</span><span class="sxs-lookup"><span data-stu-id="00051-157">[personType](persontype.md) collection</span></span>|<span data-ttu-id="00051-158">Tipo de contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-158">The type of person.</span></span>|
|<span data-ttu-id="00051-159">phones</span><span class="sxs-lookup"><span data-stu-id="00051-159">phones</span></span>|<span data-ttu-id="00051-160">Colección [phone](phone.md)</span><span class="sxs-lookup"><span data-stu-id="00051-160">[phone](phone.md) collection</span></span>|<span data-ttu-id="00051-161">Número de teléfono del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-161">The person's phone numbers.</span></span>|
|<span data-ttu-id="00051-162">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="00051-162">postalAddresses</span></span>|<span data-ttu-id="00051-163">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="00051-163">[location](location.md) collection</span></span>|<span data-ttu-id="00051-164">Direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-164">The person's addresses.</span></span>|
|<span data-ttu-id="00051-165">profession</span><span class="sxs-lookup"><span data-stu-id="00051-165">profession</span></span>|<span data-ttu-id="00051-166">String</span><span class="sxs-lookup"><span data-stu-id="00051-166">String</span></span>|<span data-ttu-id="00051-167">Profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-167">The person's profession.</span></span>|
|<span data-ttu-id="00051-168">surname</span><span class="sxs-lookup"><span data-stu-id="00051-168">surname</span></span>|<span data-ttu-id="00051-169">String</span><span class="sxs-lookup"><span data-stu-id="00051-169">String</span></span>|<span data-ttu-id="00051-170">Apellido del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-170">The person's surname.</span></span>|
|<span data-ttu-id="00051-171">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="00051-171">userPrincipalName</span></span>|<span data-ttu-id="00051-172">String</span><span class="sxs-lookup"><span data-stu-id="00051-172">String</span></span>|<span data-ttu-id="00051-p104">Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](http://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.</span><span class="sxs-lookup"><span data-stu-id="00051-p104">The user principal name (UPN) of the person. The UPN is an Internet-style login name for the person based on the Internet standard [RFC 822](http://www.ietf.org/rfc/rfc0822.txt). By convention, this should map to the person's email name. The general format is alias@domain.</span></span>|
|<span data-ttu-id="00051-177">websites</span><span class="sxs-lookup"><span data-stu-id="00051-177">websites</span></span>|<span data-ttu-id="00051-178">Colección [website](website.md)</span><span class="sxs-lookup"><span data-stu-id="00051-178">[website](website.md) collection</span></span>|<span data-ttu-id="00051-179">Sitios web del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-179">The person's websites.</span></span>|
|<span data-ttu-id="00051-180">yomiCompany</span><span class="sxs-lookup"><span data-stu-id="00051-180">yomiCompany</span></span>|<span data-ttu-id="00051-181">String</span><span class="sxs-lookup"><span data-stu-id="00051-181">String</span></span>|<span data-ttu-id="00051-182">Nombre fonético japonés de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="00051-182">The phonetic Japanese name of the person's company.</span></span>|

## <a name="relationships"></a><span data-ttu-id="00051-183">Relaciones</span><span class="sxs-lookup"><span data-stu-id="00051-183">Relationships</span></span>
<span data-ttu-id="00051-184">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="00051-184">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="00051-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="00051-185">JSON representation</span></span>

<span data-ttu-id="00051-186">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="00051-186">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
