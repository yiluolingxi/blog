`{{}}`
mustache syntax ( double curly brace syntax )

It allows us to write **JavaScript expressions

it allows us to **run valid JavaScript** within our HTML

we could be doing things like
concatenating stings  
running conditional logic with a ternary operator 
running methods on our data and so on

```html
<h1>{{ pruduct }}<h1>

<p>{{ firstName + '' + lastName }}</p>

<span>{{ clicked ? true : false }}</span>
{{ ok ? 'YES' : 'NO' }}

<div>{{ message.method() }}</div>
```
or
```js
{{ number + 1 }}

{{ message.split('').reverse().join('') }}
```


So back in the diagram if we were to change socks to boots
our expression would receive that new value and our Dom would update

But how exactly is that happening?

Well, the answer is that vue is reactive 
underneath the hood vue has an entire reactivity system that handles updating
So when a data value changes 
anywhere relying on that data value is going to automatically update for us
We don't have to do anything to make that happen


If we were using product in multiple places within our template
and product were to update
every place that was using that value is going to update
Again, this is all thanks to vue's **reactivity system**

![[Pasted image 20230425151817.png]]


By popping open the dev tools 
we can see reactivity happening live in the browser

![[Pasted image 20230425152555.png]]

I can update it to shoes and when I hit enter
our Dom is going to update automatically

![[Pasted image 20230425154759.png]]

I'll do the same for sandals hit enter
and there it goes updating reactively

![[Pasted image 20230425154948.png]]



Now you'll want to add a product description to the data object 
then display that description using an expression within a P tag

![[Pasted image 20230425155336.png]]

You'll find a link to the challenges solution code below this video 
as a reminder If you're coding along with our repo. You can check out the ending code as well. 
