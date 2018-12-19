_Notes from Robert Martin's "Clean Code"_
(some of these points aren’t super relevant, but generally they’re useful to know about)

### General principles of coding
- Name your variables very explicitly.
- You should make comments unnecessary by using very explicit variable names and clear control flow -- and don't leave around old lines of code or lines for future wishes.
- No duplication - expressiveness (both in naming and in each function doing one thing).
- Make as general/abstracted programs as possible - "early building of simple abstractions."

### Chapter 2: Meaningful Names
- indicate intent with names
- make meaningful distinctions with your nomenclature
- don't be afraid of long (but explicit) variable names
- avoid single letters except for counters - just avoid mental mapping generally
- make functions the verbs for what they do
- use one word per concept (eg select one of get, retrieve, fetch)

### Chapter 3: functions (these are less relevant for the coding we do)
- write very small functions (20-30 lines absolute MAX) with clear purpose and process
- functions should DO ONE THING
- a good heuristic for doing one thing is that a function cannot have another level of abstraction without the name of the contained function doing the same thing as the implementation of that original function call
- the point of a function is to decompose a process into its subsequent steps (level of abstraction)
- stay at one level of abstraction in a function!!
- open/closed principle - functions, modules, and classes (in object-oriented programming) should be open for extension but closed for modification - a class or function or module should allow for its effect to be changed without a change in it's source code
- don't be afraid of long and descriptive names
- more than three function arguments is excessive -- and the order should be intuitive
- group variables together by concept
- separate command and query -- don't do something AND ask something -- do one or the other
- writing coding is like writing prose -- there will be drafts and you won't get it right the first time

### Chapter 4: comments
- comments are a last-resort, necessary evil of code that cannot state everything explicitly in its variable names and function names and function construction
- a comment is a failure -- 9 of 10 times can make them unnecessary because of more explicit nomenclature and coding

### Chapter 5: spacing
- use space smartly

### Chapter 6: data objects and structures
- objects hide their data but have many functions attached to these objects; structures have no functions and have their data easily accessible (structure-centered programming can be considered procedural)
- adding functions is easier when using data structures but adding data is easier when using functions (in the former, adding a function would require that you add it to each object; in the latter, adding a data type would require adding XX instead of a single object)

### Chapter 17 :: smells
- don't put history in comments
- three inputs as a max to a function
- duplication is a missed chance for abstraction
- replace "magic numbers" with named constants
- encapsulate boundary conditions - if consistently adding or subtracting one to a variable then create a new variable
to store that case to make it clearer
- keep configurable data at a high level of abstraction
- choose names at appropriate level of abstraction
- names don't need to be encoded with type or scope information -- No Hungarian notation!
- make functions small!!