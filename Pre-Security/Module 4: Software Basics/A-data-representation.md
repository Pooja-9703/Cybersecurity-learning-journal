# A. Data Representation

## Hexadecimal

- Each **hexadecimal digit** represents **4 binary bits**.
- **1 byte = 8 bits = 2 hexadecimal digits**.
- `2^8 = 256`
- Therefore, a byte can represent values from **0 to 255**.

## RGB Colors

RGB colors use **3 bytes**:

| Color Component | Size |
|---|---:|
| Red | 1 byte |
| Green | 1 byte |
| Blue | 1 byte |

Therefore:

- **24 bits = 6 hexadecimal digits = 3 bytes**
- Each RGB component can have a value from **0–255**.

## Hexadecimal to Binary Representation

| Hexadecimal Digit | Binary Representation |
|---|---|
| `0` | `0000` |
| `1` | `0001` |
| `2` | `0010` |
| `3` | `0011` |
| `4` | `0100` |
| `5` | `0101` |
| `6` | `0110` |
| `7` | `0111` |
| `8` | `1000` |
| `9` | `1001` |
| `A` | `1010` |
| `B` | `1011` |
| `C` | `1100` |
| `D` | `1101` |
| `E` | `1110` |
| `F` | `1111` |

## Example: Hexadecimal Color to Binary

**Question:** What is the binary representation of the color `#EB0037`?

Separate the RGB components:

- **R = `EB`**
  - `E` → `1110`
  - `B` → `1011`
  - Therefore `EB` → `11101011`

- **G = `00`**
  - `0` → `0000`
  - `0` → `0000`
  - Therefore `00` → `00000000`

- **B = `37`**
  - `3` → `0011`
  - `7` → `0111`
  - Therefore `37` → `00110111`

**Answer:**

`#EB0037` → `11101011 00000000 00110111`

## Example: Hexadecimal Color to Decimal

**Question:** What is the decimal representation of the color `#D4D8DF`?

Separate the RGB components:

- **R = `D4`**
- **G = `D8`**
- **B = `DF`**

### Red: `D4`

`D` = `13`

`(13 × 16) + (4 × 1)`

`= 208 + 4`

`= 212`

### Green: `D8`

`D` = `13`

`(13 × 16) + (8 × 1)`

`= 208 + 8`

`= 216`

### Blue: `DF`

`D` = `13`

`F` = `15`

`(13 × 16) + (15 × 1)`

`= 208 + 15`

`= 223`

**Answer:**

`#D4D8DF` → **RGB(212, 216, 223)**

---

## Octal Numbers (Base-8 System)

The **octal number system** is a base-8 number system.

It uses the digits:

`0 1 2 3 4 5 6 7`

### Decimal, Octal and Binary Representation

| Decimal Number | Octal Digit | Binary Representation |
|---:|---:|---:|
| `0` | `0` | `000` |
| `1` | `1` | `001` |
| `2` | `2` | `010` |
| `3` | `3` | `011` |
| `4` | `4` | `100` |
| `5` | `5` | `101` |
| `6` | `6` | `110` |
| `7` | `7` | `111` |

## Hexadecimal and Binary

Each hexadecimal digit represents **4 bits**.

For example:

`F` → `1111`

Therefore:

`FF` → `1111 1111`

So the hexadecimal value `FF` in binary is:

`11111111`

## Example: Hexadecimal to Decimal

**Question:** What is the decimal representation of hexadecimal `AB`?

`A` = `10`

`B` = `11`

Using place values:

`(10 × 16) + (11 × 1)`

`= 160 + 11`

`= 171`

**Answer:**

`AB` → **171**

### Number System Bases

- **Decimal system** → Base `10`
- **Binary system** → Base `2`
- **Octal system** → Base `8`
- **Hexadecimal system** → Base `16`
