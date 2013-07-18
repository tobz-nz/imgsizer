# (crudly) patched ImgSizer plugin

I generally use [CE Image](http://www.causingeffect.com/software/expressionengine/ce-image) these days, and so should you. CE Image offers possibilities and Aaron is committed to support and evolve it. If you are looking for alternatives, [have a look on Devot-ee](http://devot-ee.com/search/tags/tag/resize).

## Rationale

My problem is that I have a few old ExpressionEngine sites running ImgSizer. After upgrading those sites to EE 2.6.1, I had a ton of developer_log warnings about ImgSizer using some deprecated functions. Patching it was easy enough so I did it.

Please note that I do not intend to port ImgSizer to EE2 or to maintain it, but I though sharing the patch could be useful for others.

Now I have another reason to redesign those sites and replace ImgSizer.

## Changelog

- Switched to constructor syntax
- Loaded CI string helper
- Replaced all occurences of `$this->EE->functions->remove_double_slashes()` with `reduce_double_slashes()`