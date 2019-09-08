# regex_training
* based on https://www.udemy.com/course/learn-and-understand-regular-expression-with-examples
* online regex tool: https://regex101.com/
  
# Intro
* regex is a search/find pattern
* Metacharacters are the building blocks of regular expressions(\d, \w, \W etc)
* character classes - matching one or several characters
* quantifiers - number of repetition

# Metacharacters
* ^ start of line
* $ end of line
* . period
* - range of elements in []
* [] character class to match anything inside brackets
* [^] negate character class to match string that do not follow the pattern
* \char escape metacharacter - is used to escape metacharacter in string
* '*' - 0 or more time
* +  one or more times
* {min, max} - min required, max allowed
* () groups patterns together
* * /pattern/ -> pattern goes inside double slashes
  
  # Exammples
  * [a-z] match from a to z lowercase
  * [A-Z] match from a to z uppercase
  * [0-9] from 0 to 9
  * [a-zA-Z] - upper and lower case letter
  * [a-zA-Z0-9] alphanumerical match
  * [a-z]* zero or many times a-z
  * [a-z]+ one or many times a-z
  * .* match zero or many times from any
  * (?=) positive look ahead
  * [a-z]{1,2} match one or two from a to z
  * [a-z]{1,}match one or unlimited from a to z
  * /pattern/i - case sensitive search

# literal characters
* Any character except [\^$.|?*+()
* example '/A/' matches word 'And' -> returns true
* example '/A/' doesn't match word 'and' -> return false

# Mode or Flag modifiers
* '/.../i' case non sensitive, e.g.  '/pattern/i' matches 'Pattern'
* `/.../g` global, The g modifier is used to perform a global match (find all matches rather than stopping after the first match).  e.g.  '`/a/g`' finds all  'aaaaaaa'
* while '/a/' finds only first a in 'aaaaaaaa'

# Dot metacharacter
* examples:  
  '/./' points to first symbol h in 'hello world'  
  '/./' equals to '/[...]/'

# Anchors
* '^' caret - matches the very beggining of the string. example, '/^h/' points to fist symbol in 'hello'
* '$' - matches end of the string. example '/o$/' points to last symbol in 'hello'

# Escaping metacharacters
* uses \ to escape a character. example '/^\^/' matches symbol ^ in string '^hello' or '/\$$/' matches to last symbol in 'hello$'

# Word boundary
* syntax \bword\b
* example '/\bhello\b/'matches only word hello(the second one) in 'hellohello hello world'