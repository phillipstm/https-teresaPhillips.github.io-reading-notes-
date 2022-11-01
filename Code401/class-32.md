# Context API - Behaviors

## Hooks and Context example

<https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b>

**With regard to the React Context API, what does a “provider” do?**

Our context provider is now responsible for both displaying the local state of the snackbars (we call them alerts), and for exposing an API for globally managing them.

**With regard to the React Context API, how would we implement a “consumer” role?**

It turns out that our custom hook from before is nothing more than a small wrapper around the useContext internal React hook, which consumes our new context.

**Specifically with Context, how are we “wrapping” components to achieve our goals?**

## Awesome React Context links

<https://github.com/diegohaz/awesome-react-context>

**Takeaway 1:**
    A higher-order component (HOC) is an advanced technique in React for reusing component logic. HOCs are not part of the React API, per se. They are a pattern that emerges from React’s compositional nature.

    Concretely, a higher-order component is a function that takes a component and returns a new component.
**Takeaway 2:**
    React waterfall was built on top of the new context API.
