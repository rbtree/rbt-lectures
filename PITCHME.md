#HSLIDE

<img src="/images/redux.png" width="100" style="border:none; box-shadow:none;">

## Redux
#### Filip Jovakaric

---

### What is Redux?

- Redux is a predictable state container for JavaScript apps.
- It’s an application data-flow architecture, rather than a traditional library or a framework like Underscore.js and AngularJS
- 30+ k GitHub stars
- 2.3+ million downloads in the last month on npm
- It was created by Dan Abramov

+++

### 3 core concepts

- There is a single source of truth for your entire application state
- That state is read-only
- All changes to the application state are made by pure functions

+++

### Usage

<img src="/images/vue.png" width="180" style="border:none; box-shadow:none;">
<img src="/images/react.png" width="250" style="border:none; box-shadow:none;">
<img src="/images/angular2.png" width="150" style="border:none; box-shadow:none;">

+++

### Alternatives for Redux

- [Facebook Flux](https://github.com/facebook/flux) - 13k stars on GitHub
- [MobX](https://github.com/mobxjs/mobx) - 9k stars on GitHub
- [Reflux](https://github.com/reflux/refluxjs) - 5k stars on GitHub
- [Alt](https://github.com/goatslacker/alt) - 3k stars on GitHub
- [Flummox](https://github.com/acdlite/flummox) - 1.5k stars on GitHub
- [Fluxxor](https://github.com/BinaryMuse/fluxxor) - 1.5k stars on GitHub
- more than 10 others...

---

### Unidirectional Dataflow

<img src="/images/data-flow.png" width="60%" style="border:none; box-shadow:none;">

+++

### Actions / Action Creators

<img src="/images/actions.png" width="600" style="border:none; box-shadow:none;">

+++

### Actions / Action Creators

```javascript
export function incrementCounter(step) {
    return {
        type: 'INCREMENT_COUNTER',
        step: step || 1,
    }
}

export function decrementCounter(step) {
    return {
        type: 'DECREMENT_COUNTER',
        step: step || 1,
    }
}
```

+++

### Actions / Action Creators

```javascript
export function searchMovies(movieName) {
    return (dispatch) => {
        dispatch(beginAjaxCall());
        moviesApi
            .search(movieName)
            .then((result) => {
                dispatch(searchMoviesSuccess(result.data.Search));
            })
            .catch((err) => {
                dispatch(ajaxCallError(err));
            });
    }
}
```

+++

### Store

<img src="/images/store.png" width="600" style="border:none; box-shadow:none;">

+++

### Reducers

<img src="/images/reducers.png" width="600" style="border:none; box-shadow:none;">

+++

### Reducers

```javascript
function initialState() {
    return {
        value: 0,
    };
}

export default function counterReducer($$state = initialState(), action) {

    switch (action.type) {

    case 'INCREMENT_COUNTER':
        return {
            value: $$state.value + action.step,
        };

    case 'DECREMENT_COUNTER':
        return {
            value: $$state.value - action.step,
        };

    default:
        return { ...$$state };
    }
}
```

+++

### How it all fits together

<img src="/images/how-it-works.png" width="90%" style="border:none; box-shadow:none;">

---

### Demo

---

### Testability of Redux

- Redux apps are easy for testing
- Reducers are pure functions
- Little or no mocking is needed
- Basic Actions return plain objects
- Async Actions need some levels of store mocking

---

### Resources

- [A Cartoon Intro to Redux](https://code-cartoons.com/a-cartoon-intro-to-redux-3afb775501a6)
- [The Evolution of Flux Frameworks](https://medium.com/@dan_abramov/the-evolution-of-flux-frameworks-6c16ad26bb31)
- [Redux Docs](http://redux.js.org/)
- [Redux Step by Step: A Simple and Robust Workflow for Real Life Apps](https://hackernoon.com/redux-step-by-step-a-simple-and-robust-workflow-for-real-life-apps-1fdf7df46092)
- [Redux · An Introduction](https://www.smashingmagazine.com/2016/06/an-introduction-to-redux/)
- [Getting Started with Redux: An Intro](https://scotch.io/bar-talk/getting-started-with-redux-an-intro)

+++

### Thank You!
