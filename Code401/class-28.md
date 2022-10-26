# Component Lifecycle / useEffect Hook

## Effects Hook

<https://reactjs.org/docs/hooks-effect.html>

**What purpose does useEffect serve in a function component compared to its counterpart(s) in class components?**

The Effect Hook lets you perform side effects in function components.

**When using the useEffect Hook:**
    **What does useEffect do?**
        Think of useEffect Hook as componentDidMount, componentDidUpdate, and componentWillUnmount combined.
    **Why is useEffect called inside a component?**
        In many cases we want to perform the same side effect regardless of whether the component just *mounted, or if it has been *updated.
    **Why is useEffect called inside a component?**
        Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect. We don’t need a special API to read it — it’s already in the function scope. Hooks embrace JavaScript closures and avoid introducing React-specific APIs where JavaScript already provides a solution.

**Explain the importance of properly implementing effects with Cleanup**
    It is important to clean up so that we don’t introduce a **memory leak!**
Forgetting to handle componentDidUpdate properly is a common source of bugs in React applications.

**What are your learning goals after reading and reviewing the class README?**

To write clean efficient un buggy code and to feel confident doing it.

## Things I want to know more about

Note

If you use this optimization, make sure the array includes **all values from the component scope (such as props and state) that change over time and that are used by the effect.** Otherwise, your code will reference stale values from previous renders. Learn more about how to deal with functions and what to do when the array changes too often.

If you want to run an effect and clean it up only once (on mount and unmount), you can pass an empty array ([]) as a second argument. This tells React that your effect doesn’t depend on any values from props or state, so it never needs to re-run. This isn’t handled as a special case — it follows directly from how the dependencies array always works.

If you pass an empty array ([]), the props and state inside the effect will always have their initial values. While passing [] as the second argument is closer to the familiar componentDidMount and componentWillUnmount mental model, there are usually better solutions to avoid re-running effects too often. Also, don’t forget that React defers running useEffect until after the browser has painted, so doing extra work is less of a problem.

We recommend using the exhaustive-deps rule as part of our eslint-plugin-react-hooks package. It warns when dependencies are specified incorrectly and suggests a fix.


