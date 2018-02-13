# uniform api

# Goal

A way to get a stable behavior for some critical lua functions.
Used as minimal requirement to setup more advanced stuff.

uniformapi is the minimal requirement for [lua-box](https://github.com/tst2005/lua-box).

# supported versions

* Lua 5.1
* Lua 5.2
* Lua 5.3
* LuaJIT 2.0 (equal to Lua 5.1)
* LuaJIT 2.1 (partialy equal to Lua 5.2)

# not supported versions

* Lua 5.0 seems to have too many things to be fixed to be supported (but I tried for the fun)

## uniform api content

* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-load) `load(chunk [, chunkname [, mode [, env]]])` (support of env as 4th argument)
  * do not use the Lua 5.1 `setfenv`, `getfenv`, `loadstring`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-table.unpack) `table.unpack(...)`
  * do not use the Lua 5.1 `unpack`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-debug.setmetatable) `debug.setmetatable(t, mt)` returns the `t` value
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-package.searchers) `package.searchers`
  * do not use the Lua 5.1 package.loaders
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-package.searcherpath) `package.searchpath(name, path [, sep [, rep]])`

