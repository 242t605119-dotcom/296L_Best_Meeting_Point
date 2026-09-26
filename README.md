# LeetCode 296 - Best Meeting Point

## Problem Statement

You are given a grid where:

* `1` represents a person.
* `0` represents an empty location.

Choose a meeting point so that the total Manhattan distance traveled by all people is minimized.

Return the minimum total distance.

## Example

### Input

```text id="x6c2qk"
grid = [
    [1,0,0,0,1],
    [0,0,0,0,0],
    [0,0,1,0,0]
]
```

### Output

```text id="w7n1pk"
6
```

## Approach

The minimum total distance to a group of points is obtained at the **median**.

We separate the problem into two dimensions:

* Find the median row.
* Find the median column.

Then calculate the total Manhattan distance from every person to that meeting point.

## Algorithm

```text id="r7j3ca"
Store the row position of every person.
Store the column position of every person.

Find the median row.
Find the median column.

Calculate:
sum of |person_row - median_row|
+
sum of |person_column - median_column|

Return the total distance.
```

## Time Complexity

`O(m × n + k log k)`

where `k` is the number of people.

## Space Complexity

`O(k)`

## Author

T. Nandhini
