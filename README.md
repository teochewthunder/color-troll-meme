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
- `getOne(arr)`:
- `getCondition()`:
- `getColor(max)`:
- `fillInfo()`: 
