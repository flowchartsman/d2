#### Features 🚀

- ELK now routes `sql_table` edges to the exact columns (ty @landmaj) [#1681](https://github.com/terrastruct/d2/pull/1681)
- Adds new unfilled triangle arrowhead. [#1711](https://github.com/terrastruct/d2/pull/1711)
- Grid containers can now have custom label positions. [#1715](https://github.com/terrastruct/d2/pull/1715)
- A single board from a multi-board diagram can now be rendered with `--target` flag. [#1725](https://github.com/terrastruct/d2/pull/1725)

#### Improvements 🧹

- Grid cells can now contain nested edges [#1629](https://github.com/terrastruct/d2/pull/1629)
- Edges can now go across constant nears, sequence diagrams, and grids including nested ones. [#1631](https://github.com/terrastruct/d2/pull/1631)
- All vars defined in a scope are accessible everywhere in that scope, i.e., an object can use a var defined after itself. [#1695](https://github.com/terrastruct/d2/pull/1695)
- Encoding API switches to standard zlib encoding so that decoding doesn't depend on source. [#1709](https://github.com/terrastruct/d2/pull/1709)
- `currentcolor` is accepted as a color option to inherit parent colors. (ty @hboomsma) [#1700](https://github.com/terrastruct/d2/pull/1700)
- grid containers can now be sized with `width`/`height` even when using a layout plugin without that feature. [#1731](https://github.com/terrastruct/d2/pull/1731)
- Watch mode watches for changes in both the input file and imported files [#1720](https://github.com/terrastruct/d2/pull/1720)

#### Bugfixes ⛑️

- Fixes a bug calculating grid height with only grid-rows and different horizontal-gap and vertical-gap values. [#1646](https://github.com/terrastruct/d2/pull/1646)
- Grid layout now accounts for each cell's outside labels and icons [#1624](https://github.com/terrastruct/d2/pull/1624)
- Grid layout now accounts for labels wider or taller than the shape and fixes default label positions for image grid cells. [#1670](https://github.com/terrastruct/d2/pull/1670)
- Fixes a panic with a spread substitution in a glob map [#1643](https://github.com/terrastruct/d2/pull/1643)
- Fixes use of `null` in `sql_table` constraints (ty @landmaj) [#1660](https://github.com/terrastruct/d2/pull/1660)
- Fixes elk growing shapes with width/height set [#1679](https://github.com/terrastruct/d2/pull/1679)
- Adds a compiler error when accidentally using an arrowhead on a shape [#1686](https://github.com/terrastruct/d2/pull/1686)
- Correctly reports errors from invalid values set by globs. [#1691](https://github.com/terrastruct/d2/pull/1691)
- Fixes panic when spread substitution referenced a nonexistant var. [#1695](https://github.com/terrastruct/d2/pull/1695)
- Fixes incorrect appendix icon numbering. [#1704](https://github.com/terrastruct/d2/pull/1704)
- Fixes crash when using `--watch` and navigating to an invalid board path [#1693](https://github.com/terrastruct/d2/pull/1693)
- Fixes edge case where nested edge globs were creating excess shapes [#1713](https://github.com/terrastruct/d2/pull/1713)
- Fixes a panic with a connection to a grid cell that is a container in TALA [#1729](https://github.com/terrastruct/d2/pull/1729)
- Fixes incorrect grid cell positioning when the grid has a shape set and fixes content sometimes escaping circle shapes. [#1734](https://github.com/terrastruct/d2/pull/1734)
- Fixes content sometimes escaping cloud shapes. [#1736](https://github.com/terrastruct/d2/pull/1736)
- Fixes panic using a glob filter (e.g. `&a`) outside globs. [#1748](https://github.com/terrastruct/d2/pull/1748)
