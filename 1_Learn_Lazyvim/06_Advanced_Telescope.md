# Grep And (Filtering by Path)

## Example

- use the -- separator to pass flags to the search
  - Grep And (Filtering by Path)
    - `Space / name -- -g *.json`

## Telescope Flags

- `-w` Only find one word --> `cat -- -w` finds cat, not category
- Case Sensitive
  - `-s` Don't Ignore case Sensitive
  - `-i` Ignore Case
- Files
  - `-g` Glob (File Filter) `word -- -g filename`
  - `-u` Searching in Hidden Files
  - `-t` File Type `word -- -t js` or `word -- -t lua`
  - `-T` Exclude Type `word -- -T css` Search everywhere except CSS

## Learn RegExp (ripgrep)

- Line
  - `^` Start of line --> (^function)
  - `$` End of line --> (;$)
  - `^$` Empty line

- Types of characters
  - `.` Any single character {f.te --> (Finds "fate", "fete", "fite")}
  - `\d` Any digit (0-9) {\d\d\d (Finds any 3-digit numbers)}
  - `\w` Any word character {Letters, numbers, and underscores}
  - `\s` Whitespace {Spaces, tabs, or newlines}
  - `[A-Z]` Any Uppercase letter {`[A-Z][a-z]+` (Finds TitleCase words)}

- Quantifiers (The "How many")
  - `*` 0 or more {`ba*` (Finds "b", "ba", "baaa")}
  - `+` 1 or more {`ba+` (Finds "ba", "baaa" but NOT "b")}
  - `?` 0 or 1 {`https?` (Finds "http" and "https")}
  - `{n}` Exactly n times {`\d{4}` (Finds 4-digit years like 2024)}

- Advanced Combinations
  - `(|)` The "OR" logic: `(blue|red|green)` Finds any of those three colors.
  - `\` Escaping: Search for (.com) or ([]) --> `\.com` or `\[ \]`
