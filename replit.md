# Replit.md

## Overview

This is a single-page resume website for Emilio Nájera built with Flask. The project creates a modern, responsive portfolio site with smooth animations, dark/light mode toggle, and a clean minimalist design featuring a blue-light purple gradient theme. The site serves as a digital CV showcasing professional experience, education, skills, and contact information with a sideways hero layout and glassmorphic navigation header.

## User Preferences

Preferred communication style: Simple, everyday language.
Design preferences: Blue-light purple gradient theme (#667eea to #764ba2), glassmorphic navigation with minimal borders, sideways hero layout with profile image on left, icon-only social buttons, pastel-colored skill tags.

## System Architecture

### Frontend Architecture
- **Single-page application** with server-side rendering via Flask templates
- **Vanilla JavaScript** for interactivity and animations
- **CSS Custom Properties** for theme management (light/dark mode)
- **Mobile-first responsive design** approach

### Backend Architecture
- **Flask web framework** serving static content
- **Minimal server logic** - primarily template rendering
- **Session management** capability (though not currently utilized)
- **Environment-based configuration** for sensitive data

## Key Components

### Web Framework
- **Flask**: Lightweight Python web framework chosen for simplicity
- **Template rendering**: Uses Jinja2 templating for HTML generation
- **Static file serving**: CSS, JS, and image assets served via Flask's static file handler

### Frontend Libraries
- **AOS (Animate On Scroll)**: Provides fade-in animations as user scrolls
- **Font Awesome**: Icon library for UI elements
- **Google Fonts (Inter)**: Typography system for consistent text rendering

### Theme System
- **CSS Custom Properties**: Enables dynamic theme switching
- **Local Storage**: Persists user's theme preference
- **Smooth transitions**: Animated theme changes for better UX

### Navigation
- **Fixed header navigation**: Sticky top navigation with anchor links
- **Mobile hamburger menu**: Collapsible navigation for smaller screens
- **Smooth scrolling**: JavaScript-enhanced navigation between sections

## Data Flow

### Static Content Model
The application uses a static content approach where all resume data is hardcoded in templates:

1. **Profile Information**: Name, photo, introduction text
2. **Experience Timeline**: Work history with roles, companies, dates, descriptions
3. **Highlights Section**: Key accomplishments and achievements
4. **Skills Inventory**: Technical and soft skills listing
5. **Contact Details**: Email, LinkedIn, GitHub, website links

### User Interaction Flow
1. **Initial Load**: Page loads with saved theme preference or defaults to light mode
2. **Navigation**: Users click nav links → smooth scroll to sections
3. **Theme Toggle**: Click theme button → toggle between light/dark modes
4. **Scroll Animations**: Sections animate into view as user scrolls
5. **Mobile Menu**: Toggle mobile navigation on smaller screens

## External Dependencies

### CDN Resources
- **Google Fonts API**: Inter font family for typography
- **Font Awesome CDN**: Icons for UI elements
- **AOS Library**: Animation library loaded via CDN

### Runtime Dependencies
- **Flask**: Core web framework
- **Python standard library**: OS module for environment variables

## Deployment Strategy

### Current Setup
- **Development server**: Flask's built-in development server
- **Host configuration**: Binds to all interfaces (0.0.0.0) on port 5000
- **Debug mode**: Enabled for development with auto-reload

### Environment Configuration
- **Session secret**: Configurable via SESSION_SECRET environment variable
- **Fallback values**: Development defaults for local testing

### Replit Compatibility
- **Zero-config deployment**: Runs directly on Replit with minimal setup
- **Static asset serving**: All CSS, JS, and images served via Flask
- **Port binding**: Compatible with Replit's hosting requirements

### Scalability Considerations
- **Static content**: No database required, making deployment simple
- **Minimal server resources**: Low memory and CPU requirements
- **CDN assets**: External resources reduce server load
- **Cacheable content**: Static assets can be cached for performance

The architecture prioritizes simplicity and ease of deployment while maintaining professional presentation and user experience. The choice of Flask over static site generators allows for future dynamic features while keeping the current implementation straightforward.