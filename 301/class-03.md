## Class-3 Reading Notes  
<p>The reading materials today directly relate to the current React-related set of labs.</p>

### React Docs - lists and keys

1. What does .map() return?
    * It returns a new array equal in length to the original array passed in.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    * By using the .map() function.
3. Each list item needs a unique ____.
    * Key.
4. What is the purpose of a key?
    * Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.

### The Spread Operator

1. What is the spread operator?
    * It refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.
2. List 4 things that the spread operator can do.
    * Adding items to arrays.
    * Spreading an array out into a function’s arguments.
    * Combining arrays.
    * Combining objects.
3. Give an example of using the spread operator to combine two arrays.
    * So you have one array called nums that is assigned [1,3,5], and you create a second array called numsX that is assigned [7,9,11] and create a new array called numsCombo that is assigned [...nums, ...numX], numsCombo will have following elements: [1,3,5,7,9,11]
4. Give an example of using the spread operator to add a new item to an array.
    * If you had nums that is assigned [1,3,5], you can create a new array called numY assigned [7...nums], now numsY will be assigned [7,1,3,5]
5. Give an example of using the spread operator to combine two objects into one.
    * If you start with Obj1 = {car: 'Buick'}, Obj2 = {bulb: 'Tulip'}, and assign Obj3 the following: {...Obj1,...Obj2}, Obj3 is assigned {car: 'Buick', bulb: 'Tulip'}

### How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between components?
    * Creates a function wherever it is that the state is.
2. In your own words, what does the increment function do?
    * Passed in an array of objects of people through a map function, determines which specific person is being called, and then updates the state of the count attributed to that person.
3. How can you pass a method from a parent component into a child component?
    * You can pass it just as you would any other prop.
4. How does the child component invoke a method that was passed to it from a parent component?
    * In this case child called method via this.props.increment(this.props.name).

## Things I want to know more about

1. I understand that the readings today directly relate to the current sleight of React-related labs at a high level, but actual implementation is still the challenge ahead of me.