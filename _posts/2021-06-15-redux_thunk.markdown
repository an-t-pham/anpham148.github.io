---
layout: post
title:      "Redux Thunk"
date:       2021-06-15 10:13:46 -0400
permalink:  redux_thunk
---

Redux Thunk is middleware that allows fetching data to return functions, rather than just actions, within Redux. Thunk handles asynchronous calls which allows for delayed actions, like working with promises.

One of the main reasons to utilise this middleware is for handling actions that might not be synchronous. 
Redux Thunk allows us to dispatch those actions asynchronously and resolve each promise that gets returned. 

So, I've used Thunk for my final project. Here is an example of my CollectionsContainer with and without Thunk:

* Without Thunk

```
//action
function fetchCollections(dispatch, userId) { 
    .then(resp => resp.json())
    .then(collections => dispatch({ 
		   type: 'FETCH_COLLECTIONS', 
			 payload: collections.data 
		}));
}

// component CollectionsContainer
import React from 'react';
import { connect } from 'react-redux';
import { fetchCollections } from '../../actions/fetchCollections';

componentDidMount() {
     this.props.user && (this.props.fetchCollections(this.props.dispatch, this.props.user.id))
  }
	
const mapDispatchToProps = (dispatch) => {
  return {
    fetchCollections: (userId) => fetchCollections(dispatch, userId))
  }
}
	
export default connect(mapStateToProps, mapDispatchToProps)(CollectionsContainer)
```


* With Thunk

```
//action
export const fetchCollections = (userId) => {
    return (dispatch) => {
        fetch(`${BASE_URL}/users/${userId}/collections`)
        .then(resp => resp.json())
        .then(collections => dispatch({
            type: 'FETCH_COLLECTIONS',
            payload: collections.data
        }))
    }
}

// component CollectionsContainer
import React from 'react';
import { connect } from 'react-redux';
import { fetchCollections } from '../../actions/fetchCollections';

componentDidMount() {
     this.props.user && (this.props.fetchCollections(this.props.user.id))
  }
	
export default connect(mapStateToProps, { fetchCollections } )(CollectionsContainer)
```

There is not much difference between them. However, with Thunk middleware, the component CollectionsContainer doesn't need to worry that the action is async or how it is implemented. So I just passed in fetchCollections as an object to redux and let redux take care of the rest. On the other hand, without Thunk, the component CollectionsContainer knows exactly that a specific call is async, and needs dispatch to be passed by some convention, like mapDispatchtoProp as an async parameter above.

With Thunk, we can incorporate asynchronous code in with our Redux actions. This allows us to continue keeping our components relatively simple and more focused on presentation. 
