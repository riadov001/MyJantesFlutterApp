# Overview

MY JANTES is a complete, functional Flutter-based mobile application for a French automotive wheel renovation business. The app provides customers with online booking, quote requests, and service information, while offering an admin dashboard for business management. The application supports multiple platforms (iOS, Android, Web) with a PWA-ready web version for Hostinger deployment.

**Status**: ✅ COMPLETE - Full Flutter application ready for Codemagic CI/CD builds

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: Flutter 3.x with Dart language
- **UI Design**: Material Design 3 with custom MY JANTES branding
- **Theme**: Custom theme using red (#DC2626) primary color with Roboto typography
- **Navigation**: Multi-screen architecture with dedicated screens for home, booking, quotes, admin dashboard, and legal pages
- **Responsive Design**: Adaptive layouts for mobile, tablet, and web platforms
- **State Management**: Provider pattern for authentication and API communication
- **HTTP Client**: Custom API service for WordPress backend integration

## State Management
- **Pattern**: Service-based architecture with separate API and authentication services
- **Data Flow**: Services handle API communication and state management across screens
- **Authentication**: Admin authentication system for dashboard access

## Platform Configuration
- **iOS**: Complete Xcode project structure with proper bundle identifier (fr.myjantes.app)
- **Android**: Gradle configuration with package name matching bundle identifier
- **Web**: PWA-ready configuration with manifest.json and service worker support
- **Build System**: Configured for Codemagic CI/CD pipeline with automated builds

## File Structure
- `/lib/main.dart`: Application entry point
- `/lib/models/`: Data models for booking and quote entities
- `/lib/screens/`: UI screens (home, booking, quote, dashboard, legal)
- `/lib/services/`: API communication and authentication services
- `/lib/utils/`: Theme configuration and utility functions
- `/assets/`: Application assets including icons and images

## CI/CD Pipeline
- **Platform**: Codemagic integration with automated builds
- **Outputs**: APK for Android, IPA for iOS, and web bundle for deployment
- **Configuration**: Complete codemagic.yaml for multi-platform builds
- **Deployment**: Automated web deployment to Hostinger via build artifacts

# External Dependencies

## Backend Integration
- **API Backend**: WordPress REST API integration
- **Endpoint**: Custom WordPress endpoints under `/wp-json/myjantes/v1/`
- **Services**: Booking management, quote requests, and admin authentication
- **Data Exchange**: JSON-based communication for reservations and quotes

## Hosting and Deployment
- **Web Hosting**: Hostinger with cPanel for web version deployment
- **Domain**: Custom domain integration for web application
- **SSL**: HTTPS support for secure communication

## Mobile Distribution
- **Android**: Google Play Store distribution with signed APK/Bundle
- **iOS**: TestApp.io for test distribution (without Apple Developer account)
- **Alternative iOS**: Supports Apple Developer account integration when available

## Development Tools
- **CI/CD**: Codemagic for automated builds and deployment
- **Version Control**: Git repository integration
- **Code Signing**: Android keystore and iOS certificate management
- **Asset Management**: Flutter asset pipeline for images and icons

## Third-Party Services
- **Image Upload**: Photo upload functionality for quote requests
- **PWA Features**: Service worker and offline capabilities for web version
- **Analytics**: Prepared for integration with web analytics services