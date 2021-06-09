---
layout: post
title:      "Hooks - ReactJS"
date:       2021-06-09 16:11:18 +0000
permalink:  hooks_-_reactjs
---


According to Reactjs.org, hooks are a new addition in React 16.8. They let you use state and other React features without writing a class. I feel like this is one of the most important missing knowledge that Flatiron haven't updated in their curriculum.  

Ok, so why Hooks? 

As we know it, components and top-down data flow help us organize a large application into small, independent, reusable pieces. However, after doing the final project, I find myself quite often unable to break complex components down any further due to the fact that the logic is stateful and can’t be extracted to a function or another component. Well, you might say I can use render props or higher-order components but as a new learner to React, I still haven't quite mastered these methods. Then I found out about Hooks and these methods has became quite outdated. Why not just use the most updated and simplest way to solve the problems?

Let's talk about State Hook!

Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes (React.js).

```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

So instead of define state and then setState, all we do now is to useState(the hook) to do it all at once. Also you can only use hooks in functional components. Apparently, practice standard in React now is functional components. For more details, please visit [here](https://reactjs.org/docs/hooks-state.html). There are also [useEffect](https://reactjs.org/docs/hooks-effect.html) Hooks which are very useful  as componentDidMount, componentDidUpdate, and componentWillUnmount combined. Last but not least, you can [custom your own hooks](https://reactjs.org/docs/hooks-custom.html).


