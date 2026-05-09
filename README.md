# React Side Effects Lab

## Overview
This lab demonstrates how to handle **side effects** in React using the `useEffect` hook. The app fetches and displays a random **programming joke** when the page loads and allows users to fetch a new joke with a button click.

## Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the development server:**
   ```bash
   npm run dev
   ```
   The app will be available at `http://localhost:5173`

3. **Run tests:**
   ```bash
   npm run test
   ```

## Implementation Details

### Component Structure
- **App.jsx**: Main component that manages state for `joke` and `loading`. Uses `useEffect` to fetch a joke on mount and defines the `fetchJoke` function.
- **JokeDisplay.jsx**: Displays the joke or a loading message based on the `loading` prop.
- **FetchButton.jsx**: Button component that triggers a new joke fetch via the `fetchJoke` prop.

### Key Features
✓ **Fetches a programming joke on app load** using `useEffect` with an empty dependency array.
✓ **Shows loading state** while waiting for the API response.
✓ **Displays the joke** once the API returns the data.
✓ **Fetches a new joke** when the "Get a New Joke" button is clicked.
✓ **Error handling** for failed API requests via `.catch()`.

### State Management
- `joke` (string): Stores the current joke text
- `loading` (boolean): Tracks whether a fetch request is in progress

### API Endpoint
```
GET https://v2.jokeapi.dev/joke/Programming?type=single
```

## Best Practices Implemented

- ✓ Used `useEffect` hook to fetch data when the component mounts
- ✓ Used `useState` hook for managing joke and loading state
- ✓ Created modular, reusable components with clear prop interfaces
- ✓ Implemented proper error handling in fetch operations
- ✓ Kept event handlers separate from side effect logic

## Testing

All tests pass successfully:
- ✓ Displays a loading message before joke is loaded
- ✓ Fetches and displays a joke on load
- ✓ Fetches a new joke when button is clicked

Run `npm run test` to execute the test suite.
