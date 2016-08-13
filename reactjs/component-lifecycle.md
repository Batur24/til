
# Component lifecycle

reactjs有7个Lifecycle methods, 我在这里想把这7种方法多过一下

## componentWillMount
> Invoked once, both on the client and server, immediately before the innitial rendering occurs, if you call **setState** within this method, **render()** will see the updated state and will be executed only once despite the state change.

在render之前执行, 只执行一次


## componentDidlMount
## componentWiiReceive
## shouldComponentUpdate
## componentWillUpdate
## componentDidUpdate
## componentWillUnmount
