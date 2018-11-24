# <a name="localeinfo-resource-type"></a><span data-ttu-id="8247f-101">Tipo de recurso localeInfo</span><span class="sxs-lookup"><span data-stu-id="8247f-101">localeInfo resource type</span></span>

<span data-ttu-id="8247f-102">Información sobre la configuración regional, como el idioma preferido y el país o región del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="8247f-102">Information about the locale, including the preferred language and country/region, of the signed-in user.</span></span>


## <a name="properties"></a><span data-ttu-id="8247f-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8247f-103">Properties</span></span>
| <span data-ttu-id="8247f-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8247f-104">Property</span></span>     | <span data-ttu-id="8247f-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="8247f-105">Type</span></span>   |<span data-ttu-id="8247f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8247f-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8247f-107">configuración regional</span><span class="sxs-lookup"><span data-stu-id="8247f-107">locale</span></span>|<span data-ttu-id="8247f-108">string</span><span class="sxs-lookup"><span data-stu-id="8247f-108">string</span></span>|<span data-ttu-id="8247f-p101">Representación de la configuración regional del usuario, que incluye el idioma preferido y el país o región del usuario. Por ejemplo, "es-es". El componente de idioma sigue códigos de dos letras, tal y como se define en [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm), y el componente de país sigue códigos de dos letras, tal y como se define en [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm).</span><span class="sxs-lookup"><span data-stu-id="8247f-p101">A locale representation for the user, which includes the user's preferred language and country/region. For example, "en-us". The language component follows 2-letter codes as defined in [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm), and the country component follows 2-letter codes as defined in [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm).</span></span>|
|<span data-ttu-id="8247f-112">displayName</span><span class="sxs-lookup"><span data-stu-id="8247f-112">displayName</span></span>|<span data-ttu-id="8247f-113">string</span><span class="sxs-lookup"><span data-stu-id="8247f-113">string</span></span>|<span data-ttu-id="8247f-114">Nombre que representa la configuración regional del usuario en lenguaje natural, por ejemplo, "Inglés (Estados Unidos)".</span><span class="sxs-lookup"><span data-stu-id="8247f-114">A name representing the user's locale in natural language, for example, "English (United States)".</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8247f-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8247f-115">JSON representation</span></span>

<span data-ttu-id="8247f-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8247f-116">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.localeInfo"
}-->

```json
{
  "locale": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "localeInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->