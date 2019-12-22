# Framework Comparisons

This is a repo that has source code for the same app written in 
html/css/js and then using 3 different frameworks: React, Vue, and Svelte. 
Using the app should result in completely identical user interfaces 
as well as user experiences. 

The main point of comparison here should be how the code is structured and 
what it would be like to code in these different languages. 

*Note*: I am mainly a React developer and I quickly skimmed the docs for the 
other frameworks so if there is an architectural style that isn't adhered to 
in any of these projects, please pull an issue or send a pr!

# About

The app is a simple todo app. Because there is only one page and only basic 
functionality, understand that it will likely not highlight the differences 
when building apps to scale.

### Vanilla
The vanilla folder is the app written in pure html/css/js. 

### React
The react folder is the app written in ReactJS. This repo relies on React 16.8 
and does not use the former class-based/HOC and instead uses React Hooks. It 
was created using CRA and so is compiled using Webpack.

### Vue
The Vue folder is the app written in VueJS. This repo does not explicitly 
create any Vue components (except in main.js) and uses the Single File 
Component structure. 

### Svelte
The Svelte folder is the app written in Svelte. This repo uses Svelte 3. 
Furthermore, it is also compiled using Rollup.

# Things I didn't look at

## Performance
Unless you're developing extremely large apps, the performance difference 
will not matter to you - which, if that's the case, this is probably the 
wrong repo for you to look at.

With that in mind, the only criteria I wanted to test against was developer 
experience.

## State/Memory Management
Managing state is obviously important but was not something I tested here. 
The solutions that exist for these frameworks: Vuex, Redux, etc. should be
tested separately from these. Similarly, this app is not nearly complex 
enough to leverage the benefits of these heavy machinery.

# Developer Experience

### Svelte
The first framework I want to bring up is actually svelte. Svelte is really 
interesting because it brings the component based architecture to vanilla web 
development. 

I wish I had learned Svelte sooner because I would have preferred to teach it 
over React as a first framework for students. It introduces a completely 
different software architecture without influencing much of the syntax that 
exists in vanilla web development. The entire app is structured by components 
that are written like mini html documents.

### Vue
Vue looks like a breed between React and Svelte. It follows many of the same 
programming paradigms that exist in React such as props, exports, class-like 
syntax while maintaining the same templating structure seen in Svelte. It just 
feels like Vue tries to take the best in both worlds by taking the simplicity 
in Svelte and adding the functionality of React on top of it which results in
a strangely complex codebase.

To me, it looks like Vue has been long lauded for being a much simpler, beginner-
friendly version of the other main framework giants - Angular and React - but 
I just don't see a reason why you wouldn't just pick Svelte.

### React
I think I'm much too comfortable with React to find benefits switching to these 
other frameworks. The limit to React is essentially the limits of Javascript of 
which I am fairly familiar with. Svelte and Vue essentially still have their 
own unique syntax for things such as list comprehension of components and it's 
too much to learn. 

With the advent of React Hooks, code size is much smaller and there's less about 
React internals that one would need to understand. The power in React still 
makes me prefer React over the others but I would put Svelte into a close second. 
