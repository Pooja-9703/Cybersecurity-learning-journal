# B. Data Encoding

## Representation and Encoding

**Representation** is the idea that data lives as bits and numbers in memory.

**Encoding** is the specific, agreed-upon mapping between numbers and meanings, such as which number corresponds to the character `A`.

---

## ASCII

- ASCII stands for **American Standard Code for Information Interchange**.
- It is an early character encoding from **1963** that uses numbers `0–127` to represent English letters, digits, punctuation, and some control characters.
- The original ASCII was limited to **7 bits**.
- ASCII acts as a small **bilingual dictionary** between text and numeric codes.
- Examples:
  - `A` → `65`
  - `a` → `97`

---

## European Languages

The **ISO/IEC 8859 series** created several standards, with each standard covering a set of languages.

### ISO-8859-1 (Latin-1)

- Covers Western European languages such as:
  - German
  - French
  - Spanish
  - Italian
  - Portuguese
  - Latin
  - Nordic languages

### ISO-8859-2 (Latin-2)

- Supports Central and Eastern European languages such as:
  - Polish
  - Czech
  - Hungarian
  - Croatian
  - Romanian
  - Slovak

---

## Unicode

- Unicode is a **universal character encoding standard**.
- It assigns a **unique number to every character across languages**.
- Unicode 17.0 is currently the latest version of the Unicode standard.
- It defines close to **157,000 characters**, almost 4,000 of which are emoji sequences.

---

## UTF-8 (Unicode Transformation Format)

- UTF-8 is very common on the modern web.
- It encodes Unicode code points using **1 to 4 bytes dynamically**.
- It decides the number of bytes based on the character's complexity.
- ASCII characters (`U+0000` to `U+007F`) use exactly **1 byte**, identical to the original ASCII, ensuring seamless backward compatibility.
- Non-ASCII characters generally use **2 or 3 bytes**, while complex characters such as some emojis can require **4 bytes**.
- This flexibility allows UTF-8 to cover the entire Unicode standard without wasting bytes.

---

## UTF-16

- UTF-16 uses either **2 or 4 bytes per character**.
- Common characters, such as most Latin, Cyrillic, or Chinese characters, fit in **2 bytes**.
- Some rarer characters, such as certain emoji or ancient scripts, require a pair of 16-bit units, totaling **4 bytes**.

---

## UTF-32

- UTF-32 is the simplest but also the most wasteful encoding.
- Every Unicode code point uses **exactly 4 bytes**.
