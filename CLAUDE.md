# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a Unity 6.0 Hanafuda (Japanese card game) project using Universal Render Pipeline (URP). The project is newly initialized with a solid foundation but minimal game-specific code.

## Development Commands

### Unity Editor
- Open project: Launch Unity Hub → Open → Select this project folder
- Build project: File → Build Settings → Build (or Build and Run)
- Package Manager access: Window → Package Manager
- Unity MCP commands: Available through Unity Editor menu after MCP integration

### Testing and Quality
- Unity Test Runner: Window → General → Test Runner
- No custom test commands configured yet - use Unity's built-in testing framework

## Project Architecture

### Key Technologies
- **Unity Version**: 6000.0.51f1 (Unity 6.0)
- **Render Pipeline**: Universal Render Pipeline (URP) with separate PC/Mobile quality settings
- **Input System**: New Unity Input System with comprehensive action mappings for card game interactions
- **Unity MCP**: Integrated AI assistant for development acceleration (`jp.shiranui-isuzu.unity-mcp@1.1.2`)

### Core Structure
- `Assets/Scripts/`: **Currently empty** - all Hanafuda game logic needs to be implemented here
- `Assets/Scenes/SampleScene.unity`: Main scene (rename for Hanafuda game)
- `Assets/Settings/`: URP rendering assets with platform-specific configurations
- `Assets/InputSystem_Actions.inputactions`: Comprehensive input mappings ready for card game controls

### Multi-Platform Configuration
- **Primary Targets**: Android (ARM64) and PC/Standalone
- **Mobile Optimizations**: 0.8x render scale, disabled depth/opaque textures
- **PC Settings**: Full quality with HDR, MSAA enabled
- **Input Support**: Touch, mouse, keyboard, and gamepad controls configured

### Package Dependencies
Key packages that affect development:
- `com.unity.render-pipelines.universal`: URP rendering system
- `com.unity.inputsystem`: New Input System for card game controls  
- `com.unity.ugui`: UI system for game interface
- `jp.shiranui-isuzu.unity-mcp`: AI assistant integration for development

## Development Notes

### Unity MCP Integration
The project includes Unity MCP which enables AI-assisted development directly in the Unity Editor. This provides:
- C# script generation and modification capabilities
- Asset management assistance
- Runtime code execution for testing
- Menu commands for automated development tasks

### Input System Setup
The input system is fully configured with action maps for:
- Player actions (Move, Look, Attack, Interact, Menu navigation)
- UI navigation and selection
- Cross-platform input (touch, mouse, gamepad)

### Build Configuration
- Build scenes currently contain only the sample scene
- IL2CPP backend configured for Android
- Code stripping enabled for optimized builds
- Multi-architecture support configured for all target platforms

### Current Development State
This is a clean foundation project ready for Hanafuda game implementation. The `Assets/Scripts/` folder is empty and waiting for game-specific code. All Unity infrastructure (rendering, input, platform settings) is properly configured.