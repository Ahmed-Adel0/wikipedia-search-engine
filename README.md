# wikipedia-search-engine

This project implements the debounce technique with a search input field.
The search input field allows users to enter a search query, and the debounce technique ensures that the search results are generated only after a specified delay of user inactivity.

## Task

The task is to modify the existing code to incorporate the debounce technique.
Currently, the code fetches search results from the Wikipedia API based on the user's input and displays them in the results container. However, the code immediately triggers the search results generation on each keystroke, which can result in unnecessary API calls and poor performance.

To optimize the search functionality, the debounce technique is implemented.
It introduces a delay between the user's input and the generation of search results.
The search results will be generated only after the user pauses typing for the specified delay.
This reduces the number of API calls and improves the overall user experience.

## Implementation

The following modifications were made to the existing code:

1. Created a `debounce` function that takes a function and a delay as arguments.
   It returns a new function that uses a timer to execute the original function after the specified delay.

2. Updated the `validateInput` function to use the `debounce` function.
   The `validateInput` function is now wrapped with the `debounce` function, which introduces a delay before calling the function.
   This ensures that the `generateResults` function is only called after the specified delay of user inactivity.

3. Updated the `generateResults` function to handle the fetching and display of search results as before.

By implementing the debounce technique, the search results will be generated only when the user pauses typing for the specified delay, reducing unnecessary API calls and enhancing the performance of the search functionality.
