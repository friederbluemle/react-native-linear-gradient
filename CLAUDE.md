# CLAUDE.md - Development Guide for react-native-linear-gradient

## Build/Lint/Test Commands
- Build Android: `cd android && ./gradlew build`
- Run tests: `npm test` or `yarn test` 
- Run single test: `yarn test -t "test name pattern"`
- Lint: `cd example && yarn lint`
- Flow type check: `yarn flow`

## Code Style Guidelines
- **Formatting**: Follow React Native community ESLint rules
- **Imports**: Group imports (React, then external, then internal)
- **TypeScript**: Use proper type annotations with React component Props interfaces
- **Naming**: 
  - PascalCase for components, interfaces (`LinearGradient`, `LinearGradientProps`)
  - camelCase for methods, variables, and instances
- **Error handling**: Validate props & provide clear error messages
- **Testing**: Write Jest tests for components, mock using provided mock
- **Architecture**: Support both old and new React Native architectures
- **Android-specific**: Follow Java conventions, add proper annotations
- **Comments**: Document complex code (especially gradient calculations)

## Testing with Jest
Include the provided mock in test setup:
```js
import mockRNLinearGradient from 'react-native-linear-gradient/jest/linear-gradient-mock';
jest.mock('react-native-linear-gradient', () => mockRNLinearGradient);
```