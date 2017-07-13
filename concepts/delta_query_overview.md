<span data-ttu-id="a7031-p114">\* El patrón de uso para los recursos de OneDrive es similar a los demás recursos compatibles con algunas diferencias secundarias de sintaxis. La consulta delta para unidades se actualizará en el futuro para que sea coherente con otros tipos de recursos. Para obtener más detalles sobre la sintaxis actual, vea: <https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/item_delta></span><span class="sxs-lookup"><span data-stu-id="a7031-p114">\* Tracking changes to drives and their children is already supported in v1.0. The usage pattern is similar to the other supported resources with some minor syntax differences. Delta query for drives will be updated in the future to be consistent with other resource types. For more detail about the current syntax, please see: <https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/item_delta></span></span> |


> \* El patrón de uso para los recursos de OneDrive es similar a los demás recursos compatibles con algunas diferencias secundarias de sintaxis. La consulta delta para unidades se actualizará en el futuro para que sea coherente con otros tipos de recursos. Para obtener más detalles sobre la sintaxis actual, vea: <https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/item_delta>

## <span data-ttu-id="a7031-174">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a7031-174">Prerequisites</span></span>
<a id="prerequisites" class="xliff"></a>

<span data-ttu-id="a7031-175">Los mismos [permisos](./permissions_reference.md) que se requieren para leer un recurso específico también son necesarios para realizar la consulta delta en ellos.</span><span class="sxs-lookup"><span data-stu-id="a7031-175">The same [permissions](./permissions_reference.md) that are required to read a specific resource are also required to perform delta query on that resource.</span></span>

## <span data-ttu-id="a7031-176">Ejemplos de solicitud de consulta delta</span><span class="sxs-lookup"><span data-stu-id="a7031-176">Delta query request examples</span></span>
<a id="delta-query-request-examples" class="xliff"></a> 

- [<span data-ttu-id="a7031-177">Obtener los cambios incrementales de los eventos en una vista de calendario</span><span class="sxs-lookup"><span data-stu-id="a7031-177">Get incremental changes to events in a calendar view (preview)</span></span>](../Concepts/delta_query_events.md)
- [<span data-ttu-id="a7031-178">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="a7031-178">Get incremental changes to messages in a folder (preview)</span></span>](./delta_query_messages.md)
- [<span data-ttu-id="a7031-179">Obtener los cambios incrementales en los grupos</span><span class="sxs-lookup"><span data-stu-id="a7031-179">Get incremental changes to groups (preview)</span></span>](./delta_query_groups.md)
- [<span data-ttu-id="a7031-180">Obtener los cambios incrementales en los usuarios</span><span class="sxs-lookup"><span data-stu-id="a7031-180">Get incremental changes to users (preview)</span></span>](./delta_query_users.md)