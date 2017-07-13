<span data-ttu-id="b4c26-p105">Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:</span><span class="sxs-lookup"><span data-stu-id="b4c26-p105">This table defines the possible thumbnail sizes. While you can request any arbitrary thumbnail size, the defined values are likely to exist and return a value quickly:</span></span>

Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:

| <span data-ttu-id="b4c26-162">Nombre</span><span class="sxs-lookup"><span data-stu-id="b4c26-162">Name</span></span>           | <span data-ttu-id="b4c26-163">Resolución</span><span class="sxs-lookup"><span data-stu-id="b4c26-163">Resolution</span></span>  | <span data-ttu-id="b4c26-164">Relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="b4c26-164">Aspect Ratio</span></span> | <span data-ttu-id="b4c26-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4c26-165">Description</span></span>                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | <span data-ttu-id="b4c26-166">borde más largo 96</span><span class="sxs-lookup"><span data-stu-id="b4c26-166">96 longest</span></span>  | <span data-ttu-id="b4c26-167">Original</span><span class="sxs-lookup"><span data-stu-id="b4c26-167">Original</span></span>     | <span data-ttu-id="b4c26-168">Miniatura pequeña y muy comprimida recortada en una relación de aspecto cuadrada.</span><span class="sxs-lookup"><span data-stu-id="b4c26-168">Small, highly compressed thumbnail cropped to a square aspect ratio.</span></span> |
| `medium`       | <span data-ttu-id="b4c26-169">borde más largo 176</span><span class="sxs-lookup"><span data-stu-id="b4c26-169">176 longest</span></span> | <span data-ttu-id="b4c26-170">Original</span><span class="sxs-lookup"><span data-stu-id="b4c26-170">Original</span></span>     | <span data-ttu-id="b4c26-171">Miniatura recortada al tamaño estándar del elemento para la vista web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="b4c26-171">Cropped to the standard item size for the OneDrive web view.</span></span>         |
| `large`        | <span data-ttu-id="b4c26-172">borde más largo 800</span><span class="sxs-lookup"><span data-stu-id="b4c26-172">800 longest</span></span> | <span data-ttu-id="b4c26-173">Original</span><span class="sxs-lookup"><span data-stu-id="b4c26-173">Original</span></span>     | <span data-ttu-id="b4c26-174">Miniatura con el borde más largo cambiado a un tamaño de 800 píxeles.</span><span class="sxs-lookup"><span data-stu-id="b4c26-174">Thumbnail with the longest edge resized to 800 pixels.</span></span>               |

## <span data-ttu-id="b4c26-175">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4c26-175">Remarks</span></span>
<a id="remarks" class="xliff"></a>

<span data-ttu-id="b4c26-176">**Nota** En OneDrive para la Empresa y en SharePoint:</span><span class="sxs-lookup"><span data-stu-id="b4c26-176">**Note** In OneDrive for Business and SharePoint:</span></span>

* <span data-ttu-id="b4c26-177">El uso de estas llamadas para expandir la colección de miniaturas no funcionará: `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
  `GET /drive/items/{item-id}/children?expand=thumbnails`</span><span class="sxs-lookup"><span data-stu-id="b4c26-177">Using these calls to expand the thumbnails collection will not work: `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
  `GET /drive/items/{item-id}/children?expand=thumbnails`</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "tocPath": "OneDrive/Item/List thumbnails"
} -->
