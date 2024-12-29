# Uncommon Expo CLI Bug: Module Not Found Errors

This repository demonstrates a bug in the Expo CLI where modules are reported as not found despite successful installation and prebuild commands.

The problem manifests as runtime errors when trying to use components from installed libraries. This usually occurs because of incorrect linking between the Expo managed workflow environment and the native modules required by the library.

The `uncommonExpoBug.js` file shows the code that reproduces the error. The solution, provided in `uncommonExpoBugSolution.js`, addresses the linking problem using different approaches like cleaning the cache, ensuring correct native module integration, and re-linking.

## Steps to Reproduce
1. Clone this repository.
2. Run `expo install [necessary libraries]`
3. Run `expo prebuild` (or any applicable prebuild commands).
4. Run `expo start`.
5. Observe the runtime error, and then follow the solution provided.