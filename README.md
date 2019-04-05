# VS Code Snippets - bleech
## About
Snippet that quickly inserts `bleech` SCSS media query with or without the appropriate breakpoint variables.
## SCSS:
### Installation
* **OSX:** copy the content of the `scss.json` file into respective JSON file located at your VS Code installation folder `Code/User/snippets/scss.json`

### Usage
Snippet can be called in any SCSS file type by typing `bl{breakpoint_abbreviation}`.
Full list of abreviations is as follows:

| Abb | Full name | Breakpoint [px] |
| --- | --- | --- |
| blm | $breakpoint-mobile-horizontal | 480 |
| blt | $breakpoint-tablet | 768 |
| blt1 | $breakpoint-tablet-horizontal | 1024 |
| bld | $breakpoint-desktop | 1280 |
| bld1 | $breakpoint-wide | 1440 |
| blx | ~ no breakpoint ~ | ~ xx ~ |

#### Output
```
@media (min-width: {breakpoint_variable}) {
        ...
    }
}
```

### Logic
Formula:
`{bl}+{m;t;d}+{n}`

* `bl` stands for `bleech`
* consequent letter represents a viewport width (`m`-mobile; `t`-tablet, `d`-desktop)
* the number `n=1,2,3...` represents a viewport modifier
