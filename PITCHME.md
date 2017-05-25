#HSLIDE

<img src="/images/redux.png" width="100" style="border:none; box-shadow:none;">

## Redux
#### Filip Jovakaric

---

### What is Redux?

- Redux is a predictable state container for JavaScript apps.
- It’s an application data-flow architecture, rather than a traditional library or a framework like Underscore.js and AngularJS
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

---

### How did we get to Redux?

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

    case actionTypes.INCREMENT_COUNTER:
        return {
            value: $$state.value + action.step,
        };

    case actionTypes.DECREMENT_COUNTER:
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

---

### Resources

+++

### Thank You!
