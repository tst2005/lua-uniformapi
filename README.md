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

* `load()` : like Lua 5.2+ (support of env as 4th argument)
* `table.unpack()` : like Lua 5.2+
* `debug.setmetatable(t,mt)` : like Lua 5.2+ (return the `t` value)
* `package.searchers` and `package.searchpath` : like Lua 5.2+


