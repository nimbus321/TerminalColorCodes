# Terminal Color Codes (NodeJS)
An object to smoothly use color codes on the Terminal, just use the color codes like this:
```javascript
console.log( C["&a"] + C["&l"] + "Lorem ipsum dolor sit amet" + C["&r"] )
// Will appear green and bold on the Terminal
```
Output: ![Example][example]
- `C["&a"]` means Green
- `C["&l"]` means Bold
- `C["&r"]` is to reset all previous style

More complicated example:
```javascript
console.log( C["&c"] + C["&l"] + "Danger! " + C["&r"] + C["&e"] + C["&n"] + "Don't do that!" + C["&r"] + " " +C["&bg"] + C["&b"] + " Be careful "+ C["&r"] )
```
![Example][example complicated]

# How To Use


The `C` object in the JavaScript code provides an easy way to print text with different colors in the terminal without having to remember the corresponding ANSI codes. The object contains several properties, each of which is associated with a specific color or style code that can be used to format text in the terminal. 

There are 2 types of codes; color and format. You can combine color with formats, for example, Green with Bold (example above).
To use them, just put the code like this `C["CODE"]`
> The "Codes" are just properties of the object C, on with there is the respective ANSI code that the terminal will interpret.

**Here are the Color Codes:** (For each color, there is a brighter and darker color)

![colors][colors]
> Allways remember to reset any style at the end of the line by using the reset code, `C["&r"]` 

# CheatSheet



## Colors
| Tag, o Key | JavaScript  | Result 
| :--------- | :-------------  | :---: 
| `&0`        | C["&0"]   |  ![&0][lorem &0] 
| `&1`        | C["&1"]   |  ![&1][lorem &1] 
| `&2`        | C["&2"]   |  ![&2][lorem &2] 
| `&3`        | C["&3"]   |  ![&3][lorem &3] 
| `&4`        | C["&4"]   |  ![&4][lorem &4] 
| `&5`        | C["&5"]   |  ![&5][lorem &5] 
| `&6`        | C["&6"]   |  ![&6][lorem &6] 
| `&7`        | C["&7"]   |  ![&7][lorem &7] 
| `&8`        | C["&8"]   |  ![&8][lorem &8] 
| `&9`        | C["&9"]   |  ![&9][lorem &9] 
| `&a`        | C["&a"]   |  ![&a][lorem &a] 
| `&b`        | C["&b"]   |  ![&b][lorem &b] 
| `&c`        | C["&c"]   |  ![&c][lorem &c] 
| `&d`        | C["&d"]   |  ![&d][lorem &d] 
| `&e`        | C["&e"]   |  ![&e][lorem &e] 
| `&f`        | C["&f"]   |  ![&f][lorem &f] 

## Formats

| Tag, o Key                      | JavaScript  | Result                                  |  Notes      |
| :------------                   | :-------------  | :---:                                   | :---: 
| `&r` or `reset`                 | C["&r"]   |  ![reset][lorem reset]                        | Resets all previews formats and color
| `&n`, `&u`, `&sub` or `underscore`            | C["&n"]   |  ![underscore][lorem underscore]              | 
| `&o`, `&i` or `italic`          | C["&o"]   |  ![italic][lorem italic]                      | 
| `&m`, `&s`, `&str` or `strikethrough` | C["&m"]   |  ![strikethrough][lorem strikethrough]        | 
| `&l` or `bold`                  | C["&l"]   |  ![bold][lorem bold]                          | 
| `&h` or `hidden`                | C["&h"]   |  ![&h][lorem hidden]                          | The text can still be copied, and is rendered but invisible.
| `&bg` or `background`           | C["&bg"]  |  ![background][lorem background]              | The color of the background can change if you specify it after the `&bg` code, examples below
| **Examples of background with color:**  |
| `&bg` with `&a`                 | C["&bg"] + C["&a"]  |  ![background2][lorem background2]  | 
| `&bg` with `&e`                 | C["&bg"] + C["&e"]  |  ![background3][lorem background3]  | 
| `&bg` with `&c`                 | C["&bg"] + C["&c"]  |  ![background4][lorem background4]  | 


# FAQ
## Okey, but WHY?
Because its great to use color on the terminal, if it's not for you just don't use it. :)
## Where does it work?

The main place is the terminal, and that's why I made this. But it also works on the javascript dev's console! I don't recommend it tho, there are better ways to manipulate the style and color there, here are some links: [Link 1](https://stackoverflow.com/questions/7505623/colors-in-javascript-console "CSS on JS dev's console"), [Link 2](https://stackoverflow.com/questions/24828107/javascript-adding-style-to-the-text-of-console-log "CSS on JS dev's console").






## Why that strange naming of the color codes?
Because I pretty much took the colors from Minecraft's color codes and made them into ANSI codes. Also, on there, the way of using them is to put a `&` before the code, so that's why I made it this way. I already knew the color and their code so it was really easy for me to make it this way.

[colors]: https://i.imgur.com/8c0cIUx.png "Every color and his code"

[lorem &0]: https://i.imgur.com/S73Atnw.png "&0"
[lorem &1]: https://i.imgur.com/dX9QXd5.png "&1"
[lorem &2]: https://i.imgur.com/Ocheojw.png "&2"
[lorem &3]: https://i.imgur.com/jdIZiun.png "&3"
[lorem &4]: https://i.imgur.com/1bzqzNU.png "&4"
[lorem &5]: https://i.imgur.com/exsE5gH.png "&5"
[lorem &6]: https://i.imgur.com/Sb3z3ZL.png "&6"
[lorem &7]: https://i.imgur.com/FV3qqCF.png "&7"
[lorem &8]: https://i.imgur.com/0FibUC3.png "&8"
[lorem &9]: https://i.imgur.com/HrsXX1a.png "&9"

[lorem &a]: https://i.imgur.com/hc1eth0.png "&a"
[lorem &b]: https://i.imgur.com/2v4YaLc.png "&b"
[lorem &c]: https://i.imgur.com/w8Yu7jN.png "&c"
[lorem &d]: https://i.imgur.com/mkLP21D.png "&d"
[lorem &e]: https://i.imgur.com/xr4keeL.png "&e"
[lorem &f]: https://i.imgur.com/hbv9X2q.png "&f"

[lorem underscore]: https://i.imgur.com/AS4Tu5S.png "Underscore"
[lorem italic]: https://i.imgur.com/AhTlAnq.png "Italic"
[lorem strikethrough]: https://i.imgur.com/26Xkhr3.png "Strikethrough"
[lorem bold]: https://i.imgur.com/bIqxU7R.png "Bold"
[lorem reset]: https://i.imgur.com/oAikaz3.png "Reset"
[lorem hidden]: https://i.imgur.com/rZv6DjU.png "Hidden"
[lorem background]: https://i.imgur.com/wyOzqy6.png "Background"
[lorem background2]: https://i.imgur.com/Hp2HBzO.png "Background2"
[lorem background3]: https://i.imgur.com/rmqLNu9.png "Background3"
[lorem background4]: https://i.imgur.com/xRmpToc.png "Background4"
[example]: https://i.imgur.com/8oyKdnj.png "Example"
[example complicated]: https://i.imgur.com/m73Qnij.png "Example"
