---
layout: post
title: "Markup: Syntax Highlighting"
excerpt: "Post displaying the various ways of highlighting code in Markdown."
tags: 
  - code
  - syntax highlighting
---

Syntax highlighting is a feature that displays source code, in different colors and fonts according to the category of terms. This feature facilitates writing in a structured language such as a programming language or a markup language as both structures and syntax errors are visually distinct. Highlighting does not affect the meaning of the text itself; it is intended only for human readers.[^1]

[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>

### GFM Code Blocks

GitHub Flavored Markdown [fenced code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) are supported. To modify styling and highlight colors edit `/_sass/syntax.scss`.

#### CSS
```css
.dashboard-buttons {
    margin-top: 50px;
}

.dashboard-buttons > .btn {
    position: relative;
    border-left-width: 7px;
    border-radius: 10px;
    margin-bottom: 20px;
    border-right-width: 7px;
    font-size: 1.5em;
    font-weight: bold;
}

.dashboard-buttons > .btn:hover {
    background-color: #F7F7F7;
}
```

#### HTML
```html
{% raw %}
    <nav class="pagination" role="navigation">
        {% if page.previous %}
            <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
        {% endif %}
        {% if page.next %}
            <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
        {% endif %}
    </nav><!-- /.pagination -->
{% endraw %}
```

#### Ruby
```ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
        @site = site
        @base = base
        @dir = dir
        @name = 'index.html'
        self.process(@name)
        self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
        self.data['tag'] = tag
        tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
        tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
        self.data['title'] = "#{tag_title_prefix}#{tag}"
        self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
```

#### Javascript
```js
/**
 * An array forEach with a delay between steps.
 *
 * @param {Function} callback Function to execute for each element. It receives three arguments, the element value, the element index and the array being traversed, respectivily.
 * @param {Number} timeout Number of milliseconds that the function call should be delayed by.
 * @param {Object} thisArg Object to use as this when executing callback.
 * @this {Array}
 * @return {undefined}
 */
Array.prototype.delayedForEach = function(callback, timeout, thisArg){
    var i = 0,
        l = this.length,
        self = this,
        caller = function(){
            callback.call(thisArg || self, self[i], i, self);
            (++i < l) && setTimeout(caller, timeout);
        };
    caller();
};

/*
=== Usage ===
var numbers = [100, 2,"abc", 4, true];
numbers.delayedForEach(function(elem, index, array){
    console.log("this = " + this);
    console.log("elem = " + elem);
    console.log("index = " + index);
    console.log("array = " + array);
}, 1000);
var myScope = {foo: "bar"};
numbers.delayedForEach(function(){ console.log(this); }, 1000, myScope);
*/
```

#### Python
```python
BOARD_SIZE = 8

class BailOut(Exception):
    pass

def validate(queens):
    left = right = col = queens[-1]
    for r in reversed(queens[:-1]):
        left, right = left-1, right+1
        if r in (left, col, right):
            raise BailOut

def add_queen(queens):
    for i in range(BOARD_SIZE):
        test_queens = queens + [i]
        try:
            validate(test_queens)
            if len(test_queens) == BOARD_SIZE:
                return test_queens
            else:
                return add_queen(test_queens)
        except BailOut:
            pass
    raise BailOut

queens = add_queen([])
print queens
print "\n".join(". "*q + "Q " + ". "*(BOARD_SIZE-q-1) for q in queens)
```



### Code Blocks in Lists

Indentation matters. Be sure the indent of the code block aligns with the first non-space character after the list item marker (e.g., `1.`). Usually this will mean indenting 3 spaces instead of 4.

1. Do step 1.
2. Now do this:
   
    ```ruby
    def print_hi(name)
        puts "Hi, #{name}"
    end
    print_hi('Tom')
    #=> prints 'Hi, Tom' to STDOUT.
    ```
        
3. Now you can do this.

### GitHub Gist Embed

An example of a Gist embed below.

{% gist 6011834 %}
