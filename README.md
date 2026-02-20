# array

Array search, transform, and aggregation utilities for Otter.

## API Reference

### `array.contains(data:arr<int>, value:int) -> bool`

Check if an array contains a specific value.

- **Parameters:**
  - `data` — Array to search
  - `value` — Value to look for
- **Returns:** `true` if found, `false` otherwise

```otter
rock nums:arr<int> = {1, 2, 3, 4, 5};
rock has3:bool = array.contains(nums, 3);  // true
rock has9:bool = array.contains(nums, 9);  // false
```

---

### `array.find(data:arr<int>, value:int) -> int`

Find the index of the first occurrence of a value.

- **Parameters:**
  - `data` — Array to search
  - `value` — Value to find
- **Returns:** Zero-based index, or `-1` if not found

```otter
rock idx:int = array.find({10, 20, 30}, 20);  // 1
rock missing:int = array.find({10, 20, 30}, 99);  // -1
```

---

### `array.reverse(data:arr<int>) -> void`

Reverse the elements of an array in place.

- **Parameters:**
  - `data` — Array to reverse (must be `flow`)

```otter
flow nums:arr<int> = {1, 2, 3};
array.reverse(nums);
// nums is now {3, 2, 1}
```

---

### `array.sum(data:arr<int>) -> int`

Sum all elements of an integer array.

- **Parameters:**
  - `data` — Array of integers
- **Returns:** Sum of all elements

```otter
rock total:int = array.sum({10, 20, 30});  // 60
```

---

### `array.min(data:arr<int>) -> int`

Find the minimum value in an array.

- **Parameters:**
  - `data` — Non-empty array of integers
- **Returns:** The smallest element

```otter
rock smallest:int = array.min({5, 2, 8, 1, 9});  // 1
```

---

### `array.max(data:arr<int>) -> int`

Find the maximum value in an array.

- **Parameters:**
  - `data` — Non-empty array of integers
- **Returns:** The largest element

```otter
rock largest:int = array.max({5, 2, 8, 1, 9});  // 9
```

---

### `array.length(data:arr<int>) -> int`

Get the number of elements in an array.

- **Parameters:**
  - `data` — Array
- **Returns:** Element count

```otter
rock len:int = array.length({1, 2, 3});  // 3
```

## Dependencies

- `memory` — for internal operations

## Install

```
otter pkg add array
otter pkg pull
```
