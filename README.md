# Color Troll Meme (TBC)
VueJS setup for fun medical meme display

HTML/CSS:
- Series of divs. `v-for` over `ctms`. Each is styled using `ctm`.
- `ctm` is a circular div.
- `h1` tags inside `ctm` are styled to appear in the middle.

Data:
- `ctms`: An array of objects. Number of objects cannot exceed number of elements in `wordTypes.condition`. Each object has the following properties.
  - `name`: A string.
  - `color`: An array of 3 integers.
  - `textColor`: An array of 3 integers.
- `wordTypes`
  - `xx`:
  - `xx`:
  - `xx`:
  - `xx`:
- `inUse`:

Methods:
- `getRandomNo(max)`:
  - `max` is a positive integer.
  - Return a random number from 0 to `max` - 1.
- `getOne(arr)`:
  - `arr` is an array.
  - Use `getRandomNo()` to obtain a random value from `arr`.
- `getCondition(condition, prefix)`:
  - `condition` is a string and `prefix` is a Boolean.
  - if `prefix` is `true`:
    - Use `getOne()` to obtain a random value from the array `condition_prefix`.
    - Return that value concatnated with `condition`.
  - if `prefix` is `false`:
    - Use `getOne()` to obtain a random value from the array `condition_suffix`.
    - Return `condition` concatenated with that value.
- `getColor(max)`:
  - `max` is a positive integer.
  - Declare `r` as a random integer between 0 and `max` - 1.
  - Declare `g` as a random integer between 0 and `max` - 1.
  - Declare `b` as a random integer between 0 and `max` - 1.
  - Return an array containing `r`, `g` and `b`.
- `fillInfo()`: 
  - For each element in ctms, fill in the `name`, `color` and `textColor` properties.
    - `color` is derived from using `getColor()` with an argument of 100.
    - `textColor` is derived by adding 150 to each value of `color`, and `opacity`.
      - `opacity` is 0.05 if it is the last element, and randomly derived otherwise. (between 0.7 and 0.9)
    - `name` is derived by:
      - if last element, use `getOne()` on `condition` array.
      - if not, `getOne()` on `area` array, then determine 0 or 1 from `getRandomNo()` and pass both results to `getCondition()`.
