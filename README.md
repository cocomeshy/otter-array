# otter-array

Array helpers: search, transform, and aggregate arr<int>.

Part of the Otter standard library. Otter is a compiled systems language with no garbage collector and no libc dependency (pthread for threading is the one exception); everything else goes through raw syscalls and DLL imports.

## Install

In your `otter.nest`:

```nest
deps {
  use "array" want "1.0.0"
}
```

Then:

```sh
otter pkg pull
```

## API reference

### `array.contains(data:arr<int>, value:int) -> bool`

Checks whether an integer array contains the given value. Performs a linear scan from index 0 to data.len - 1.

Parameters:

- `data`: The array to search
- `value`: The value to find

Returns: true if the value exists in the array, false otherwise

### `array.find(data:arr<int>, value:int) -> int`

Returns the index of the first occurrence of a value, or -1 if absent.

Parameters:

- `data`: The array to search
- `value`: The value to locate

Returns: Zero-based index, or -1

### `array.reverse(data:arr<int>)`

Reverses an integer array in-place using a two-pointer swap.

Parameters:

- `data`: The array to reverse

### `array.sum(data:arr<int>) -> int`

Returns the sum of all elements in an integer array. Returns 0 for empty arrays.

Parameters:

- `data`: The array to sum

Returns: The total sum

### `array.min(data:arr<int>) -> int`

Returns the smallest value in an integer array. The array must contain at least one element.

Parameters:

- `data`: The array to search

Returns: The minimum value

### `array.max(data:arr<int>) -> int`

Returns the largest value in an integer array. The array must contain at least one element.

Parameters:

- `data`: The array to search

Returns: The maximum value

### `array.length(data:arr<int>) -> int`

Returns the number of elements in an integer array.

Parameters:

- `data`: The array

Returns: Element count

---

## Dependencies

memory (for internal allocation).

## License

MIT.
