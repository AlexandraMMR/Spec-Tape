# Technology Stack

## Core Technologies

- **TypeScript 5.0+**: Primary language with strict type checking
- **Node.js**: Runtime environment (ES2020 target)
- **Jest**: Testing framework with ts-jest preset

## Dependencies

- **qrcode**: QR code generation for Digital Spirit Shard sharing
- **@types/qrcode**: TypeScript definitions for QR code library

## Build System

- **TypeScript Compiler (tsc)**: Compiles to CommonJS modules in `dist/` directory
- **Source Maps**: Enabled for debugging
- **Declaration Files**: Generated for type definitions

## Common Commands

```bash
# Development
npm run dev          # Watch mode compilation
npm run build        # Production build
npm start           # Run compiled application

# Testing
npm test            # Run all tests
npm run test:watch  # Run tests in watch mode

# Installation
npm install         # Install dependencies
```

## Project Configuration

- **Output Directory**: `dist/`
- **Source Directory**: `src/`
- **Test Pattern**: `**/__tests__/**/*.ts` and `**/?(*.)+(spec|test).ts`
- **Test Timeout**: 10 seconds
- **Coverage**: Text, LCOV, and HTML reports in `coverage/` directory

## TypeScript Configuration

- Strict mode enabled
- ES2020 target with DOM libraries
- Source maps and declaration maps generated
- JSON module resolution enabled
- Tests excluded from compilation