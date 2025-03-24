# What's New in .NET 6

## Table of Contents
1. [Performance Enhancements](#performance-enhancements)
   - FileStream Rewrite
   - Profile-Guided Optimization (PGO)
   - Crossgen2
2. [Development Experience](#development-experience)
   - C# 10 Enhancements
   - Hot Reload
   - Minimal APIs
3. [Platform & Framework Support](#platform-framework-support)
   - .NET MAUI
   - Arm64 Support
4. [SDK & Tooling Improvements](#sdk-tooling-improvements)
   - Optional SDK Workloads
   - New `dotnet workload` Commands
5. [ASP.NET Core & Web Development](#aspnet-core-web-development)
   - HTTP/3 Support
   - Blazor Enhancements
   - Minimal APIs
6. [Improved JSON Handling](#improved-json-handling)
   - System.Text.Json Source Generator
   - Writable JSON DOM
   - IAsyncEnumerable Serialization
7. [Security & Compatibility](#security-compatibility)
   - Intel CET Security Support
   - IL Trimming Improvements
   - Breaking Changes
8. [Other Notable Features](#other-notable-features)
   - Generic Math
   - PriorityQueue<TElement, TPriority>
   - DateOnly & TimeOnly
   - NuGet Package Validation

---

## Performance Enhancements
### FileStream Rewrite
- Improved speed and reliability.
- Now never blocks when created for asynchronous I/O on Windows.

### Profile-Guided Optimization (PGO)
- JIT compiler optimizations based on runtime behavior.
- Can be enabled with `DOTNET_TieredPGO` environment variable.

### Crossgen2
- New Ahead-of-Time (AOT) compilation tool.
- Faster app startup and better optimization compared to previous Crossgen.

## Development Experience
### C# 10 Enhancements
- **Global Using Directives**: Reduces the need for repetitive using statements.
- **File-Scoped Namespaces**: Less indentation in files.
- **Record Structs**: Better struct support for immutable data.

### Hot Reload
- Modify source code and apply changes instantly without restarting the app.
- Works with most .NET applications.

### Minimal APIs
- New streamlined syntax for building lightweight microservices.
- Less boilerplate code needed.

## Platform & Framework Support
### .NET MAUI
- Multi-platform App UI for building desktop and mobile apps with a single codebase.
- Expected general availability in mid-2022.

### Arm64 Support
- Native support for Apple Silicon (macOS) and Windows Arm64.
- x64 and Arm64 .NET installers now install side-by-side.

## SDK & Tooling Improvements
### Optional SDK Workloads
- Reduces the size of the SDK installation.
- Components like .NET MAUI and Blazor WebAssembly AOT moved to optional workloads.

### New `dotnet workload` Commands
- `dotnet workload search`: Searches for available workloads.
- `dotnet workload install`: Installs specified workloads.
- `dotnet workload uninstall`: Removes specified workloads.
- `dotnet workload update`: Updates installed workloads.
- `dotnet workload repair`: Reinstalls workloads to fix issues.
- `dotnet workload list`: Lists installed workloads.

## ASP.NET Core & Web Development
### HTTP/3 Support
- Uses QUIC protocol for better performance and connectivity.
- Improves mobile client support with seamless switching between Wi-Fi and cellular networks.

### Blazor Enhancements
- Ahead-of-Time (AOT) compilation for Blazor WebAssembly apps.
- JavaScript integration allows Blazor components to be used in JavaScript apps.

### Minimal APIs
- Provides a simpler way to define and run web APIs.
- Reduces boilerplate code significantly.

## Improved JSON Handling
### System.Text.Json Source Generator
- Improves serialization performance.
- Reduces memory usage and facilitates assembly trimming.

### Writable JSON DOM
- New types: `JsonNode`, `JsonArray`, `JsonObject`, `JsonValue`.
- Enables direct JSON manipulation without needing POCO objects.

### IAsyncEnumerable Serialization
- Supports async streaming serialization.
- New method: `JsonSerializer.DeserializeAsyncEnumerable<T>(Stream, JsonSerializerOptions, CancellationToken)`.

## Security & Compatibility
### Intel CET Security Support
- Protects against control-flow hijacking attacks.
- Enabled explicitly for Windows x64 apps.

### IL Trimming Improvements
- Removes unused types and members to reduce application size.
- Trim warnings enabled by default.

### Breaking Changes
- Some APIs have changed behavior or been removed.
- Notable areas include ASP.NET Core, networking, and serialization.

## Other Notable Features
### Generic Math
- Supports static abstract members in interfaces.
- Enhances operator support for generic types.

### PriorityQueue<TElement, TPriority>
- Implements a **min-heap** data structure.
- Items are dequeued in increasing priority order.

### DateOnly & TimeOnly
- `DateOnly`: Represents a date without time.
- `TimeOnly`: Represents a time without date.
- Useful for birthdays, schedules, and alarms.

### NuGet Package Validation
- Ensures package consistency and backward compatibility.
- Helps detect breaking changes across package versions.

---

This document provides a high-level overview of the major changes in .NET 6. For detailed information, visit the official [Microsoft documentation](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-6).

