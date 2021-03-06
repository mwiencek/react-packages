# react-packages

**These packages are obsolete as of React v16, which natively supports returning an array of elements from `render()`.**

---

These packages are built from [mwiencek/react#frag-component](https://github.com/mwiencek/react/tree/frag-component), which includes a solution for React issue [#2127](https://github.com/facebook/react/issues/2127) (Add fragment API to allow returning multiple components from render). The frag feature can be used like this:

```JSX
// Common scenario (returning multiple components from render)
const ComponentA = () => (
  <frag>
    <p>You’ve never seen</p>
    <p>Magic like this</p>
  </frag>
);

// Pointless example to showcase behavior
const ComponentB = () => (
  <frag>
    <frag key="1">
      <ComponentA />
      {'Nestin’'}
    </frag>
    <frag key="2">
      <p>More</p>
      <p>Nestin’</p>
    </frag>
  </frag>
);
```

Current packages are based on React v15.0.2.
