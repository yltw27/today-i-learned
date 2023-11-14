# JSX

JSX is syntatic sugar to create JS objects in a clean way

```
const tag = <h1>Title</h1>;
```

is the same with

```
const tag = React.createElement("h1", {}, "Hello");
```
