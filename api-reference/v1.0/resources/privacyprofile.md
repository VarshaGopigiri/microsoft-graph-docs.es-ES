# <a name="privacyprofile-resource-type"></a><span data-ttu-id="ee264-101">Tipo de recurso privacyProfile</span><span class="sxs-lookup"><span data-stu-id="ee264-101">privacyProfile resource type</span></span>

<span data-ttu-id="ee264-102">Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="ee264-102">Represents a company's privacy profile, which includes a privacy statement URL and a contact person for questions regarding the privacy statement.</span></span>

## <a name="properties"></a><span data-ttu-id="ee264-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee264-103">Properties</span></span>
| <span data-ttu-id="ee264-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee264-104">Property</span></span>   | <span data-ttu-id="ee264-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee264-105">Type</span></span>|<span data-ttu-id="ee264-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee264-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee264-107">contactEmail</span><span class="sxs-lookup"><span data-stu-id="ee264-107">contactEmail</span></span>|<span data-ttu-id="ee264-108">String</span><span class="sxs-lookup"><span data-stu-id="ee264-108">String</span></span>| <span data-ttu-id="ee264-109">Dirección de correo electrónico smtp válida para el contacto de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="ee264-109">A valid smtp email address for the privacy statement contact.</span></span> <span data-ttu-id="ee264-110">No se requiere.</span><span class="sxs-lookup"><span data-stu-id="ee264-110">Not required</span></span>|
|<span data-ttu-id="ee264-111">statementUrl</span><span class="sxs-lookup"><span data-stu-id="ee264-111">statementUrl</span></span>|<span data-ttu-id="ee264-112">String</span><span class="sxs-lookup"><span data-stu-id="ee264-112">String</span></span>| <span data-ttu-id="ee264-113">Formato de URL válido que empiece por http:// o https://.</span><span class="sxs-lookup"><span data-stu-id="ee264-113">A valid URL format that begins with http:// or https://.</span></span> <span data-ttu-id="ee264-114">La longitud máxima es de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee264-114">The maximum length is 255 characters.</span></span> <span data-ttu-id="ee264-115">Dirección URL que se dirige a la declaración de privacidad de la compañía.</span><span class="sxs-lookup"><span data-stu-id="ee264-115">The URL that directs to the company's privacy statement.</span></span> <span data-ttu-id="ee264-116">No se requiere.</span><span class="sxs-lookup"><span data-stu-id="ee264-116">Not required</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ee264-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee264-117">JSON representation</span></span>

<span data-ttu-id="ee264-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ee264-118">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privacyProfile"
}-->

```json
{
  "contactEmail": "string",
  "statementUrl": "string"
}
```