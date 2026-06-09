# starmap patches

Temporary patches applied during CI before installing [starmap](https://github.com/nozomi-koborinai/starmap).

## `starmap-graphql-resource-limits.patch`

Fixes `RESOURCE_LIMITS_EXCEEDED` when exporting large Star Lists. The upstream
client fetched up to 100 list items per list inside a single GraphQL query; this
patch fetches list metadata first and paginates items per list instead.

Remove this patch once the fix lands in `nozomi-koborinai/starmap` and the
workflow can go back to `cargo install --git`.
