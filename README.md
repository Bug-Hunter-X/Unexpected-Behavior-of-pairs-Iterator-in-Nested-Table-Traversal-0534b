# Lua pairs Iterator Unexpected Behavior

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables.  Modifying a table during iteration using `pairs` can lead to unexpected behavior such as skipped or duplicated elements. This example highlights this issue with a recursive function traversing a nested table structure.  The solution showcases a safer way to iterate through tables to avoid this problem.

## Bug Description

The `pairs` iterator in Lua doesn't guarantee a specific order of iteration.  Furthermore, modifying the table during iteration can disrupt the internal state of the iterator, resulting in elements being skipped or visited multiple times. This is particularly problematic in recursive scenarios, as demonstrated in the `bug.lua` file.