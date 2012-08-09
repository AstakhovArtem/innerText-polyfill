# HTMLElement#innerText polyfill

I am well aware that `innerText` is nonstandard, and should generally be avoided.
However, I've ran into a few situations where `textContent` is utterly useless, and `innerHTML` opens up the usual issues come around with embedding user-supplied HTML.

So, I decided to make a polyfill for `innerText`, even though it probably shouldn't be used if there's an alternative available.

IE has had innerText for a long time, so we basically only need a polyfill for Firefox. This means we can take advantage of `Selection`s.

The code's pretty self explanatory, and commented, so read that if you want to figure out how it works.
