# Cybernetics Releases

This repository hosts the official release builds of Cybernetics, a mobile-first AI platform built for mass automation of digital tasks across communication, media, development, and system management.

## What is Cybernetics

Cybernetics is a self-hosted AI operating system designed to give a single user the operational capacity of an entire team. It runs persistently in the cloud and exposes a unified interface for controlling every digital workflow from one place — a phone, a browser, or a terminal.

The platform is built around the idea that software should work for you without requiring constant supervision. Every component is designed to run autonomously, report back, and take action without manual intervention.

## Core Capabilities

**WhatsApp Automation** — Full programmatic control over WhatsApp including reading threads, sending messages, broadcasting to multiple contacts, reacting to statuses, and executing bot commands. The bot runs 24/7 and can be directed by the AI to communicate on your behalf.

**AI Orchestration** — A multi-model AI layer that routes tasks between Gemini, Groq, and other providers depending on context. Supports real-time voice interaction, tool use, shell execution, and long-running agentic workflows.

**Integrated Development Environment** — A full browser-based IDE with file management, multi-terminal support, real-time file watching, and direct deployment to the cloud backend.

**Media Pipeline** — Automated search, download, conversion, and delivery of audio and video content from YouTube, TikTok, and other sources.

**Shell Access** — Persistent server-side shell sessions accessible from any device. Commands run on the backend and stream output back in real time.

**Session Persistence** — All AI sessions, WhatsApp connections, terminal states, and user data persist across disconnections and server restarts via MongoDB.

## Architecture

The system is split across three services. The main backend handles AI sessions, shell execution, IDE functionality, and WebSocket communication. A dedicated WhatsApp service manages multi-user bot sessions with full isolation between accounts. Authentication is handled via HMAC-signed tokens delivered through WhatsApp OTP — no passwords, no email.

The mobile app is a Capacitor-wrapped React application that connects to the backend over WebSocket and provides a native Android experience with the full feature set of the web interface.

## Distribution

Release APKs are published to this repository automatically on every push to the main branch of the source repository. Each release is signed with a consistent keystore so updates install directly over previous versions without requiring an uninstall.

To install, download the latest APK from the releases page and open it on your Android device.
