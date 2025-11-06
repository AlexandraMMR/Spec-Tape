# Project Structure

## Directory Organization

```
src/
├── types/           # Core TypeScript interfaces and type definitions
├── interfaces/      # Component interface definitions and contracts
├── audio/          # Audio processing engine and playback management
├── ghost-writer/   # AI agent for analysis, effects, and narrative generation
├── spirit-shard/   # Digital token management and sharing
├── connectivity/   # Wi-Fi, Bluetooth, NFC communication handlers
├── ui/            # User interface components and controls
├── utils/         # Utility functions and helper modules
├── models/        # Data model implementations
├── index.ts       # Main entry point
└── SpecTapeApp.ts # Main application controller
```

## Architecture Patterns

### Interface-First Design
- All major components define interfaces in `src/interfaces/`
- Implementations follow interface contracts strictly
- Enables easy testing and mocking

### Type Safety
- Core types defined in `src/types/index.ts`
- Comprehensive type definitions for all data structures
- Enums used for controlled vocabularies (EffectType, AudioFormat, etc.)

### Test Organization
- Tests located in `__tests__/` subdirectories within each module
- Test files follow `*.test.ts` naming convention
- Each component has corresponding test coverage

## Key Components

### Core Data Types
- `SpectralMix`: Main audio collection with manifestation reports
- `DigitalSpiritShard`: Shareable tokens containing spectral mixes
- `AudioFile`: Audio file metadata and properties
- `ManifestationReport`: AI-generated spooky narratives

### Manager Classes
- `AudioEngine`: Core audio processing
- `GhostWriterAgent`: AI analysis and narrative generation
- `ConnectivityManager`: Wireless communication handling
- `SpecTapeApp`: Main application orchestrator

## Naming Conventions

- **Files**: PascalCase for classes, camelCase for utilities
- **Interfaces**: PascalCase with descriptive names
- **Types**: PascalCase for interfaces, UPPER_CASE for enums
- **Methods**: camelCase with descriptive verbs
- **Constants**: UPPER_SNAKE_CASE for configuration values

## Module Dependencies

- `types/` - No dependencies (base layer)
- `interfaces/` - Depends only on `types/`
- `models/` - Implements interfaces, uses types
- `utils/` - Standalone helper functions
- All other modules can depend on types, interfaces, utils, and models