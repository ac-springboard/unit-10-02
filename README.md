# unit-10-02-Exercise



## `var`, `let`, `const`, and Hoisting[1]

| Keyword | Redeclare? | Reassign? | Mutate? | Scope? | Used Before Declaration? | Declared with No Assignment? | Used before Assignment? |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **var** | yes | yes | yes | function or 'window' object | yes | yes | yes |
| **let**  | no  | yes  | yes  | code block  | no  | yes  | yes[2]  | yes  |
| **const**   | no  | no  | yes[3]  | code-block  | no  | no  | no  |

[1] There are some imprecisions in the definition of **hoisting** when we search on the internet. Moreover, the problem worsen when the concept is applied to the `let` and `const`. For exmple, [some says](https://medium.com/javascript-in-plain-english/how-hoisting-works-with-let-and-const-in-javascript-725616df7085) that the `let` declaration **is hoisted**, but without being initialized until they are evaluated (at runtime); on the other hand, [others says](https://www.w3schools.com/js/js_hoisting.asp) that the those declarations are not hoisted at all. So, there's more research to do.

[2] In [this](https://levelup.gitconnected.com/how-does-hoisting-work-in-javascript-es6-b0e06727e071) article the author says that this will throw an error; however, the [actual tests](https://medium.com/@almircampos/thank-your-for-the-explanation-jasmine-fc71e2b8f87f) worked.

[3] When using Array or Object type, but not for primitives. In the code `const a=[]; a[0]='azero'` will work; but `const a=[]; a=['azero']` (reassignment) won't.
