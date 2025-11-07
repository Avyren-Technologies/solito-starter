# AvyMart Universal E-Commerce & Service Platform
## Developer Technical Specification Document

---

### Document Information
- **Project Name:** AvyMart Universal E-Commerce & Service Platform
- **Document Type:** Developer Technical Specification
- **Version:** 1.0
- **Date:** November 2025
- **Target Platforms:** Web (Next.js) & Mobile (React Native)
- **Document Purpose:** Comprehensive developer guide for building the application

---

## Table of Contents

- [1. Project Overview](#1-project-overview)
  - [1.1 Application Architecture](#11-application-architecture)
  - [1.2 Core Business Logic](#12-core-business-logic)
  - [1.3 Platform Scope](#13-platform-scope)
- [2. Technology Stack](#2-technology-stack)
  - [2.1 Web Application Stack](#21-web-application-stack)
  - [2.2 Mobile Application Stack](#22-mobile-application-stack)
  - [2.3 Backend Stack](#23-backend-stack)
  - [2.4 Infrastructure Stack](#24-infrastructure-stack)
  - [2.5 Development Tools](#25-development-tools)
- [3. Development Environment Setup](#3-development-environment-setup)
  - [3.1 Prerequisites](#31-prerequisites)
  - [3.2 Project Structure](#32-project-structure)
  - [3.3 Environment Configuration](#33-environment-configuration)
  - [3.4 Local Development Setup](#34-local-development-setup)
- [4. System Architecture](#4-system-architecture)
  - [4.1 Multi-Platform Architecture](#41-multi-platform-architecture)
  - [4.2 Backend Architecture (Medusa + Motia)](#42-backend-architecture-medusa--motia)
  - [4.3 Data Flow Architecture](#43-data-flow-architecture)
  - [4.4 Security Architecture](#44-security-architecture)
- [5. Core Features & Implementation](#5-core-features--implementation)
  - [5.1 User Management & Authentication](#51-user-management--authentication)
  - [5.2 UID/QR Code System](#52-uidqr-code-system)
  - [5.3 E-Commerce Module](#53-e-commerce-module)
  - [5.4 Service Booking Module](#54-service-booking-module)
    - [5.4.1 Industry-Specific Service Modules](#541-industry-specific-service-modules)
  - [5.5 Family Group Management](#55-family-group-management)
  - [5.6 Transportation Services](#56-transportation-services)
  - [5.7 Delivery Agency Network](#57-delivery-agency-network)
  - [5.8 Payment Integration](#58-payment-integration)
  - [5.9 Chat-Based Interface](#59-chat-based-interface)
  - [5.10 Theme System & Customization](#510-theme-system--customization)
  - [5.11 Analytics & Reporting](#511-analytics--reporting)
  - [5.12 Advanced Features & Capabilities](#512-advanced-features--capabilities)
    - [5.12.1 Dynamic Configuration Management](#5121-dynamic-configuration-management)
    - [5.12.2 Dynamic Menu Management](#5122-dynamic-menu-management)
    - [5.12.3 Dynamic Role Creation & Management](#5123-dynamic-role-creation--management)
    - [5.12.4 Dynamic Formulas & Calculations](#5124-dynamic-formulas--calculations)
    - [5.12.5 Multiple Graph Types & Visualization](#5125-multiple-graph-types--visualization)
    - [5.12.6 Super Admin Interface](#5126-super-admin-interface)
    - [5.12.7 Notification Management](#5127-notification-management)
    - [5.12.8 Timezone Management & Globalization](#5128-timezone-management--globalization)
    - [5.12.9 Multi-language Support](#5129-multi-language-support)
    - [5.12.10 Granular Role-Based Access Control](#51210-granular-role-based-access-control)
    - [5.12.11 Device Management](#51211-device-management)
    - [5.12.12 Custom Fields & Attributes](#51212-custom-fields--attributes)
    - [5.12.13 Export Scheduling & Automated Reports](#51213-export-scheduling--automated-reports)
    - [5.12.14 Custom Report Templates](#51214-custom-report-templates)
    - [5.12.15 Custom Field Excel Reports](#51215-custom-field-excel-reports)
    - [5.12.16 License Expiry & Renewal Management](#51216-license-expiry--renewal-management)
    - [5.12.17 Super Admin Logs & Production Monitoring](#51217-super-admin-logs--production-monitoring)
    - [5.12.18 Advertising & Campaign Management System](#51218-advertising--campaign-management-system)
  - [5.13 Quality Assurance Module](#513-quality-assurance-module)
  - [5.14 Inventory Module](#514-inventory-module)
  - [5.15 Seller Management Module](#515-seller-management-module)
  - [5.16 Company Module](#516-company-module)
- [6. API Specifications](#6-api-specifications)
  - [6.1 API Architecture](#61-api-architecture)
  - [6.2 Authentication APIs](#62-authentication-apis)
  - [6.3 User Management APIs](#63-user-management-apis)
  - [6.4 E-Commerce APIs](#64-e-commerce-apis)
  - [6.5 Service Provider APIs](#65-service-provider-apis)
  - [6.6 Payment APIs](#66-payment-apis)
  - [6.7 UID Management APIs](#67-uid-management-apis)
  - [6.8 Family Group APIs](#68-family-group-apis)
  - [6.9 Transportation APIs](#69-transportation-apis)
  - [6.10 Delivery Network APIs](#610-delivery-network-apis)
  - [6.11 Chat & Communication APIs](#611-chat--communication-apis)
  - [6.12 Analytics APIs](#612-analytics-apis)
- [7. Database Design](#7-database-design)
  - [7.1 Database Architecture](#71-database-architecture)
  - [7.2 Core Entity Models](#72-core-entity-models)
  - [7.3 Relationships & Constraints](#73-relationships--constraints)
  - [7.4 Indexing Strategy](#74-indexing-strategy)
  - [7.5 Data Migration Strategy](#75-data-migration-strategy)
- [8. Frontend Development](#8-frontend-development)
  - [8.1 Web Application Development (Future Phase)](#81-web-application-development-future-phase)
  - [8.2 Mobile Application Development (Solito-Enhanced)](#82-mobile-application-development-solito-enhanced)
  - [8.3 Shared Components & Logic (Solito)](#83-shared-components--logic-solito)
  - [8.4 State Management](#84-state-management)
  - [8.5 Routing & Navigation](#85-routing--navigation)
  - [8.6 UI/UX Implementation](#86-uiux-implementation)
  - [8.7 Performance Optimization](#87-performance-optimization)
- [9. Backend Development](#9-backend-development)
  - [9.1 API Development](#91-api-development)
  - [9.2 Business Logic Implementation](#92-business-logic-implementation)
  - [9.3 Data Access Layer](#93-data-access-layer)
  - [9.4 Service Layer Architecture](#94-service-layer-architecture)
  - [9.5 Event-Driven Architecture](#95-event-driven-architecture)
  - [9.6 Caching Strategy](#96-caching-strategy)
- [10. Security Implementation](#10-security-implementation)
  - [10.1 Authentication & Authorization](#101-authentication--authorization)
  - [10.2 Data Encryption](#102-data-encryption)
  - [10.3 API Security](#103-api-security)
  - [10.4 Input Validation](#104-input-validation)
  - [10.5 Security Best Practices](#105-security-best-practices)
- [11. Integration Requirements](#11-integration-requirements)
  - [11.1 Payment Gateway Integration](#111-payment-gateway-integration)
  - [11.2 Third-Party Service Integration](#112-third-party-service-integration)
  - [11.3 GPS & Location Services](#113-gps--location-services)
  - [11.4 Notification Services](#114-notification-services)
  - [11.5 Analytics Integration](#115-analytics-integration)
- [12. Testing Requirements](#12-testing-requirements)
  - [12.1 Testing Strategy](#121-testing-strategy)
  - [12.2 Unit Testing](#122-unit-testing)
  - [12.3 Integration Testing](#123-integration-testing)
  - [12.4 End-to-End Testing](#124-end-to-end-testing)
  - [12.5 Performance Testing](#125-performance-testing)
  - [12.6 Security Testing](#126-security-testing)
- [13. Performance Requirements](#13-performance-requirements)
  - [13.1 Performance Targets](#131-performance-targets)
  - [13.2 Optimization Strategies](#132-optimization-strategies)
  - [13.3 Monitoring & Metrics](#133-monitoring--metrics)
- [14. Deployment & DevOps](#14-deployment--devops)
  - [14.1 CI/CD Pipeline](#141-cicd-pipeline)
  - [14.2 Environment Management](#142-environment-management)
  - [14.3 Deployment Strategy](#143-deployment-strategy)
  - [14.4 Monitoring & Logging](#144-monitoring--logging)
- [15. Development Best Practices](#15-development-best-practices)
  - [15.1 Code Standards](#151-code-standards)
  - [15.2 Git Workflow](#152-git-workflow)
  - [15.3 Code Review Process](#153-code-review-process)
  - [15.4 Documentation Standards](#154-documentation-standards)
- [16. Feature Implementation Roadmap](#16-feature-implementation-roadmap)
  - [16.1 Phase 1: Foundation](#161-phase-1-foundation)
  - [16.2 Phase 2: Core Features](#162-phase-2-core-features)
  - [16.3 Phase 3: Advanced Features](#163-phase-3-advanced-features)
- [17. Error Handling & Recovery Specifications](#17-error-handling--recovery-specifications)
  - [17.1 Error Classification Framework](#171-error-classification-framework)
  - [17.2 Error Response Standards](#172-error-response-standards)
  - [17.3 Error Response Format](#173-error-response-format)
  - [17.4 Error Handling Strategies](#174-error-handling-strategies)
  - [17.5 Recovery Mechanisms](#175-recovery-mechanisms)
  - [17.6 Monitoring and Alerting](#176-monitoring-and-alerting)
  - [17.7 UID System Error Handling](#177-uid-system-error-handling)
  - [17.8 Multi-Platform Error Handling](#178-multi-platform-error-handling)
  - [17.9 Compliance and Security Error Handling](#179-compliance-and-security-error-handling)
  - [17.10 User Communication During Errors](#1710-user-communication-during-errors)
  - [17.11 Error Recovery Testing](#1711-error-recovery-testing)
- [18. Audit Trail & Compliance Logging Requirements](#18-audit-trail--compliance-logging-requirements)
  - [18.1 Audit Trail Framework](#181-audit-trail-framework)
  - [18.2 Audit Event Categories](#182-audit-event-categories)
  - [18.3 Audit Log Data Structure](#183-audit-log-data-structure)
  - [18.4 Compliance-Specific Logging Requirements](#184-compliance-specific-logging-requirements)
  - [18.5 Audit Log Storage and Retention](#185-audit-log-storage-and-retention)
  - [18.6 Audit Log Access and Security](#186-audit-log-access-and-security)
  - [18.7 Audit Log Analytics and Reporting](#187-audit-log-analytics-and-reporting)
  - [18.8 UID System Audit Requirements](#188-uid-system-audit-requirements)
  - [18.9 Multi-Platform Audit Integration](#189-multi-platform-audit-integration)
  - [18.10 Audit Log Testing and Validation](#1810-audit-log-testing-and-validation)
  - [18.11 Legal and Forensic Requirements](#1811-legal-and-forensic-requirements)
  - [18.12 Audit Log Performance Requirements](#1812-audit-log-performance-requirements)
- [19. Data Management & Privacy](#19-data-management--privacy)
  - [19.1 Data Retention Policies](#191-data-retention-policies)
  - [19.2 Privacy & Compliance](#192-privacy--compliance)
  - [19.3 Data Anonymization and Deletion](#193-data-anonymization-and-deletion)
  - [19.4 Data Localization and Cross-Border Transfers](#194-data-localization-and-cross-border-transfers)
  - [19.5 Privacy by Design](#195-privacy-by-design)
- [20. Support & Maintenance](#20-support--maintenance)
  - [20.1 Customer Support Structure](#201-customer-support-structure)
  - [20.2 Maintenance Procedures](#202-maintenance-procedures)
  - [20.3 Support Metrics and KPIs](#203-support-metrics-and-kpis)
  - [20.4 Maintenance Windows and Communication](#204-maintenance-windows-and-communication)
- [21. Documentation & Training](#21-documentation--training)
  - [21.1 Technical Documentation](#211-technical-documentation)
  - [21.2 User Documentation](#212-user-documentation)
  - [21.3 Training Programs](#213-training-programs)
  - [21.4 Documentation Maintenance](#214-documentation-maintenance)

---

## 1. Project Overview

### 1.1 Application Architecture

**Platform Type:** Multi-platform Universal E-Commerce & Service Booking Platform

**Core Concept:**
AvyMart is a billion-user scalable platform that combines e-commerce and service booking capabilities with a unique UID/QR Code-based customer exclusivity system. The platform ensures customers see only their registered seller's store or service, creating a closed-loop ecosystem that eliminates marketplace competition.

**Architecture Pattern:**
- **Frontend:** Solito-based multi-platform applications (Web & Mobile) with shared codebase
- **Backend:** Medusa e-commerce backend + Motia workflow orchestration
- **Database:** Multi-tenant architecture with data isolation (PostgreSQL + MikroORM)
- **Communication:** RESTful APIs (Medusa Store/Admin APIs) with GraphQL support
- **Workflows:** Motia workflow orchestration for complex business processes
- **Real-time:** WebSocket connections for live updates (family carts, GPS tracking, chat)

**Key Architectural Principles:**
- **Multi-Tenancy:** Complete data isolation between sellers/service providers
- **UID-Based Routing:** Customer-seller relationship determines content visibility
- **Scalability:** Horizontal scaling capability for billion-user support
- **Performance:** Sub-100ms API responses with 99.99% uptime
- **Security:** Zero-trust architecture with end-to-end encryption

### 1.2 Core Business Logic

**UID/QR Code System:**
- Each seller/service provider generates unique UID codes
- Customers register using seller's UID/QR code
- Registration creates exclusive customer-seller relationship
- Customers can only see products/services from their registered sellers
- System prevents competitive shopping across multiple sellers

**Multi-Business Model Support:**
- **White Label:** Complete platform rebranding for enterprise clients
- **Regional Rental:** Territory-based platform rental with revenue sharing
- **Global Marketplace:** Multi-vendor marketplace with commission model

**Business Model Implementation Details:**

**White Label Solution:**

**White-Label Customization Engine:**

**Branding Configuration System:**
- **Logo Management:** Upload and manage logos (header, favicon, email templates, mobile app icons)
- **Color Scheme Engine:** Primary, secondary, accent color customization with color picker
- **Typography System:** Google Fonts integration with font family selection
- **CSS Injection:** Custom CSS injection for advanced styling (sandboxed for security)
- **Theme System:** Dark/light mode theme options with custom theme creation
- **Asset Management:** CDN-based asset hosting for white-label clients

**Configuration per Tenant:**
- **Tenant Isolation:** Complete data and configuration isolation per white-label client
- **Configuration Storage:** Store tenant configurations in database with JSONB columns
- **Configuration API:** RESTful API for tenant configuration management
- **Configuration Versioning:** Track configuration changes with version history
- **Configuration Templates:** Pre-built configuration templates for quick setup
- **Configuration Validation:** Validate configurations before deployment

**Functional Customization:**
- **Feature Toggle Management:** Enable/disable features per tenant via feature flags
- **Custom Workflow Definitions:** Define custom business workflows per tenant
- **Business Rule Configuration:** Configure business rules (pricing, discounts, policies)
- **Integration API Endpoints:** Tenant-specific API endpoints and webhooks
- **Family Group Customization:** Customize family group features per tenant
- **Delivery Network Integration:** Configure delivery network settings per tenant
- **Transportation Service Coordination:** Customize transportation services per tenant

**Deployment Automation for Multiple Branded Instances:**

**Multi-Instance Deployment:**
- **Infrastructure as Code:** Terraform/Bicep templates for automated infrastructure provisioning
- **Container Orchestration:** Kubernetes namespaces per white-label instance
- **Database Per Tenant:** Separate database or schema per tenant (optional)
- **Domain Management:** Custom domain assignment and SSL certificate automation
- **CDN Configuration:** Tenant-specific CDN configuration and asset delivery
- **Environment Variables:** Tenant-specific environment configuration

**Deployment Pipeline:**
1. **Configuration Validation:** Validate tenant configuration before deployment
2. **Infrastructure Provisioning:** Automated infrastructure setup via IaC
3. **Application Deployment:** Deploy application with tenant-specific configuration
4. **Database Migration:** Run database migrations for tenant setup
5. **Asset Deployment:** Deploy tenant-specific assets (logos, themes) to CDN
6. **DNS Configuration:** Automated DNS and SSL certificate setup
7. **Health Checks:** Automated health checks and smoke tests
8. **Rollback Capability:** Automated rollback on deployment failure

**Deployment Timeline:** 2-4 weeks for customization and deployment

**Regional Rental Model:**

**Territory / Region Management Model + Routing Logic:**

**Territory Definition:**
- **Geographic Boundaries:** Define territories by city, state, country, or custom polygons
- **Territory Hierarchy:** Hierarchical territory structure (country → state → city)
- **Territory Database:** Store territory definitions in database with geographic data
- **Geographic Queries:** Use PostGIS for geographic queries and boundary checks
- **Territory Assignment:** Assign exclusive territories to regional partners
- **Territory Validation:** Validate user location against assigned territories

**Routing Logic:**
- **Location Detection:** Detect user location via IP geolocation or GPS
- **Territory Resolution:** Resolve user's territory based on location
- **Access Control:** Route users to appropriate regional instance or filter data
- **Fallback Logic:** Default territory assignment when location cannot be determined
- **Multi-Territory Support:** Handle users with access to multiple territories
- **Territory Switching:** Allow users to switch between accessible territories

**Regional Access Control:**
- **Data Filtering:** Filter products, services, sellers by territory
- **Regional Pricing:** Territory-specific pricing and currency
- **Regional Content:** Territory-specific content and localization
- **Regional Delivery:** Territory-specific delivery network and options
- **Regional Compliance:** Territory-specific compliance and regulations

**Local Market Customization:**
- **Language Localization:** Territory-specific language settings
- **Currency Configuration:** Territory-specific currency and payment methods
- **Cultural Adaptation:** Territory-specific cultural adaptations (date formats, etc.)
- **Family Group Localization:** Localize family group features for territory
- **Regional Features:** Enable/disable features based on territory requirements

**Revenue Sharing Model:**
- **Tiered Commission Structure:** 5-15% commission based on transaction volume
- **Volume Tiers:** Define volume tiers and corresponding commission rates
- **Performance-Based Bonuses:** Additional bonuses for exceeding targets
- **Marketing Contribution:** Required marketing contribution from regional partners
- **Monthly Minimum Guarantees:** Minimum revenue guarantees for exclusivity
- **Transparent Revenue Tracking:** Real-time revenue tracking and reporting

**Commission Calculation Engine (Tiers, Percentages, Settlement Rules):**

**Commission Structure:**
- **Category-Based Rates:** Different commission rates per product/service category (5-20%)
- **Volume-Based Discounts:** Reduced commission rates for high-volume sellers
- **Tier System:** Seller tiers (Basic, Professional, Premium, Enterprise) with different rates
- **Performance-Based Incentives:** Bonus commissions for high-performing sellers
- **Featured Listing Fees:** Additional fees for featured product listings
- **Advertising Revenue Sharing:** Revenue sharing from advertising placements

**Commission Calculation Logic:**
- **Order Processing:** Calculate commission on order placement
- **Multi-Item Orders:** Calculate commission per item with category-specific rates
- **Discount Application:** Apply volume discounts based on seller's monthly volume
- **Tier-Based Rates:** Apply commission rate based on seller's current tier
- **Currency Conversion:** Handle multi-currency commission calculations
- **Tax Handling:** Separate commission from tax calculations

**Settlement Rules:**
- **Settlement Frequency:** Weekly, bi-weekly, or monthly settlement cycles
- **Minimum Payout:** Minimum commission amount before payout (e.g., ₹1000)
- **Payout Methods:** Bank transfer, UPI, PayPal, or other payment methods
- **Settlement Processing:** Automated settlement processing and payment initiation
- **Settlement Reports:** Detailed settlement reports with transaction breakdown
- **Dispute Resolution:** Handle commission disputes and adjustments
- **Hold Period:** Hold period for refunds and chargebacks before final settlement

**Multi-Tenant Billing + Subscription/License Handling:**

**Billing System Architecture:**
- **Subscription Management:** Manage subscriptions (Basic ₹2,407/month, Professional ₹8,217/month, Enterprise ₹24,817/month)
- **License Management:** Track and manage industry module licenses (₹16,517-₹82,917 one-time)
- **Usage-Based Billing:** Track usage metrics (API calls, storage, transactions) for billing
- **Billing Cycles:** Monthly, quarterly, or annual billing cycles
- **Proration:** Prorate charges for mid-cycle upgrades/downgrades
- **Invoice Generation:** Automated invoice generation and delivery

**Payment Processing:**
- **Payment Gateway Integration:** Stripe, PayPal, Razorpay integration for subscription payments
- **Recurring Payments:** Automated recurring payment processing
- **Payment Retry:** Automatic retry for failed payments with exponential backoff
- **Payment Methods:** Support multiple payment methods (credit card, UPI, bank transfer)
- **Payment Notifications:** Email/SMS notifications for payment success/failure
- **Refund Processing:** Automated refund processing for cancellations

**Subscription Management:**
- **Plan Management:** Create, update, cancel subscription plans
- **Plan Upgrades/Downgrades:** Handle plan changes with proration
- **Trial Periods:** Support free trial periods with automatic conversion
- **Grace Periods:** Grace period for failed payments before service suspension
- **Cancellation Handling:** Handle subscription cancellations and data retention
- **Renewal Management:** Automated subscription renewal processing

**License Management:**
- **License Types:** One-time licenses for industry modules
- **License Activation:** Activate licenses with unique license keys
- **License Validation:** Validate licenses on system startup and periodically
- **License Expiry:** Track license expiry and renewal requirements
- **License Transfer:** Handle license transfers between tenants
- **License Reporting:** Track license usage and compliance

**Billing Analytics:**
- **Revenue Tracking:** Track revenue by subscription tier, license type, region
- **Churn Analysis:** Analyze subscription churn and retention rates
- **Usage Analytics:** Track feature usage and correlate with billing
- **Forecasting:** Revenue forecasting based on subscription trends
- **Billing Reports:** Comprehensive billing and revenue reports

**Global E-Commerce Platform:**
- Multi-vendor marketplace architecture
- Seller tiers: Basic, Professional, Premium, Enterprise sellers
- Commission structure: Category-based rates (5-20%), volume-based discounts
- Performance-based incentives, featured listing fees, advertising revenue sharing
- Global operations: Multi-currency support (50+ currencies), multi-language platform (10+ languages)
- International shipping integration and cross-border tax calculation
- Regional compliance management
- Family group marketplace access
- Global delivery network integration
- Transportation service booking

**Family Group System:**
- Family groups with up to 8 members
- Hierarchical roles: Family Head, Adult, Teen, Child
- Shared shopping carts with approval workflows
- Real-time expense tracking and budget management
- Collaborative shopping experience

**Service Booking System:**
- Appointment scheduling with intelligent slot optimization
- Advance payment system (UPI/BNPL only)
- Refund policies based on cancellation timing
- GPS tracking for transportation services
- Multi-modal delivery network integration

### 1.3 Platform Scope

**Web Application (Solito):**
- Next.js 16+ with App Router
- Solito integration for code sharing with mobile
- Server-side rendering for SEO optimization
- Progressive Web App capabilities
- Responsive design for all screen sizes
- Real-time updates via WebSocket

**Mobile Application (Solito):**
- React Native 0.82 with New Architecture
- Expo SDK 54 with Expo Router
- Solito integration for code sharing with web
- iOS and Android native apps
- Offline functionality with sync
- Push notifications
- Native camera for QR code scanning
- GPS tracking integration

**Shared Codebase (Solito):**
- Unified components in `mobile-app/packages/app`
- Shared business logic and utilities
- Consistent navigation patterns
- Shared state management (Zustand, TanStack Query)
- Shared styling (TailwindCSS/NativeWind)
- Ready for future Next.js web app integration

**Excluded from Current Scope:**
- Desktop application (Electron) - Future phase
- Legacy browser support (IE11, older versions)

---

## 2. Technology Stack

### 2.1 Web Application Stack

**Core Framework:**
- **Next.js 16+:** React framework with App Router for optimal performance and SEO
- **Solito:** Monorepo integration for unified Next.js and Expo development
- **React 19:** UI library with concurrent features and automatic batching
- **TypeScript 5.0:** Type-safe development with strict mode enabled

**UI & Styling:**
- **TailwindCSS:** Utility-first CSS framework with custom design system
- **NativeWind:** TailwindCSS for React Native (shared styling)
- **Shadcn/UI:** Accessible component library built on Radix UI
- **Custom Design System:** 10 default themes with vendor-specific customization
- **Responsive Framework:** Mobile-first approach with breakpoints (320px, 768px, 1024px, 1440px+)

**State Management:**
- **Zustand:** Lightweight state management for client-side state
- **TanStack Query (React Query):** Server state management with caching and synchronization
- **React Context:** For theme and user preference management

**Form Handling:**
- **React Hook Form:** Performant form library with minimal re-renders
- **Zod:** Schema validation shared across frontend and backend
- **Form validation:** Real-time validation with helpful error messages

**Data Visualization:**
- **Chart.js:** Primary charting library for analytics dashboards
- **Recharts:** Alternative charting library for complex visualizations
- **Custom Charts:** Multiple graph types (bar, line, pie, area, scatter, heatmap)

**Internationalization:**
- **React i18next:** Multi-language support (20+ languages)
- **Language Detection:** Automatic based on browser, location, and UID context
- **RTL Support:** Right-to-left layout for Arabic and Hebrew

**Testing:**
- **Jest:** Unit and integration testing framework
- **React Testing Library:** Component testing with user-centric approach
- **Playwright:** End-to-end testing for web application

**Code Quality:**
- **ESLint:** Code linting with custom rules
- **Prettier:** Code formatting
- **Husky:** Git hooks for pre-commit checks
- **TypeScript Strict Mode:** Type safety enforcement

### 2.2 Mobile Application Stack

**Core Framework:**
- **React Native 0.82:** Cross-platform mobile framework with New Architecture
- **Expo SDK 54:** Development platform with managed workflow
- **Solito:** Monorepo integration for unified Next.js and Expo development
- **Expo Router:** File-based routing for navigation (shared with Solito)
- **TypeScript 5.0:** Type-safe mobile development

**UI Components:**
- **NativeWind:** TailwindCSS for React Native (shared with web via Solito)
- **React Native Paper:** Material Design components (optional)
- **React Native Reanimated:** Smooth animations and gestures
- **React Native Gesture Handler:** Native gesture recognition

**Navigation:**
- **Expo Router:** File-based routing with deep linking support (Solito integration)
- **Solito Navigation:** Unified navigation between web and mobile
- **Stack Navigation:** For hierarchical navigation flows
- **Tab Navigation:** For main app sections
- **Deep Linking:** UID/QR code scanning integration

**State Management:**
- **Zustand:** Lightweight state management (shared with web via Solito)
- **TanStack Query:** Server state synchronization (shared with web)
- **MMKV:** Fast key-value storage for offline data
- **React Context:** Theme and user preference management

**Shared Code with Web:**
- **Solito Packages:** Shared components, hooks, and utilities
- **Unified API Client:** Shared API client between platforms
- **Shared Types:** TypeScript types shared across platforms
- **Shared Validation:** Zod schemas shared with backend

**Native Modules:**
- **Camera Module:** QR code scanning functionality
- **GPS Module:** Location tracking and navigation
- **Push Notifications:** Expo Notifications with Firebase
- **Biometric Auth:** Face ID, Touch ID, Fingerprint support
- **File System:** Document and image handling

**Offline Support:**
- **MMKV Storage:** Fast local storage for cached data
- **TanStack Query Persistence:** Query cache persistence
- **Queue System:** Offline request queuing and sync
- **Conflict Resolution:** Data synchronization strategies

**Testing:**
- **Jest:** Unit testing
- **React Native Testing Library:** Component testing
- **Detox:** End-to-end testing for mobile apps
- **Appium:** Cross-platform mobile testing (optional)

**Build & Deployment:**
- **Expo Application Services (EAS):** Cloud build service
- **EAS Build:** iOS and Android native builds
- **EAS Submit:** App store submission automation
- **Code Signing:** Automated certificate management

### 2.3 Backend Stack

**E-Commerce Backend (Medusa):**
- **Medusa.js:** Open-source e-commerce backend framework
- **Node.js 24.11.0 LTS:** JavaScript runtime
- **TypeScript 5.9.3:** Type-safe backend development
- **PostgreSQL 17:** Primary relational database for Medusa
- **Medusa Modules:** Extensible module system for custom features
- **Medusa Admin API:** Admin dashboard API endpoints
- **Medusa Store API:** Customer-facing store API endpoints
- **Medusa Workflows:** Built-in workflow system for order processing

**Workflow Orchestration (Motia):**
- **Motia:** Workflow orchestration and automation platform
- **Node.js 24.11.0 LTS:** JavaScript runtime
- **TypeScript 5.9.3:** Type-safe workflow development
- **Workflow Engine:** Visual and code-based workflow creation
- **Node System:** Reusable workflow nodes for common operations
- **HTTP Triggers:** HTTP-based workflow triggers
- **Step Execution:** Modular step-based workflow execution
- **Metrics & Tracing:** OpenTelemetry integration for monitoring

**API Design:**
- **RESTful APIs:** Resource-based URL structure (Medusa Store/Admin APIs)
- **GraphQL:** Medusa GraphQL support for complex queries
- **Workflow APIs:** Motia HTTP-based workflow endpoints
- **JSON API Specification:** Standardized API responses
- **API Gateway:** Unified API gateway for routing

**Authentication & Security:**
- **JWT (JSON Web Tokens):** Stateless authentication (Medusa)
- **Refresh Tokens:** Secure token rotation mechanism
- **OAuth 2.0:** Social media login integration
- **bcrypt:** Password hashing
- **Helmet:** Security headers middleware
- **Rate Limiting:** Request throttling and DDoS protection
- **Workflow Authentication:** Motia workflow authentication and authorization

**Database & ORM:**
- **PostgreSQL 17:** Primary relational database (Medusa)
- **MikroORM:** Medusa's ORM for database operations
- **Database Migrations:** Medusa migration system
- **Connection Pooling:** Database connection management
- **Multi-tenant Support:** Tenant-based data isolation

**Caching:**
- **Redis 8.2 Cluster:** High-performance caching layer
- **Redis Sessions:** Session storage
- **Medusa Cache:** Medusa's built-in caching mechanisms
- **Cache Strategies:** Write-through, write-back, cache-aside patterns
- **TTL Management:** Time-to-live for cached data

**Search & Indexing:**
- **Elasticsearch:** Full-text search and product discovery
- **Medusa Search:** Medusa's search plugin system
- **Search Analytics:** Search query analytics and optimization
- **Faceted Search:** Multi-dimensional filtering

**File Storage:**
- **Azure Blob Storage:** Media and document storage
- **Medusa File Service:** Medusa's file upload service
- **CDN Integration:** Cloudflare for global content delivery
- **Image Processing:** Resize, compress, format conversion
- **Virus Scanning:** File upload security

**Event System:**
- **Medusa Events:** Built-in event system for e-commerce operations
- **Event Subscribers:** Event-driven architecture for business logic
- **Workflow Events:** Motia workflow event triggers
- **Pub/Sub Pattern:** Real-time event distribution

**Background Jobs:**
- **Medusa Jobs:** Built-in job queue system
- **Bull Queue:** Redis-based job queue (if needed)
- **Cron Jobs:** Scheduled task execution
- **Workflow Jobs:** Motia workflow background execution
- **Email Queue:** Asynchronous email sending
- **Report Generation:** Background report processing

**Monitoring & Logging:**
- **Winston:** Structured logging
- **OpenTelemetry:** Distributed tracing (Motia integration)
- **Prometheus:** Metrics collection
- **Grafana:** Metrics visualization
- **Azure Application Insights:** Application monitoring
- **Error Tracking:** Sentry integration

### 2.4 Infrastructure Stack

**Cloud Provider:**
- **AWS (Primary):** EC2, RDS, ElastiCache, S3, CloudFront, Route 53, ECS/EKS, Lambda, CloudWatch
- **Azure (Secondary):** Cosmos DB, Blob Storage, Application Insights
- **Cloudflare:** CDN, DDoS protection, edge computing

**Containerization:**
- **Docker:** Container runtime with multi-stage builds
- **Docker Compose:** Local development environment
- **Container Registry:** Docker Hub or AWS ECR

**Orchestration:**
- **Kubernetes (Azure AKS):** Container orchestration
- **Auto-scaling:** Horizontal Pod Autoscaler (HPA)
- **Service Mesh:** Istio for service-to-service communication
- **Helm Charts:** Application deployment and configuration

**CI/CD:**
- **GitHub Actions:** Continuous integration and deployment
- **Turborepo:** Monorepo build caching and task orchestration
- **Matrix Builds:** Multi-platform build support
- **Automated Testing:** Test execution in CI pipeline
- **Deployment Automation:** Staging and production deployments

**Monitoring & Observability:**
- **Prometheus:** Metrics collection
- **Grafana:** Metrics visualization and dashboards
- **AlertManager:** Alert routing and notification
- **ELK Stack:** Log aggregation and analysis
- **New Relic:** Application Performance Monitoring (APM)

**Security Infrastructure:**
- **Azure Key Vault:** Secrets management
- **AWS KMS:** Key management service
- **Azure WAF:** Web Application Firewall
- **DDoS Protection:** Cloudflare and Azure DDoS Protection
- **SSL/TLS:** Let's Encrypt for certificate management

### 2.5 Development Tools

**Version Control:**
- **Git:** Source code management
- **GitHub:** Repository hosting and collaboration
- **Git Flow:** Branching strategy
- **Semantic Versioning:** Version numbering (MAJOR.MINOR.PATCH)

**Package Management:**
- **npm/yarn/pnpm:** Node.js package management
- **Monorepo:** Turborepo for multi-package management
- **Workspace Management:** Shared dependencies and code

**Code Quality:**
- **ESLint:** JavaScript/TypeScript linting
- **Prettier:** Code formatting
- **Husky:** Git hooks
- **lint-staged:** Pre-commit linting
- **SonarQube:** Code quality analysis (optional)

**Documentation:**
- **TypeDoc:** TypeScript documentation generation
- **Storybook:** Component documentation and testing
- **OpenAPI/Swagger:** API documentation
- **Markdown:** Project documentation

**Development Utilities:**
- **Postman/Insomnia:** API testing
- **DBeaver/TablePlus:** Database management
- **Redis Insight:** Redis management
- **VS Code Extensions:** Development environment setup

---

## 3. Development Environment Setup

### 3.1 Prerequisites

**Required Software:**
- **Node.js:** Version 24.11.0 LTS or higher
- **npm/yarn/pnpm:** Latest stable version
- **Git:** Version 2.30+ for version control
- **Docker Desktop:** For local database and services
- **PostgreSQL:** Version 17 (or use Docker)
- **Redis:** Version 8.2 (or use Docker)

**For Web Development:**
- **VS Code:** Recommended IDE with extensions
- **Chrome/Edge:** For development and debugging
- **Node.js:** Runtime environment

**For Mobile Development:**
- **Xcode:** For iOS development (macOS only)
- **Android Studio:** For Android development
- **Expo CLI:** For Expo development workflow
- **iOS Simulator:** For iOS testing
- **Android Emulator:** For Android testing

**Optional Tools:**
- **Postman:** API testing and documentation
- **DBeaver:** Database management
- **Redis Insight:** Redis management
- **Figma:** Design file access

### 3.2 Project Structure

**Monorepo Structure (Solito + Medusa + Motia):**
```
avy-mart-platform/
├── mobile-app/                # Solito-enhanced mobile app (Expo + shared code)
│   ├── src/                   # Mobile app source (from mobile-app-project-structure)
│   │   ├── app/               # Expo Router pages (Solito integration)
│   │   │   ├── (app)/         # App routes
│   │   │   │   ├── _layout.tsx
│   │   │   │   ├── index.tsx
│   │   │   │   ├── settings.tsx
│   │   │   │   └── style.tsx
│   │   │   ├── _layout.tsx    # Root layout
│   │   │   ├── feed/          # Feed routes
│   │   │   │   ├── [id].tsx
│   │   │   │   └── add-post.tsx
│   │   │   ├── login.tsx      # Login screen
│   │   │   └── onboarding.tsx # Onboarding
│   │   ├── api/               # API client (Solito shared patterns)
│   │   │   ├── common/        # Common API utilities
│   │   │   │   ├── api-provider.tsx
│   │   │   │   ├── client.tsx
│   │   │   │   ├── index.tsx
│   │   │   │   └── utils.tsx
│   │   │   ├── index.tsx
│   │   │   ├── posts/         # Example API module
│   │   │   │   ├── index.ts
│   │   │   │   ├── types.ts
│   │   │   │   ├── use-add-post.ts
│   │   │   │   ├── use-post.ts
│   │   │   │   └── use-posts.ts
│   │   │   └── types.ts
│   │   ├── components/        # React Native components
│   │   │   ├── buttons.tsx
│   │   │   ├── card.tsx
│   │   │   ├── colors.tsx
│   │   │   ├── cover.tsx
│   │   │   ├── inputs.tsx
│   │   │   ├── login-form.tsx
│   │   │   ├── settings/       # Settings components
│   │   │   │   ├── item.tsx
│   │   │   │   ├── items-container.tsx
│   │   │   │   ├── language-item.tsx
│   │   │   │   └── theme-item.tsx
│   │   │   ├── title.tsx
│   │   │   ├── typography.tsx
│   │   │   └── ui/            # UI components (Solito-compatible)
│   │   │       ├── button.tsx
│   │   │       ├── checkbox.tsx
│   │   │       ├── input.tsx
│   │   │       ├── modal.tsx
│   │   │       ├── select.tsx
│   │   │       ├── text.tsx
│   │   │       └── icons/     # Icon components
│   │   ├── lib/               # Libraries
│   │   │   ├── auth/          # Authentication
│   │   │   │   ├── index.tsx
│   │   │   │   └── utils.tsx
│   │   │   ├── hooks/         # Custom hooks
│   │   │   │   ├── index.tsx
│   │   │   │   ├── use-is-first-time.tsx
│   │   │   │   └── use-selected-theme.tsx
│   │   │   ├── i18n/          # Internationalization
│   │   │   │   ├── index.tsx
│   │   │   │   ├── react-i18next.d.ts
│   │   │   │   ├── resources.ts
│   │   │   │   ├── types.ts
│   │   │   │   └── utils.tsx
│   │   │   ├── storage.tsx     # Storage utilities
│   │   │   ├── test-utils.tsx
│   │   │   ├── use-theme-config.tsx
│   │   │   └── utils.ts
│   │   ├── screens/           # Screen components
│   │   │   ├── OrderTrackingScreen.tsx
│   │   │   └── ProductScreen.tsx
│   │   ├── services/          # Business services
│   │   │   └── api.ts
│   │   ├── translations/      # i18n translations
│   │   │   ├── ar.json
│   │   │   └── en.json
│   │   └── types/             # TypeScript types
│   │       └── index.ts
│   ├── packages/              # Solito shared packages (within mobile-app)
│   │   └── app/               # Shared app code (Solito pattern)
│   │       ├── components/    # Shared React components
│   │       │   ├── button.tsx  # Shared button (works on web & mobile)
│   │       │   ├── card.tsx
│   │       │   ├── typography.tsx
│   │       │   └── index.ts
│   │       ├── features/       # Feature modules
│   │       │   ├── home/       # Home feature
│   │       │   │   └── screen.tsx
│   │       │   └── user/       # User feature
│   │       │       └── detail-screen.tsx
│   │       ├── navigation/     # Navigation configuration
│   │       │   └── native/     # Native navigation
│   │       ├── provider/       # Context providers
│   │       │   ├── index.tsx   # Main provider
│   │       │   ├── navigation/ # Navigation provider
│   │       │   └── safe-area/  # Safe area provider
│   │       │       ├── index.native.tsx
│   │       │       ├── index.tsx
│   │       │       ├── use-safe-area.native.ts
│   │       │       └── use-safe-area.ts
│   │       ├── utils/          # Utility functions
│   │       │   └── cn.ts       # Class name utility
│   │       ├── rnw-overrides.d.ts
│   │       ├── index.ts
│   │       └── package.json
│   ├── __mocks__/             # Jest mocks
│   │   ├── @gorhom/
│   │   ├── expo-localization.ts
│   │   ├── moti.ts
│   │   ├── react-native-gesture-handler.ts
│   │   └── react-native-keyboard-controller.ts
│   ├── assets/                # Assets
│   │   └── fonts/
│   │       └── Inter.ttf
│   ├── prompts/               # AI prompts for development
│   ├── scripts/               # Utility scripts
│   │   ├── genrate-apk-and-install
│   │   └── i18next-syntax-validation.js
│   ├── app.config.ts          # Expo configuration
│   ├── eas.json               # EAS Build configuration
│   ├── babel.config.js         # Babel configuration
│   ├── metro.config.js         # Metro bundler config
│   ├── tailwind.config.js      # NativeWind configuration
│   ├── jest.config.js          # Jest configuration
│   ├── tsconfig.json           # TypeScript configuration
│   ├── package.json            # Dependencies
│   └── global.css              # Global styles
│
├── medusa-backend/            # Medusa e-commerce backend
│   ├── src/
│   │   ├── admin/             # Admin customizations
│   │   │   └── custom/        # Custom admin routes
│   │   ├── api/               # API routes
│   │   │   ├── admin/         # Admin API routes
│   │   │   │   └── custom/    # Custom admin routes
│   │   │   └── store/         # Store API routes
│   │   │       └── custom/    # Custom store routes
│   │   ├── jobs/              # Background jobs
│   │   ├── links/             # Link modules
│   │   ├── modules/           # Custom Medusa modules
│   │   ├── scripts/           # Utility scripts
│   │   │   └── seed.ts        # Database seeding
│   │   ├── services/          # Business logic services
│   │   │   ├── order.service.ts
│   │   │   └── product.service.ts
│   │   ├── subscribers/       # Event subscribers
│   │   │   ├── order.subscriber.ts
│   │   │   ├── product.subscriber.ts
│   │   │   └── product-updated.subscriber.ts
│   │   └── workflows/         # Medusa workflows
│   ├── medusa-config.ts       # Medusa configuration
│   ├── Dockerfile             # Docker configuration
│   ├── docker-compose.yml     # Local development
│   └── package.json           # Dependencies
│
├── motia-backend/             # Motia workflow orchestration
│   ├── src/
│   │   ├── AppRoutes.ts       # Application routes
│   │   ├── Nodes.ts           # Node definitions
│   │   ├── Workflows.ts       # Workflow definitions
│   │   ├── index.ts           # Entry point
│   │   ├── nodes/             # Custom workflow nodes
│   │   ├── runner/            # Workflow execution engine
│   │   │   ├── HttpTrigger.ts # HTTP trigger handler
│   │   │   ├── MessageDecode.ts
│   │   │   ├── Util.ts        # Utility functions
│   │   │   ├── metrics/       # OpenTelemetry metrics
│   │   │   │   ├── opentelemetry_metrics.ts
│   │   │   │   └── opentelemetry_traces.ts
│   │   │   └── types/         # Type definitions
│   │   ├── steps/             # Workflow steps
│   │   │   ├── ai-service.step.ts
│   │   │   ├── api-gateway.step.ts
│   │   │   ├── health-check.step.ts
│   │   │   ├── medusa-client.step.ts
│   │   │   ├── order-processor.step.ts
│   │   │   └── webhook-handler.step.ts
│   │   └── workflows/         # Workflow definitions
│   │       ├── countries-helper.ts
│   │       └── empty.ts
│   ├── workflows/             # Workflow files (JSON/YAML/TOML)
│   │   ├── json/              # JSON workflows
│   │   ├── toml/              # TOML workflows
│   │   └── yaml/              # YAML workflows
│   ├── infra/                 # Infrastructure configs
│   │   ├── docker-compose.yml # Docker setup
│   │   └── metrics/           # Monitoring stack
│   │       ├── prometheus.yml
│   │       ├── grafana/
│   │       └── loki-config.yaml
│   ├── Dockerfile             # Docker configuration
│   ├── Dockerfile.dev         # Development Docker
│   └── package.json           # Dependencies
│
├── azure-infrastructure/      # Azure deployment configs
│   ├── main.bicep             # Bicep templates
│   ├── deploy.sh              # Deployment script
│   └── setup-secrets.sh       # Secrets setup
│
├── nginx/                     # Nginx configuration
│   ├── nginx.conf             # Nginx config
│   └── ssl/                   # SSL certificates
│
├── scripts/                   # Utility scripts
│   └── init-db.sql            # Database initialization
│
├── docker-compose.yml         # Root docker-compose
├── setup.sh                   # Setup script (Linux/Mac)
├── setup.ps1                  # Setup script (Windows)
├── package.json               # Root package.json
├── turbo.json                 # Turborepo configuration
├── tsconfig.json              # Root TypeScript config
└── README.md                  # Project README
```

**Important Notes on Structure:**

1. **Mobile-App Solito Integration:**
   - The `mobile-app/` directory contains the Solito-enhanced mobile application
   - Structure combines: `mobile-app-project-structure.md` (solid foundation) + `solito-project-structure.md` (code sharing)
   - `mobile-app/src/` contains mobile-specific code (Expo Router, React Native components)
   - `mobile-app/packages/app/` contains Solito shared code ready for web app integration
   - When Next.js web app is added, it will reference `mobile-app/packages/app/` for shared components

2. **Code Sharing Strategy:**
   - Mobile-specific code: `mobile-app/src/` (components, screens, services)
   - Shared code: `mobile-app/packages/app/` (components, features, providers, utils)
   - Future web app will import from `mobile-app/packages/app/` for shared components
   - This structure enables seamless code sharing when the Next.js app is added

3. **Backend Services:**
   - `medusa-backend/` handles all e-commerce operations
   - `motia-backend/` handles workflow orchestration
   - Both services are independent and communicate via HTTP/events

### 3.3 Environment Configuration

**Environment Variables Structure:**

**Web Application (.env.local):**
- `NEXT_PUBLIC_API_URL`: Backend API base URL
- `NEXT_PUBLIC_APP_URL`: Web application URL
- `NEXT_PUBLIC_ENVIRONMENT`: Environment (development/staging/production)
- `NEXT_PUBLIC_GOOGLE_MAPS_API_KEY`: Google Maps API key
- `NEXT_PUBLIC_ANALYTICS_ID`: Analytics tracking ID

**Mobile Application (.env):**
- `EXPO_PUBLIC_API_URL`: Backend API base URL
- `EXPO_PUBLIC_ENVIRONMENT`: Environment
- `EXPO_PUBLIC_GOOGLE_MAPS_API_KEY`: Google Maps API key
- `EXPO_PUBLIC_FIREBASE_CONFIG`: Firebase configuration

**Medusa Backend (.env):**
- `NODE_ENV`: Environment
- `DATABASE_URL`: PostgreSQL connection string
- `REDIS_URL`: Redis connection string
- `JWT_SECRET`: JWT signing secret
- `COOKIE_SECRET`: Cookie encryption secret
- `MEDUSA_BACKEND_URL`: Medusa backend URL
- `MEDUSA_ADMIN_ONBOARDING_TYPE`: Admin onboarding type
- `MEDUSA_ADMIN_ONBOARDING_NEXTJS_DIRECTORY`: Next.js admin directory
- `STRIPE_API_KEY`: Stripe payment key
- `PAYPAL_CLIENT_ID`: PayPal credentials
- `UPI_MERCHANT_ID`: UPI merchant ID
- `BNPL_API_KEY`: BNPL provider key
- `AZURE_STORAGE_CONNECTION_STRING`: Azure Blob Storage
- `TWILIO_ACCOUNT_SID`: Twilio SMS credentials
- `SENDGRID_API_KEY`: Email service key
- `FIREBASE_SERVER_KEY`: Firebase push notifications

**Motia Backend (.env):**
- `NODE_ENV`: Environment
- `PORT`: Motia server port
- `MOTIA_WORKFLOW_DIR`: Workflow files directory
- `MOTIA_METRICS_ENABLED`: Enable OpenTelemetry metrics
- `MOTIA_TRACING_ENABLED`: Enable OpenTelemetry tracing
- `MEDUSA_API_URL`: Medusa API URL for integration
- `REDIS_URL`: Redis connection string (for workflow state)

**Environment-Specific Configurations:**
- Development: Local services, mock external APIs, debug logging
- Staging: Production-like setup, test payment gateways, full monitoring
- Production: Multi-region deployment, production credentials, optimized performance

### 3.4 Local Development Setup

**Initial Setup Steps:**

1. **Clone Repository:**
   - Clone the monorepo from GitHub
   - Install dependencies using package manager
   - Set up Git hooks with Husky

2. **Database Setup:**
   - Start PostgreSQL using Docker or local installation
   - Run Prisma migrations to create database schema
   - Seed database with initial data (optional)

3. **Redis Setup:**
   - Start Redis using Docker or local installation
   - Verify Redis connection

4. **Medusa Backend Setup:**
   - Navigate to medusa-backend directory
   - Install dependencies
   - Copy .env.example to .env and configure
   - Run database migrations: `npx medusa migrations run`
   - Seed database (optional): `npm run seed`
   - Start development server: `npm run dev`

5. **Motia Backend Setup:**
   - Navigate to motia-backend directory
   - Install dependencies
   - Copy .env.example to .env and configure
   - Start development server: `npm run dev`

6. **Mobile Application Setup (Solito-Enhanced):**
   - Navigate to mobile-app directory
   - Install dependencies
   - Copy .env.example to .env
   - Start Expo development server: `npm start`
   - Run on iOS simulator or Android emulator
   - Note: The mobile-app contains Solito integration for future web app code sharing

**Development Workflow:**
- Use feature branches for new development
- Run tests before committing
- Follow code review process
- Use development environment for testing
- Staging environment for integration testing

---

## 4. System Architecture

### 4.1 Multi-Platform Architecture

**Architecture Overview:**
The platform follows a multi-platform architecture where Web and Mobile applications share business logic while maintaining platform-specific optimizations. Both platforms communicate with the same backend API, ensuring consistency across user experiences.

**Platform Communication:**
- **Web:** HTTP/HTTPS requests with WebSocket for real-time features
- **Mobile:** HTTP/HTTPS requests with WebSocket for real-time features
- **Backend:** Unified API layer serving both platforms
- **Real-time:** WebSocket connections for live updates (family carts, GPS, chat)

**Shared Business Logic:**
- API client libraries shared between platforms
- Validation schemas (Zod) shared across frontend and backend
- Type definitions shared via TypeScript
- Utility functions in shared packages
- Constants and configuration shared

**Platform-Specific Optimizations:**
- **Web:** Server-side rendering, SEO optimization, progressive web app features
- **Mobile:** Native modules, offline support, push notifications, biometric auth

### 4.2 Backend Architecture (Medusa + Motia)

**Backend Service Breakdown:**

**Medusa E-Commerce Backend:**
- **Store API:** Customer-facing e-commerce API (products, cart, orders, checkout)
- **Admin API:** Admin dashboard API (product management, order management, analytics)
- **Core Services:** Product service, order service, cart service, payment service
- **Custom Services:** UID service, family group service, transportation service
- **Event Subscribers:** Order processing, inventory management, notifications
- **Workflows:** Order processing workflows, payment workflows

**Motia Workflow Orchestration:**
- **Workflow Engine:** Central workflow execution and orchestration
- **HTTP Triggers:** HTTP-based workflow triggers
- **Workflow Steps:** Modular steps for Medusa integration, API calls, data processing
- **Node System:** Reusable workflow nodes
- **Metrics & Monitoring:** OpenTelemetry integration for workflow observability

**Service Communication:**
- **Synchronous:** HTTP/REST for real-time operations (Medusa APIs)
- **Asynchronous:** Medusa events and jobs for event-driven communication
- **Workflow Integration:** Motia workflows triggered by Medusa events
- **API Gateway:** Nginx for routing and load balancing
- **Circuit Breakers:** Resilience patterns for service failures

### 4.3 Data Flow Architecture

**Request Flow:**
1. Client (Web/Mobile via Solito) sends request to Nginx API Gateway
2. Nginx routes request to Medusa Store API or Admin API
3. Medusa authenticates and authorizes request
4. Medusa service processes request using business logic
5. MikroORM data access layer queries PostgreSQL database or Redis cache
6. Response returned through gateway to client
7. Optionally, Medusa events trigger Motia workflows for complex processing

**Real-time Data Flow:**
1. Client (Web/Mobile via Solito) establishes WebSocket connection
2. Server subscribes client to relevant channels (family cart, GPS tracking, chat)
3. Medusa events published for state changes (orders, products, etc.)
4. Event subscribers process events and trigger workflows
5. Motia workflows execute for complex processing
6. Updates pushed to connected clients via WebSocket

**Caching Strategy:**
- **L1 Cache:** Application-level in-memory cache
- **L2 Cache:** Redis cluster for distributed caching
- **CDN Cache:** Cloudflare for static assets and API responses
- **Cache Invalidation:** Event-driven cache invalidation

### 4.4 Security Architecture

**Authentication Flow:**
1. User provides credentials (email/phone + password or social login)
2. Backend validates credentials
3. JWT access token and refresh token generated
4. Tokens stored securely (httpOnly cookies for web, secure storage for mobile)
5. Subsequent requests include token in Authorization header
6. Token validated on each request
7. Refresh token used to obtain new access token when expired

**Authorization Flow:**
1. Request includes JWT token
2. Token validated and decoded
3. User roles and permissions retrieved
4. Resource access checked against permissions
5. UID-based access control applied (if applicable)
6. Request allowed or denied based on authorization

**Data Security:**
- **Encryption at Rest:** AES-256 encryption for sensitive data
- **Encryption in Transit:** TLS 1.3 for all communications
- **Field-Level Encryption:** PII data encrypted at application level
- **Key Management:** Azure Key Vault for key storage and rotation

**Multi-Tenant Security:**
- **Data Isolation:** Row-level security based on tenant ID
- **Query Filtering:** Automatic tenant filtering in all queries
- **Access Control:** Tenant-based permission enforcement
- **Audit Logging:** Complete activity tracking per tenant

---

## 5. Core Features & Implementation

### 5.1 User Management & Authentication

**Feature Overview:**
Comprehensive user management system supporting multiple registration methods, authentication mechanisms, and user profile management with family account integration.

**Registration Methods:**
- **Email Registration:** Standard email and password registration
- **Phone Registration:** Phone number and OTP verification
- **Social Login:** OAuth 2.0 integration with Google, Facebook, Apple
- **UID Registration:** Registration with seller's UID/QR code for exclusive access

**Authentication Mechanisms:**
- **Password Authentication:** Secure password hashing with bcrypt
- **Multi-Factor Authentication (MFA):** SMS OTP, TOTP (Google Authenticator), Biometric (mobile)
- **Session Management:** JWT-based stateless sessions with refresh tokens
- **Social Authentication:** OAuth 2.0 flow for social media login

**User Profile Management:**
- **Profile Information:** Name, email, phone, address, preferences
- **Profile Picture:** Image upload with processing and storage
- **Preferences:** Language, timezone, notification preferences
- **Privacy Settings:** Data sharing and visibility controls

**Family Account Integration:**
- **Parent Account Creation:** Family head account setup
- **Child Account Management:** Adding and managing child accounts
- **Role Assignment:** Family Head, Adult, Teen, Child roles
- **Permission Configuration:** Spending limits and approval requirements

**Implementation Requirements:**
- Implement JWT token generation and validation
- Create password hashing and verification functions
- Build OAuth 2.0 integration for social login
- Develop MFA flow with OTP generation and verification
- Create user profile CRUD operations
- Implement family account relationship management
- Build session management with token refresh
- Create password reset and account recovery flows

**Security Considerations:**
- Password complexity requirements (minimum 8 characters, complexity rules)
- Account lockout after 5 failed login attempts (15-minute lockout)
- Session timeout after 30 minutes of inactivity
- MFA mandatory for administrators
- Rate limiting on authentication endpoints (1000 requests/hour/user)

### 5.2 UID/QR Code System

**Feature Overview:**
Core system enabling customer exclusivity through unique UID/QR codes that create exclusive relationships between customers and sellers/service providers.

**UID Generation:**
- **Code Format:** Unique alphanumeric codes (e.g., "AVY-ABC-123-XYZ")
- **QR Code Generation:** Scannable QR codes with embedded UID
- **Uniqueness Validation:** Database-level uniqueness constraints
- **Expiration Management:** Optional expiration dates for codes
- **Bulk Generation:** Generate multiple codes for sellers

**UID Distribution:**
- **Digital Distribution:** Downloadable QR codes and UID strings
- **Print-Ready Formats:** PDF, PNG, SVG formats for printing
- **Marketing Materials:** Branded QR code templates
- **Analytics Tracking:** Track code distribution channels

**UID Verification:**
- **Scanning:** Mobile camera QR code scanning
- **Manual Entry:** UID code manual input option
- **Validation:** Real-time code validation against database
- **Seller Lookup:** Retrieve seller/service provider information
- **Relationship Creation:** Establish customer-seller relationship

**Customer Onboarding:**
- **Registration Flow:** UID-based registration workflow
- **Relationship Establishment:** Link customer to seller
- **Access Configuration:** Configure exclusive access permissions
- **Welcome Experience:** Personalized onboarding for UID customers

**UID Analytics:**
- **Usage Tracking:** Track code scans and verifications
- **Customer Acquisition:** Monitor customer onboarding through codes
- **Conversion Metrics:** Track registration to purchase conversion
- **Geographic Distribution:** Analyze code usage by location
- **Performance Dashboards:** Real-time analytics for sellers

**Implementation Requirements:**
- Create UID generation algorithm with uniqueness guarantee
- Implement QR code generation library integration
- Build UID validation service with Redis caching
- Develop customer-seller relationship management
- Create UID analytics collection and reporting
- Implement fraud detection for UID system
- Build code expiration and renewal management
- Create distribution tools and download functionality

**Performance Requirements:**
- UID lookup: <50ms response time (95th percentile)
- QR code generation: <100ms per code
- Verification: <50ms including database lookup
- Redis caching: Sub-millisecond cache hits

### 5.3 E-Commerce Module

**Feature Overview:**
Complete e-commerce functionality including product catalog, shopping cart, checkout, order management, and inventory tracking with UID-based personalization.

**Product Catalog:**
- **Product Management:** Create, update, delete products with variants
- **Category System:** Hierarchical category structure
- **Product Attributes:** Industry-specific attributes (automotive, medical, etc.)
- **Media Management:** Image and video uploads with processing
- **Inventory Tracking:** Real-time stock levels and availability
- **Pricing:** Base pricing with UID-based discounts
- **Visibility Control:** UID-based product visibility filtering

**Product Search & Discovery:**
- **Full-Text Search:** Elasticsearch-powered search
- **Advanced Filtering:** Category, price, brand, rating, attributes
- **Sorting Options:** Price, popularity, rating, newest
- **Faceted Navigation:** Multi-dimensional filtering
- **Search Analytics:** Track search queries and results

**Elasticsearch Implementation Details:**

**Index and Mapping Schema Design:**

**Product Index (`products`):**
- **Mapping Fields:**
  - `id` (keyword): Product unique identifier
  - `title` (text with analyzer): Product name with full-text search
  - `description` (text): Product description with stemming
  - `category` (keyword): Category hierarchy
  - `seller_id` (keyword): Seller identifier for UID filtering
  - `price` (float): Product price for range queries
  - `in_stock` (boolean): Stock availability
  - `attributes` (nested): Industry-specific attributes (VIN, medical specs, etc.)
  - `tags` (keyword): Product tags for filtering
  - `rating` (float): Average rating
  - `review_count` (integer): Number of reviews
  - `created_at` (date): Product creation timestamp
  - `updated_at` (date): Last update timestamp
- **Analyzers:** Custom analyzers for multi-language support, stemming, synonyms
- **Index Settings:** Shards (5), Replicas (1), Refresh interval (1s for real-time)

**User Index (`users`):**
- **Mapping Fields:**
  - `user_id` (keyword): User unique identifier
  - `email` (keyword): Email address (exact match)
  - `phone` (keyword): Phone number
  - `name` (text): User name with search capability
  - `role` (keyword): User role (customer, seller, admin)
  - `uid_relationships` (nested): UID-seller relationships
  - `location` (geo_point): User location for geographic queries
  - `preferences` (object): User preferences and settings

**Service Index (`services`):**
- **Mapping Fields:**
  - `service_id` (keyword): Service unique identifier
  - `name` (text): Service name
  - `category` (keyword): Service category
  - `provider_id` (keyword): Service provider identifier
  - `location` (geo_point): Service location
  - `availability` (object): Time slots and availability
  - `rating` (float): Service rating
  - `price_range` (float_range): Service pricing range

**Order Index (`orders`):**
- **Mapping Fields:**
  - `order_id` (keyword): Order unique identifier
  - `user_id` (keyword): Customer identifier
  - `seller_id` (keyword): Seller identifier
  - `status` (keyword): Order status
  - `total_amount` (float): Order total
  - `created_at` (date): Order creation timestamp
  - `items` (nested): Order items with product details

**Real-time Indexing Pipeline (DB → ES):**

**Indexing Architecture:**
- **Change Data Capture (CDC):** Monitor PostgreSQL changes using logical replication or triggers
- **Event-Driven Indexing:** Trigger Elasticsearch updates on database events (INSERT, UPDATE, DELETE)
- **Message Queue:** Use Kafka or Redis Streams for reliable event delivery
- **Indexing Service:** Dedicated microservice for Elasticsearch operations
- **Batch Processing:** Bulk indexing for initial data load and bulk updates

**Indexing Workflow:**
1. **Database Change Detection:** PostgreSQL trigger or CDC captures data changes
2. **Event Publishing:** Publish change event to message queue (Kafka/Redis)
3. **Event Processing:** Indexing service consumes events from queue
4. **Data Transformation:** Transform database records to Elasticsearch documents
5. **Index Update:** Update Elasticsearch index with transformed document
6. **Acknowledgment:** Confirm successful indexing back to source

**Real-time Sync Strategy:**
- **Immediate Updates:** Critical entities (products, orders) indexed within 1 second
- **Async Processing:** Non-critical updates processed asynchronously
- **Retry Mechanism:** Automatic retry on indexing failures with exponential backoff
- **Conflict Resolution:** Handle concurrent updates with versioning
- **Bulk Operations:** Batch multiple updates for efficiency

**Search Query Logic (Relevance Scoring, Pagination):**

**Query Types:**
- **Match Query:** Full-text search with relevance scoring
- **Multi-Match Query:** Search across multiple fields with field boosting
- **Bool Query:** Combine multiple queries with AND/OR/NOT logic
- **Range Query:** Numeric and date range filtering
- **Term Query:** Exact match for keywords
- **Prefix Query:** Prefix matching for autocomplete
- **Fuzzy Query:** Typo-tolerant search with edit distance

**Relevance Scoring:**
- **TF-IDF Scoring:** Term frequency-inverse document frequency for relevance
- **Field Boosting:** Boost title (3x) over description (1x) for better relevance
- **Function Score:** Custom scoring based on popularity, rating, recency
- **UID Context Boosting:** Boost products from user's registered sellers
- **Seller Reputation:** Factor seller rating into product relevance
- **Recency Boost:** Boost recently added/updated products

**Pagination Strategy:**
- **From/Size Pagination:** Simple offset-based pagination (max 10,000 results)
- **Scroll API:** For deep pagination and large result sets
- **Search After:** Cursor-based pagination for consistent results
- **Page Size Limits:** Maximum 100 results per page for performance
- **Total Hits:** Approximate total count for large result sets

**Faceted and Filtered Search Design:**

**Facet Implementation:**
- **Category Facets:** Hierarchical category filtering with counts
- **Price Range Facets:** Price buckets (0-100, 100-500, 500-1000, etc.)
- **Brand Facets:** Brand filtering with product counts
- **Rating Facets:** Star rating filters (4+, 3+, etc.)
- **Attribute Facets:** Industry-specific attributes (size, color, material, etc.)
- **Availability Facets:** In-stock, out-of-stock, pre-order filters

**Filter Combination:**
- **AND Logic:** All selected filters must match (default)
- **OR Logic:** Any selected filter matches (for same attribute type)
- **UID Filtering:** Automatic filtering by user's registered sellers
- **Location Filtering:** Geographic proximity filtering for services
- **Date Range Filtering:** Filter by creation date, availability dates

**Filter UI/UX:**
- **Dynamic Counts:** Show result count per filter option
- **Filter Persistence:** Maintain filters during pagination
- **Clear Filters:** Quick clear all or individual filters
- **Filter Breadcrumbs:** Show active filters with remove option
- **Mobile Optimization:** Collapsible filter panel for mobile

**Performance Tuning (Shards, Replicas, Cache Strategy):**

**Index Configuration:**
- **Shard Count:** 5 primary shards per index (adjust based on data volume)
- **Replica Count:** 1 replica for high availability (increase for read scaling)
- **Refresh Interval:** 1 second for near real-time search (balance performance)
- **Translog Settings:** Optimize translog for write performance
- **Merge Policy:** Configure merge policy for optimal segment size

**Caching Strategy:**
- **Query Cache:** Cache frequent queries in Elasticsearch query cache
- **Request Cache:** Cache filter results for repeated filter combinations
- **Field Data Cache:** Cache field data for aggregations and sorting
- **Application-Level Cache:** Cache search results in Redis (5-15 minutes TTL)
- **CDN Caching:** Cache static search result pages via CDN

**Performance Optimization:**
- **Index Aliases:** Use aliases for zero-downtime reindexing
- **Index Templates:** Auto-create indices with consistent settings
- **Bulk Operations:** Batch multiple operations for efficiency
- **Connection Pooling:** Reuse Elasticsearch client connections
- **Query Optimization:** Use `_source` filtering to reduce response size
- **Aggregation Optimization:** Use approximate aggregations for large datasets

**Monitoring and Maintenance:**
- **Cluster Health Monitoring:** Monitor cluster status, shard allocation
- **Query Performance:** Track slow queries (>100ms) and optimize
- **Index Size Monitoring:** Monitor index growth and plan capacity
- **Reindexing Strategy:** Periodic reindexing for optimization
- **Backup Strategy:** Snapshot indices for disaster recovery

**Shopping Cart:**
- **Individual Cart:** Standard shopping cart for single users
- **Family Cart:** Shared cart for family groups
- **Cart Persistence:** Save cart across sessions and devices
- **Real-time Sync:** Family cart synchronization within 1 second
- **Cart Analytics:** Abandoned cart tracking and recovery

**Checkout Process:**
- **Cart Review:** Review items and quantities
- **Address Management:** Multiple saved addresses
- **Payment Selection:** Multiple payment methods
- **Family Approval:** Approval workflow for family purchases
- **Order Summary:** Complete order breakdown with taxes and shipping
- **Order Confirmation:** Order placement confirmation

**Order Management:**
- **Order Creation:** Order generation with unique order numbers
- **Order Status:** Status tracking (pending, confirmed, processing, shipped, delivered)
- **Order History:** Complete order history for users
- **Order Tracking:** Real-time delivery tracking integration
- **Order Modifications:** Cancellation and modification workflows

**Industry-Specific Product Categories:**
- **Provisional Stores:** Grocery and daily essentials with expiration tracking
- **Medical Shops:** Pharmaceuticals with prescription management and FDA compliance
- **Jewelry Sellers:** Precious metals and gems with certification and valuation
- **Textile/Fashion Stores:** Clothing and fabrics with size charts and care instructions
- **Stationery:** Office supplies and educational materials
- **Hardware Shops:** Tools and construction materials with specifications
- **Home Decorators:** Furniture and home improvement with room planning
- **Household Goods:** General household items and appliances
- **Others:** Expandable category system for future industries

**Implementation Requirements:**
- Build product CRUD operations with validation
- Implement category hierarchy management
- Create product search with Elasticsearch integration
- Develop shopping cart with Redis persistence
- Build family cart synchronization system
- Implement checkout flow with payment integration
- Create order management system
- Develop inventory tracking and reservation
- Build product recommendation engine
- Implement UID-based product filtering

**Performance Requirements:**
- Product listing: <300ms response time
- Search results: <300ms for full-text search
- Cart operations: <100ms for add/update/remove
- Family cart sync: Real-time within 1 second

### 5.4 Service Booking Module

**Feature Overview:**
Advanced service appointment booking system with intelligent scheduling, availability management, advance payment, and GPS tracking integration.

**Service Provider Management:**
- **Provider Registration:** Service provider onboarding and verification
- **Service Catalog:** Create and manage service offerings
- **Service Categories:** Industry-specific service categories
- **Pricing Models:** Fixed pricing, hourly, package deals
- **Provider Profiles:** Detailed provider information and ratings

**Availability Management:**
- **Calendar Integration:** Provider availability calendar
- **Time Slot Management:** Define available time slots
- **Staff Scheduling:** Multi-staff availability management
- **Recurring Availability:** Set recurring availability patterns
- **Blocked Times:** Mark unavailable time periods

**Intelligent Scheduling Engine:**
- **Slot Optimization:** Minimize gaps, maximize utilization
- **Conflict Detection:** Automatic booking conflict detection
- **Waitlist Management:** Automatic notification when slots open
- **Recurring Appointments:** Weekly, bi-weekly, monthly patterns
- **Group Bookings:** Multiple participants with shared scheduling
- **Buffer Times:** Automatic buffer time between appointments

**Appointment Booking:**
- **Slot Selection:** Customer selects available time slot
- **Service Selection:** Choose specific service and provider
- **Customer Information:** Collect customer details
- **Advance Payment:** Mandatory advance payment (UPI/BNPL only)
- **Confirmation:** Appointment confirmation with details
- **Reminders:** Automated reminders via email, SMS, push

**Advance Payment System:**
- **Payment Requirement:** Mandatory advance payment for all bookings
- **Payment Options:** Fixed amount or percentage-based (20%, 50%, 100%)
- **Payment Methods:** UPI or BNPL only for advance payments
- **Refund Policy:** Tiered refund based on cancellation timing
  - 24+ hours before: Full refund
  - 12-24 hours before: 50% refund
  - Less than 12 hours: No refund
- **Balance Payment:** Remaining payment before or after service

**Appointment Management:**
- **Rescheduling:** Customer and provider rescheduling options
- **Cancellation:** Cancellation with refund processing
- **Status Updates:** Real-time appointment status updates
- **Communication:** Provider-customer messaging integration
- **History:** Complete appointment history

**Implementation Requirements:**
- Build service provider registration and management
- Create availability calendar system
- Implement intelligent scheduling algorithm
- Develop appointment booking flow
- Build advance payment integration (UPI/BNPL)
- Create refund processing system
- Implement appointment reminder system
- Build provider dashboard for appointment management
- Develop conflict resolution logic
- Create waitlist management system

**Performance Requirements:**
- Availability check: <300ms response time
- Booking creation: <500ms including payment
- Schedule optimization: <1 second for complex schedules

### 5.4.1 Industry-Specific Service Modules

**Automotive Module:**
- VIN-based parts compatibility checking
- Integration with automotive databases (Mitchell, AllData)
- Fitment guides and technical specifications
- Warranty tracking and claims processing
- Service appointment scheduling for registered customers
- Vehicle information management
- Parts catalog with OEM and aftermarket options

**Medical Module:**
- FDA compliance tracking and verification
- UID-based patient-clinic relationships
- Prescription management with verification workflows
- HIPAA-compliant data handling and storage
- Medical device certification tracking
- Drug interaction warnings and alerts
- Electronic Health Records (EHR) integration
- Telemedicine platform integration

**Restaurant Module:**
- UID-based menu access for registered customers
- POS system integration with customer-specific pricing
- Food safety tracking and compliance
- Supplier relationship management
- Advanced ordering and pickup scheduling
- Family account ordering for restaurants
- Nutritional information and allergen tracking
- Table reservation system

**Implementation Requirements:**
- Build industry-specific attribute management
- Create VIN decoding and compatibility checking (Automotive)
- Develop prescription management system (Medical)
- Implement POS integration (Restaurant)
- Build compliance tracking and verification
- Create industry-specific workflows
- Develop integration with industry databases
- Build industry-specific analytics and reporting

### 5.5 Family Group Management

**Feature Overview:**
Comprehensive family account system enabling collaborative shopping, expense tracking, budget management, and approval workflows for family groups up to 8 members.

**Family Group Structure:**
- **Group Creation:** Family head creates family group
- **Member Limit:** Maximum 8 members per family group
- **Role Hierarchy:** Family Head, Adult, Teen, Child roles
- **Member Management:** Add, remove, and manage family members
- **Group Settings:** Family-wide settings and preferences

**Role Permissions:**
- **Family Head:** Full control, order placement, budget management, member management
- **Adult Members:** Add items, view expenses, request purchases, manage own profile
- **Teen Members:** Limited spending, approval required, view family expenses
- **Child Members:** View-only access, wishlist creation, parental supervision

**Collaborative Shopping:**
- **Shared Cart:** Family members can add items to shared cart
- **Real-time Sync:** Cart updates synchronized within 1 second
- **Item Attribution:** Track which member added each item
- **Cart Collaboration:** Multiple members can modify cart simultaneously
- **Cart Approval:** Family head approval for purchases above limits

**Expense Tracking:**
- **Real-time Tracking:** Track all family purchases in real-time
- **Expense Categories:** Categorize expenses (groceries, utilities, entertainment, etc.)
- **Spending Analytics:** Analyze spending patterns by member and category
- **Budget Management:** Set and track family budgets
- **Expense Reports:** Generate expense reports by period and category

**Approval Workflows:**
- **Spending Limits:** Set spending limits per member role
- **Approval Triggers:** Automatic approval requests for purchases above limits
- **Approval Process:** Family head reviews and approves/rejects purchases
- **Notification System:** Real-time notifications for approval requests
- **Approval History:** Track all approval decisions

**Budget Management:**
- **Budget Setting:** Set monthly or category-based budgets
- **Budget Tracking:** Real-time budget utilization tracking
- **Budget Alerts:** Notifications when approaching or exceeding budgets
- **Budget Reports:** Budget vs actual spending reports
- **Budget Adjustments:** Modify budgets as needed

**Implementation Requirements:**
- Create family group CRUD operations
- Implement member management with role assignment
- Build shared cart system with real-time synchronization
- Develop expense tracking and categorization
- Create approval workflow system
- Implement budget management and alerts
- Build family analytics and reporting
- Create permission system based on roles
- Develop real-time notification system for family activities
- Implement conflict resolution for simultaneous cart updates

**Performance Requirements:**
- Cart sync: Real-time within 1 second
- Expense tracking: <100ms for expense recording
- Approval workflow: <200ms for approval processing

### 5.6 Transportation Services

**Feature Overview:**
Comprehensive transportation service management with GPS tracking, flexible pricing models, vehicle management, and real-time booking system.

**Vehicle Management:**
- **Vehicle Registration:** Register vehicles with complete details
- **Vehicle Types:** Car, Bus, Truck, Auto-rickshaw, Bike support
- **Vehicle Information:** Make, model, year, registration, capacity, fuel type
- **Document Management:** Insurance, license, registration documents
- **Vehicle Status:** Available, booked, maintenance, inactive statuses

**GPS Tracking Integration:**
- **Real-time Tracking:** Live GPS location updates every 5 seconds
- **Route Optimization:** Optimal route calculation and navigation
- **Location Sharing:** Share live location with customers
- **Geofencing:** Service area boundaries and alerts
- **Trip History:** Complete trip history with route data
- **Emergency Features:** SOS button with emergency contact integration

**Pricing Models:**
- **Kilometer-based Rental:** Per km rates with flexible pricing
- **Day Rental:** Full day, half day rental options
- **Hourly Rental:** Hourly booking with minimum hours
- **Package Deals:** Multi-day packages with discounts
- **Peak/Off-peak Pricing:** Time-based pricing variations
- **Additional Charges:** Driver, fuel, tolls, waiting time charges

**Booking Management:**
- **Booking Creation:** Create transportation bookings
- **Vehicle Selection:** Select appropriate vehicle type
- **Route Planning:** Define pickup and drop-off locations
- **Pricing Calculation:** Dynamic pricing based on distance/time
- **Booking Confirmation:** Confirm booking with details
- **Booking Modifications:** Reschedule or cancel bookings

**Customer Communication:**
- **Driver Information:** Share driver details with customer
- **Live Updates:** Real-time location and ETA updates
- **Messaging:** Direct messaging between customer and driver
- **Trip Sharing:** Share trip details with family/friends
- **Rating System:** Post-trip rating and feedback

**Implementation Requirements:**
- Build vehicle registration and management system
- Integrate GPS tracking service (Google Maps, Mapbox)
- Implement real-time location updates with WebSocket
- Create flexible pricing calculation engine
- Develop booking management system with availability checks
- Build route optimization algorithm
- Implement customer-driver communication system
- Create trip history and analytics tracking
- Develop geofencing and service area management
- Build emergency SOS feature integration

**Performance Requirements:**
- GPS location updates: Every 5 seconds during active trips
- Route calculation: <500ms response time
- Booking creation: <500ms including pricing calculation
- Real-time tracking: <1 second latency for location updates

### 5.7 Delivery Agency Network

**Feature Overview:**
Comprehensive independent delivery agency network enabling local entrepreneurs to manage delivery operations with team coordination, service area management, and dynamic pricing.

**Agency Registration:**
- **Agency Onboarding:** Independent delivery agency registration and verification
- **Document Management:** Business registration, licenses, insurance documents
- **Service Area Definition:** Define delivery coverage areas with geographic boundaries
- **Agency Profile:** Complete agency information and service capabilities
- **Verification Process:** Background check and document verification workflow

**Team Management:**
- **Team Member Registration:** Add delivery agents and team members
- **Subordinate Management:** Hierarchical team structure with roles
- **Agent Assignment:** Assign agents to specific delivery zones
- **Performance Tracking:** Track individual agent performance metrics
- **Commission Management:** Configure commission structures for agents

**Service Area Management:**
- **Geographic Boundaries:** Define delivery service areas with polygons
- **Zone Management:** Create and manage multiple delivery zones
- **Coverage Optimization:** Optimize service area coverage
- **Capacity Planning:** Manage delivery capacity per zone
- **Expansion Management:** Add or modify service areas

**Dynamic Pricing:**
- **Base Pricing:** Set base delivery charges per zone
- **Distance-based Pricing:** Pricing based on delivery distance
- **Time-based Pricing:** Peak/off-peak pricing variations
- **Weight-based Pricing:** Additional charges for heavy items
- **Urgent Delivery:** Premium pricing for express deliveries
- **Bulk Discounts:** Volume-based pricing for multiple deliveries

**Order Management:**
- **Order Assignment:** Assign orders to delivery agents
- **Route Optimization:** Optimize delivery routes for efficiency
- **Multi-stop Deliveries:** Manage multiple deliveries in single route
- **Delivery Tracking:** Real-time tracking of delivery status
- **Proof of Delivery:** Digital signature and photo capture
- **Delivery History:** Complete delivery history and analytics

**Revenue Management:**
- **Commission Calculation:** Automatic commission calculation
- **Payout Management:** Manage payouts to agencies and agents
- **Revenue Analytics:** Track revenue by zone, agent, and time period
- **Performance Metrics:** Delivery success rate, on-time delivery, customer satisfaction
- **Financial Reports:** Generate financial reports for agencies

**Implementation Requirements:**
- Build agency registration and verification system
- Create team and subordinate management system
- Implement service area definition with geographic boundaries
- Develop dynamic pricing calculation engine
- Build order assignment and routing optimization
- Create delivery tracking system with GPS integration
- Implement proof of delivery with digital signatures
- Develop commission and payout management system
- Build revenue analytics and reporting
- Create performance metrics tracking

**Performance Requirements:**
- Order assignment: <300ms response time
- Route optimization: <1 second for multi-stop routes
- Delivery tracking: Real-time updates within 2 seconds
- Commission calculation: <200ms per order

### 5.8 Payment Integration

**Feature Overview:**
Comprehensive payment processing system supporting multiple payment methods including credit cards, digital wallets, UPI, BNPL, and cash on delivery with secure transaction processing.

**Payment Methods:**
- **Credit/Debit Cards:** Visa, Mastercard, American Express support
- **Digital Wallets:** Apple Pay, Google Pay, Samsung Pay
- **UPI Integration:** Google Pay, PhonePe, Paytm, BHIM
- **BNPL Services:** Simpl, LazyPay, ZestMoney, PayLater
- **Bank Transfers:** Net Banking, ACH, SEPA
- **Cash on Delivery:** COD with payment verification

**Payment Gateway Integration:**
- **Stripe:** Primary payment gateway for international payments
- **PayPal:** Alternative payment method for global customers
- **Square:** Point-of-sale and online payment processing
- **Razorpay:** Payment gateway for Indian market
- **Authorize.net:** Payment processing for US market
- **Multi-gateway Support:** Automatic failover and routing

**UPI Payment System:**
- **Multiple UPI Apps:** Support for all major UPI providers
- **QR Code Payments:** Generate and scan UPI QR codes
- **UPI ID Payments:** VPA-based payment processing
- **Real-time Confirmation:** Instant payment confirmation
- **Transaction Limits:** UPI transaction limits as per guidelines
- **Refund Processing:** UPI refund handling

**BNPL Integration:**
- **Provider Integration:** Multiple BNPL provider support
- **Credit Limit Verification:** Real-time credit limit checks
- **EMI Options:** Flexible EMI options for eligible orders
- **Payment Tenure:** 15/30/45/60 day payment options
- **Automatic Reminders:** Payment reminder notifications
- **Default Management:** Late payment and default handling

**Advance Payment System:**
- **Service Bookings:** Mandatory advance payment for service bookings
- **Payment Options:** Fixed amount or percentage-based (20%, 50%, 100%)
- **Payment Methods:** UPI or BNPL only for advance payments
- **Refund Processing:** Tiered refund based on cancellation timing
- **Balance Payment:** Remaining payment before or after service

**Transaction Management:**
- **Transaction Recording:** Complete transaction history
- **Payment Status:** Real-time payment status tracking
- **Refund Processing:** Automated and manual refund workflows
- **Dispute Management:** Payment dispute resolution system
- **Reconciliation:** Payment reconciliation with accounting systems
- **Audit Trail:** Complete payment audit logging

**Security & Compliance:**
- **PCI DSS Compliance:** Level 1 PCI DSS compliance
- **Tokenization:** Secure card tokenization
- **Encryption:** End-to-end encryption for payment data
- **Fraud Detection:** Real-time fraud detection and prevention
- **3D Secure:** Strong Customer Authentication (SCA) support
- **KYC/AML:** Know Your Customer and Anti-Money Laundering compliance

**Implementation Requirements:**
- Integrate multiple payment gateways with failover support
- Build UPI payment processing with QR code generation
- Implement BNPL provider integrations
- Create advance payment system for service bookings
- Develop refund processing workflows
- Build transaction management and reconciliation
- Implement fraud detection and prevention
- Create payment audit and compliance logging
- Develop multi-currency support
- Build payment analytics and reporting

**Performance Requirements:**
- Payment processing: <3 seconds for payment confirmation
- UPI payments: <2 seconds for UPI transaction
- Refund processing: <24 hours for refund completion
- Transaction lookup: <100ms for transaction retrieval

### 5.9 Chat-Based Interface

**Feature Overview:**
Chat interface serves as the PRIMARY interaction method for customers to interact with vendors. This conversational commerce approach enables seamless product ordering, service booking, and customer support through real-time messaging with complete order and communication history within chat threads.

**Core Concept - Conversational Commerce:**
- **Primary Interaction Method:** Chat interface is the main way customers interact with vendors
- **Integrated Commerce:** Seamless product ordering through chat conversations
- **Complete History:** Order and communication history within organized chat threads
- **Real-time Communication:** Live messaging between customers and vendors
- **Multimedia Support:** Image, video, and document sharing in conversations
- **Order Status Updates:** Real-time order tracking and updates within chat
- **Payment Integration:** Secure payment processing directly through chat interface
- **Appointment Booking:** Service scheduling through conversational interface

**Chat Interface Features:**
- **Message Types:** Text, images, product cards, order confirmations, payment requests
- **Typing Indicators:** Real-time typing status and read receipts
- **Message Status:** Sent, delivered, read status indicators
- **Quick Actions:** Pre-built responses, product recommendations, order templates
- **Voice Messages:** Audio recording and playback capabilities
- **File Attachments:** Document and image sharing with preview
- **Emoji and Reactions:** Rich emoji support and message reactions
- **Message Search:** Full-text search within chat history

**Vendor Chat Dashboard:**
- **Multi-conversation Management:** Handle multiple customer chats simultaneously
- **Chat Prioritization:** Urgent orders, new customers, and VIP customer highlighting
- **Automated Responses:** AI-powered quick replies and common question handling
- **Chat Analytics:** Response time tracking, customer satisfaction metrics
- **Integration with Operations:** Direct links to inventory, orders, and customer profiles
- **Offline Message Handling:** Queue messages when vendor is unavailable

**Customer Chat Experience:**
- **Vendor Discovery:** Browse and initiate chats with registered vendors
- **Product Browsing:** View vendor catalogs directly within chat interface
- **Cart Management:** Add/remove items and manage orders through chat
- **Order Tracking:** Real-time order status updates and delivery notifications
- **Support Integration:** Direct customer support through dedicated chat channels
- **Family Collaboration:** Share cart items and orders with family members via chat

**Conversation Management:**
- **Customer-Seller Chat:** Direct messaging between customers and sellers
- **Service Provider Chat:** Communication for service bookings
- **Delivery Agent Chat:** Real-time communication during deliveries
- **Family Group Chat:** Family member communication
- **Group Chats:** Multi-participant group conversations
- **Chat Threading:** Organized conversation threads

**Notification System:**
- **Push Notifications:** Real-time push notifications for new messages
- **Email Notifications:** Email alerts for important messages
- **SMS Notifications:** SMS alerts for critical communications
- **In-app Notifications:** In-app notification center
- **Notification Preferences:** User-configurable notification settings

**Chat Moderation:**
- **Content Filtering:** Automated content moderation
- **Spam Detection:** Spam message detection and prevention
- **Report System:** User reporting for inappropriate content
- **Block Functionality:** Block users from messaging
- **Admin Moderation:** Admin tools for chat moderation

**Implementation Requirements:**
- Build WebSocket-based real-time messaging system as primary communication channel
- Create conversational commerce interface with product ordering capabilities
- Implement product cards and order confirmations within chat
- Develop vendor chat dashboard with multi-conversation management
- Build customer chat experience with vendor discovery and catalog browsing
- Create cart management through chat interface
- Implement order tracking and status updates within chat
- Develop payment processing directly through chat
- Build service appointment booking through conversational interface
- Create message search and history management
- Implement read receipts and typing indicators
- Develop chat analytics and reporting for vendors
- Build integration with orders, services, and deliveries
- Create admin moderation tools

**Performance Requirements:**
- Message delivery: Real-time within 1 second
- Media upload: <5 seconds for image uploads
- Message history: <300ms for message retrieval
- Notification delivery: <2 seconds for push notifications
- Product card rendering: <200ms for product display in chat
- Order processing through chat: <500ms response time

### 5.10 Theme System & Customization

**Feature Overview:**
Comprehensive theme system providing 10 default themes randomly assigned to vendors for uniqueness, along with extensive customization options for vendor-specific branding and user experience personalization.

**10 Default Themes:**
- **Professional Theme:** Clean, corporate design with blue-gray color scheme
- **Modern Theme:** Contemporary design with vibrant colors and gradients
- **Minimalist Theme:** Simple, clean design with minimal elements
- **Vibrant Theme:** Bold, energetic design with bright colors
- **Elegant Theme:** Sophisticated design with refined aesthetics
- **Tech Theme:** Technology-focused design with futuristic elements
- **Nature Theme:** Organic design with natural color palettes
- **Creative Theme:** Artistic design with creative elements
- **Luxury Theme:** Premium design with gold and dark accents
- **Classic Theme:** Traditional design with timeless aesthetics

**Theme Assignment System:**
- **Random Assignment:** Automated theme selection during vendor onboarding
- **Uniqueness Guarantee:** Each vendor receives a distinct theme for differentiation
- **Theme Categories:** Themes organized by style and industry fit
- **Theme Inheritance:** Family accounts can inherit or customize parent account themes
- **Theme Switching:** Vendors can request theme changes (with approval)

**Customization Framework:**
- **Accent Colors:** Primary, secondary, and accent color customization
- **Chat Backgrounds:** Solid colors, gradients, patterns, or custom image uploads
- **Typography:** Font family, size, and weight adjustments
- **Layout Density:** Compact, comfortable, and spacious layout options
- **Animation Preferences:** Motion effects and transition customizations
- **Accessibility Themes:** High contrast, color-blind friendly, and dyslexia-friendly options

**Brand Integration:**
- **Logo Placement:** Custom logo integration in header, favicon, and email templates
- **Color Scheme Adaptation:** Brand colors integrated into theme palette
- **Brand Asset Integration:** Custom images, icons, and visual elements
- **Email Template Branding:** Branded email templates with vendor identity
- **Mobile App Branding:** Vendor-specific app icons and splash screens

**Implementation Requirements:**
- Build theme system with 10 pre-designed default themes
- Create random theme assignment algorithm during vendor onboarding
- Develop theme customization interface for vendors
- Implement accent color and chat background customization
- Build typography and layout density options
- Create accessibility theme variants
- Develop brand integration system for logos and assets
- Implement theme inheritance for family accounts
- Build theme switching and approval workflow
- Create theme preview and testing interface

**Performance Requirements:**
- Theme loading: <100ms for theme application
- Customization save: <500ms for theme updates
- Theme preview: Real-time preview during customization
- Brand asset upload: <3 seconds for logo/image uploads

### 5.11 Analytics & Reporting

**Feature Overview:**
Comprehensive analytics and business intelligence system providing real-time insights, reporting, and data visualization for all platform stakeholders.

**Real-time Dashboards:**
- **Executive Summary:** KPI overview with trend analysis
- **Revenue Analytics:** Daily, weekly, monthly, yearly revenue tracking
- **User Engagement:** Activity heatmaps and funnel analysis
- **Platform Health:** System performance and uptime metrics
- **Business Metrics:** Sales, orders, customer acquisition metrics

**Revenue Analytics:**
- **Revenue Breakdown:** Revenue by product categories and services
- **Commission Tracking:** Commission earnings and payout tracking
- **Regional Performance:** Regional performance comparisons
- **Forecasting Models:** Predictive analytics for revenue forecasting
- **Trend Analysis:** Revenue trends and growth patterns

**User Engagement Metrics:**
- **Activity Heatmaps:** User interaction patterns by time and feature
- **Funnel Analysis:** Conversion tracking through user journey
- **Cohort Analysis:** User retention and lifetime value analysis
- **Family Group Metrics:** Collaboration and spending patterns
- **Service Utilization:** Transportation and delivery service usage

**Business Intelligence:**
- **Sales Analytics:** Product sales performance and trends
- **Inventory Analytics:** Stock levels, turnover, and optimization
- **Customer Analytics:** Customer behavior and segmentation
- **Service Analytics:** Service booking patterns and utilization
- **Delivery Analytics:** Delivery performance and efficiency metrics

**Custom Reports:**
- **Report Builder:** Custom report creation with drag-and-drop interface
- **Scheduled Reports:** Automated report generation and delivery
- **Export Options:** CSV, Excel, PDF export formats
- **Report Templates:** Pre-built report templates
- **Data Visualization:** Multiple chart types (bar, line, pie, area, scatter, heatmap)

**Advanced Analytics:**
- **Predictive Analytics:** Machine learning-based predictions
- **Recommendation Engine:** AI-powered product and service recommendations
- **Anomaly Detection:** Automated detection of unusual patterns
- **A/B Testing:** Experiment tracking and analysis
- **Attribution Analysis:** Marketing attribution and ROI analysis

**Implementation Requirements:**
- Build real-time dashboard with live data updates
- Create revenue analytics with forecasting models
- Develop user engagement tracking and analytics
- Implement business intelligence reporting system
- Build custom report builder with templates
- Create data visualization with multiple chart types
- Develop predictive analytics and ML models
- Implement A/B testing framework
- Build export and scheduling functionality
- Create analytics API for third-party integrations

**Performance Requirements:**
- Dashboard load: <2 seconds for dashboard rendering
- Report generation: <5 seconds for standard reports
- Real-time updates: <1 second for metric updates
- Data export: <10 seconds for large data exports

---

## 5.12 Advanced Features & Capabilities

### 5.12.1 Dynamic Configuration Management

**Feature Overview:**
Enable companies to customize and configure the platform according to their specific requirements and workflows with UID-based personalization.

**Core Capabilities:**
- **Feature Flags:** Enable/disable features based on company needs and UID relationships
- **Workflow Customization:** Adapt business processes to company requirements with UID integration
- **Field Customization:** Add/remove fields from forms and reports based on industry needs
- **Validation Rules:** Company-specific data validation rules with UID context
- **Integration Settings:** Customize external system integrations per UID relationship

**Configuration Workflow:**
- Configuration request submission and analysis
- Requirement assessment and UID strategy planning
- Technical and UI design planning
- Development and testing with UID integration
- Configuration deployment and user training
- Performance monitoring and continuous optimization

**Implementation Requirements:**
- Build configuration engine with feature flag management
- Create workflow customization system
- Develop field customization interface
- Implement validation rule engine
- Build integration settings management
- Create configuration workflow management system
- Develop configuration analytics and monitoring

### 5.12.2 Dynamic Menu Management

**Feature Overview:**
Provide flexible, role-based menu systems that adapt to company needs, user permissions, and UID-based access control.

**Core Capabilities:**
- **Company-Specific Menus:** Each seller/service provider can have customized menu structures
- **UID-Based Visibility:** Menus adapt based on customer-seller UID relationships
- **Role-Based Access:** Menus change based on user roles and permissions
- **Dynamic Menu Items:** Menu items can be added/removed based on seller features
- **Multi-level Navigation:** Support for nested menu structures with UID context
- **Icon and Styling:** Customizable menu appearance and seller branding

**Menu Architecture:**
- Menu configuration layer with company, role, UID, and user settings
- Menu engine layer with builder, permission engine, UID router, and dynamic renderer
- User interface layer with navigation, sidebar, breadcrumbs, and UID personalization

**Implementation Requirements:**
- Build dynamic menu builder system
- Create permission-based menu filtering
- Develop UID-based menu routing
- Implement menu customization interface
- Build breadcrumb navigation system
- Create menu analytics and usage tracking

### 5.12.3 Dynamic Role Creation & Management

**Feature Overview:**
Enable flexible role creation and permission management for different organizational structures, seller types, and UID-based access control. Unified role and permission system that manages both E-commerce and Service systems within the same application.

**Core Capabilities:**
- **Custom Role Creation:** Company and UID-specific role creation and management
- **Permission Assignment:** Granular permission assignment with UID context
- **Role Hierarchy:** Role hierarchy and inheritance management
- **Dynamic Permissions:** Context-aware permission assignment based on UID relationships
- **Role Templates:** Predefined role templates for common seller and customer scenarios
- **Unified System Management:** Single role system managing both E-commerce and Service modules

**Unified Role & Permission Architecture for E-Commerce and Service Systems:**

**System Architecture:**
The platform uses a unified role and permission system that seamlessly manages access control for both E-commerce and Service modules within the same application. This approach ensures consistent security, simplified management, and flexible access control across all platform features.

**Core Components:**
1. **Unified Role System:** Single role definition system that applies to both E-commerce and Service modules
2. **Module-Specific Permissions:** Permissions can be scoped to specific modules (E-commerce, Service, or both)
3. **Context-Aware Access:** Permissions adapt based on user context (vendor, service provider, customer, admin)
4. **Cross-Module Permissions:** Permissions that span both modules (e.g., user management, analytics)

**Role Types & Hierarchy:**

**Platform-Level Roles:**
- **Super Admin:** Full platform access across all modules and features
- **Platform Admin:** Administrative access to platform configuration and management
- **Support Admin:** Customer support and issue resolution access

**Module-Level Roles:**

**E-Commerce Module Roles:**
- **E-Commerce Admin:** Full access to e-commerce module (products, orders, inventory)
- **E-Commerce Manager:** Management access to e-commerce operations
- **E-Commerce Staff:** Limited access for order processing and customer service
- **Vendor/Seller:** Vendor-specific access to their own store and products
- **Vendor Staff:** Staff access to vendor's store with limited permissions

**Service Module Roles:**
- **Service Admin:** Full access to service module (services, appointments, providers)
- **Service Manager:** Management access to service operations
- **Service Staff:** Limited access for appointment management
- **Service Provider:** Provider-specific access to their own services and appointments
- **Provider Staff:** Staff access to provider's services with limited permissions

**Customer Roles:**
- **Customer:** Standard customer access to shopping and service booking
- **Family Head:** Family group management with approval authority
- **Family Member:** Family group member with collaborative shopping access

**Permission Management:**

**Permission Categories:**
- **View Permissions:** Read access to data and resources
- **Create Permissions:** Ability to create new resources
- **Edit Permissions:** Ability to modify existing resources
- **Delete Permissions:** Ability to remove resources
- **Export Permissions:** Ability to export data
- **Manage Permissions:** Administrative access to manage resources

**Permission Scope:**
- **Global Permissions:** Platform-wide access across all modules
- **Module Permissions:** Access scoped to specific module (E-commerce or Service)
- **Feature Permissions:** Access to specific features within modules
- **Resource Permissions:** Access to specific resources (products, services, orders, appointments)
- **UID Permissions:** Access based on UID relationships and seller associations
- **User Permissions:** Individual user-specific permissions
- **Family Permissions:** Family group-based permissions

**Unified Permission Matrix:**

**E-Commerce Module Permissions:**
- **Product Management:**
  - `ecommerce:product:view` - View products
  - `ecommerce:product:create` - Create products
  - `ecommerce:product:edit` - Edit products
  - `ecommerce:product:delete` - Delete products
  - `ecommerce:product:export` - Export product data
- **Order Management:**
  - `ecommerce:order:view` - View orders
  - `ecommerce:order:create` - Create orders
  - `ecommerce:order:edit` - Edit orders
  - `ecommerce:order:cancel` - Cancel orders
  - `ecommerce:order:refund` - Process refunds
- **Inventory Management:**
  - `ecommerce:inventory:view` - View inventory
  - `ecommerce:inventory:edit` - Update inventory
  - `ecommerce:inventory:export` - Export inventory data

**Service Module Permissions:**
- **Service Management:**
  - `service:service:view` - View services
  - `service:service:create` - Create services
  - `service:service:edit` - Edit services
  - `service:service:delete` - Delete services
  - `service:service:export` - Export service data
- **Appointment Management:**
  - `service:appointment:view` - View appointments
  - `service:appointment:create` - Create appointments
  - `service:appointment:edit` - Edit appointments
  - `service:appointment:cancel` - Cancel appointments
  - `service:appointment:confirm` - Confirm appointments
- **Provider Management:**
  - `service:provider:view` - View providers
  - `service:provider:create` - Create providers
  - `service:provider:edit` - Edit providers
  - `service:provider:manage` - Manage provider settings

**Cross-Module Permissions:**
- **User Management:**
  - `platform:user:view` - View users across modules
  - `platform:user:create` - Create users
  - `platform:user:edit` - Edit user profiles
  - `platform:user:manage` - Manage user accounts
- **Analytics:**
  - `platform:analytics:view` - View analytics across modules
  - `platform:analytics:export` - Export analytics data
- **UID Management:**
  - `platform:uid:view` - View UID codes
  - `platform:uid:create` - Create UID codes
  - `platform:uid:manage` - Manage UID system

**Permission Assignment Strategy:**

**Role-Based Assignment:**
- Assign permissions to roles, then assign roles to users
- Users can have multiple roles (e.g., Vendor + Service Provider)
- Role inheritance allows child roles to inherit parent permissions
- Role templates provide pre-configured permission sets

**Context-Based Assignment:**
- Permissions adapt based on user context (vendor, service provider, customer)
- UID relationships automatically grant additional permissions
- Module access determined by user's role in that module
- Cross-module access controlled by global permissions

**Dynamic Permission Resolution:**

**Permission Resolution Flow:**
1. **User Authentication:** User logs in and is authenticated
2. **Role Retrieval:** System retrieves all roles assigned to user
3. **Permission Aggregation:** All permissions from user's roles are aggregated
4. **Context Application:** Permissions filtered based on user context (UID, module, resource)
5. **Access Decision:** Permission engine makes access decision for requested action
6. **Audit Logging:** Access decision logged for audit trail

**Permission Engine Components:**
- **Permission Validator:** Validates user permissions for requested actions
- **Access Controller:** Enforces access control based on permission validation
- **UID Resolver:** Resolves UID-based permissions and relationships
- **Context Resolver:** Resolves module and resource context for permissions
- **Audit Logger:** Logs all permission checks and access decisions

**Multi-Module Access Management:**

**Solution for Managing E-Commerce and Service Systems:**

**1. Unified Permission Store:**
- Single database table/store for all permissions across modules
- Permission keys prefixed with module identifier (`ecommerce:`, `service:`, `platform:`)
- Centralized permission management interface

**2. Module-Specific Role Templates:**
- Pre-defined role templates for E-commerce (Vendor, E-Commerce Admin)
- Pre-defined role templates for Service (Service Provider, Service Admin)
- Hybrid role templates for users with access to both modules

**3. Context-Aware Permission Checking:**
- Permission checks include module context
- API endpoints validate module-specific permissions
- UI components check permissions before rendering

**4. Role Assignment Flexibility:**
- Users can have roles in one or both modules
- Role assignment independent per module
- Support for users who are both vendors and service providers

**5. Permission Inheritance:**
- Platform-level roles inherit permissions across modules
- Module-level roles inherit only within their module
- Custom roles can combine permissions from multiple modules

**Implementation Example:**

**User with Multiple Roles:**
- User: "John Doe"
- Roles: `vendor` (E-commerce), `service_provider` (Service)
- Permissions:
  - E-commerce: Can manage products, view orders, manage inventory
  - Service: Can manage services, view appointments, manage schedule
  - Cross-module: Can view analytics, manage UID codes

**Permission Check Flow:**
```
Request: POST /api/v1/ecommerce/products
1. Extract user from authentication token
2. Retrieve user roles: ['vendor', 'service_provider']
3. Aggregate permissions from both roles
4. Check if user has 'ecommerce:product:create' permission
5. Validate UID context (if applicable)
6. Grant/Deny access based on permission check
```

**Implementation Requirements:**
- Build unified role management system with module-aware permissions
- Create permission assignment interface supporting both modules
- Develop role hierarchy management with module-specific inheritance
- Implement dynamic permission engine with context-aware resolution
- Build role template library for E-commerce, Service, and hybrid roles
- Create permission analytics and audit logging across modules
- Develop module-specific permission checking middleware
- Build cross-module permission management interface
- Implement permission caching for performance optimization
- Create permission testing framework for both modules

### 5.12.4 Dynamic Formulas & Calculations

**Feature Overview:**
Enable companies to define custom formulas and calculations for their specific business requirements, pricing models, and UID-based personalization.

**Core Capabilities:**
- **Custom Formula Creation:** Seller and UID-specific formula creation and management
- **Dynamic Calculations:** Real-time calculation based on custom formulas
- **Formula Validation:** Formula syntax and logic validation with UID context
- **Performance Optimization:** Formula execution optimization and caching
- **Version Control:** Formula version control and change management

**Formula Components:**
- Base price, UID discount, dynamic pricing, tax calculation, shipping cost
- Custom formulas: Seller pricing, UID pricing, promotional pricing, volume pricing
- Calculation engine with parser, UID resolver, data resolver, and result calculator

**Implementation Requirements:**
- Build formula engine with parser and validator
- Create formula builder interface
- Develop UID-aware calculation system
- Implement formula caching and optimization
- Build formula version control system
- Create formula testing and validation tools

### 5.12.5 Multiple Graph Types & Visualization

**Feature Overview:**
Provide flexible and dynamic charting capabilities for data visualization and analytics across the platform.

**Core Capabilities:**
- **Multiple Chart Types:** Bar, line, pie, area, scatter plots, heatmaps, gauges
- **Dynamic Configuration:** Client-side chart configuration and UID-based customization
- **Real-time Updates:** Live data updates and chart refresh
- **Interactive Features:** Zoom, pan, drill-down, filtering, and cross-filtering
- **Responsive Design:** Mobile-responsive chart rendering and touch interactions

**Chart Types:**
- Bar charts for categorical data comparison
- Line charts for trend and time series data
- Pie charts for proportional data distribution
- Area charts for cumulative data visualization
- Scatter plots for correlation and distribution
- Heatmaps for density and pattern analysis

**Implementation Requirements:**
- Build chart rendering engine with multiple chart types
- Create chart configuration interface
- Develop real-time data binding system
- Implement interactive chart features
- Build responsive chart components
- Create chart export and sharing functionality

### 5.12.6 Super Admin Interface

**Feature Overview:**
Provide comprehensive system administration and tenant management capabilities for platform administrators with UID system oversight.

**Core Capabilities:**
- **Tenant Management:** System-wide tenant overview and UID relationship mapping
- **Tenant Creation:** New seller/service provider onboarding with UID setup
- **Tenant Configuration:** Tenant-specific configuration and UID policy management
- **Performance Monitoring:** Tenant performance and UID usage analytics
- **Support Management:** Tenant support and UID-related issue resolution

**UID System Management:**
- UID generation oversight and distribution monitoring
- Fraud detection and security monitoring
- Analytics dashboard for UID usage patterns
- Policy management and compliance monitoring
- Relationship mapping and visualization

**License Management:**
- License distribution with UID feature entitlements
- Feature management based on UID relationships
- Expiry tracking with UID system integration
- Usage analytics and UID-based feature adoption
- Compliance monitoring and regulatory adherence

**Implementation Requirements:**
- Build super admin dashboard with tenant overview
- Create tenant management interface
- Develop UID system oversight tools
- Implement license management system
- Build performance monitoring dashboards
- Create support management tools

### 5.12.7 Notification Management

**Feature Overview:**
Provide comprehensive notification and alert management for system events, UID-based communications, and user engagement.

**Core Capabilities:**
- **Event-driven Notifications:** Automatic notifications based on system and UID events
- **Multi-channel Delivery:** Email, SMS, WhatsApp, push notifications, in-app messaging
- **Template Management:** Customizable notification templates with UID personalization
- **Delivery Scheduling:** Scheduled notification delivery and UID-based timing
- **Delivery Tracking:** Notification delivery tracking and UID relationship analytics

**Notification Types:**
- UID system alerts (verification, relationship establishment, exclusivity notifications)
- Order and service alerts (status updates, confirmations, delivery updates)
- Seller communications (new customer registrations, performance alerts, system updates)
- Family notifications (purchase approvals, budget alerts, collaborative activity updates)
- Platform announcements (feature updates, maintenance notices, promotional campaigns)

**Implementation Requirements:**
- Build notification engine with event processing
- Create multi-channel delivery system
- Develop notification template management
- Implement delivery scheduling system
- Build delivery tracking and analytics
- Create notification preference management

### 5.12.8 Timezone Management & Globalization

**Feature Overview:**
Provide comprehensive timezone and globalization support for multi-region operations with UID-based localization.

**Core Capabilities:**
- **Multi-timezone Support:** Support for global timezones with UID relationship context
- **Automatic Conversion:** Automatic timezone conversion for appointments and orders
- **User Preferences:** User-specific timezone preferences with UID-based defaults
- **Seller Settings:** Seller-specific timezone configuration for service availability
- **Data Consistency:** Timezone-aware data storage with UTC standardization

**Globalization Features:**
- Multi-language support (20+ languages) with UID-based language detection
- Regional settings (date, time, number formats) with seller preferences
- Currency support with real-time conversion and UID-based pricing
- Cultural adaptation for different regions and UID customer segments
- Compliance support for regional regulations and global operations

**Implementation Requirements:**
- Build timezone management system with automatic conversion
- Create timezone preference management
- Develop multi-language support system
- Implement currency conversion and localization
- Build cultural adaptation framework
- Create regional compliance management

### 5.12.9 Multi-language Support

**Feature Overview:**
Provide comprehensive multi-language support for global operations and UID-based customer experiences.

**Core Capabilities:**
- **Multi-language Interface:** Support for 20+ languages with UID-based language detection
- **Dynamic Language Switching:** Real-time language switching without page reload
- **Language Detection:** Automatic language detection based on user location and UID context
- **Translation Management:** Centralized translation management with seller customization
- **Cultural Adaptation:** Cultural adaptation and localization for different UID customer segments

**Supported Languages:**
- Phase 1: English, Spanish, French, German, Portuguese (5 languages)
- Phase 2: Hindi, Mandarin, Japanese, Arabic, Russian (+5 languages)
- Phase 3: Expansion to 20+ languages

**Translation Management Workflow:**

**String Extraction Pipeline:**
- **Automated Extraction:** Scan codebase for translatable strings using i18next extraction tools
- **Translation Keys:** Generate unique translation keys with namespace organization (e.g., `common:button.save`, `product:title.add`)
- **Context Preservation:** Maintain context information for translators (file location, component name, usage)
- **Pluralization Support:** Handle singular/plural forms and complex plural rules per language
- **Variable Interpolation:** Support dynamic values in translations (e.g., `Welcome, {{name}}!`)
- **Nested Keys:** Support hierarchical translation keys for organization

**Translation Pipeline:**
- **Translation Storage:** Store translations in JSON/YAML files or database (per tenant for white-label)
- **Translation Workflow:** Draft → Review → Approved → Published workflow
- **Version Control:** Track translation versions and changes over time
- **Translation Memory:** Reuse existing translations for similar strings
- **Machine Translation:** Optional integration with Google Translate API for initial translations
- **Professional Translation:** Integration with translation services (Crowdin, Lokalise) for human translation
- **Seller Customization:** Allow sellers to customize translations for their brand voice

**Multi-language Content Storage Strategy:**

**Content Storage Architecture:**
- **Static Content:** Translation files stored in `translations/` directory (JSON/YAML format)
- **Dynamic Content:** Product descriptions, seller content stored in database with language columns
- **Caching Strategy:** Cache translations in Redis with language-specific keys
- **CDN Distribution:** Serve translation files via CDN for global performance
- **Database Schema:** Multi-language fields using JSONB columns or separate language tables
- **Content Versioning:** Track content versions per language for rollback capability

**Storage Patterns:**
- **Key-Value Storage:** Translation keys mapped to language-specific values
- **Namespace Organization:** Group translations by feature/module (auth, products, orders, etc.)
- **Fallback Chain:** Default language → Seller language → User preference → Browser language
- **Lazy Loading:** Load translations on-demand per route/feature to reduce initial bundle size

**UI/UX Language Toggle and Persistence:**

**Language Toggle Implementation:**
- **Language Selector:** Dropdown/button in header/navigation with flag icons and language names
- **Real-time Switching:** Instant language change without page reload using React Context/State
- **Visual Feedback:** Loading indicator during translation loading
- **Accessibility:** Keyboard navigation support and screen reader announcements
- **Mobile Optimization:** Native mobile language picker integration

**Persistence Strategy:**
- **User Preference Storage:** Save language preference in user profile (database)
- **Local Storage:** Cache language preference in browser localStorage for quick access
- **Session Storage:** Maintain language during session for guest users
- **UID-based Persistence:** Store language preference per UID relationship
- **Cookie Storage:** Set language cookie for server-side rendering (Next.js)
- **Device Sync:** Sync language preference across user devices via account

**Dynamic Locale Loading and Fallback Rules:**

**Locale Loading Strategy:**
- **Code Splitting:** Split translation files by language for lazy loading
- **Dynamic Imports:** Load translation files on-demand using dynamic imports
- **Preloading:** Preload common translations (navigation, buttons) for instant display
- **Bundle Optimization:** Include only active language in initial bundle

**Fallback Rules (Priority Order):**
1. **User Explicit Selection:** Highest priority - user manually selected language
2. **UID Context Language:** Language of seller associated with UID
3. **Seller Default Language:** Default language configured by seller
4. **User Location:** Geographic location-based language detection
5. **Browser Language:** Browser/system language preference
6. **Default Language:** Platform default (English) as final fallback

**Fallback Implementation:**
- **Partial Translation Handling:** Show default language for missing translations
- **Missing Key Detection:** Log missing translation keys for monitoring
- **Fallback Chain Resolution:** Automatic resolution through fallback chain
- **Error Handling:** Graceful degradation when translations unavailable

**Language Detection Logic:**
- **Browser Detection:** Read `navigator.language` or `Accept-Language` header
- **IP Geolocation:** Use IP-based geolocation for initial language suggestion
- **UID Relationship:** Detect language from seller's default language
- **User History:** Learn from user's previous language selections
- **Device Settings:** Respect device/system language settings

**Implementation Requirements:**
- Build translation management system with extraction pipeline
- Create language detection and switching with persistence
- Develop translation workflow and approval system
- Implement cultural adaptation system (RTL, date formats, number formats)
- Build language preference management with multi-level fallback
- Create translation analytics and usage tracking
- Implement string extraction and translation pipeline automation
- Build multi-language content storage with caching strategy
- Create UI language toggle with real-time switching
- Develop dynamic locale loading with code splitting
- Implement comprehensive fallback rules and error handling

### 5.12.10 Granular Role-Based Access Control

**Feature Overview:**
Provide fine-grained access control for different organizational structures, seller types, and UID-based relationships.

**Core Capabilities:**
- **Resource-level Permissions:** Granular permissions for individual resources and actions
- **Data-level Security:** Row-level and column-level data access with UID filtering
- **Time-based Access:** Time-based access control and business hour restrictions
- **Location-based Access:** Geographic access control for regional operations
- **Device-based Access:** Device-specific access control and security policies

**Permission Matrix:**
- Permission levels: Platform, Seller, UID, User, Family permissions
- Permission types: View, Create, Edit, Delete, Export, Manage access
- Permission engine with validator, access controller, UID resolver, audit logger, security manager

**Implementation Requirements:**
- Build granular permission system
- Create resource-level access control
- Develop data-level security with UID filtering
- Implement time and location-based access
- Build device-based access control
- Create permission analytics and audit logging

### 5.12.11 Device Management

**Feature Overview:**
Comprehensive IoT and device management for smart commerce and service operations with UID integration.

**Core Capabilities:**
- **Device Registration:** Automatic device discovery and UID-based registration
- **Configuration Management:** Device configuration and seller-specific parameter management
- **Health Monitoring:** Device health monitoring and UID relationship tracking
- **Performance Tracking:** Device performance monitoring and optimization
- **Maintenance Scheduling:** Device maintenance scheduling with seller coordination

**Device Types:**
- IoT devices (smart sensors and equipment)
- Mobile devices (customer and seller apps)
- POS devices (point of sale terminals)
- Scanner devices (UID/QR code scanners)
- Smart displays (digital signage and kiosks)

**Communication Protocols:**
- HTTP/REST for web-based API communication
- WebSocket for real-time bidirectional communication
- Bluetooth for short-range device communication
- NFC for near field communication
- MQTT for lightweight IoT messaging

**Implementation Requirements:**
- Build device registration and discovery system
- Create device configuration management
- Develop device health monitoring
- Implement device communication protocols
- Build device analytics and performance tracking
- Create device maintenance scheduling system

### 5.12.12 Custom Fields & Attributes

**Feature Overview:**
Enable companies to customize data structures and fields according to their specific business requirements and UID-based personalization.

**Core Capabilities:**
- **Dynamic Field Creation:** Add custom fields to products, services, and user profiles
- **Field Types:** Support for text, number, date, boolean, file, and relationship fields
- **Validation Rules:** Custom validation rules with UID context awareness
- **Field Relationships:** Custom field relationships and UID-based dependencies
- **Field Templates:** Pre-built field templates for different industries and seller types

**Field Types:**
- Text fields for string and character data
- Number fields for numeric and decimal data
- Date fields for date and time data
- Boolean fields for true/false and yes/no data
- File fields for document and media uploads
- Relationship fields for UID-based associations

**Implementation Requirements:**
- Build custom field creation system
- Create field type management
- Develop field validation engine
- Implement field relationship management
- Build field template library
- Create field analytics and usage tracking

### 5.12.13 Export Scheduling & Automated Reports

**Feature Overview:**
Provide automated report generation and delivery for operational efficiency and UID-based business intelligence.

**Core Capabilities:**
- **Automated Export:** Scheduled automated report generation with UID filtering
- **Multiple Formats:** Support for PDF, Excel, CSV, and UID-customized formats
- **Email Delivery:** Automated email delivery with UID-based personalization
- **Storage Management:** Report storage and UID-specific archival management
- **Delivery Tracking:** Report delivery tracking and UID relationship analytics

**Export Types:**
- PDF export for professional document format
- Excel export for spreadsheet and data analysis
- CSV export for comma-separated values
- JSON export for API and integration format
- Custom export for UID-customized formats

**Implementation Requirements:**
- Build export scheduling system
- Create report generation engine
- Develop UID-based data filtering
- Implement format conversion system
- Build email delivery system
- Create delivery tracking and analytics

### 5.12.14 Custom Report Templates

**Feature Overview:**
Enable companies to create custom report layouts and content according to their specific requirements and UID-based personalization.

**Core Capabilities:**
- **Template Designer:** Visual report template designer with drag-and-drop interface
- **Layout Customization:** Custom report layout with UID-specific branding
- **Content Management:** Dynamic content integration with UID-filtered data
- **Branding Integration:** Seller branding and UID-based customization
- **Template Library:** Pre-built report template library for different seller types

**Template Components:**
- Header section with seller branding and UID context
- Body section with main content and UID data display
- Footer section with summary and UID relationship details
- Charts and graphs with UID-filtered data visualization
- Data tables with customer-specific data display
- UID insights with relationship and loyalty metrics

**Implementation Requirements:**
- Build template designer with drag-and-drop interface
- Create layout customization system
- Develop content management with UID filtering
- Implement branding integration
- Build template library
- Create template sharing and versioning

### 5.12.15 Custom Field Excel Reports

**Feature Overview:**
Enable companies to create custom Excel reports with specific data selection and UID-based filtering.

**Core Capabilities:**
- **Data Selection:** Custom data selection with UID relationship filtering
- **Module Selection:** Module-specific data and UID-contextual report generation
- **Format Customization:** Excel format and UID-based styling customization
- **Formula Integration:** Excel formula integration with UID-specific calculations
- **Chart Generation:** Excel chart and graph generation with seller branding

**Data Sources:**
- Sales data (revenue and transaction records)
- UID data (customer relationship metrics)
- Service data (appointment and booking records)
- Inventory data (stock and product information)
- Customer data (profile and behavior analytics)

**Implementation Requirements:**
- Build Excel report generation system
- Create data selection interface with UID filtering
- Develop module-specific data access
- Implement Excel formatting and styling
- Build formula integration system
- Create chart generation with branding

### 5.12.16 License Expiry & Renewal Management

**Feature Overview:**
Comprehensive license management with expiry tracking and renewal processes integrated with UID system.

**Core Capabilities:**
- **License Tracking:** Comprehensive license tracking with UID feature allocation
- **Expiry Monitoring:** License expiry monitoring with UID system integration
- **Renewal Process:** Automated renewal process with seller-specific workflows
- **Feature Allocation:** License-based feature allocation with UID relationship management
- **Compliance Monitoring:** License compliance monitoring and UID system auditing

**License Lifecycle:**
- License creation and activation with UID setup
- License usage and active platform utilization
- Expiry warnings (30 days, 7 days, 1 day before expiry)
- License expiry with access suspension
- Renewal process with payment and UID system updates
- License renewal with access restoration

**Implementation Requirements:**
- Build license management system
- Create expiry monitoring and alerting
- Develop renewal process automation
- Implement feature allocation system
- Build compliance monitoring
- Create license analytics and reporting

### 5.12.17 Super Admin Logs & Production Monitoring

**Feature Overview:**
Provide comprehensive system monitoring and logging for production-level operations with UID system oversight.

**Core Capabilities:**
- **Comprehensive Logging:** Complete system activity logging with UID context
- **Multi-level Logs:** Application, system, security, and UID-specific logging
- **Log Retention:** Configurable log retention with UID relationship preservation
- **Log Analysis:** Log analysis and UID pattern recognition
- **Alert Generation:** Automated alert generation based on UID and system events

**Monitoring Sources:**
- System metrics (platform performance and health)
- Application logs (feature usage and errors)
- Security logs (access and UID authentication events)
- UID logs (relationship and code usage tracking)
- User activity (customer and seller behavior)
- Family cart logs (collaborative shopping events)
- GPS tracking logs (transportation and delivery location data)
- Delivery network logs (agency and agent activity)
- Payment transaction logs (UPI, BNPL, and gateway transactions)

**Implementation Requirements:**
- Build comprehensive logging system
- Create multi-level log management
- Develop log retention and archival
- Implement log analysis and pattern recognition
- Build alert generation system
- Create monitoring dashboards and reporting

### 5.12.18 Advertising & Campaign Management System

**Feature Overview:**
Comprehensive advertising and campaign management system serving as a primary revenue source. Super-admin controlled ad placement system with vendor campaign request functionality for promotional banners and status-like displays.

**Core Capabilities:**
- **Super-Admin Ad Control:** Complete control over ad placement, targeting, and display across all user types
- **Multi-User Type Ads:** Separate ad systems for vendors, service admins, and customers
- **Vendor Campaign Requests:** Vendors can request promotional campaigns for their products
- **Flexible Ad Display:** Carousel banners, status-like UI (WhatsApp-style), banner ads, interstitial ads
- **Targeting & Analytics:** Advanced targeting options and comprehensive ad performance analytics
- **Revenue Management:** Ad revenue tracking and billing system

**Super-Admin Ad Management:**

**Ad Placement Control:**
- **Section-Based Placement:** Control which sections show ads (homepage, product listing, service booking, checkout, profile, etc.)
- **User Type Targeting:** Configure ads for specific user types:
  - **Vendor Dashboard Ads:** Ads shown to vendors in their admin dashboard
  - **Service Admin Ads:** Ads shown to service providers in their management interface
  - **Customer Ads:** Ads shown to customers in shopping and service booking flows
- **Ad Slot Management:** Define and manage ad slots across the application
- **Ad Priority System:** Set priority levels for different ads (high, medium, low)
- **Scheduling:** Schedule ads with start/end dates and time-based display rules
- **Geographic Targeting:** Target ads based on user location, territory, or region
- **UID-Based Targeting:** Target ads based on UID relationships and seller associations

**Ad Types & Formats:**
- **Banner Ads:** Standard banner advertisements (top, bottom, sidebar)
- **Carousel Banners:** Rotating carousel banners at top of pages (vendor campaign requests)
- **Status-Style Ads:** WhatsApp-style status UI for vendor campaigns (swipeable stories)
- **Interstitial Ads:** Full-screen ads between page transitions
- **Native Ads:** Content-integrated ads matching app design
- **Video Ads:** Video advertisements with autoplay or click-to-play
- **Sponsored Listings:** Sponsored product/service listings in search results
- **Push Notification Ads:** Promotional push notifications (opt-in)

**Vendor Campaign Request System:**

**Campaign Request Workflow:**
1. **Vendor Request:** Vendor submits campaign request through dashboard
2. **Campaign Details:** Vendor provides:
   - Campaign name and description
   - Target products/services
   - Campaign duration (start/end dates)
   - Budget allocation
   - Preferred ad format (carousel, status-style, banner)
   - Target audience (if applicable)
3. **Super-Admin Review:** Super-admin reviews and approves/rejects campaign
4. **Campaign Approval:** Approved campaigns are scheduled and activated
5. **Campaign Monitoring:** Real-time monitoring of campaign performance
6. **Campaign Reporting:** Detailed reports for vendors on campaign performance

**Campaign Display Options:**

**Carousel Banner Display:**
- **Top Carousel:** Rotating banner carousel at top of homepage/product pages
- **Auto-Rotate:** Automatic rotation with configurable interval (3-5 seconds)
- **Manual Swipe:** Users can manually swipe through campaign banners
- **Click Action:** Clicking banner navigates to vendor's store or specific product
- **Campaign Badge:** Visual indicator showing "Sponsored" or "Campaign" badge
- **Multiple Campaigns:** Support for multiple active campaigns in carousel

**Status-Style UI (WhatsApp-like):**
- **Status Stories:** Swipeable story-style interface for vendor campaigns
- **Story Format:** Vertical image/video stories with tap-to-advance
- **Story Duration:** Configurable story duration (5-15 seconds per story)
- **Story Navigation:** Swipe left/right to navigate between vendor stories
- **Story Indicators:** Visual indicators showing story progress and available stories
- **Story Analytics:** Track story views, interactions, and engagement
- **Story Expiry:** Stories expire after campaign end date

**Ad Targeting & Personalization:**

**Targeting Options:**
- **User Type:** Target vendors, service admins, or customers
- **Geographic:** Target by location, city, state, country, or territory
- **UID Context:** Target based on UID relationships and registered sellers
- **User Behavior:** Target based on browsing history, purchase history, preferences
- **Device Type:** Target mobile, tablet, or desktop users
- **Time-Based:** Target based on time of day, day of week, or special events
- **Demographic:** Target based on user profile data (age, gender, etc.)

**Personalization:**
- **Dynamic Content:** Show relevant ads based on user's current context
- **Product Recommendations:** Show ads for products similar to user's interests
- **Seller Recommendations:** Promote sellers based on UID relationships
- **Service Recommendations:** Show service ads based on booking history
- **Frequency Capping:** Limit ad frequency per user to prevent ad fatigue

**Ad Revenue Management:**

**Revenue Model:**
- **CPC (Cost Per Click):** Revenue based on ad clicks
- **CPM (Cost Per Mille):** Revenue based on ad impressions (1000 views)
- **CPV (Cost Per View):** Revenue for video ad views
- **Campaign Fees:** Fixed fees for vendor campaign requests
- **Featured Placement:** Premium fees for featured ad placements
- **Performance-Based:** Revenue sharing based on conversions/sales

**Billing & Settlement:**
- **Advertiser Billing:** Bill advertisers based on selected pricing model
- **Vendor Campaign Billing:** Bill vendors for approved campaigns
- **Revenue Tracking:** Track ad revenue by ad type, user type, section
- **Settlement:** Automated settlement and payment processing
- **Revenue Reports:** Comprehensive revenue reports for super-admin

**Ad Analytics & Performance:**

**Performance Metrics:**
- **Impressions:** Number of ad views
- **Clicks:** Number of ad clicks
- **Click-Through Rate (CTR):** Percentage of clicks per impression
- **Conversions:** Number of conversions (purchases, bookings) from ads
- **Conversion Rate:** Percentage of conversions per click
- **Revenue Generated:** Revenue generated from ad-driven transactions
- **Engagement Rate:** User engagement with ads (time spent, interactions)
- **Campaign ROI:** Return on investment for vendor campaigns

**Analytics Dashboard:**
- **Super-Admin Dashboard:** Platform-wide ad performance analytics
- **Vendor Campaign Dashboard:** Campaign-specific analytics for vendors
- **Real-Time Metrics:** Real-time ad performance tracking
- **Historical Reports:** Historical performance trends and analysis
- **Comparative Analysis:** Compare performance across different ad types and campaigns

**Ad Content Management:**

**Content Requirements:**
- **Image Specifications:** Standardized image sizes and formats for different ad types
- **Video Specifications:** Video format, duration, and quality requirements
- **Content Moderation:** Automated and manual content moderation for ad compliance
- **Brand Guidelines:** Ensure ads comply with platform brand guidelines
- **Legal Compliance:** Ensure ads comply with advertising regulations and laws

**Content Approval:**
- **Super-Admin Approval:** All ads require super-admin approval before going live
- **Vendor Campaign Approval:** Vendor campaign content reviewed and approved
- **Content Rejection:** Rejection workflow with feedback for advertisers
- **Revision Workflow:** Support for content revisions and re-submission

**Implementation Requirements:**
- Build super-admin ad management interface with section-based placement control
- Create ad slot management system with user type targeting
- Develop vendor campaign request workflow and approval system
- Implement carousel banner display with auto-rotate and manual swipe
- Build status-style UI (WhatsApp-like) for vendor campaigns
- Create ad targeting engine with geographic, UID, and behavioral targeting
- Develop ad revenue management system with multiple pricing models
- Build comprehensive ad analytics dashboard for super-admin and vendors
- Implement ad content management with moderation and approval workflows
- Create ad scheduling system with time-based display rules
- Build ad performance tracking and reporting system
- Develop ad personalization engine with dynamic content

**Performance Requirements:**
- Ad loading: <500ms for banner ads
- Carousel rotation: Smooth 60fps animation
- Status-style UI: <200ms transition between stories
- Ad targeting: <100ms for targeting resolution
- Analytics tracking: Real-time metrics with <1 second delay

### 5.13 Quality Assurance Module

**Feature Overview:**
Comprehensive quality management system ensuring platform reliability, content quality, and user satisfaction through review systems, quality control dashboards, and automated moderation.

**Review & Rating System:**
- **Structured Reviews:** Guided review process with rating categories (product quality, service, delivery, value)
- **Photo & Video Reviews:** Multimedia review content with verification and moderation
- **Review Analytics:** Sentiment analysis and trend identification for quality insights
- **Review Moderation:** Automated and manual content moderation for inappropriate content
- **Response Management:** Seller response system for customer communication and issue resolution
- **Review Aggregation:** Average ratings calculation and review summary generation
- **Verified Purchase Reviews:** Verified purchase badge for authentic reviews
- **Review Helpfulness:** Helpful/not helpful voting system for review quality

**Quality Control Dashboard:**
- **Quality Metrics:** Platform-wide quality KPIs and benchmarking (average ratings, review counts, response rates)
- **Issue Tracking:** Problem identification and resolution workflows
- **Performance Monitoring:** Quality trend analysis and improvement tracking
- **Compliance Checking:** Regulatory compliance and quality standard verification
- **User Feedback:** Systematic feedback collection and analysis
- **Quality Alerts:** Real-time alerts for quality issues and threshold breaches

**Automated Moderation:**
- **AI-Powered Assessment:** AI-powered content quality assessment for reviews and ratings
- **Spam Detection:** Automated spam and fake review detection
- **Sentiment Analysis:** Automated sentiment analysis for review content
- **Content Filtering:** Inappropriate content filtering and flagging
- **Review Verification:** Automated verification of review authenticity

**Quality Features:**
- **Real-time Alerts:** Quality issue detection and immediate notification
- **Trend Analysis:** Quality improvement tracking and predictive insights
- **Compliance Reporting:** Regulatory compliance documentation and reporting
- **User Experience:** Quality-driven feature improvements and user satisfaction
- **Seller Quality Scores:** Seller quality scores based on reviews and ratings

**Implementation Requirements:**
- Build review and rating system with structured review process
- Create photo and video review upload and verification
- Develop review analytics with sentiment analysis
- Implement automated and manual review moderation
- Build seller response management system
- Create quality control dashboard with metrics and KPIs
- Develop issue tracking and resolution workflows
- Implement compliance checking and reporting
- Build user feedback collection and analysis system
- Create quality alerts and notification system

**Performance Requirements:**
- Review submission: <500ms response time
- Review moderation: <2 seconds for automated moderation
- Review analytics: <1 second for sentiment analysis
- Quality dashboard: <2 seconds for dashboard rendering

### 5.14 Inventory Module

**Feature Overview:**
Advanced inventory management system enabling efficient stock control, optimization, and automated replenishment with multi-location support and demand forecasting.

**Inventory Tracking:**
- **Real-time Stock:** Live inventory levels across all locations and channels
- **Multi-location Support:** Warehouse, store, and virtual inventory management
- **Batch & Serial Tracking:** Detailed product tracking with expiration management
- **Automated Alerts:** Low stock, overstock, and expiration warnings
- **Stock Movement:** Complete audit trail of inventory movements
- **Stock Reservations:** Order-based stock reservation and release
- **Stock Transfers:** Inter-location stock transfer management

**Demand Forecasting:**
- **Sales Analytics:** Historical sales data and trend analysis
- **Predictive Modeling:** AI-powered demand forecasting and planning
- **Seasonal Adjustments:** Automatic seasonal demand pattern recognition
- **Market Intelligence:** External market data integration for forecasting
- **Accuracy Tracking:** Forecast accuracy monitoring and model improvement
- **Reorder Point Calculation:** Dynamic reorder point optimization based on forecast

**Automated Replenishment:**
- **Reorder Point Calculation:** Dynamic reorder point optimization
- **Supplier Integration:** Automated purchase order generation and tracking
- **Just-in-Time Ordering:** Optimized ordering to minimize holding costs
- **Bulk Purchase Optimization:** Volume discount and supplier negotiation support
- **Lead Time Management:** Supplier lead time tracking and optimization
- **Auto-Reorder:** Automated reorder triggers based on stock levels

**Inventory Features:**
- **Real-time Visibility:** Live inventory across all sales channels
- **Automated Optimization:** AI-driven inventory optimization and replenishment
- **Cost Management:** Carrying cost minimization and cash flow optimization
- **Supplier Integration:** Seamless supplier relationship and order management
- **Compliance Tracking:** Regulatory compliance and quality assurance
- **Expiration Management:** Product expiration tracking and alerts

**Implementation Requirements:**
- Build real-time inventory tracking system
- Create multi-location inventory management
- Develop batch and serial tracking system
- Implement automated stock alerts and notifications
- Build demand forecasting engine with AI/ML
- Create automated replenishment system
- Develop supplier integration for purchase orders
- Implement stock movement audit trail
- Build inventory analytics and reporting
- Create expiration management system

**Performance Requirements:**
- Stock updates: Real-time within 1 second
- Inventory queries: <200ms response time
- Forecast calculation: <5 seconds for demand forecasting
- Reorder point calculation: <1 second response time

### 5.15 Seller Management Module

**Feature Overview:**
Comprehensive seller onboarding, management, and support system ensuring seller success and platform growth with performance tracking and support tools.

**Seller Onboarding:**
- **Business Verification:** Comprehensive seller verification and compliance checking
- **UID Generation:** Automated UID/QR code generation and distribution tools
- **Store Setup:** Guided store creation with template selection and customization
- **Integration Setup:** Payment, shipping, and third-party service integration
- **Training & Support:** Comprehensive onboarding training and ongoing support
- **Document Management:** Business registration, licenses, and compliance documents
- **Profile Configuration:** Store profile, branding, and customization setup

**Performance Management:**
- **Seller Dashboard:** Comprehensive performance metrics and insights
- **Sales Analytics:** Revenue tracking, conversion rates, and growth metrics
- **Customer Analytics:** Customer acquisition, retention, and satisfaction
- **Product Performance:** Top products, categories, and optimization recommendations
- **Market Intelligence:** Competitive analysis and market positioning
- **UID Performance:** UID code usage and customer acquisition metrics
- **Conversion Funnels:** Sales funnel analysis and optimization

**Seller Support System:**
- **24/7 Support:** Multi-channel support with priority escalation
- **Knowledge Base:** Comprehensive seller resources and best practices
- **Community Forum:** Seller-to-seller collaboration and knowledge sharing
- **Training Programs:** Ongoing education and skill development
- **Success Metrics:** Seller success tracking and improvement recommendations
- **Support Tickets:** Ticket management and resolution tracking
- **Live Chat Support:** Real-time support chat for sellers

**Seller Features:**
- **Automated Onboarding:** Streamlined seller registration and verification
- **Performance Optimization:** Data-driven seller success recommendations
- **Comprehensive Support:** Multi-channel support with expert assistance
- **Growth Tools:** Marketing, analytics, and expansion support
- **Compliance Management:** Regulatory compliance and risk management
- **Seller Tiers:** Basic, Professional, Premium, Enterprise seller tiers
- **Commission Management:** Commission calculation and payout tracking

**Implementation Requirements:**
- Build seller onboarding workflow with verification
- Create automated UID generation and distribution
- Develop store setup and configuration system
- Implement seller dashboard with performance metrics
- Build sales and customer analytics system
- Create seller support system with multi-channel support
- Develop knowledge base and training resources
- Implement seller tier management and commission tracking
- Build seller success tracking and recommendations
- Create compliance management system

**Performance Requirements:**
- Seller onboarding: <5 minutes for basic setup
- Dashboard load: <2 seconds for seller dashboard
- Analytics queries: <1 second for performance metrics
- Support response: <2 hours for support ticket response

### 5.16 Company Module

**Feature Overview:**
Multi-tenant company management system enabling efficient administration of diverse business entities on the platform with complete data isolation and customization.

**Company Setup & Configuration:**
- **Business Profiling:** Comprehensive company information and verification
- **Industry Configuration:** Vertical-specific feature activation and customization
- **Brand Management:** Logo, colors, and branding customization
- **Legal Compliance:** Regulatory compliance configuration and documentation
- **Integration Setup:** Third-party service and ERP system integration
- **White Label Configuration:** Complete brand customization for white-label clients
- **Regional Configuration:** Regional settings and localization

**Multi-tenant Management:**
- **Data Isolation:** Complete data separation and security between tenants
- **Resource Allocation:** Computing resources, storage, and API limits management
- **Performance Monitoring:** Tenant-specific performance tracking and optimization
- **Usage Analytics:** Resource consumption and usage pattern analysis
- **Billing Integration:** Automated billing and subscription management
- **Tenant Onboarding:** Company onboarding and setup workflows
- **Tenant Migration:** Data migration and tenant transfer capabilities

**Company Analytics:**
- **Business Intelligence:** Company performance and growth analytics
- **User Behavior:** Employee and customer behavior insights
- **Operational Efficiency:** Process optimization and automation insights
- **Competitive Analysis:** Market positioning and competitive intelligence
- **Strategic Planning:** Data-driven strategic decision support
- **Revenue Analytics:** Revenue tracking and financial analytics
- **Usage Analytics:** Feature adoption and usage patterns

**Company Features:**
- **Flexible Configuration:** Company-specific customization and feature control
- **Scalable Architecture:** Support for companies of all sizes and industries
- **Security & Compliance:** Enterprise-grade security and regulatory compliance
- **Integration Capabilities:** Seamless integration with existing business systems
- **Performance Optimization:** Automated performance monitoring and optimization
- **Multi-location Support:** Multiple location and subsidiary management
- **License Management:** License tracking and renewal management

**Implementation Requirements:**
- Build company setup and configuration system
- Create business profiling and verification workflow
- Develop industry-specific feature configuration
- Implement multi-tenant data isolation
- Build resource allocation and monitoring system
- Create company analytics and business intelligence
- Develop billing and subscription management
- Implement tenant onboarding and migration tools
- Build white-label customization framework
- Create compliance and security management

**Performance Requirements:**
- Company setup: <10 minutes for basic configuration
- Data isolation: Zero cross-tenant data leakage
- Analytics queries: <2 seconds for company analytics
- Resource monitoring: Real-time resource usage tracking

---

## 6. API Specifications

### 6.1 API Architecture

**API Design Principles:**
- **RESTful Design:** Resource-based URL structure following REST conventions
- **GraphQL Support:** GraphQL endpoints for complex queries and data fetching
- **JSON API Specification:** Standardized API response format
- **Versioning:** API versioning strategy (v1, v2) for backward compatibility
- **HATEOAS:** Hypermedia-driven API design for discoverability
- **Rate Limiting:** Request throttling and rate limiting per user/IP
- **Authentication:** JWT-based authentication with refresh tokens
- **Error Handling:** Consistent error response format across all endpoints

**API Gateway Architecture:**
- **Single Entry Point:** All API requests routed through API Gateway
- **Authentication & Authorization:** Centralized auth handling
- **Request Routing:** Route requests to appropriate microservices
- **Load Balancing:** Distribute requests across service instances
- **Rate Limiting:** Global and per-endpoint rate limiting
- **Request/Response Transformation:** Data transformation and validation
- **Monitoring & Logging:** Centralized API monitoring and logging

**API Response Format:**
- **Success Response:** Standardized success response with data payload
- **Error Response:** Consistent error format with error codes and messages
- **Pagination:** Cursor-based and offset-based pagination support
- **Filtering & Sorting:** Query parameter-based filtering and sorting
- **Field Selection:** GraphQL-style field selection for REST APIs
- **Metadata:** Response metadata including pagination info, timestamps

**API Documentation:**

**OpenAPI 3.1 Specification:**

**Specification Structure:**
- **OpenAPI Version:** OpenAPI 3.1.0 specification format
- **Info Section:** API title, version, description, contact, license
- **Servers:** Production, staging, development server URLs
- **Paths:** All API endpoints with HTTP methods (GET, POST, PUT, DELETE, PATCH)
- **Components:** Reusable schemas, parameters, responses, security schemes
- **Tags:** Endpoint grouping and organization
- **External Documentation:** Links to additional documentation

**Endpoint Documentation:**
- **Path Parameters:** Documented path variables (e.g., `/api/v1/products/{id}`)
- **Query Parameters:** All query parameters with types, required flags, descriptions
- **Request Bodies:** Complete request body schemas with examples
- **Response Schemas:** Response structure for all status codes (200, 400, 401, 404, 500, etc.)
- **Headers:** Request and response headers documentation
- **Authentication:** Security scheme documentation (JWT, OAuth 2.0, API keys)

**API Request/Response Examples:**

**Request Examples:**
- **JSON Examples:** Complete JSON request examples for each endpoint
- **cURL Examples:** Command-line examples for testing
- **JavaScript Examples:** Fetch API and Axios examples
- **TypeScript Examples:** TypeScript examples with type safety
- **Python Examples:** Requests library examples
- **PHP Examples:** cURL examples for PHP

**Response Examples:**
- **Success Responses:** 200 OK responses with complete data structures
- **Error Responses:** 400, 401, 404, 500 error responses with error details
- **Pagination Examples:** Paginated response examples with metadata
- **Filter Examples:** Filtered response examples
- **Real-world Scenarios:** Complete request/response flows for common use cases

**Standardized Error Response Format + Error Code Catalog:**

**Error Response Structure:**
```json
{
  "error": {
    "code": "PRODUCT_NOT_FOUND",
    "message": "Product with ID 12345 not found",
    "details": {
      "product_id": "12345",
      "suggestion": "Check product ID or try searching for similar products"
    },
    "timestamp": "2024-01-15T10:30:00Z",
    "request_id": "req_abc123xyz",
    "path": "/api/v1/products/12345"
  }
}
```

**Error Code Catalog:**
- **Authentication Errors (AUTH_*):**
  - `AUTH_INVALID_TOKEN`: Invalid or expired JWT token
  - `AUTH_MISSING_TOKEN`: Authentication token not provided
  - `AUTH_INSUFFICIENT_PERMISSIONS`: User lacks required permissions
  - `AUTH_ACCOUNT_LOCKED`: Account locked due to security reasons

- **Validation Errors (VALIDATION_*):**
  - `VALIDATION_REQUIRED_FIELD`: Required field missing
  - `VALIDATION_INVALID_FORMAT`: Invalid data format (email, phone, etc.)
  - `VALIDATION_OUT_OF_RANGE`: Value outside allowed range
  - `VALIDATION_INVALID_TYPE`: Invalid data type

- **Resource Errors (RESOURCE_*):**
  - `RESOURCE_NOT_FOUND`: Requested resource not found
  - `RESOURCE_ALREADY_EXISTS`: Resource with same identifier exists
  - `RESOURCE_CONFLICT`: Resource state conflict
  - `RESOURCE_DELETED`: Resource has been deleted

- **Business Logic Errors (BUSINESS_*):**
  - `BUSINESS_INSUFFICIENT_STOCK`: Product out of stock
  - `BUSINESS_INVALID_OPERATION`: Invalid business operation
  - `BUSINESS_PAYMENT_FAILED`: Payment processing failed
  - `BUSINESS_ORDER_CANCELLED`: Order cannot be processed

- **System Errors (SYSTEM_*):**
  - `SYSTEM_INTERNAL_ERROR`: Internal server error
  - `SYSTEM_SERVICE_UNAVAILABLE`: Service temporarily unavailable
  - `SYSTEM_TIMEOUT`: Request timeout
  - `SYSTEM_MAINTENANCE`: System under maintenance

**Error Code Documentation:**
- **Error Code Reference:** Complete catalog with all error codes
- **Resolution Steps:** Step-by-step resolution for each error
- **HTTP Status Mapping:** Error codes mapped to HTTP status codes
- **Retry Guidelines:** When and how to retry failed requests
- **Support Contact:** When to contact support for specific errors

**API Versioning Documentation:**

**Versioning Strategy:**
- **URL Versioning:** `/api/v1/`, `/api/v2/` in URL path
- **Header Versioning:** `API-Version: 1.0` in request headers (alternative)
- **Semantic Versioning:** MAJOR.MINOR.PATCH version numbering
- **Backward Compatibility:** Maintain backward compatibility within major version
- **Deprecation Policy:** 6-month deprecation notice before removal

**Version Documentation:**
- **Current Version:** Latest stable API version (v1)
- **Deprecated Versions:** List of deprecated versions with end-of-life dates
- **Migration Guides:** Step-by-step guides for migrating between versions
- **Breaking Changes:** Documented breaking changes between versions
- **Version Timeline:** Version release history and timeline

**Rate Limiting and Throttling Rules per Endpoint:**

**Rate Limiting Strategy:**
- **Per-User Limits:** Individual user rate limits based on subscription tier
- **Per-IP Limits:** IP-based rate limiting for DDoS protection
- **Per-Endpoint Limits:** Different limits for different endpoint categories
- **Burst Allowance:** Allow short bursts above base rate
- **Time Windows:** Sliding window or fixed window rate limiting

**Rate Limit Headers:**
```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 999
X-RateLimit-Reset: 1642248000
X-RateLimit-Used: 1
```

**Endpoint-Specific Rate Limits:**
- **Authentication Endpoints:** 100 requests/hour per IP
- **Product Search:** 1000 requests/hour per user
- **Product Creation:** 100 requests/hour per seller
- **Order Placement:** 500 requests/hour per user
- **Payment Processing:** 50 requests/hour per user
- **Admin Endpoints:** 5000 requests/hour per admin user
- **Public Endpoints:** 10000 requests/hour per IP

**Throttling Rules:**
- **Soft Throttling:** Return 429 with Retry-After header, allow retry
- **Hard Throttling:** Block requests for extended period after threshold
- **Progressive Throttling:** Increase throttling duration with repeated violations
- **Whitelist Exemptions:** Exempt certain users/IPs from rate limiting
- **Dynamic Adjustment:** Adjust limits based on system load

**Rate Limit Response:**
```json
{
  "error": {
    "code": "RATE_LIMIT_EXCEEDED",
    "message": "Rate limit exceeded. Please try again later.",
    "details": {
      "limit": 1000,
      "remaining": 0,
      "reset_at": "2024-01-15T11:00:00Z"
    },
    "retry_after": 3600
  }
}
```

**Interactive Documentation:**
- **Swagger UI:** Interactive API explorer with try-it-out functionality
- **ReDoc:** Alternative API documentation interface
- **Postman Collection:** Importable Postman collection for API testing
- **SDK Generation:** Auto-generated SDKs for JavaScript, Python, Ruby, PHP
- **Code Snippets:** Copy-paste code examples for all endpoints

### 6.2 Authentication APIs

**Authentication Endpoints:**
- **POST /api/v1/auth/register:** User registration with email/phone
- **POST /api/v1/auth/login:** User login with credentials
- **POST /api/v1/auth/social-login:** OAuth 2.0 social media login
- **POST /api/v1/auth/uid-register:** Registration with UID/QR code
- **POST /api/v1/auth/refresh-token:** Refresh access token
- **POST /api/v1/auth/logout:** User logout and token invalidation
- **POST /api/v1/auth/forgot-password:** Password reset request
- **POST /api/v1/auth/reset-password:** Password reset confirmation
- **POST /api/v1/auth/verify-email:** Email verification
- **POST /api/v1/auth/verify-phone:** Phone OTP verification

**Multi-Factor Authentication:**
- **POST /api/v1/auth/mfa/enable:** Enable MFA for user account
- **POST /api/v1/auth/mfa/verify:** Verify MFA code (TOTP/SMS)
- **POST /api/v1/auth/mfa/disable:** Disable MFA for user account
- **POST /api/v1/auth/mfa/backup-codes:** Generate backup codes

**Token Management:**
- **Access Token:** Short-lived JWT token (15 minutes)
- **Refresh Token:** Long-lived token (7 days) for token renewal
- **Token Storage:** httpOnly cookies for web, secure storage for mobile
- **Token Rotation:** Automatic refresh token rotation on use
- **Token Revocation:** Token blacklisting for logout and security

**Implementation Requirements:**
- Implement JWT token generation and validation
- Create password hashing with bcrypt
- Build OAuth 2.0 integration for social login
- Develop MFA flow with TOTP and SMS OTP
- Create token refresh mechanism
- Implement password reset workflow
- Build email and phone verification
- Create session management system

### 6.3 User Management APIs

**User Profile APIs:**
- **GET /api/v1/users/me:** Get current user profile
- **PUT /api/v1/users/me:** Update user profile
- **POST /api/v1/users/me/avatar:** Upload profile picture
- **GET /api/v1/users/{userId}:** Get user profile by ID
- **PUT /api/v1/users/{userId}:** Update user profile (admin)
- **DELETE /api/v1/users/{userId}:** Delete user account

**User Preferences:**
- **GET /api/v1/users/me/preferences:** Get user preferences
- **PUT /api/v1/users/me/preferences:** Update user preferences
- **GET /api/v1/users/me/notifications:** Get notification preferences
- **PUT /api/v1/users/me/notifications:** Update notification preferences

**Address Management:**
- **GET /api/v1/users/me/addresses:** Get user addresses
- **POST /api/v1/users/me/addresses:** Add new address
- **PUT /api/v1/users/me/addresses/{addressId}:** Update address
- **DELETE /api/v1/users/me/addresses/{addressId}:** Delete address
- **PUT /api/v1/users/me/addresses/{addressId}/default:** Set default address

**Family Account Management:**
- **POST /api/v1/users/me/family-group:** Create family group
- **GET /api/v1/users/me/family-group:** Get family group details
- **POST /api/v1/users/me/family-group/members:** Add family member
- **PUT /api/v1/users/me/family-group/members/{memberId}:** Update member
- **DELETE /api/v1/users/me/family-group/members/{memberId}:** Remove member

**Implementation Requirements:**
- Build user profile CRUD operations
- Create address management system
- Develop family account management APIs
- Implement preference management
- Build profile picture upload and processing
- Create user search and filtering
- Develop user activity tracking

### 6.4 E-Commerce APIs

**Product Catalog APIs:**
- **GET /api/v1/products:** Get product list with filtering
- **GET /api/v1/products/{productId}:** Get product details
- **POST /api/v1/products:** Create new product (seller)
- **PUT /api/v1/products/{productId}:** Update product (seller)
- **DELETE /api/v1/products/{productId}:** Delete product (seller)
- **GET /api/v1/products/search:** Search products with Elasticsearch
- **GET /api/v1/products/categories:** Get product categories
- **GET /api/v1/products/{productId}/variants:** Get product variants

**Shopping Cart APIs:**
- **GET /api/v1/cart:** Get user shopping cart
- **POST /api/v1/cart/items:** Add item to cart
- **PUT /api/v1/cart/items/{itemId}:** Update cart item quantity
- **DELETE /api/v1/cart/items/{itemId}:** Remove item from cart
- **DELETE /api/v1/cart:** Clear shopping cart
- **GET /api/v1/cart/family:** Get family shared cart
- **POST /api/v1/cart/family/items:** Add item to family cart
- **POST /api/v1/cart/family/approve:** Approve family cart purchase

**Order Management APIs:**
- **POST /api/v1/orders:** Create new order
- **GET /api/v1/orders:** Get user orders with filtering
- **GET /api/v1/orders/{orderId}:** Get order details
- **PUT /api/v1/orders/{orderId}/cancel:** Cancel order
- **PUT /api/v1/orders/{orderId}/status:** Update order status (seller)
- **GET /api/v1/orders/{orderId}/tracking:** Get order tracking information
- **POST /api/v1/orders/{orderId}/review:** Submit order review

**Checkout APIs:**
- **POST /api/v1/checkout/initiate:** Initiate checkout process
- **POST /api/v1/checkout/validate:** Validate checkout data
- **POST /api/v1/checkout/confirm:** Confirm and place order
- **GET /api/v1/checkout/shipping-options:** Get available shipping options
- **GET /api/v1/checkout/payment-methods:** Get available payment methods

**Implementation Requirements:**
- Build product catalog management APIs
- Create shopping cart with Redis persistence
- Develop order management system
- Implement checkout flow APIs
- Build product search with Elasticsearch
- Create UID-based product filtering
- Develop inventory reservation system

### 6.5 Service Provider APIs

**Service Management APIs:**
- **GET /api/v1/services:** Get service list
- **GET /api/v1/services/{serviceId}:** Get service details
- **POST /api/v1/services:** Create new service (provider)
- **PUT /api/v1/services/{serviceId}:** Update service (provider)
- **DELETE /api/v1/services/{serviceId}:** Delete service (provider)
- **GET /api/v1/services/categories:** Get service categories

**Availability Management APIs:**
- **GET /api/v1/services/{serviceId}/availability:** Get service availability
- **POST /api/v1/services/{serviceId}/availability:** Set availability (provider)
- **PUT /api/v1/services/{serviceId}/availability/{slotId}:** Update time slot
- **DELETE /api/v1/services/{serviceId}/availability/{slotId}:** Block time slot

**Appointment Booking APIs:**
- **POST /api/v1/appointments:** Book new appointment
- **GET /api/v1/appointments:** Get user appointments
- **GET /api/v1/appointments/{appointmentId}:** Get appointment details
- **PUT /api/v1/appointments/{appointmentId}/reschedule:** Reschedule appointment
- **PUT /api/v1/appointments/{appointmentId}/cancel:** Cancel appointment
- **POST /api/v1/appointments/{appointmentId}/payment:** Process advance payment

**Provider Dashboard APIs:**
- **GET /api/v1/providers/me/appointments:** Get provider appointments
- **PUT /api/v1/providers/me/appointments/{appointmentId}/status:** Update status
- **GET /api/v1/providers/me/analytics:** Get provider analytics
- **GET /api/v1/providers/me/calendar:** Get provider calendar view

**Implementation Requirements:**
- Build service management APIs
- Create availability calendar system
- Develop appointment booking APIs
- Implement intelligent scheduling logic
- Build advance payment processing
- Create provider dashboard APIs
- Develop waitlist management

### 6.6 Payment APIs

**Payment Processing APIs:**
- **POST /api/v1/payments/initiate:** Initiate payment
- **POST /api/v1/payments/confirm:** Confirm payment
- **GET /api/v1/payments/{paymentId}:** Get payment status
- **POST /api/v1/payments/{paymentId}/refund:** Process refund
- **GET /api/v1/payments:** Get payment history

**UPI Payment APIs:**
- **POST /api/v1/payments/upi/generate-qr:** Generate UPI QR code
- **POST /api/v1/payments/upi/verify:** Verify UPI payment
- **POST /api/v1/payments/upi/status:** Check UPI payment status

**BNPL Payment APIs:**
- **POST /api/v1/payments/bnpl/check-eligibility:** Check BNPL eligibility
- **POST /api/v1/payments/bnpl/initiate:** Initiate BNPL payment
- **POST /api/v1/payments/bnpl/confirm:** Confirm BNPL payment
- **GET /api/v1/payments/bnpl/installments:** Get installment schedule

**Transaction Management APIs:**
- **GET /api/v1/transactions:** Get transaction history
- **GET /api/v1/transactions/{transactionId}:** Get transaction details
- **POST /api/v1/transactions/{transactionId}/dispute:** Create dispute
- **GET /api/v1/transactions/reconciliation:** Get reconciliation data

**Implementation Requirements:**
- Integrate payment gateway APIs
- Build UPI payment processing
- Implement BNPL provider integrations
- Create refund processing workflows
- Develop transaction management
- Build payment reconciliation
- Implement fraud detection

### 6.7 UID Management APIs

**UID Generation APIs:**
- **POST /api/v1/uid/generate:** Generate new UID codes (seller)
- **POST /api/v1/uid/generate-bulk:** Generate multiple UIDs
- **GET /api/v1/uid/codes:** Get seller's UID codes
- **GET /api/v1/uid/{uidCode}:** Get UID details

**QR Code APIs:**
- **GET /api/v1/uid/{uidCode}/qr-code:** Get QR code image
- **POST /api/v1/uid/{uidCode}/qr-code/download:** Download QR code
- **GET /api/v1/uid/{uidCode}/qr-code/print:** Get print-ready QR code

**UID Verification APIs:**
- **POST /api/v1/uid/verify:** Verify UID code
- **POST /api/v1/uid/scan:** Scan and process QR code
- **GET /api/v1/uid/{uidCode}/seller:** Get seller information from UID

**UID Analytics APIs:**
- **GET /api/v1/uid/{uidCode}/analytics:** Get UID usage analytics
- **GET /api/v1/uid/{uidCode}/customers:** Get customers registered via UID
- **GET /api/v1/uid/analytics/overview:** Get overall UID analytics

**Implementation Requirements:**
- Build UID generation service
- Create QR code generation APIs
- Develop UID verification system
- Implement UID analytics tracking
- Build customer-seller relationship management
- Create UID distribution tools

### 6.8 Family Group APIs

**Family Group Management APIs:**
- **POST /api/v1/family-groups:** Create family group
- **GET /api/v1/family-groups/me:** Get user's family group
- **PUT /api/v1/family-groups/{groupId}:** Update family group
- **DELETE /api/v1/family-groups/{groupId}:** Delete family group

**Family Member APIs:**
- **POST /api/v1/family-groups/{groupId}/members:** Add family member
- **GET /api/v1/family-groups/{groupId}/members:** Get family members
- **PUT /api/v1/family-groups/{groupId}/members/{memberId}:** Update member
- **DELETE /api/v1/family-groups/{groupId}/members/{memberId}:** Remove member
- **PUT /api/v1/family-groups/{groupId}/members/{memberId}/role:** Update role

**Family Cart APIs:**
- **GET /api/v1/family-groups/{groupId}/cart:** Get family cart
- **POST /api/v1/family-groups/{groupId}/cart/items:** Add item to family cart
- **PUT /api/v1/family-groups/{groupId}/cart/items/{itemId}:** Update item
- **DELETE /api/v1/family-groups/{groupId}/cart/items/{itemId}:** Remove item
- **POST /api/v1/family-groups/{groupId}/cart/approve:** Approve purchase

**Family Expense APIs:**
- **GET /api/v1/family-groups/{groupId}/expenses:** Get family expenses
- **POST /api/v1/family-groups/{groupId}/expenses:** Record expense
- **GET /api/v1/family-groups/{groupId}/expenses/analytics:** Get expense analytics
- **GET /api/v1/family-groups/{groupId}/budget:** Get budget information
- **PUT /api/v1/family-groups/{groupId}/budget:** Update budget

**Implementation Requirements:**
- Build family group management APIs
- Create family member management
- Develop family cart synchronization
- Implement expense tracking APIs
- Build budget management APIs
- Create approval workflow APIs
- Develop real-time synchronization

### 6.9 Transportation APIs

**Vehicle Management APIs:**
- **POST /api/v1/transportation/vehicles:** Register vehicle
- **GET /api/v1/transportation/vehicles:** Get provider's vehicles
- **GET /api/v1/transportation/vehicles/{vehicleId}:** Get vehicle details
- **PUT /api/v1/transportation/vehicles/{vehicleId}:** Update vehicle
- **DELETE /api/v1/transportation/vehicles/{vehicleId}:** Delete vehicle

**GPS Tracking APIs:**
- **POST /api/v1/transportation/tracking/update:** Update GPS location
- **GET /api/v1/transportation/tracking/{bookingId}:** Get tracking data
- **GET /api/v1/transportation/tracking/{bookingId}/route:** Get route data
- **POST /api/v1/transportation/tracking/{bookingId}/share:** Share location

**Booking Management APIs:**
- **POST /api/v1/transportation/bookings:** Create transportation booking
- **GET /api/v1/transportation/bookings:** Get user bookings
- **GET /api/v1/transportation/bookings/{bookingId}:** Get booking details
- **PUT /api/v1/transportation/bookings/{bookingId}/cancel:** Cancel booking
- **POST /api/v1/transportation/bookings/{bookingId}/pricing:** Calculate pricing

**Implementation Requirements:**
- Build vehicle management APIs
- Integrate GPS tracking service
- Create booking management APIs
- Develop pricing calculation engine
- Implement route optimization
- Build real-time tracking system
- Create trip history APIs

### 6.10 Delivery Network APIs

**Agency Management APIs:**
- **POST /api/v1/delivery/agencies:** Register delivery agency
- **GET /api/v1/delivery/agencies:** Get agencies list
- **GET /api/v1/delivery/agencies/{agencyId}:** Get agency details
- **PUT /api/v1/delivery/agencies/{agencyId}:** Update agency
- **POST /api/v1/delivery/agencies/{agencyId}/verify:** Verify agency

**Team Management APIs:**
- **POST /api/v1/delivery/agencies/{agencyId}/agents:** Add delivery agent
- **GET /api/v1/delivery/agencies/{agencyId}/agents:** Get agents list
- **PUT /api/v1/delivery/agencies/{agencyId}/agents/{agentId}:** Update agent
- **DELETE /api/v1/delivery/agencies/{agencyId}/agents/{agentId}:** Remove agent

**Service Area APIs:**
- **POST /api/v1/delivery/agencies/{agencyId}/service-areas:** Define service area
- **GET /api/v1/delivery/agencies/{agencyId}/service-areas:** Get service areas
- **PUT /api/v1/delivery/agencies/{agencyId}/service-areas/{areaId}:** Update area

**Order Assignment APIs:**
- **POST /api/v1/delivery/orders/{orderId}/assign:** Assign order to agent
- **GET /api/v1/delivery/orders:** Get delivery orders
- **PUT /api/v1/delivery/orders/{orderId}/status:** Update delivery status
- **POST /api/v1/delivery/orders/{orderId}/proof:** Upload proof of delivery

**Implementation Requirements:**
- Build agency management APIs
- Create team management system
- Develop service area management
- Implement order assignment logic
- Build route optimization APIs
- Create delivery tracking system
- Develop commission calculation APIs

### 6.11 Chat & Communication APIs

**Messaging APIs:**
- **POST /api/v1/chat/conversations:** Create conversation
- **GET /api/v1/chat/conversations:** Get user conversations
- **GET /api/v1/chat/conversations/{conversationId}:** Get conversation details
- **POST /api/v1/chat/conversations/{conversationId}/messages:** Send message
- **GET /api/v1/chat/conversations/{conversationId}/messages:** Get messages
- **PUT /api/v1/chat/messages/{messageId}:** Update message
- **DELETE /api/v1/chat/messages/{messageId}:** Delete message

**WebSocket Events:**
- **message.sent:** New message sent event
- **message.delivered:** Message delivery confirmation
- **message.read:** Message read receipt
- **typing.start:** User started typing
- **typing.stop:** User stopped typing
- **user.online:** User came online
- **user.offline:** User went offline

**Media Sharing APIs:**
- **POST /api/v1/chat/upload:** Upload media file
- **GET /api/v1/chat/media/{mediaId}:** Get media file
- **DELETE /api/v1/chat/media/{mediaId}:** Delete media file

**Implementation Requirements:**
- Build RESTful messaging APIs
- Create WebSocket server for real-time messaging
- Implement media upload and sharing
- Develop conversation management
- Build notification system
- Create message search functionality
- Implement chat moderation tools

### 6.12 Analytics APIs

**Dashboard APIs:**
- **GET /api/v1/analytics/dashboard:** Get dashboard data
- **GET /api/v1/analytics/kpis:** Get KPI metrics
- **GET /api/v1/analytics/revenue:** Get revenue analytics
- **GET /api/v1/analytics/users:** Get user engagement metrics

**Report APIs:**
- **GET /api/v1/analytics/reports:** Get available reports
- **POST /api/v1/analytics/reports:** Create custom report
- **GET /api/v1/analytics/reports/{reportId}:** Get report data
- **POST /api/v1/analytics/reports/{reportId}/export:** Export report

**Real-time Analytics APIs:**
- **GET /api/v1/analytics/realtime/metrics:** Get real-time metrics
- **WebSocket /api/v1/analytics/realtime:** Subscribe to real-time updates

**Implementation Requirements:**
- Build analytics data aggregation
- Create dashboard API endpoints
- Develop custom report generation
- Implement real-time analytics streaming
- Build data export functionality
- Create analytics caching layer
- Develop predictive analytics APIs

---

## 7. Database Design

### 7.1 Database Architecture

**Database Strategy:**
- **Primary Database:** PostgreSQL 17 for transactional data (Medusa)
- **Medusa Database:** PostgreSQL with MikroORM for Medusa entities
- **Global Database:** Azure Cosmos DB for worldwide product catalogs (optional)
- **Caching Layer:** Redis 8.2 Cluster for high-performance caching
- **Search Engine:** Elasticsearch for full-text search and product discovery
- **File Storage:** Azure Blob Storage for media and documents
- **Workflow State:** Redis for Motia workflow execution state

**Multi-Tenant Architecture:**
- **Row-Level Security:** Tenant-based data isolation using company_id
- **Query Filtering:** Automatic tenant filtering in all database queries
- **Data Partitioning:** Partition large tables by tenant for performance
- **Backup Strategy:** Tenant-specific backup and recovery procedures
- **Compliance:** GDPR and regional compliance with data localization

**Database Design Principles:**
- **Normalization:** Third normal form (3NF) for data integrity
- **Indexing Strategy:** Strategic indexing for query performance
- **Foreign Key Constraints:** Referential integrity enforcement
- **Soft Deletes:** Logical deletion with deleted_at timestamps
- **Audit Trails:** Complete audit logging for all data changes
- **Versioning:** Optimistic locking with version fields

**Connection Management:**
- **Connection Pooling:** PgBouncer for PostgreSQL connection management
- **Read Replicas:** Read replicas for scaling read operations
- **Connection Limits:** Per-tenant connection limits
- **Query Timeout:** Configurable query timeouts for long-running queries
- **Transaction Management:** Proper transaction boundaries and isolation levels

### 7.2 Core Entity Models

**User Management Entities:**
- **Users:** Core user accounts with authentication credentials
- **User Profiles:** Extended user profile information
- **User Preferences:** User-specific settings and preferences
- **User Addresses:** Multiple shipping and billing addresses
- **User Sessions:** Active user sessions and token management

**Company & Tenant Entities:**
- **Companies:** Multi-tenant company/seller entities
- **Company Settings:** Company-specific configuration and settings
- **Company Branding:** Logo, colors, and branding assets
- **Company Subscriptions:** Subscription and billing information
- **Company Locations:** Multi-location support for companies

**UID System Entities:**
- **UID Codes:** Unique identifier codes for customer exclusivity
- **UID Relationships:** Customer-seller relationship mappings
- **UID Analytics:** Usage tracking and analytics data
- **QR Codes:** QR code generation and storage
- **UID Settings:** UID-specific configuration and rules

**Product Catalog Entities:**
- **Products:** Product master data with UID-based visibility
- **Product Variants:** Product variations (size, color, etc.)
- **Product Categories:** Hierarchical category structure
- **Product Attributes:** Industry-specific product attributes
- **Product Media:** Images, videos, and documents
- **Product Reviews:** Customer reviews and ratings
- **Inventory:** Stock levels and inventory tracking

**Order Management Entities:**
- **Orders:** Order header information
- **Order Items:** Individual order line items
- **Order Status History:** Order status change tracking
- **Order Shipments:** Shipping and delivery information
- **Order Tracking:** Real-time order tracking data

**Service Booking Entities:**
- **Services:** Service master data
- **Service Providers:** Service provider information
- **Service Categories:** Service categorization
- **Appointments:** Appointment bookings
- **Availability:** Provider availability calendar
- **Advance Payments:** Advance payment records
- **Service Reviews:** Service provider reviews

**Family Group Entities:**
- **Family Groups:** Family group master data
- **Family Members:** Family member relationships
- **Family Carts:** Shared shopping carts
- **Family Expenses:** Expense tracking records
- **Family Budgets:** Budget configuration and tracking
- **Approval Requests:** Purchase approval workflows

**Transportation Entities:**
- **Transportation Providers:** Provider registration
- **Vehicles:** Vehicle registration and details
- **Transportation Bookings:** Booking records
- **GPS Tracking:** Real-time location tracking data
- **Trip History:** Historical trip data

**Delivery Network Entities:**
- **Delivery Agencies:** Agency registration
- **Delivery Agents:** Agent information
- **Service Areas:** Geographic service area definitions
- **Delivery Requests:** Delivery order assignments
- **Delivery Tracking:** Real-time delivery tracking
- **Proof of Delivery:** Delivery confirmation data

**Payment Entities:**
- **Payments:** Payment transaction records
- **Payment Methods:** Saved payment methods
- **Refunds:** Refund transaction records
- **Payment Gateways:** Gateway configuration
- **Transaction History:** Complete transaction audit trail

**Chat & Communication Entities:**
- **Conversations:** Chat conversation records
- **Messages:** Individual message records
- **Media Files:** Shared media files
- **Message Status:** Read receipts and delivery status

**Analytics Entities:**
- **Analytics Events:** Event tracking data
- **User Analytics:** User behavior analytics
- **Business Metrics:** Aggregated business metrics
- **Custom Reports:** Report definitions and data

### 7.3 Relationships & Constraints

**Primary Relationships:**
- **Company → Users:** One-to-many relationship (company employs users)
- **Company → Products:** One-to-many relationship (company sells products)
- **Company → Services:** One-to-many relationship (company provides services)
- **Company → UIDs:** One-to-many relationship (company owns UIDs)
- **User → Orders:** One-to-many relationship (user places orders)
- **User → Family Groups:** Many-to-many relationship (user belongs to family groups)
- **UID → UID Relationships:** One-to-many relationship (UID connects customers to sellers)
- **Product → Product Variants:** One-to-many relationship (product has variants)
- **Order → Order Items:** One-to-many relationship (order contains items)
- **Service → Appointments:** One-to-many relationship (service has appointments)

**Foreign Key Constraints:**
- **Referential Integrity:** All foreign keys enforce referential integrity
- **Cascade Rules:** Appropriate CASCADE and RESTRICT rules for deletions
- **Indexed Foreign Keys:** All foreign keys indexed for join performance
- **Nullable Foreign Keys:** Strategic use of nullable foreign keys where appropriate

**Unique Constraints:**
- **Email Uniqueness:** Unique email addresses per user
- **Phone Uniqueness:** Unique phone numbers per user
- **UID Code Uniqueness:** Unique UID codes globally
- **SKU Uniqueness:** Unique SKUs per company
- **Order Number Uniqueness:** Unique order numbers globally

**Check Constraints:**
- **Data Validation:** Check constraints for data integrity
- **Status Values:** Enumerated status values with check constraints
- **Amount Validation:** Positive amount validation
- **Date Validation:** Date range validation
- **Email Format:** Email format validation

### 7.4 Indexing Strategy

**Primary Indexes:**
- **Primary Keys:** All tables have primary key indexes
- **Foreign Keys:** All foreign keys indexed for join performance
- **Unique Constraints:** Unique indexes for unique constraints

**Performance Indexes:**
- **User Lookups:** Indexes on email, phone, and user_id
- **Product Search:** Full-text search indexes on product names and descriptions
- **Order Queries:** Composite indexes on user_id, status, and created_at
- **UID Lookups:** Indexes on uid_code for fast UID resolution
- **Date Range Queries:** Indexes on timestamp columns for date range queries
- **Status Filters:** Indexes on status columns for filtering

**Composite Indexes:**
- **Multi-column Queries:** Composite indexes for common query patterns
- **Filtering + Sorting:** Indexes supporting both filtering and sorting
- **Join Optimization:** Indexes optimized for common join patterns

**Partial Indexes:**
- **Active Records:** Partial indexes on active records only
- **Status-based:** Partial indexes for specific status values
- **Tenant-specific:** Partial indexes for tenant-specific queries

**Index Maintenance:**
- **Regular Reindexing:** Scheduled index maintenance
- **Index Monitoring:** Monitor index usage and effectiveness
- **Index Optimization:** Remove unused indexes, add missing indexes
- **Query Plan Analysis:** Regular query plan analysis for optimization

### 7.5 Data Migration Strategy

**Migration Tools:**
- **Medusa Migrations:** Medusa's built-in migration system
- **MikroORM Migrations:** MikroORM migration tool for custom entities
- **Version Control:** All migrations version controlled in Git
- **Rollback Support:** Ability to rollback migrations if needed
- **Migration Scripts:** Custom migration scripts for data transformations

**Migration Process:**
- **Development:** Create migrations in development environment
- **Medusa Migrations:** Use `npx medusa migrations create` for Medusa entities
- **Custom Migrations:** Use MikroORM migrations for custom entities
- **Testing:** Test migrations in staging environment
- **Review:** Code review for migration scripts
- **Backup:** Backup production database before migration
- **Execution:** Execute migrations during maintenance window
- **Verification:** Verify migration success and data integrity
- **Rollback Plan:** Prepared rollback plan for failed migrations

**Data Migration Types:**
- **Schema Migrations:** Database structure changes (Medusa + custom)
- **Data Migrations:** Data transformation and migration
- **Seed Data:** Initial data seeding for new environments (`npm run seed`)
- **Reference Data:** Migration of reference data

**Migration Best Practices:**
- **Idempotent Migrations:** Migrations should be idempotent
- **Backward Compatibility:** Maintain backward compatibility where possible
- **Gradual Rollout:** Gradual rollout for large migrations
- **Monitoring:** Monitor migration progress and performance
- **Documentation:** Document all migrations with purpose and impact
- **Medusa Compatibility:** Ensure migrations are compatible with Medusa updates

---

## 8. Frontend Development

### 8.1 Web Application Development (Future Phase)

**Note:** Web application will be added in a future phase. The mobile-app structure is prepared with Solito integration to enable seamless code sharing when the Next.js web app is added.

**Planned Next.js Application Structure (Solito):**
- **App Router:** Next.js 16+ App Router for file-based routing
- **Solito Integration:** Unified codebase with mobile-app for code sharing
- **Server Components:** React Server Components for optimal performance
- **Client Components:** Client-side interactivity where needed
- **API Routes:** Next.js API routes for server-side endpoints
- **Middleware:** Next.js middleware for authentication and routing

**Component Architecture (When Web App Added):**
- **Solito Shared Components:** Components in `mobile-app/packages/app` shared with web
- **Atomic Design:** Component hierarchy (atoms, molecules, organisms, templates)
- **Platform-Specific Components:** Web-only components when needed
- **Feature Components:** Feature-specific components in shared packages
- **Layout Components:** Layout and page structure components
- **UI Components:** Shadcn/UI component library integration

**State Management (Shared with Mobile):**
- **Zustand Stores:** Lightweight state management (shared via Solito)
- **TanStack Query:** Server state management with caching (shared)
- **React Context:** Theme and user preference management
- **Local State:** useState and useReducer for component-level state
- **URL State:** Query parameters and route state management

**Data Fetching (Shared Patterns):**
- **Server Components:** Data fetching in Server Components
- **TanStack Query:** Client-side data fetching with caching (shared with mobile)
- **Shared API Client:** Unified API client in `mobile-app/packages/app`
- **Real-time Updates:** WebSocket integration for live data
- **Optimistic Updates:** Optimistic UI updates for better UX

**Form Handling (Shared):**
- **React Hook Form:** Form library with minimal re-renders
- **Zod Validation:** Schema validation shared with backend and mobile
- **Form State Management:** Form state and error handling
- **File Uploads:** Image and document upload handling
- **Form Submission:** Async form submission with loading states

**Routing & Navigation (Solito Unified):**
- **File-based Routing:** Next.js App Router file-based routing
- **Solito Navigation:** Unified navigation patterns with mobile
- **Dynamic Routes:** Dynamic route segments and parameters
- **Route Protection:** Authentication and authorization guards
- **Deep Linking:** Deep linking support for UID/QR codes
- **Navigation Guards:** Route guards for protected pages

**Performance Optimization:**
- **Code Splitting:** Automatic code splitting with Next.js
- **Image Optimization:** Next.js Image component for optimized images
- **Font Optimization:** Next.js font optimization
- **Bundle Analysis:** Webpack bundle analyzer for optimization
- **Lazy Loading:** Lazy loading for components and routes
- **Caching Strategy:** Static and dynamic caching strategies
- **Shared Code Optimization:** Solito enables code sharing without duplication

### 8.2 Mobile Application Development (Solito-Enhanced)

**React Native Application Structure:**
- **Location:** `mobile-app/` directory (Solito-enhanced structure)
- **Expo Router:** File-based routing with Expo Router (`src/app/`)
- **Solito Integration:** Shared code in `mobile-app/packages/app` ready for web sharing
- **Screen Components:** Screen-level components in `src/screens/` and `src/app/`
- **Navigation:** Stack and tab navigation (Expo Router with Solito patterns)
- **Native Modules:** Custom native modules for platform-specific features
- **Expo SDK:** Expo SDK for managed workflow

**Component Architecture:**
- **Mobile Components:** React Native components in `src/components/`
- **Solito Shared Components:** Components in `mobile-app/packages/app/components` (ready for web sharing)
- **Platform-specific Components:** Native components for mobile-only features
- **Navigation Components:** Navigation and routing components (Expo Router)
- **UI Components:** NativeWind and custom UI components in `src/components/ui/`
- **Form Components:** Mobile-optimized form components

**State Management:**
- **Zustand:** Lightweight state management (ready for web sharing via Solito)
- **TanStack Query:** Server state synchronization (ready for web sharing)
- **MMKV:** Fast local storage for mobile-specific data
- **Context API:** Theme and user preference management
- **Query Persistence:** TanStack Query cache persistence

**Solito Package Structure:**
- **Location:** `mobile-app/packages/app/`
- **Components:** Shared React components (works on web & mobile when web app added)
- **Features:** Feature modules with screens (`mobile-app/packages/app/features/`)
- **Navigation:** Navigation configuration (`mobile-app/packages/app/navigation/`)
- **Providers:** Context providers (`mobile-app/packages/app/provider/`)
- **Utils:** Utility functions (`mobile-app/packages/app/utils/`)

**Navigation:**
- **Expo Router:** File-based routing (Solito integration)
- **Solito Navigation:** Unified navigation patterns with web
- **Stack Navigation:** Hierarchical navigation
- **Tab Navigation:** Bottom tab navigation
- **Deep Linking:** UID/QR code deep linking
- **Navigation Guards:** Authentication guards

**Native Features:**
- **Camera Integration:** QR code scanning with camera
- **GPS Tracking:** Location services and GPS tracking
- **Push Notifications:** Expo Notifications with Firebase
- **Biometric Auth:** Face ID, Touch ID, Fingerprint
- **File System:** Document and image handling
- **Offline Support:** Offline functionality with sync

**Performance Optimization:**
- **Code Splitting:** Metro bundler code splitting
- **Image Optimization:** Optimized image loading
- **List Optimization:** FlatList and VirtualizedList optimization
- **Memory Management:** Memory optimization for large lists
- **Bundle Size:** Bundle size optimization
- **Native Performance:** Native module optimization
- **Shared Code Benefits:** Solito enables code sharing without bundle bloat

### 8.3 Shared Components & Logic (Solito)

**Solito Shared Package (`mobile-app/packages/app`):**
- **Location:** Shared code within mobile-app directory
- **Components:** React components ready to be shared with future Next.js app
- **Features:** Feature modules with screens (`mobile-app/packages/app/features/`)
- **Navigation:** Unified navigation configuration (`mobile-app/packages/app/navigation/`)
- **Providers:** Context providers for theme, navigation, safe area (`mobile-app/packages/app/provider/`)
- **Utils:** Utility functions shared between platforms (`mobile-app/packages/app/utils/`)
- **Types:** TypeScript types shared across platforms

**Component Sharing Strategy:**
- **Mobile-First Structure:** Current structure in `mobile-app/src/` for mobile-specific code
- **Shared Components:** UI components in `mobile-app/packages/app/components` ready for web
- **Feature Modules:** Feature screens in `mobile-app/packages/app/features` ready for web
- **Platform Detection:** Use platform-specific code when needed
- **Conditional Rendering:** Platform-specific rendering with Solito utilities
- **Native Components:** Platform-specific components in `mobile-app/src/components/`

**Code Reusability:**
- **DRY Principle:** Don't Repeat Yourself principle enforced by Solito
- **Single Source of Truth:** Shared types, constants, and components in `mobile-app/packages/app`
- **Platform Abstraction:** Platform-agnostic business logic in shared package
- **Solito Utilities:** Platform detection and conditional rendering helpers
- **Feature Flags:** Feature flags for platform-specific features

**Solito Benefits:**
- **Unified Codebase:** Write once, run on web and mobile (when web app added)
- **Type Safety:** Shared TypeScript types across platforms
- **Navigation Consistency:** Unified navigation patterns
- **State Management:** Shared state management (Zustand, TanStack Query)
- **Styling:** Shared TailwindCSS/NativeWind styling
- **Future-Ready:** Structure prepared for seamless web app integration

### 8.4 State Management

**State Management Strategy:**
- **Server State:** TanStack Query for server state
- **Client State:** Zustand/Redux for client state
- **Form State:** React Hook Form for form state
- **URL State:** Query parameters for URL state
- **Cache Strategy:** Caching strategy for different data types

**State Persistence:**
- **Web:** localStorage and sessionStorage
- **Mobile:** Redux Persist with MMKV
- **Offline Support:** Offline state persistence
- **Sync Strategy:** Data synchronization on reconnect
- **Conflict Resolution:** Conflict resolution for offline changes

### 8.5 Routing & Navigation

**Web Routing (Future Phase):**
- **Next.js App Router:** File-based routing system (when web app added)
- **Dynamic Routes:** Dynamic route segments
- **Route Groups:** Route organization with groups
- **Layouts:** Nested layouts for page structure
- **Loading States:** Loading UI for route transitions
- **Solito Integration:** Shared routing patterns with mobile

**Mobile Navigation (Current):**
- **Location:** `mobile-app/src/app/` (Expo Router)
- **Expo Router:** File-based routing with Expo Router
- **Stack Navigation:** Stack-based navigation
- **Tab Navigation:** Tab-based navigation
- **Modal Navigation:** Modal presentation
- **Deep Linking:** Deep linking support for UID/QR codes
- **Solito Patterns:** Navigation patterns ready for web sharing

**Navigation Guards:**
- **Authentication:** Route protection for authenticated routes
- **Authorization:** Permission-based route access
- **UID Routing:** UID-based route filtering
- **Redirects:** Automatic redirects based on user state

### 8.6 UI/UX Implementation

**Design System:**
- **Design Tokens:** Colors, typography, spacing tokens
- **Component Library:** Shadcn/UI component library
- **Theme System:** Light and dark theme support
- **Responsive Design:** Mobile-first responsive design
- **Accessibility:** WCAG 2.1 AA compliance

**User Experience:**
- **Loading States:** Skeleton loaders and loading indicators
- **Error States:** User-friendly error messages
- **Empty States:** Helpful empty state designs
- **Success Feedback:** Success notifications and confirmations
- **Form Validation:** Real-time form validation with helpful errors

**Internationalization:**
- **Multi-language Support:** React i18next integration
- **Language Detection:** Automatic language detection
- **RTL Support:** Right-to-left layout support
- **Locale Formatting:** Date, time, and number formatting
- **Translation Management:** Translation key management

### 8.7 Performance Optimization

**Web Performance:**
- **Core Web Vitals:** Optimize LCP, FID, CLS metrics
- **Image Optimization:** Next.js Image optimization
- **Code Splitting:** Automatic code splitting
- **Caching:** Static and dynamic caching
- **CDN:** Content delivery network for static assets

**Mobile Performance:**
- **Bundle Size:** Optimize bundle size
- **Startup Time:** Fast app startup
- **List Performance:** Optimize list rendering
- **Memory Usage:** Memory optimization
- **Battery Usage:** Battery-efficient operations

---

## 9. Backend Development

### 9.1 API Development

**Medusa API Architecture:**
- **Medusa Store API:** Customer-facing RESTful API for e-commerce operations
- **Medusa Admin API:** Admin dashboard RESTful API for management operations
- **Medusa GraphQL:** GraphQL endpoints for complex queries
- **Custom API Routes:** Custom routes in `src/api/store/custom` and `src/api/admin/custom`
- **API Versioning:** Medusa API versioning strategy
- **Error Handling:** Consistent error response format
- **Request Validation:** Input validation with Zod and Medusa validators

**Motia Workflow API:**
- **HTTP Triggers:** HTTP-based workflow trigger endpoints
- **Workflow Execution API:** API for executing workflows programmatically
- **Workflow Management API:** API for creating, updating, and managing workflows
- **Node Execution API:** API for executing individual workflow nodes
- **Metrics API:** API for workflow metrics and monitoring

**API Endpoints:**
- **Resource-based URLs:** RESTful URL structure (Medusa)
- **Workflow URLs:** Workflow-specific URL patterns (Motia)
- **HTTP Methods:** Proper use of GET, POST, PUT, DELETE
- **Status Codes:** Appropriate HTTP status codes
- **Response Format:** Standardized JSON response format
- **Pagination:** Cursor and offset-based pagination (Medusa)

**API Documentation:**
- **Medusa API Docs:** Medusa's built-in API documentation
- **OpenAPI Specification:** OpenAPI 3.0 documentation
- **Swagger UI:** Interactive API documentation
- **Code Examples:** Code samples in multiple languages
- **Postman Collection:** Postman collection for testing
- **SDK Generation:** Auto-generated SDKs

### 9.2 Business Logic Implementation

**Medusa Service Layer:**
- **Medusa Services:** Business logic in Medusa service classes (`src/services/`)
- **Custom Services:** Custom business logic services extending Medusa services
- **Transaction Management:** Medusa's built-in transaction handling
- **Error Handling:** Business logic error handling with Medusa error types
- **Validation:** Business rule validation with Medusa validators
- **Service Extension:** Extend Medusa services for custom functionality

**Motia Workflow Layer:**
- **Workflow Steps:** Modular workflow steps in `src/steps/`
- **Workflow Execution:** Workflow orchestration and execution engine
- **Node System:** Reusable workflow nodes for common operations
- **Step Composition:** Compose complex workflows from simple steps
- **Error Handling:** Workflow error handling and retry logic

**Business Rules:**
- **UID Logic:** UID-based customer exclusivity rules (custom Medusa service)
- **Pricing Engine:** Dynamic pricing calculations (Medusa pricing service)
- **Inventory Management:** Stock reservation and management (Medusa inventory)
- **Order Processing:** Order creation and processing (Medusa workflows + Motia)
- **Payment Processing:** Payment gateway integration (Medusa payment providers)

**Event-Driven Architecture:**
- **Medusa Events:** Built-in event system for e-commerce operations
- **Event Subscribers:** Subscribe to Medusa events in `src/subscribers/`
- **Workflow Events:** Motia workflow event triggers
- **Event Publishing:** Publish events for state changes
- **Event Sourcing:** Event sourcing for audit trails
- **CQRS:** Command Query Responsibility Segregation
- **Message Queues:** Asynchronous task processing (Medusa jobs)

### 9.3 Data Access Layer

**Medusa Data Access:**
- **MikroORM:** Medusa's ORM for database operations
- **Repository Pattern:** Medusa repository classes for data access
- **Query Builders:** Type-safe query building with MikroORM
- **Transaction Management:** Medusa's transaction handling
- **Connection Management:** Database connection pooling
- **Query Optimization:** Optimized database queries

**Medusa Entity Management:**
- **Entity Extensions:** Extend Medusa entities for custom fields
- **Custom Entities:** Create custom entities when needed
- **Migration Management:** Medusa migration system
- **Type Safety:** Type-safe database operations with MikroORM
- **Relationship Management:** Entity relationship handling

**Caching Strategy:**
- **Redis Caching:** Redis for caching layer
- **Medusa Cache:** Medusa's built-in caching mechanisms
- **Cache Invalidation:** Cache invalidation strategies
- **Cache Patterns:** Write-through, write-back, cache-aside
- **TTL Management:** Time-to-live for cached data
- **Cache Warming:** Pre-populate cache with frequently accessed data

**Workflow Data:**
- **Workflow State:** Workflow execution state management
- **Node Data:** Workflow node data storage
- **Execution History:** Workflow execution history tracking
- **Metrics Storage:** Workflow metrics and analytics storage

### 9.4 Service Layer Architecture

**Medusa Module Architecture:**
- **Medusa Modules:** Extensible module system for custom features
- **Module Boundaries:** Clear module boundaries and responsibilities
- **Module Communication:** Module-to-module communication patterns
- **Module Registration:** Module registration and initialization
- **Module Dependencies:** Module dependency management

**Motia Workflow Architecture:**
- **Workflow Engine:** Central workflow execution engine
- **Node System:** Reusable workflow nodes
- **Step Execution:** Modular step-based execution
- **Workflow Composition:** Compose workflows from nodes and steps
- **Workflow Versioning:** Workflow version management

**Service Design:**
- **Single Responsibility:** Each service/module has single responsibility
- **Loose Coupling:** Services are loosely coupled
- **High Cohesion:** Services have high internal cohesion
- **API Contracts:** Well-defined API contracts (Medusa APIs)
- **Versioning:** Service versioning strategy
- **Medusa Integration:** Custom services integrate with Medusa core
- **Motia Integration:** Workflows integrate with Medusa via steps

### 9.5 Event-Driven Architecture

**Medusa Event System:**
- **Medusa Events:** Built-in event system for e-commerce operations
- **Event Publishing:** Publish events for state changes (orders, products, etc.)
- **Event Subscribers:** Subscribe to events in `src/subscribers/`
- **Event Types:** Order events, product events, customer events, etc.
- **Event Payloads:** Structured event payloads
- **Event Versioning:** Event schema versioning

**Motia Workflow Events:**
- **Workflow Triggers:** HTTP and event-based workflow triggers
- **Workflow Events:** Workflow execution events
- **Node Events:** Individual node execution events
- **Step Events:** Step execution events
- **Event-Driven Workflows:** Workflows triggered by Medusa events

**Message Queues:**
- **Medusa Jobs:** Built-in job queue system
- **Bull Queue:** Redis-based job queue (if needed)
- **Task Processing:** Asynchronous task processing
- **Retry Logic:** Automatic retry for failed tasks
- **Dead Letter Queue:** Failed task handling
- **Workflow Jobs:** Motia workflow background execution

### 9.6 Caching Strategy

**Caching Layers:**
- **L1 Cache:** Application-level in-memory cache
- **L2 Cache:** Redis distributed cache
- **CDN Cache:** Cloudflare CDN caching
- **Browser Cache:** HTTP caching headers
- **Database Query Cache:** Database-level query caching

**Cache Patterns:**
- **Cache-Aside:** Application manages cache
- **Write-Through:** Write to cache and database
- **Write-Back:** Write to cache, async to database
- **Refresh-Ahead:** Proactive cache refresh
- **Cache Invalidation:** Event-driven cache invalidation

---

## 10. Security Implementation

### 10.1 Authentication & Authorization

**Authentication Mechanisms:**
- **JWT Tokens:** Stateless authentication with JWT
- **Refresh Tokens:** Secure token rotation mechanism
- **OAuth 2.0:** Social media login integration
- **MFA:** Multi-factor authentication (TOTP, SMS)
- **Biometric Auth:** Face ID, Touch ID, Fingerprint (mobile)

**Authorization:**
- **Role-Based Access Control (RBAC):** Role-based permissions
- **Permission System:** Granular permission management
- **UID-Based Access:** UID-based customer exclusivity
- **Resource-Level Permissions:** Resource-specific access control
- **Dynamic Permissions:** Context-aware permission assignment

**Security Best Practices:**
- **Password Policy:** Strong password requirements
- **Account Lockout:** Account lockout after failed attempts
- **Session Management:** Secure session handling
- **Token Expiration:** Short-lived access tokens
- **Secure Storage:** Secure token storage (httpOnly cookies, secure storage)

### 10.2 Data Encryption

**Encryption at Rest:**
- **Database Encryption:** AES-256 encryption for sensitive data
- **File Encryption:** Encrypted file storage
- **Backup Encryption:** Encrypted backups
- **Key Management:** Azure Key Vault for key storage
- **Key Rotation:** Regular key rotation

**Encryption in Transit:**
- **TLS 1.3:** TLS 1.3 for all communications
- **HTTPS:** HTTPS for all web traffic
- **API Encryption:** Encrypted API communications
- **Certificate Management:** Automated certificate management
- **Perfect Forward Secrecy:** PFS for secure communications

**Field-Level Encryption:**
- **PII Encryption:** Encrypt personally identifiable information
- **Payment Data:** PCI DSS compliant encryption
- **Sensitive Fields:** Encrypt sensitive data fields
- **Encryption Keys:** Secure key management

### 10.3 API Security

**API Security Measures:**
- **Rate Limiting:** Request throttling and rate limiting
- **API Keys:** Secure API key management
- **Request Validation:** Input validation and sanitization
- **SQL Injection Prevention:** Parameterized queries
- **XSS Prevention:** Cross-site scripting prevention
- **CSRF Protection:** Cross-site request forgery protection

**API Gateway Security:**
- **Authentication:** Centralized authentication
- **Authorization:** Centralized authorization
- **Request Filtering:** Malicious request filtering
- **DDoS Protection:** Distributed denial-of-service protection
- **WAF:** Web Application Firewall integration

### 10.4 Input Validation

**Validation Strategy:**
- **Schema Validation:** Zod schema validation
- **Type Validation:** Type checking for all inputs
- **Format Validation:** Format validation (email, phone, etc.)
- **Range Validation:** Value range validation
- **Sanitization:** Input sanitization to prevent injection attacks

**Validation Layers:**
- **Client-Side Validation:** Real-time client-side validation
- **Server-Side Validation:** Server-side validation (mandatory)
- **Database Constraints:** Database-level constraints
- **Business Rule Validation:** Business logic validation

### 10.5 Security Best Practices

**Security Standards:**
- **OWASP Top 10:** Address OWASP Top 10 vulnerabilities
- **PCI DSS:** Payment Card Industry compliance
- **GDPR:** General Data Protection Regulation compliance
- **Security Audits:** Regular security audits
- **Penetration Testing:** Regular penetration testing

**Security Monitoring:**
- **Security Logging:** Comprehensive security event logging
- **Intrusion Detection:** Intrusion detection and prevention
- **Anomaly Detection:** Anomaly detection for suspicious activity
- **Alerting:** Real-time security alerts
- **Incident Response:** Security incident response procedures

---

## 11. Integration Requirements

### 11.1 Payment Gateway Integration

**Payment Gateway Integration:**
- **Stripe Integration:** Stripe payment processing
- **PayPal Integration:** PayPal payment processing
- **UPI Integration:** UPI payment processing (Google Pay, PhonePe, Paytm, BHIM)
- **BNPL Integration:** Buy Now Pay Later providers (Simpl, LazyPay, ZestMoney)
- **Multi-Gateway Support:** Support for multiple payment gateways
- **Failover Strategy:** Automatic failover between gateways

**Payment Processing:**
- **Payment Initiation:** Secure payment initiation
- **Payment Confirmation:** Payment confirmation handling
- **Refund Processing:** Automated refund processing
- **Transaction Reconciliation:** Payment reconciliation
- **Fraud Detection:** Real-time fraud detection

### 11.2 Third-Party Service Integration

**External Services:**
- **Email Service:** SendGrid, SMTP for email delivery
- **SMS Service:** Twilio for SMS notifications
- **Push Notifications:** Firebase Cloud Messaging
- **Maps & GPS:** Google Maps, Mapbox for location services
- **Analytics:** Google Analytics, custom analytics
- **Social Login:** OAuth 2.0 for social media login

**Integration Patterns:**
- **API Integration:** RESTful API integration
- **Webhook Integration:** Webhook-based integration
- **Event-Driven Integration:** Event-driven integration
- **Retry Logic:** Automatic retry for failed integrations
- **Error Handling:** Comprehensive error handling

### 11.3 GPS & Location Services

**GPS Integration:**
- **Google Maps API:** Google Maps integration
- **Mapbox API:** Mapbox integration
- **Location Services:** Native location services
- **Geocoding:** Address to coordinates conversion
- **Reverse Geocoding:** Coordinates to address conversion
- **Route Optimization:** Route calculation and optimization

**Location Features:**
- **Real-time Tracking:** Real-time GPS tracking
- **Geofencing:** Geographic boundary management
- **Location Sharing:** Share location with users
- **Trip History:** Historical location data
- **Privacy Controls:** Location privacy controls

### 11.4 Notification Services

**Notification Channels:**
- **Email Notifications:** Email delivery via SendGrid
- **SMS Notifications:** SMS delivery via Twilio
- **Push Notifications:** Mobile push notifications via Firebase
- **In-App Notifications:** In-app notification system
- **Web Push:** Web push notifications

**Notification Management:**
- **Template System:** Notification templates
- **Personalization:** Personalized notifications
- **Delivery Tracking:** Notification delivery tracking
- **Preference Management:** User notification preferences
- **Batching:** Batch notification delivery

### 11.5 Analytics Integration

**Analytics Services:**
- **Google Analytics:** Web analytics integration
- **Custom Analytics:** Custom analytics implementation
- **Event Tracking:** User event tracking
- **Conversion Tracking:** Conversion funnel tracking
- **Performance Monitoring:** Application performance monitoring

**Analytics Implementation:**
- **Event Collection:** Comprehensive event collection
- **Data Processing:** Analytics data processing
- **Reporting:** Analytics reporting and dashboards
- **Privacy Compliance:** GDPR-compliant analytics
- **Data Retention:** Analytics data retention policies

---

## 12. Testing Requirements

### 12.1 Testing Strategy

**Testing Approach:**
- **Test Pyramid:** Unit tests, integration tests, E2E tests
- **Test Coverage:** Minimum 80% code coverage
- **Test Automation:** Automated test execution
- **CI/CD Integration:** Tests in CI/CD pipeline
- **Test Data Management:** Test data management strategy

**Testing Types:**
- **Unit Testing:** Component and function unit tests
- **Integration Testing:** Service integration tests
- **End-to-End Testing:** Complete user flow tests
- **Performance Testing:** Load and performance tests
- **Security Testing:** Security vulnerability tests

### 12.2 Unit Testing

**Unit Test Requirements:**
- **Test Framework:** Jest for unit testing
- **Test Coverage:** High coverage for business logic
- **Mocking:** Mock external dependencies
- **Test Isolation:** Isolated test execution
- **Fast Execution:** Fast test execution for quick feedback

**Unit Test Best Practices:**
- **Test Naming:** Descriptive test names
- **Test Organization:** Organized test structure
- **Assertions:** Clear and meaningful assertions
- **Test Data:** Realistic test data
- **Edge Cases:** Test edge cases and error scenarios

### 12.3 Integration Testing

**Integration Test Requirements:**
- **API Testing:** API endpoint integration tests
- **Database Testing:** Database integration tests
- **Service Testing:** Microservice integration tests
- **Third-Party Integration:** External service integration tests
- **End-to-End Flows:** Complete flow integration tests

**Integration Test Best Practices:**
- **Test Environment:** Dedicated test environment
- **Test Data:** Isolated test data
- **Cleanup:** Proper test cleanup
- **Test Isolation:** Isolated test execution
- **Error Scenarios:** Test error and failure scenarios

### 12.4 End-to-End Testing

**E2E Test Requirements:**
- **Web E2E:** Playwright for web E2E testing
- **Mobile E2E:** Detox for mobile E2E testing
- **User Flows:** Critical user flow testing
- **Cross-Browser:** Cross-browser testing
- **Cross-Platform:** Cross-platform testing

**E2E Test Best Practices:**
- **Test Scenarios:** Realistic user scenarios
- **Test Data:** Production-like test data
- **Test Stability:** Stable and reliable tests
- **Test Maintenance:** Maintainable test code
- **Visual Testing:** Visual regression testing

### 12.5 Performance Testing

**Performance Test Requirements:**
- **Load Testing:** Load testing for expected traffic
- **Stress Testing:** Stress testing for peak loads
- **Performance Benchmarks:** Performance benchmark validation
- **Response Time:** Response time validation
- **Throughput:** Throughput validation

**Performance Test Tools:**
- **Load Testing Tools:** k6, Artillery for load testing
- **Monitoring:** Performance monitoring during tests
- **Bottleneck Identification:** Identify performance bottlenecks
- **Optimization:** Performance optimization based on results

### 12.6 Security Testing

**Security Test Requirements:**
- **Vulnerability Scanning:** Automated vulnerability scanning
- **Penetration Testing:** Regular penetration testing
- **Security Audits:** Security code audits
- **OWASP Testing:** OWASP Top 10 testing
- **Compliance Testing:** Security compliance validation

**Security Test Best Practices:**
- **Regular Testing:** Regular security testing schedule
- **Automated Scanning:** Automated security scanning
- **Manual Testing:** Manual security testing
- **Remediation:** Security issue remediation
- **Documentation:** Security test documentation

---

## 13. Performance Requirements

### 13.1 Performance Targets

**Response Time Targets:**
- **API Endpoints:** 95th percentile < 500ms
- **Database Queries:** Complex queries < 1 second
- **Search Results:** Full-text search < 300ms
- **GPS Tracking Updates:** ≤ 5 seconds
- **Family Cart Sync:** Real-time within 1 second
- **Payment Processing:** ≤ 3 seconds

**Throughput Targets:**
- **API Requests:** 10,000+ requests per second
- **Database Transactions:** 5,000+ transactions per second
- **Concurrent Users:** Support 100,000+ concurrent users
- **Real-time Connections:** 50,000+ WebSocket connections

### 13.2 Optimization Strategies

**Frontend Optimization:**
- **Code Splitting:** Automatic code splitting
- **Image Optimization:** Optimized image delivery
- **Caching:** Aggressive caching strategy
- **Lazy Loading:** Lazy load components and routes
- **Bundle Optimization:** Optimize JavaScript bundles

**Backend Optimization:**
- **Database Optimization:** Query optimization and indexing
- **Caching:** Multi-layer caching strategy
- **Connection Pooling:** Efficient connection pooling
- **Async Processing:** Asynchronous task processing
- **Load Balancing:** Load balancing across instances

### 13.3 Monitoring & Metrics

**Performance Monitoring:**
- **Application Monitoring:** OpenTelemetry for application monitoring
- **Infrastructure Monitoring:** Prometheus and Grafana
- **Real-time Metrics:** Real-time performance metrics
- **Alerting:** Performance alerting and notifications
- **Dashboards:** Performance dashboards

**Key Metrics:**
- **Response Time:** API response time metrics
- **Error Rate:** Error rate monitoring
- **Throughput:** Request throughput metrics
- **Resource Usage:** CPU, memory, disk usage
- **Database Performance:** Database query performance

---

## 14. Deployment & DevOps

### 14.1 CI/CD Pipeline

**CI/CD Strategy:**
- **GitHub Actions:** CI/CD platform
- **Automated Testing:** Automated test execution
- **Automated Builds:** Automated build process
- **Automated Deployment:** Automated deployment to environments
- **Rollback Capability:** Quick rollback capability

**Pipeline Stages:**
- **Build Stage:** Code compilation and bundling
- **Test Stage:** Automated test execution
- **Security Scan:** Security vulnerability scanning
- **Deploy Stage:** Deployment to target environment
- **Verification Stage:** Post-deployment verification

### 14.2 Environment Management

**Environments:**
- **Development:** Local development environment
- **Staging:** Staging environment for testing
- **Production:** Production environment
- **Environment Configuration:** Environment-specific configuration
- **Secrets Management:** Secure secrets management

**Environment Best Practices:**
- **Environment Parity:** Similar environments across stages
- **Configuration Management:** Centralized configuration
- **Secrets Rotation:** Regular secrets rotation
- **Access Control:** Environment access control
- **Monitoring:** Environment monitoring

### 14.3 Deployment Strategy

**Deployment Methods:**
- **Blue-Green Deployment:** Zero-downtime deployment
- **Canary Deployment:** Gradual rollout deployment
- **Rolling Deployment:** Rolling update deployment
- **Feature Flags:** Feature flag-based deployment
- **Database Migrations:** Safe database migration strategy

**Deployment Best Practices:**
- **Zero Downtime:** Zero-downtime deployments
- **Health Checks:** Application health checks
- **Rollback Plan:** Prepared rollback plan
- **Monitoring:** Post-deployment monitoring
- **Documentation:** Deployment documentation

### 14.4 Monitoring & Logging

**Monitoring:**
- **Application Monitoring:** OpenTelemetry, New Relic
- **Infrastructure Monitoring:** Prometheus, Grafana
- **Real-time Alerts:** Real-time alerting
- **Dashboards:** Monitoring dashboards
- **Log Aggregation:** Centralized log aggregation

**Logging:**
- **Structured Logging:** Structured logging with Winston
- **Log Levels:** Appropriate log levels
- **Log Retention:** Log retention policies
- **Log Analysis:** Log analysis and search
- **Audit Logging:** Complete audit logging

---

## 15. Development Best Practices

### 15.1 Code Standards

**Code Quality:**
- **TypeScript:** Strict TypeScript configuration
- **ESLint:** Code linting with ESLint
- **Prettier:** Code formatting with Prettier
- **Code Review:** Mandatory code reviews
- **Documentation:** Code documentation standards

**Code Organization:**
- **File Structure:** Consistent file structure
- **Naming Conventions:** Consistent naming conventions
- **Module Organization:** Logical module organization
- **Separation of Concerns:** Clear separation of concerns
- **DRY Principle:** Don't Repeat Yourself

### 15.2 Git Workflow

**Git Strategy:**
- **Branch Strategy:** Feature branch workflow
- **Commit Messages:** Conventional commit messages
- **Pull Requests:** Pull request process
- **Code Review:** Code review requirements
- **Merge Strategy:** Merge and rebase strategy

**Git Best Practices:**
- **Small Commits:** Small, focused commits
- **Descriptive Messages:** Clear commit messages
- **Branch Naming:** Consistent branch naming
- **Clean History:** Clean git history
- **Backup:** Regular backups

### 15.3 Code Review Process

**Code Review Requirements:**
- **Mandatory Reviews:** All code requires review
- **Review Checklist:** Code review checklist
- **Review Feedback:** Constructive feedback
- **Approval Process:** Approval before merge
- **Automated Checks:** Automated code quality checks

**Review Best Practices:**
- **Timely Reviews:** Quick review turnaround
- **Constructive Feedback:** Helpful and constructive feedback
- **Learning Opportunity:** Use reviews for learning
- **Documentation:** Review documentation updates
- **Testing:** Review test coverage

### 15.4 Documentation Standards

**Documentation Requirements:**
- **API Documentation:** Complete API documentation
- **Code Documentation:** Inline code documentation
- **README Files:** Comprehensive README files
- **Architecture Documentation:** Architecture documentation
- **User Guides:** User and developer guides

**Documentation Best Practices:**
- **Keep Updated:** Keep documentation current
- **Clear and Concise:** Clear and concise documentation
- **Examples:** Include code examples
- **Diagrams:** Use diagrams where helpful
- **Accessibility:** Make documentation accessible

---

## 16. Feature Implementation Roadmap

### 16.1 Phase 1: Foundation

**Months 1-2: Core Infrastructure**
- Multi-platform architecture setup
- Development environment configuration
- Database schema design and migrations
- Authentication and authorization system
- UID/QR Code generation and validation
- Basic API structure

**Months 3-4: Core Features**
- User management and profiles
- Product catalog management
- Shopping cart functionality
- Basic order management
- Payment gateway integration
- Admin dashboard foundation

### 16.2 Phase 2: Core Features

**Months 5-6: E-Commerce Enhancement**
- Advanced product search
- Order tracking and management
- Inventory management
- Review and rating system
- Seller dashboard
- Customer dashboard

**Months 7-8: Service Booking**
- Service provider registration
- Availability calendar
- Appointment booking system
- Intelligent scheduling engine
- Advance payment system
- Service provider dashboard

**Months 9-10: Family Groups**
- Family group creation and management
- Shared shopping cart
- Expense tracking
- Approval workflows
- Budget management
- Family analytics

### 16.3 Phase 3: Advanced Features

**Months 11-12: Transportation & Delivery**
- Transportation service registration
- GPS tracking integration
- Vehicle management
- Delivery agency network
- Route optimization
- Real-time tracking

**Months 13-14: Advanced Features**
- Chat and messaging system
- Advanced analytics and reporting
- Custom report builder
- Multi-language support
- Advanced payment methods (UPI, BNPL)
- Performance optimization

**Months 15-18: Polish & Scale**
- Performance optimization
- Security hardening
- Scalability improvements
- Advanced monitoring
- Documentation completion
- Production readiness

---

## 17. Error Handling & Recovery Specifications

### 17.1 Error Classification Framework

**System Error Categories:**

**Critical Errors:**
- System crashes requiring immediate intervention
- Data corruption or loss scenarios
- Security breaches or unauthorized access
- Complete service unavailability

**Major Errors:**
- Partial system degradation affecting core functionality
- Performance degradation beyond acceptable thresholds
- Data inconsistencies requiring manual intervention
- Integration failures with critical third-party services

**Minor Errors:**
- Individual user request failures
- Non-critical feature malfunctions
- Performance warnings and alerts
- Temporary service disruptions

**Informational Events:**
- System warnings and notifications
- Performance monitoring alerts
- Usage pattern anomalies
- Maintenance and update notifications

### 17.2 Error Response Standards

**HTTP Status Code Mapping:**

**2xx Success Codes:**
- 200 OK: Successful request processing
- 201 Created: Resource successfully created
- 202 Accepted: Request accepted for asynchronous processing
- 204 No Content: Successful request with no response body

**4xx Client Error Codes:**
- 400 Bad Request: Invalid request syntax or parameters
- 401 Unauthorized: Authentication required or failed
- 403 Forbidden: Insufficient permissions for requested resource
- 404 Not Found: Requested resource does not exist
- 409 Conflict: Request conflicts with current resource state
- 422 Unprocessable Entity: Semantic validation errors
- 429 Too Many Requests: Rate limiting exceeded

**5xx Server Error Codes:**
- 500 Internal Server Error: Unexpected server condition
- 502 Bad Gateway: Invalid response from upstream service
- 503 Service Unavailable: Service temporarily unavailable
- 504 Gateway Timeout: Upstream service response timeout

**Custom Application Error Codes:**
- 1001: UID Code Invalid or Expired
- 1002: Seller/Service Provider Not Found
- 1003: Insufficient Inventory for Order
- 1004: Payment Processing Failed
- 1005: Appointment Slot Unavailable
- 1006: Family Account Permission Denied
- 1007: Cart Item Out of Stock
- 1008: Delivery Area Not Covered
- 1009: Service Provider Unavailable
- 1010: UID Relationship Already Exists

### 17.3 Error Response Format

**Standard Error Response Structure:**
- **Error Code:** Unique application error code
- **Message:** Human-readable error description
- **Details:** Field-specific error details and reasons
- **Timestamp:** Error occurrence timestamp
- **Request ID:** Unique request identifier for tracking
- **Suggestions:** Actionable suggestions for error resolution

**Validation Error Response:**
- Multiple validation errors in array format
- Field-level error details with values and reasons
- Comprehensive validation feedback for forms

### 17.4 Error Handling Strategies

**Client-Side Error Handling:**
- **Network Error Handling:** Automatic retry with exponential backoff, offline mode with queued requests
- **User Input Validation:** Real-time field validation with immediate feedback
- **Application State Management:** Error boundaries for React component isolation, global error state management
- **Session Preservation:** User session preservation during errors, cart and form data recovery

**Server-Side Error Handling:**
- **Request Processing Errors:** Input sanitization and validation middleware, structured error logging
- **Business Logic Errors:** Domain-specific error handling, transaction rollback for consistency
- **Infrastructure Errors:** Database connection failure handling, circuit breaker pattern implementation
- **Medusa Error Handling:** Medusa error types and handling patterns
- **Motia Error Handling:** Workflow error handling and retry logic

### 17.5 Recovery Mechanisms

**Automatic Recovery Strategies:**
- **Transient Failure Recovery:** Automatic retry with configurable backoff, circuit breaker pattern
- **Data Consistency Recovery:** Transaction rollback and compensation, event sourcing for state reconstruction
- **Service Degradation Recovery:** Graceful service degradation levels, feature flags for selective functionality
- **User Session Recovery:** Session state preservation, automatic re-authentication workflows

**Recovery Implementation:**
- **Medusa Recovery:** Medusa's built-in transaction handling and rollback
- **Motia Recovery:** Workflow retry logic and compensation steps
- **Database Recovery:** Transaction rollback, data reconciliation processes
- **Cache Recovery:** Cache invalidation and refresh strategies

### 17.6 Monitoring and Alerting

**Error Monitoring:**
- Real-time error tracking and aggregation
- Error rate monitoring with thresholds
- Performance impact assessment
- Trend analysis and anomaly detection

**Alerting System:**
- Critical error immediate notifications
- Escalation procedures for unresolved issues
- On-call rotation and response protocols
- Stakeholder communication templates

**Error Analytics:**
- Error pattern identification
- Root cause analysis workflows
- Preventive measure implementation
- Continuous improvement tracking

### 17.7 UID System Error Handling

**UID Validation Errors:**
- Invalid code format detection
- Expired code handling with renewal options
- Seller/provider mismatch resolution
- Fraud detection and blocking

**UID Onboarding Errors:**
- Code scanning failure recovery
- Registration process interruption handling
- Duplicate relationship prevention
- Permission and access control errors

**UID Performance Errors:**
- High-latency code verification handling
- Cache miss and recovery strategies
- Database performance degradation management
- Global distribution synchronization issues

### 17.8 Multi-Platform Error Handling

**Web Platform Errors:**
- Browser compatibility issue detection
- JavaScript error boundary implementation
- Progressive enhancement fallback strategies
- Cross-origin and CORS error handling

**Mobile Platform Errors:**
- App crash reporting and analysis
- Offline synchronization conflict resolution
- Push notification delivery failure handling
- App store update and compatibility issues

**Platform-Specific Recovery:**
- Web: Error boundaries, offline queue management
- Mobile: Offline sync conflict resolution, app state recovery
- Shared: Unified error handling via Solito shared code

### 17.9 Compliance and Security Error Handling

**Data Privacy Errors:**
- GDPR consent and processing violation detection
- CCPA data access request error handling
- Data breach notification and response procedures
- Privacy-compliant error message formatting

**Security Errors:**
- Authentication failure handling and logging
- Authorization violation detection and response
- Security event monitoring and alerting
- Incident response and recovery procedures

**Regulatory Compliance Errors:**
- Industry-specific compliance violation detection
- Audit trail integrity maintenance
- Regulatory reporting failure handling
- Compliance monitoring and alerting

### 17.10 User Communication During Errors

**Error Message Guidelines:**
- Clear, actionable error descriptions
- User-friendly language avoiding technical jargon
- Specific guidance for error resolution
- Contact information for additional support

**Progressive Error Disclosure:**
- Initial error summary with expansion options
- Technical details for advanced users
- Support ticket creation integration
- Self-service troubleshooting resources

**Error Prevention Strategies:**
- Proactive validation and user guidance
- Common error pattern identification
- User education and onboarding improvements
- Interface design for error reduction

### 17.11 Error Recovery Testing

**Recovery Scenario Testing:**
- Service failure and restoration simulation
- Data corruption and recovery validation
- Network partition and healing testing
- Load spike and recovery performance testing

**Disaster Recovery Testing:**
- Complete system failure simulation
- Data center failover validation
- Backup and restore procedure verification
- Business continuity plan validation

**User Experience Recovery Testing:**
- Error state user interface validation
- Recovery workflow usability testing
- Communication effectiveness assessment
- User satisfaction during error scenarios

**Implementation Requirements:**
- Implement error classification framework
- Create standardized error response format
- Build client-side error handling with retry logic
- Develop server-side error handling with Medusa/Motia integration
- Implement recovery mechanisms for all error types
- Build error monitoring and alerting system
- Create UID-specific error handling
- Develop multi-platform error handling
- Implement compliance and security error handling
- Build user communication system for errors
- Create error recovery testing procedures

---

## 18. Audit Trail & Compliance Logging Requirements

### 18.1 Audit Trail Framework

**Audit Trail Objectives:**
- Provide comprehensive tracking of all system activities
- Ensure regulatory compliance across all jurisdictions
- Enable forensic analysis and incident investigation
- Support business intelligence and analytics
- Maintain data integrity and non-repudiation

**Audit Trail Principles:**
- **Completeness:** All user actions and system events logged
- **Accuracy:** Logs contain accurate, unaltered information
- **Timeliness:** Events logged in real-time with precise timestamps
- **Security:** Audit logs protected from unauthorized access/modification
- **Retention:** Logs retained for required regulatory periods

### 18.2 Audit Event Categories

**User Authentication Events:**
- Login attempts (successful and failed)
- Logout events
- Password changes and resets
- Multi-factor authentication activities
- Session timeout and renewal events
- UID/QR code access and validation

**User Data Operations:**
- Profile creation, updates, and deletions
- Personal information modifications
- Family account relationship changes
- Consent and preference updates
- Data export and portability requests

**Business Transactions:**
- Order placement and modifications
- Payment processing events
- Appointment booking and changes
- Service delivery confirmations
- Refund and dispute processing
- Inventory adjustments and transfers

**Administrative Actions:**
- User account management (creation, suspension, deletion)
- Role and permission changes
- System configuration modifications
- Feature flag toggles and updates
- Security policy changes

**UID System Events:**
- UID code generation and distribution
- Customer onboarding through UID codes
- UID validation and access attempts
- Relationship establishment and termination
- Analytics data collection and processing

### 18.3 Audit Log Data Structure

**Standard Audit Log Entry:**
- **Audit ID:** Unique audit identifier
- **Timestamp:** Precise event timestamp (ISO 8601 format)
- **Event Type:** Event category and type
- **Event Category:** Authentication, Transaction, Administrative, etc.
- **User ID:** User who performed the action
- **Session ID:** Session identifier
- **IP Address:** Source IP address
- **User Agent:** Browser/client information
- **Location:** Geographic location (country, region, city)
- **Device Info:** Device type, OS, version, model
- **Resource:** Resource type, ID, and action
- **Before State:** Resource state before change
- **After State:** Resource state after change
- **Metadata:** Additional context (source, correlation ID, business context)
- **Compliance Flags:** GDPR, PCI DSS, HIPAA flags

**Sensitive Data Handling:**
- Personally Identifiable Information (PII) masked or tokenized
- Payment card data never stored in audit logs
- Medical data audit entries aggregated for privacy
- Location data generalized for privacy compliance

### 18.4 Compliance-Specific Logging Requirements

**GDPR Compliance Logging:**
- Consent record creation and updates
- Data processing activity logs
- Data subject access request processing
- Data erasure and portability operations
- Consent withdrawal tracking
- Data breach notification logs

**HIPAA Compliance Logging:**
- Electronic Protected Health Information (ePHI) access
- Medical record viewing and modifications
- Prescription management activities
- Patient consent and authorization tracking
- Healthcare provider credential validation
- Audit trail integrity verification

**PCI DSS Compliance Logging:**
- Cardholder data access attempts
- Payment processing authorization events
- Transaction approval and decline logging
- Security control access and modifications
- Intrusion detection and prevention alerts

**Industry-Specific Compliance:**
- FDA audit trails for medical devices
- Automotive compliance for parts traceability
- Restaurant safety compliance logging
- Financial services transaction logging

### 18.5 Audit Log Storage and Retention

**Storage Architecture:**
- Dedicated audit database with immutable storage
- Time-based partitioning for performance
- Geographic distribution for availability
- Encryption at rest and in transit
- Blockchain-based integrity verification (future)

**Retention Policies:**
- **Operational Logs:** 90 days active retention
- **Security Events:** 1 year minimum retention
- **Financial Transactions:** 7 years retention (PCI DSS)
- **Medical Records:** 7 years retention (HIPAA)
- **GDPR Subject Data:** 10 years retention
- **Legal Holds:** Indefinite retention during investigations

**Archival Strategy:**
- Automated archival to long-term storage
- Compression and deduplication for efficiency
- Metadata preservation for searchability
- Regulatory hold capabilities
- Secure deletion procedures

### 18.6 Audit Log Access and Security

**Access Control:**
- Role-based access to audit logs
- Multi-factor authentication for audit viewers
- Principle of least privilege enforcement
- Audit log access itself is audited
- Segregation of duties for audit personnel

**Security Measures:**
- Tamper-evident log storage
- Cryptographic signatures for integrity
- Secure transmission protocols
- Regular integrity verification
- Intrusion detection and alerting

**Monitoring and Alerting:**
- Unusual access pattern detection
- Log tampering attempt alerts
- Storage capacity monitoring
- Retention policy compliance checking
- Audit log system health monitoring

### 18.7 Audit Log Analytics and Reporting

**Real-time Analytics:**
- Security event correlation and analysis
- Fraud detection and anomaly identification
- Performance monitoring and trend analysis
- Compliance violation detection
- Business intelligence insights

**Reporting Capabilities:**
- Automated compliance reports
- Custom audit trail queries
- Executive dashboards and summaries
- Regulatory submission formats
- Forensic investigation tools

**Alerting and Notifications:**
- Real-time security incident alerts
- Compliance threshold breach notifications
- Audit log system failure alerts
- Regulatory reporting deadline reminders
- Unusual activity pattern alerts

### 18.8 UID System Audit Requirements

**UID Generation Audits:**
- Code generation event logging
- Distribution method tracking
- Associated seller/provider linkage
- Code expiration and renewal tracking
- Fraud prevention measure activation

**UID Access Audits:**
- Code scanning and validation attempts
- Customer onboarding success/failure tracking
- Relationship establishment logging
- Access pattern analysis
- Geographic usage distribution

**UID Analytics Audits:**
- Data collection consent verification
- Analytics processing activity logging
- Data retention compliance tracking
- Third-party sharing audit trails
- Privacy impact assessment logging

### 18.9 Multi-Platform Audit Integration

**Web Platform Auditing:**
- Browser fingerprinting and session tracking
- JavaScript error and performance logging
- User interaction event capture
- Cross-origin request logging
- Progressive Web App event tracking

**Mobile Platform Auditing:**
- App installation and update tracking
- Push notification delivery logging
- Offline activity synchronization logging
- Device permission and sensor access logging
- App crash and performance event capture

**Platform-Specific Audit:**
- Web: Browser events, JavaScript errors, user interactions
- Mobile: App lifecycle, native module access, offline sync
- Shared: Unified audit logging via Solito shared code

### 18.10 Audit Log Testing and Validation

**Audit Log Integrity Testing:**
- Tamper detection mechanism validation
- Cryptographic signature verification testing
- Log sequence and completeness checking
- Backup and recovery testing
- Long-term storage integrity validation

**Compliance Testing:**
- Regulatory requirement validation
- Audit trail completeness verification
- Retention policy enforcement testing
- Access control validation
- Reporting accuracy testing

**Performance Testing:**
- High-volume audit logging performance
- Query and search performance validation
- Storage and retrieval scalability testing
- Archival and compression efficiency testing

### 18.11 Legal and Forensic Requirements

**Chain of Custody:**
- Evidence collection and preservation procedures
- Forensic analysis methodology
- Legal hold and preservation orders
- Court-admissible evidence procedures
- Expert witness preparation protocols

**Incident Response Integration:**
- Audit log integration with incident response
- Automated evidence collection workflows
- Timeline reconstruction capabilities
- Root cause analysis support
- Remediation tracking and verification

**Regulatory Examinations:**
- Audit log preparation for regulatory reviews
- Examiner access provisioning and monitoring
- Documentation and evidence packaging
- Response to regulatory inquiries
- Remediation plan tracking

### 18.12 Audit Log Performance Requirements

**Logging Performance:**
- Sub-millisecond logging latency
- Zero performance impact on production systems
- Asynchronous logging with buffering
- High-throughput event processing (100K+ events/second)
- Global distribution with low-latency replication

**Query Performance:**
- Sub-second query response times
- Complex filtering and aggregation support
- Real-time alerting and monitoring queries
- Historical data analysis capabilities
- Export and reporting performance

**Storage Performance:**
- Efficient compression and deduplication
- Fast archival and retrieval operations
- Scalable storage capacity management
- Cost-effective long-term storage
- Regulatory compliance storage tiers

**Implementation Requirements:**
- Build comprehensive audit trail framework
- Create audit event categorization system
- Develop audit log data structure and format
- Implement compliance-specific logging (GDPR, HIPAA, PCI DSS)
- Build audit log storage with retention policies
- Create audit log access control and security
- Develop audit log analytics and reporting
- Implement UID system audit requirements
- Build multi-platform audit integration
- Create audit log testing and validation procedures
- Develop legal and forensic capabilities
- Implement high-performance audit logging

---

## 19. Data Management & Privacy

### 19.1 Data Retention Policies

**User Data:**
- **Active User Data:** Retained indefinitely while account is active
- **Inactive Accounts:** 3-year retention, then anonymization
- **Deleted Accounts:** 30-day grace period, then permanent deletion
- **Personal Data:** Right to erasure upon request (GDPR)
- **Profile Data:** Retained while account is active, deleted upon account deletion

**Transaction Data:**
- **Order History:** 7 years (regulatory compliance)
- **Payment Records:** 7 years (audit requirements)
- **Invoices:** 7 years (tax compliance)
- **Refund Records:** 7 years (financial records)
- **Transaction Logs:** 7 years for financial audit trails

**GPS and Location Data:**
- **Real-time Tracking:** 24 hours live data
- **Trip History:** 90 days detailed data
- **Aggregated Analytics:** 2 years anonymized data
- **Emergency Data:** 1 year retention
- **Location History:** 90 days for active trips, then anonymization

**Family Group Data:**
- **Active Family Data:** Retained while group is active
- **Family Expense History:** 3 years detailed records
- **Shared Cart History:** 90 days
- **Communication Logs:** 1 year retention
- **Family Member Relationships:** Retained while group is active

**UID System Data:**
- **UID Codes:** Retained while seller/service provider is active
- **Customer-Seller Relationships:** Retained while relationship is active
- **UID Analytics:** 2 years aggregated data
- **UID Events:** 1 year detailed event logs
- **UID Distribution Records:** Retained while seller is active

**Chat & Communication Data:**
- **Message History:** 1 year retention for active conversations
- **Media Files:** 90 days retention, then archival
- **Chat Analytics:** 2 years aggregated data
- **Deleted Messages:** 30 days grace period before permanent deletion

**Analytics & Reporting Data:**
- **User Analytics:** 2 years detailed data, then anonymization
- **Business Metrics:** 7 years for financial reporting
- **Custom Reports:** 1 year retention
- **Dashboard Data:** 90 days active, then archival

### 19.2 Privacy & Compliance

**GDPR Compliance:**

**Data Subject Rights:**
- **Right to Access:** User data export within 48 hours
- **Right to Rectification:** Real-time data correction
- **Right to Erasure:** Deletion within 30 days
- **Right to Portability:** Data export in standard formats (JSON, CSV)
- **Right to Restrict Processing:** Processing limitation options
- **Right to Object:** Opt-out of marketing and analytics

**GDPR Implementation:**
- Consent management system with granular consent tracking
- Data processing activity logging
- Data breach notification procedures (72-hour notification)
- Privacy impact assessments for new features
- Data protection officer (DPO) support
- Cross-border data transfer compliance (Standard Contractual Clauses)

**Regional Compliance:**

**United States:**
- **CCPA (California Consumer Privacy Act):** California resident data rights
- **COPPA (Children's Online Privacy Protection):** Children's data protection
- **State-specific Privacy Laws:** Compliance with state privacy regulations
- **FTC Compliance Guidelines:** Federal Trade Commission compliance

**Europe:**
- **GDPR (General Data Protection Regulation):** EU data protection compliance
- **ePrivacy Directive:** Electronic communications privacy
- **Country-specific Regulations:** Local data protection laws
- **Data Localization Requirements:** Regional data storage requirements

**Payment Compliance:**
- **PCI DSS Level 1:** Payment Card Industry Data Security Standard compliance
- **Strong Customer Authentication (SCA):** Two-factor authentication for payments
- **Anti-Money Laundering (AML):** AML compliance and reporting
- **Know Your Customer (KYC):** Customer identity verification

**Industry-Specific Compliance:**
- **HIPAA:** Healthcare data protection (medical module)
- **FDA Regulations:** Medical device and pharmaceutical compliance
- **Food Safety:** Restaurant and food service regulations
- **Automotive Standards:** Parts certification and warranty compliance

### 19.3 Data Anonymization and Deletion

**Anonymization Procedures:**
- **User Data Anonymization:** Remove PII while preserving analytics value
- **Aggregated Data:** Create anonymized datasets for analytics
- **Pseudonymization:** Replace identifiers with pseudonyms
- **Data Masking:** Mask sensitive data in logs and exports
- **Anonymization Verification:** Verify anonymization completeness

**Deletion Procedures:**
- **Account Deletion:** Complete user data deletion workflow
- **Data Erasure Requests:** GDPR right to erasure implementation
- **Cascade Deletion:** Delete related data across all systems
- **Backup Deletion:** Remove data from backups and archives
- **Deletion Verification:** Verify complete data removal

**Data Portability:**
- **Data Export:** Export user data in standard formats (JSON, CSV)
- **Format Support:** Multiple export formats for compatibility
- **Complete Export:** Include all user data across modules
- **Export Scheduling:** Scheduled data export capabilities
- **Export Verification:** Verify export completeness and accuracy

### 19.4 Data Localization and Cross-Border Transfers

**Data Localization:**
- **Regional Data Storage:** Store data in user's region when required
- **Data Residency Requirements:** Compliance with local data residency laws
- **Multi-Region Deployment:** Deploy data storage in multiple regions
- **Data Replication:** Replicate data for availability while respecting localization

**Cross-Border Data Transfers:**
- **Transfer Mechanisms:** Standard Contractual Clauses (SCCs), Privacy Shield alternatives
- **Transfer Impact Assessments:** Assess risks of cross-border transfers
- **User Consent:** Obtain consent for cross-border data transfers
- **Transfer Documentation:** Document all cross-border data transfers

### 19.5 Privacy by Design

**Privacy-First Architecture:**
- **Data Minimization:** Collect only necessary data
- **Purpose Limitation:** Use data only for stated purposes
- **Storage Limitation:** Retain data only as long as necessary
- **Access Control:** Limit access to personal data
- **Encryption:** Encrypt sensitive data at rest and in transit

**Privacy Controls:**
- **User Privacy Settings:** Granular privacy control for users
- **Consent Management:** Granular consent tracking and management
- **Opt-out Mechanisms:** Easy opt-out for marketing and analytics
- **Data Sharing Controls:** Control data sharing with third parties
- **Family Privacy:** Privacy controls for family group data

**Implementation Requirements:**
- Implement data retention policies for all data types
- Build GDPR compliance system with data subject rights
- Create data anonymization and deletion procedures
- Develop data portability system
- Implement data localization and cross-border transfer compliance
- Build privacy by design architecture
- Create consent management system
- Develop data breach notification procedures
- Implement industry-specific compliance (HIPAA, FDA, etc.)
- Build privacy controls and user settings
- Create data export and deletion workflows

---

## 20. Support & Maintenance

### 20.1 Customer Support Structure

**Multi-Channel Support:**
- **Email Support:** Email ticketing system with automated routing
- **Live Chat:** Real-time chat support for immediate assistance
- **Phone Support:** Voice support for critical issues (Enterprise tier)
- **In-App Support:** In-app help center and support ticket creation
- **Knowledge Base:** Self-service knowledge base with search functionality
- **Community Forum:** User community forum for peer support

**Support Tiers:**
- **Basic Support:** Email support with 48-hour response time
- **Professional Support:** Email and chat support with 24-hour response time
- **Premium Support:** Priority support with 12-hour response time
- **Enterprise Support:** 24/7 support with 4-hour response time and dedicated account manager

**Support SLAs:**
- **Critical Issues:** 1-hour response, 4-hour resolution target
- **Major Issues:** 4-hour response, 24-hour resolution target
- **Minor Issues:** 24-hour response, 72-hour resolution target
- **General Inquiries:** 48-hour response, 5-day resolution target

**Support Tools:**
- **Ticketing System:** Integrated ticketing system for issue tracking
- **Knowledge Base:** Searchable knowledge base with articles and FAQs
- **Remote Support:** Screen sharing and remote assistance capabilities
- **Support Analytics:** Support metrics and performance tracking
- **Customer Feedback:** Support satisfaction surveys and feedback collection

### 20.2 Maintenance Procedures

**Scheduled Maintenance:**
- **Regular Maintenance Windows:** Weekly maintenance windows during low-traffic periods
- **Maintenance Notifications:** Advance notification to users (48 hours, 24 hours, 1 hour)
- **Maintenance Duration:** Maximum 4-hour maintenance windows
- **Rollback Procedures:** Prepared rollback plan for failed maintenance
- **Maintenance Communication:** Status page and in-app notifications

**Emergency Maintenance:**
- **Critical Fixes:** Emergency maintenance for critical security or stability issues
- **Immediate Notification:** Real-time notification to affected users
- **Minimal Downtime:** Target <30 minutes for emergency maintenance
- **Post-Maintenance Communication:** Summary of changes and impact

**Update Procedures:**
- **Feature Updates:** Gradual rollout with feature flags
- **Security Updates:** Immediate deployment for security patches
- **Database Migrations:** Zero-downtime migration strategies
- **API Versioning:** Backward-compatible API updates
- **Mobile App Updates:** App store submission and update notifications

### 20.3 Support Metrics and KPIs

**Support Performance Metrics:**
- **Response Time:** Average time to first response
- **Resolution Time:** Average time to issue resolution
- **First Contact Resolution:** Percentage of issues resolved in first contact
- **Customer Satisfaction:** Support satisfaction scores (CSAT)
- **Ticket Volume:** Number of support tickets per period
- **Ticket Trends:** Support ticket trend analysis

**Support Quality Metrics:**
- **Resolution Rate:** Percentage of tickets resolved successfully
- **Escalation Rate:** Percentage of tickets requiring escalation
- **Knowledge Base Usage:** Self-service resolution rate
- **Support Agent Performance:** Individual agent metrics and performance
- **Support Channel Distribution:** Usage across support channels

### 20.4 Maintenance Windows and Communication

**Maintenance Scheduling:**
- **Low-Traffic Windows:** Schedule during low-traffic periods (off-peak hours)
- **Regional Considerations:** Consider time zones for global operations
- **Advance Planning:** Schedule maintenance 2 weeks in advance
- **Emergency Procedures:** Emergency maintenance protocols and approval

**Communication Strategy:**
- **Pre-Maintenance:** 48-hour, 24-hour, and 1-hour advance notifications
- **During Maintenance:** Real-time status updates and progress communication
- **Post-Maintenance:** Summary of changes and any known issues
- **Status Page:** Public status page for system health and maintenance
- **In-App Notifications:** In-app notifications for active users

**Implementation Requirements:**
- Build multi-channel support system (email, chat, phone, in-app)
- Create support ticketing system with routing
- Develop knowledge base with search functionality
- Implement support SLAs and escalation procedures
- Build support analytics and reporting
- Create maintenance scheduling and notification system
- Develop emergency maintenance procedures
- Implement status page for system health
- Build support metrics and KPI tracking
- Create customer feedback collection system

---

## 21. Documentation & Training

### 21.1 Technical Documentation

**API Documentation:**
- **OpenAPI 3.0 Specification:** Complete API specification with all endpoints
- **Interactive API Explorer:** Swagger UI for interactive API testing
- **Code Examples:** Code samples in multiple languages (JavaScript, TypeScript, Python, PHP)
- **Authentication Guides:** Authentication and authorization documentation
- **Rate Limiting Documentation:** Rate limiting policies and best practices
- **Error Code Reference:** Complete error code reference with resolution steps
- **API Versioning:** API versioning strategy and migration guides
- **Webhook Documentation:** Webhook setup and event documentation

**Developer Documentation:**
- **Architecture Overview:** System architecture diagrams and explanations
- **Database Schema Documentation:** Complete database schema with ER diagrams
- **Integration Guides:** Third-party service integration documentation
- **SDK Documentation:** SDK documentation for JavaScript, Python, Ruby
- **Code Style Guides:** Coding standards and style guidelines
- **Contribution Guidelines:** Open-source contribution guidelines
- **Development Workflow:** Development setup and workflow documentation
- **Deployment Guides:** Deployment procedures and best practices

**Medusa Documentation:**
- **Medusa API Documentation:** Medusa Store API and Admin API documentation
- **Medusa Customization:** Custom module and service development guides
- **Medusa Workflows:** Workflow creation and management documentation
- **Medusa Events:** Event system and subscriber documentation
- **Medusa Migrations:** Database migration procedures

**Motia Documentation:**
- **Motia Workflow Engine:** Workflow engine documentation and usage
- **Workflow Steps:** Custom step development and integration
- **HTTP Triggers:** HTTP trigger setup and configuration
- **Workflow Metrics:** Monitoring and metrics documentation
- **OpenTelemetry Integration:** Tracing and metrics integration

### 21.2 User Documentation

**End User Guides:**
- **Getting Started Guides:** Quick start tutorials for new users
- **Feature Tutorials:** Product shopping, service booking, family groups tutorials
- **Family Group Setup:** Family group setup and management guide
- **Transportation Booking:** Transportation service booking guide
- **Delivery Service:** Delivery service usage guide
- **Mobile App Manual:** Complete mobile app user manual
- **FAQ and Troubleshooting:** Frequently asked questions and troubleshooting
- **Video Tutorials:** Screen recordings and video tutorials

**Seller Documentation:**
- **Seller Onboarding:** Complete seller onboarding guide
- **Store Setup:** Store configuration and customization guide
- **Product Management:** Product catalog management guide
- **Order Management:** Order processing and fulfillment guide
- **Analytics Guide:** Seller analytics and reporting guide
- **UID Management:** UID code generation and distribution guide

**Service Provider Documentation:**
- **Provider Onboarding:** Service provider registration and setup
- **Availability Management:** Calendar and time slot management
- **Appointment Management:** Appointment booking and management
- **Service Catalog:** Service creation and management
- **Provider Dashboard:** Dashboard usage and analytics

### 21.3 Training Programs

**Internal Training:**

**Development Team Training:**
- **Platform Architecture Deep-Dive:** 8-hour comprehensive architecture training
- **Technology Stack Training:** 16-hour training on Medusa, Motia, Solito, React Native
- **Security Best Practices:** 4-hour security training and best practices
- **Code Review Guidelines:** 2-hour code review process and standards
- **Testing Methodologies:** 4-hour testing strategies and tools
- **DevOps Procedures:** 4-hour deployment and operations training

**External Training:**

**White Label Client Training:**
- **Platform Overview:** 4-hour platform overview and capabilities
- **Administration Training:** 8-hour admin dashboard and management training
- **Customization Workshop:** 4-hour customization and configuration workshop
- **Operations Training:** 4-hour day-to-day operations training
- **Ongoing Support:** Continuous support and consultation

**Regional Partner Training:**
- **Platform Setup:** 8-hour platform setup and configuration training
- **Sales and Marketing:** 4-hour sales and marketing training
- **Customer Support:** 4-hour customer support training
- **Business Development:** Business development assistance and guidance
- **Performance Reviews:** Regular performance review meetings

**Seller Training:**
- **Seller Onboarding:** Comprehensive seller onboarding program
- **Store Management:** Store setup and product management training
- **Order Processing:** Order fulfillment and customer service training
- **Analytics Training:** Analytics and reporting training
- **Best Practices:** Seller success best practices and tips

### 21.4 Documentation Maintenance

**Documentation Lifecycle:**
- **Version Control:** Documentation version control and tracking
- **Regular Updates:** Quarterly documentation review and updates
- **Change Management:** Documentation change tracking and approval
- **User Feedback:** Documentation feedback collection and improvement
- **Accessibility:** Documentation accessibility compliance (WCAG 2.1 AA)

**Documentation Tools:**
- **Documentation Platform:** Centralized documentation platform (GitBook, Notion, etc.)
- **Version Control:** Git-based documentation versioning
- **Search Functionality:** Full-text search across all documentation
- **Multi-language Support:** Documentation in multiple languages
- **Interactive Examples:** Interactive code examples and demos

**Implementation Requirements:**
- Create comprehensive API documentation (OpenAPI 3.0)
- Build interactive API explorer (Swagger UI)
- Develop developer documentation with architecture diagrams
- Create user guides and tutorials
- Build knowledge base with search functionality
- Develop training programs for internal and external teams
- Create documentation maintenance procedures
- Implement documentation version control
- Build documentation feedback collection system
- Create multi-language documentation support

---

## Conclusion

This Developer Technical Specification document provides comprehensive guidance for building the AvyMart Universal E-Commerce & Service Platform. The document covers all aspects of development from project setup to deployment, including detailed specifications for features, APIs, database design, frontend and backend development, security, testing, and best practices.

**Key Takeaways:**
- **Multi-Platform Architecture:** Web (Next.js) and Mobile (React Native) with shared business logic
- **Microservices Backend:** Scalable microservices architecture with API Gateway
- **UID System:** Core customer exclusivity system with UID/QR codes
- **Comprehensive Features:** E-commerce, service booking, family groups, transportation, delivery network
- **Security First:** Comprehensive security implementation with encryption, authentication, and authorization
- **Performance Focus:** Optimized for billion-user scalability with sub-100ms API responses
- **Developer-Friendly:** Clear documentation, best practices, and implementation guidelines

Developers should use this document as the primary reference for understanding the project architecture, implementing features, and following best practices throughout the development lifecycle.