# (crudly) patched ImgSizer plugin

I generally use CE Image these days but I have a few old ExpressionEngine sites running ImgSizer.

## Rationale

After upgrading those sites to EE 2.6.1, I had a ton of developer_log warnings about ImgSizer using some deprecated functions. Patching it was easy enough so I did it.

Please note that I do not intend to part ImgSizer or to maintain it, but I though sharing the patch could be useful for others.

## Changelog

- Switched to constructor syntax
- Loaded CI string helper
- Replaced all occurences of `$this->EE->functions->remove_double_slashes()` by `reduce_double_slashes()`