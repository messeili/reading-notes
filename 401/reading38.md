## Reading38:Redux - Additional Topics

Other ways to build and manage a Redux store

- Let's face it, Redux is great, but there's a lot of "boilerplate" code that you have write, and every developer or company will have their own internal pattern for putting it all together.

- File Directory Names

- Reducer and Action Styles

- How do we model our data in the reducers

- There's a few projects out there that are attempting to unify the community around some simple standard ways to build stores so that as you move between projects, you'll recognize what you see.

### Redux Toolkit

- The makers of Redux have recognized that Redux is complicated and have introduced a "Batteries Included, Highly Opinionated" framework for making stores called the Redux Toolkit.

- This toolkit specifies a few different means of building a reducer and action set that work well together and are easier to understand and integrate.

- Ultimately, your store code can be as simple and declarative as this:

```

const postsSlice = createSlice({ name: 'posts', initialState: [], reducers: { createPost(state, action) {}, updatePost(state, action) {}, deletePost(state, action) {} } })

// Extract the action creators object and the reducer const { actions, reducer } = postsSlice // Extract and export each action creator by name export const { createPost, updatePost, deletePost } = actions // Export the reducer, either as a default or named export export default reducer

// ----- Sample Use ----- // console.log(createPost({ id: 123, title: 'Hello World' })) // {type : "posts/createPost", payload : {id : 123, title : "Hello World"}}

// Notice how createSlice transforms your defiition? console.log(postsSlice) /* { name: 'posts', actions : { createPost, updatePost, deletePost, }, reducer } */

```
