# eHospital Frontend Module (Next.js)

## Overview

This project is a **frontend module** built with **Next.js (App Router)**, **React 19**, **TypeScript**, and **Tailwind CSS**.  
It is designed to be **integrated into a larger e-hospital (eHOS) system** rather than deployed as a standalone application.

The primary focus of this project is on **UI architecture, reusable components, and frontend interaction logic**.  
It does **not** include backend services, authentication mechanisms, or persistent data storage.

---

## Tech Stack

### Framework
- Next.js v16 (App Router, React Server Components enabled)

### Language
- TypeScript

### UI & Styling
- Tailwind CSS  
- shadcn/ui (New York style)  
- Radix UI  
- Lucide Icons  

### State Management & Forms
- React Hook Form  
- Zod (schema validation)

### Charts & Visualization
- Recharts  
- d3 (scale, shape, format)

### Theme Support
- next-themes

---

## Project Structure

```text
.
├── app/                # Next.js App Router pages and layouts
├── components/         # Reusable UI and feature components
│   └── ui/             # shadcn/ui-based atomic components
├── hooks/              # Custom React hooks
├── lib/                # Shared utilities and helper functions
├── public/             # Static assets
├── next.config.mjs     # Next.js configuration
├── tsconfig.json       # TypeScript configuration
├── components.json     # shadcn/ui configuration
├── package.json
└── pnpm-lock.yaml
Architectural Notes
No backend APIs are hard-coded

No database or persistence layer is included

Components are modular, reusable, and loosely coupled

Suitable for use as a micro-frontend or frontend submodule

Getting Started
Prerequisites
Node.js 18 or higher

pnpm (recommended) or npm

Install Dependencies
bash
复制代码
pnpm install
or

bash
复制代码
npm install
Run Development Server
bash
复制代码
pnpm dev
The application will be available at:

arduino
复制代码
http://localhost:3000
Integration Guide
Option 1: Micro-Frontend Integration
Use this repository as an independent frontend module

Mount or embed it within the main eHOS frontend

Share common infrastructure such as:

Authentication context

Global styling and theming

API communication layer

Option 2: Feature & Component Extraction
Reuse selected parts of the codebase:

components/

hooks/

lib/

Merge these into an existing frontend repository

Adapt routes under app/ to match the host application's routing strategy

Configuration Details
TypeScript
ts
复制代码
typescript: {
  ignoreBuildErrors: true
}
Type checking errors are ignored during builds to avoid blocking integration workflows.
This setting can be tightened or removed in production environments.

Image Handling
ts
复制代码
images: {
  unoptimized: true
}
Suitable for internal systems

Avoids constraints related to Next.js image optimization

Path Aliases
ts
复制代码
@/components
@/components/ui
@/hooks
@/lib
Scope & Limitations
Included
Frontend layouts and page structure

Reusable UI components

Form handling and validation

Data visualization components

Theme and dark mode support

Not Included
Authentication and authorization

Backend services or APIs

Database or persistent storage

Production deployment configuration

Intended Use Cases
Frontend feature module within an e-hospital system

UI prototype or reference implementation

Foundation for hospital-facing dashboards and workflows

Notes
Frontend-only implementation

No sensitive data or credentials included

Designed for extensibility and system integration

复制代码
