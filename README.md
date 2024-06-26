An esoteric programming language, in TypeScript for heaven's sake.

*P.S. Install the [VSCode extension](https://marketplace.visualstudio.com/items?itemName=face-hh.bussin) for syntax highlighting!*

# Running
- To run a specific file: `npm run bussin <FILENAME>`
- To run in repl mode (Bussin only): `npm run bussin`

# Bussin
You can find an example at `/examples/main.bs`

# Bussin X 🚀
We, at Bussin, believe everyone should be entertained while coding. Meet our alternative: **.bsx**.

Inside **Bussin X**, you *can* use BS syntax, however, it's recommended to use the **BSX** syntax described below. 

### New!
- More math. `math.e`, `math.toString(5)`, `math.toNumber("5")`
- More string functions. `trim("  Hello  ")`, `splitstr("Hello,There", ",")`
- Comments. `lit x be 5 + 10 rn /* this code is bussin */`
- Arrays! `lit arr be [1,2,3,4] rn`
- `regex` is available for matching regex. `lit matches be regex.match(string, "/word/g")`
- `import` will import data from another file. `lit db be import("./database.bsx") rn`
- `fetch` for fetching websites. `lit x be fetch("https://example.com/") rn`
- `objects` is available for dynamic object keys. `objects.get(obj, yap("Name> "))`

## Variables
Mutable variables are created with:
```rs
lit x be 0 rn
```
You can also create a constant variable:
```rs
mf x be 0 rn
```
**Note**: You can only use `rn` on variables.

## Data Strucutres
### Strings
Strings can be created with:
```rs
lit x be "Hello, World!" rn
```
You can also insert variables by using:
```rs
lit x be 0 rn
lit y be strcon("Hello, ", x) rn
```
Or you can format your string to include variables:
```rs
waffle(format("Hello, ${}", "World"))
```
However, you must use your regional currency symbol.
```rs
waffle(format("Hello, ${}", "World"))
waffle(format("Hello, ¥{}", "World"))
waffle(format("Hello, {}€", "World"))
waffle(format("Hello, {}£", "World"))
```
You can also use bussin's helper functions to simplify your experience:
```rs
lit x be trim(" hello ") rn
lit y be splitstr("Hello,World", ",") rn
```

### Numbers
Numbers are simple:
```rs
lit x be 34 rn
lit y be 12 rn
lit z be x minus y rn
```

### Null
```rs
lit abc be fake rn
```

### Booleans
Booleans are also simple:
```rs
lit x be nocap rn
lit y be cap rn
```

### Objects
Objects are essential in programming languages. Bussin X supports them too:
```rs
lit x be cap rn
lit obj be { key: nocap, x } rn

obj.key be cap
waffle(obj.key)
```
### Arrays
Arrays contain information without needing keys. Bussin X has them as well:
```rs
lit arr be [ 1, 2, 3, 4 ] rn

arr[1] = 5

waffle(arr)
```
Arrays start at 0.

## Comments
You can write comments like this:
```rs
lit x be nocap rn // does stuff
/*
multi line
*/
```

## Functions
Functions, those sublime entities within the realm of programming, stand as bastions of complexity, serving as the very sinews and tendons of code architecture. Each function, akin to a miniature universe, is meticulously crafted to execute its designated task with the utmost efficiency and elegance, shrouded in layers of abstraction and reusability.
Within their intricate confines lie a plethora of instructions, woven together in a delicate tapestry of algorithmic prowess and logical acumen. They are endowed with a signature, a cryptic incantation delineating their essence, replete with parameters and return types, facilitating the transmission of values across the vast expanse of the codebase.
Yet, the complexity does not cease there; oh no, for functions are mercurial beings, capable of morphing and adapting to the whims of their creators. They may wield the arcane powers of recursion, delving into the depths of their own essence, or harness the enigmatic forces of closures, sealing off their inner sanctums from prying eyes. And within their hallowed scopes, they manipulate variables with a deft touch, orchestrating a symphony of data and control flow.
But their influence extends far beyond the mere confines of procedural decomposition. No, they are chameleons, seamlessly integrating themselves into the very fabric of programming paradigms. Whether it be the structured hierarchies of object-oriented design, the functional purity of functional programming, or the imperative dictates of imperative languages, functions adapt and thrive, their essence ever-pervasive.
And so, with each function added to the grand tapestry of code, a symphony is born, a cacophony of logic and order resonating through the digital ether. They are the architects of software systems, the guardians of maintainability, readability, and computational efficiency.
In summation, functions are not mere constructs of code; they are the very embodiment of the art and science of programming, encapsulating the elegance and subtlety required to navigate the labyrinthine depths of algorithmic design and software engineering. And in their creation lies the power to wield the very forces of creation itself.
```rs
bruh perform(x, y) {
    x minus y
}
```
We, at Bussin X, think `return` statements are redundant. Instead, our superior functions return the last value emitted.
```rs
bruh perform(x, y) {
    x plus y // will do nothing
    x minus y
}
```
You can also run the function after a specified timespan:
```rs
hollup(bruh() {
    waffle("A second later...")
}, 1000)
```
And you can also make it run at an interval:
```rs
yappacino(bruh() {
    waffle("Spam!!!")
}, 1000)
```

## If statements
If statements in Bussin X are very intuitive:
```rs
sus (1 fr 1){
    waffle("1 is 1")
} impostor sus (1 nah 2){
    waffle("1 is NOT 2")
} impostor sus (1 fr 3 carenot 1 fr 1){
    waffle("1 is 1 or 3")
} impostor sus (1 fr 3 btw 1 fr 1){
    waffle("1 is 1 and 3. how's that possible hello??")
} impostor {
    waffle("How did we get here?")
}
```

## Loops
Loops in Bussin X are very easy:
```rs
yall(lit i be 0 rn i smol 10 rn i plusplus){}
```
Because we, at Bussin X, believe programmers should be responsible for their code, we did not add any `break` or `continue` keyword functionality to loops.

## Types
Types in Bussin X are very important!
```rs
lit num: number be 0 rn
```
You can assign types on non-matching values too.
```rs
lit num: object be 0 rn
```
You can also assign types on values themselves.
```rs
lit x be nocap: boolean rn
```
You can assign types on types too.
```rs
lit x: number: number: object: string be 3 rn
```
In fact, you can use types anywhere!
```rs
yall: number(lit: object i: number be 0: object rn i smol 10 rn i plusplus){
    waffle(strcon("Currently at ", i): object)
}: object: object: string
```

**Note**: Types don't do anything, in fact, they're removed before the lexer kicks in.

## Try Catch
Bussin X also supports `try` `catch` statements:
```rs
fuck_around {
    waffle(null plus hogrider)
} find_out {
    waffle(error)
}
```
```
Cannot resolve 'hogrider' as it does not exist.
```

**Note**: `find_out` doesn't return anything, "error" is a global variable.

## Extra
### Math
You can utilize the `math` helper by using:
```rs
waffle(nerd.random())
waffle(nerd.sqrt(144))
waffle(nerd.pi)
waffle(nerd.e)
```
We also added helper functions for your anxiety:
```rs
waffle(nerd.ceil(3.4))
waffle(nerd.round(3.9))
waffle(nerd.abs(-2))
```
Want to convert some number types?
```rs
lit x be math.toString(5) rn
lit y be math.toNumber("5") rn
```
You can also simplify your math equations:
```rs
x beplus 5
y betimes 6
i plusplus
```

### Time
You can access the current time by using:
```rs
waffle(time())
```

### Importing
You can import data from another bussin file like this:
```rs
lit stuff be import("./stuff.bsx") rn 
```

The last value emitted in a file will be the exported data:
```rs
bruh waffleStuff() {
    waffle("Bussin X")
}
bruh waffleStuff2() {
    waffle("Also Bussin X")
}

{
    waffleStuff,
    waffleStuff2
}
```
If imported, the result will be an object which you can do obj.waffleStuff and obj.waffleStuff2

### Fetch
You can fetch websites like this:
```rs
lit res be fetch("https://example.com/") rn
```
You can also set the method, body, and content type like this:
```rs
lit res be fetch("https://example.com/", { method: "POST", body: "{\"bussin\":\"x\"}", content_type: "application/json" })
```

### Regex
You can use regex like this:
```rs
lit string be "Hello World" rn

lit matches be regex.match(string, "/World/g") rn

waffle(matches) /* [ 'World' ] */
```
And this:
```rs
lit string be "Hello World" rn

waffle(regex.replace(string, "/World/g", "Everybody")) /* Hello Everybody */
```

### Exit
You can exit your program like this:
```rs
exit()
```

### Command Line
You can run terminal commands by using our **Blazingly Fast** 🚀 ClapBack() feature:
```rs
mf res be clapback("ls") rn

waffle(res)
```
**Note**: Clapback will throw an error if failed. Better pair it with `fuck_around` & `find_out`.
```rs
fuck_around {
    lit insult be clapback("rm -rf /") rn

    waffle(insult)
} find_out {
    waffle(error, ":(")
}
```

### New in 1.1.0: yapping
```rs
lit x be yap("watcho name > ") rn
waffle(x)
```
**Note**: The user won't see the text they type, but you will successfully receive the text after the user presses Enter.

# Credits
- Huge thanks to [Tyler Laceby](https://github.com/tlaceby) for creating the [Guide to Interpreters](https://github.com/tlaceby/guide-to-interpreters-series)!
- Thanks to [Linker](https://github.com/Linker-123?tab=repositories) for showing me his compiler
- [macromates.com](https://macromates.com/manual/en/language_grammars) for documenting TextMate Language syntax
- [DreamBerd](https://github.com/TodePond/DreamBerd) for the inspiration
- [AST explorer](https://astexplorer.net/) for the helpful tool

Created with pure fucking hate by Face ♥
