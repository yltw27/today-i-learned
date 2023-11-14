# Principles - React

- Use `key` attribute in a list to help React have better performance - To insert a new node in a list, without keys React will destroy the first node, assign the new node to the first node; destroy the second node, assign the newly create old first node to it...etc.

## Zustand

- Fetch state by selectors instead of fetching everything to prevent unnecessary re-renders
