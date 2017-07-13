<span data-ttu-id="86bb8-p102">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los id. de usuario como propiedades y sus valores deben ser el booleano `true`. Si los id. de usuario ya no se comparten, las propiedades se quitarán automáticamente estableciendo sus valores en el booleano `false`.</span><span class="sxs-lookup"><span data-stu-id="86bb8-p102">Properties of an Open Type can be defined by the client. In this case, the client should provide user ids as properties with their values being the `true` boolean. When user ids are no longer shared with, properties are automatically removed by setting their values to the `false` boolean.</span></span>
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los id. de usuario como propiedades y sus valores deben ser el booleano `true`. Si los id. de usuario ya no se comparten, las propiedades se quitarán automáticamente estableciendo sus valores en el booleano `false`.


## <span data-ttu-id="86bb8-110">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="86bb8-110">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>

<span data-ttu-id="86bb8-111">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="86bb8-111">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUserIds"
}-->

```json
{
  "String-value": true
}
```

<span data-ttu-id="86bb8-112">// Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86bb8-112">// Example</span></span>
```json
{
  "400723e1-102b-43aa-aba9-f35524827084": true, // property name is user id
  "f117339e-c914-4a9c-9b66-1c062b027556": true,
  "e886d105-23b9-47e2-bde1-757e75ee4a28": true
}

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerUserIds resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->