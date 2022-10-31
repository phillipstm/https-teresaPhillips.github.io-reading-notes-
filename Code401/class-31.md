# Context API

<https://reactjs.org/docs/context.html>

**What can React Context provide your app?**
    Context provides a way to pass data through the component tree without having to pass props down manually at every level.
**Why might we use Context?**
    Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.
**Why should we use it sparingly?**
     Apply it sparingly because it makes component reuse more difficult.

## Awesome React Context links

<https://github.com/diegohaz/awesome-react-context>

Consume content from (at least) two of the Awesome React Context links. Share your take-away from each:
**Takeaway 1:**
    React-zap lets you tie the new APi feature in to the similarly powerful concept of higher-order components.

    One aspect of the new context API which has been much talked about in the community is that it uses the function-as-a-child pattern (also called render props) for its Consumers. This pattern has been positioned by some as an alternative to higher-order components, so the general impression is that you need to choose: either use HoCs or use Render Props.

**Takeaway 2:**
    Context allows you to pass props to child data to get the data only where needed. Default providers are used if you don't have a provider above your consumer. The *provider* is where your data lives the *consumer* is where you access the data.
