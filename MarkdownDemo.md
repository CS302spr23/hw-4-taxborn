# This is a H1 with a [link to my profile README](https://github.com/taxborn/taxborn)
## This is a H2 with a [link to the repository of what I don't understand](https://github.com/taxborn/ThisIDontUnderstand)
### This is a H3
#### :space_invader: This is a H4, with emojis!
##### This is a H5, need I go on ..?
###### This is a H6, I must
I can **bold** text, _italicise_ it, and ~~strikethrough~~.

***

Here is a table and a list, taken from the [mAuth Research team](https://github.com/taxborn/mauth-research-project).

| ID  | Timestamp          | X    | Y   | Button | Duration             |
|-----|--------------------|------|-----|--------|----------------------|
| 2   | 1676925152.344601  | 901  | 488 | -1     | -1                   |
| 2   | 1676925152.3605819 | 915  | 482 | -1     | -1                   |
| 2   | 1676925157.8644285 | 975  | 301 | -1     | -1                   |
| 2   | 1676925158.0728395 | 975  | 301 | 1      | -1                   |
| 2   | 1676925158.1127932 | 975  | 301 | 1      | 0.03995370864868164  |
| 2   | 1676925152.368573  | 924  | 480 | -1     | -1                   |
| ... | ...                | ...  | ... | ...    | ...                  |

- **ID:** Subject ID
- **Timestamp:** UNIX Timestamp of the event
- **X, Y**: The X and Y positions of the event, where it happened on the screen
- **Button**: The button that was pressed, for this, we used the following mapping:
  1. Left click
  2. Right Click
  3. Middle Click
  4. Scrolling Down
  5. Scrolling Up
  6. Button X1 *(rarely used)*
  7. Button X2 *(rarely used)*
- **Duration**: The duration of the event, only used to track how long a button press event was

***

> You can also do blockquotes!
> Premature optimization is the root of all evil
> > Donald Knuth

with some code, taken from my compiler

```rust
    pub fn accumulate_while(&mut self, predicate: &dyn Fn(&char) -> bool) -> &str {
        let mut size = 0;

        while let Some(&chr) = self.lookahead.peek() {
            // Check if the next character does not pass the predicate.
            if !predicate(&chr) {
                break;
            }

            // increment the size by the UTF-8 length to ensure we don't index
            // into the 'middle' of a character.
            size += chr.len_utf8();

            // advance the iterator
            self.lookahead.next();
        }

        // increment the position of the lexer
        self.pos += size;
        // get the relevant slice
        &self.input[(*self.pos - size)..*self.pos]
    }
```


