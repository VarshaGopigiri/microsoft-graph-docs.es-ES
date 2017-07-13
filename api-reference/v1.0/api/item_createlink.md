<span data-ttu-id="fb424-p110">Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.</span><span class="sxs-lookup"><span data-stu-id="fb424-p110">When using the `embed` link type, the webUrl returned can be embedded in an `<iframe>` HTML element. When an embed link is created the `webHtml` property contains the HTML code for an `<iframe>` to host the content.</span></span>

Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.

<span data-ttu-id="fb424-164">**Nota:** Los vínculos para insertar solo se admiten en [unidades](../resources/drive.md) donde el **driveType** es `personal`.</span><span class="sxs-lookup"><span data-stu-id="fb424-164">**Note:** Embed links are only supported in [Drives](../resources/drive.md) where the **driveType** is `personal`.</span></span>

## <span data-ttu-id="fb424-165">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb424-165">Remarks</span></span>
<a id="remarks" class="xliff"></a>

* <span data-ttu-id="fb424-166">Los vínculos creados con esta acción no caducan a menos que la organización fuerce una política de caducidad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fb424-166">Links created using this action do not expire unless a default expiration policy is enforced for the organization.</span></span>
* <span data-ttu-id="fb424-167">Los vínculos se pueden ver en los permisos de uso compartido del elemento y los puede eliminar un propietario del elemento.</span><span class="sxs-lookup"><span data-stu-id="fb424-167">Links are visible in the sharing permissions for the item and can be removed by an owner of the item.</span></span>
* <span data-ttu-id="fb424-168">Los vínculos siempre señalan la versión actual de un elemento, a menos que el elemento esté desprotegido (solo en SharePoint).</span><span class="sxs-lookup"><span data-stu-id="fb424-168">Links always point to the current version of a item unless the item is checked out (SharePoint only).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "item: createLink",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Create sharing link"
} -->
