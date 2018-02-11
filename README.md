# uniform api

uniformapi provide an uniq API behavior for a short set of standard lua functions/modules.

# supported versions

* Lua 5.1
* Lua 5.2
* Lua 5.3
* LuaJIT 2.0 (equal to Lua 5.1)
* LuaJIT 2.1 (partialy equal to Lua 5.2)
* (I also tried Lua 5.0 for the fun)

# Goal

Fix a minimum functions used to build lua-box.


## what is fixed

* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-load) `load(chunk [, chunkname [, mode [, env]]])` (support of env as 4th argument)
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-table.unpack) `table.unpack(...)`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-debug.setmetatable) `debug.setmetatable(t, mt)` returns the `t` value
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-package.searchers) `package.searchers`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-package.searcherpath) `package.searchpath(name, path [, sep [, rep]])`


