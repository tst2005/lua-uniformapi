# uniform api

# Goal

A way to get a stable/uniform behavior for some critical lua functions.
Uniformapi needs some minimal requirement.
Uniformapi is made to build more advanced stuff over the top of him ([lua-box](https://github.com/tst2005/lua-box) in my case).

# How to use

## Quickly

```lua
_G = require "uniformapi"(_G)
```

## Run code

```lua

local G = require "uniformapi"(_G)
local x = G.load([[
assert(unpack)
print(table.unpack({1,2,3}))
print("deprecated:", _DEPRECATED)
]], "", "t", G)()

```

## Uniform api content

* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-load) `load(chunk [, chunkname [, mode [, env]]])` (support of env as 4th argument)
  * do not use the Lua 5.1 `setfenv`, `getfenv`, `loadstring`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-table.unpack) `table.unpack(...)`
  * do not use the Lua 5.1 `unpack`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-debug.setmetatable) `debug.setmetatable(t, mt)` returns the `t` value
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-package.searchers) `package.searchers`
  * do not use the Lua 5.1 `package.loaders`
* Like Lua [5.2](https://tst2005.github.io/manual/lua/5.2/manual.html#pdf-package.searcherpath) `package.searchpath(name, path [, sep [, rep]])`

# Supported versions

* Lua 5.1
* Lua 5.2
* Lua 5.3
* LuaJIT 2.0 (equal to Lua 5.1)
* LuaJIT 2.1 (partialy equal to Lua 5.2)

# Not supported versions

* Lua 5.0 seems to have too many things to be fixed to be supported but I have tried for the fun!

If you want even try

```lua
local G=_G
if string.sub(_VERSION,1,7)=="Lua 5.0" then
        G=require"uniformapi/lua50"(G)
end
G = require "uniformapi"(G)
```

