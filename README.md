# How to Build a CometChat UI Kit

## What You'll Be Building

![Chat UI Screenshot](https://github.com/HADES248/CometChatReact-UI-Kit/blob/master/src/assets/CometChat.png)  
*Alt text: Screenshot of a working CometChat-powered React app with a user logged in and active chat visible*

You’ll build a simple React application that allows users log in, view conversations, and exchange real-time text messages using CometChat’s UI Kit.

---

## Introduction

In this Section, you’ll learn how to integrate CometChat into a React application using the official CometChat UI Kit.

Real-time chat is a foundational feature in many modern apps, from customer support to social platforms. CometChat offers a robust SDK and UI Kit that makes it fast and reliable to add chat functionality without building everything from scratch.

---

## Prerequisites

**Knowledge Required**
- Basic React hooks
- React component structure (functional components, JSX)
- ES6+ JavaScript

**Tools Required**
- Node.js v16+  
- npm (v8+)  
- Git (optional, for cloning the repository)  
- A modern code editor (e.g., VS Code)

---

# CometChat Integration

## Step 1: Set Up Your Project

Create a new React project using Create React App with the TypeScript template:

```bash
npm create vite@latest cometchat-react-ts-app --template react-ts
cd cometchat-react-ts-app

```
## Step 2: Install Dependencies

To integrate CometChat into your project, install the required SDK and UI Kit using:

```bash
npm install @cometchat/chat-sdk-javascript @cometchat/chat-uikit-react
```
## Step 3: Initialize CometChat

### Configuration in `src/cometchatConfig.ts`
- The file initializes CometChat using TypeScript.
- It imports CometChat from the SDK, builds `AppSettings` with presence subscription, and calls `CometChat.init()`.
- Logs success or error messages to the console for debugging.

### Integration in `src/App.tsx`
- The function `initializeCometChat()` is called before rendering the `App` component.
- This ensures CometChat is fully initialized before any UI elements load, preventing runtime issues.

With this setup, CometChat is properly integrated and ready for real-time communication.

## Step 4: Build the UI

### Components
- `Login.tsx` – Handles user authentication via `CometChat.login(userID)`.
- `CometChatSelector.tsx` – Tracks logged-in users, displays conversations, and updates selected chat items.
- `App.tsx` – Manages state, handles conversation selection, and renders chat interface components.

This setup ensures a seamless chat experience.

## Step 5: Test & Verify

### Testing
1. Start the development server:
   ```bash
   npm run dev
   ```
- Open http://localhost:3000 in your browser.
- Log in, select a conversation, and send messages in real-time.
Troubleshooting- Ensure .env values (APP_ID, REGION, AUTH_KEY) are correct.
- Verify at least one user exists in the CometChat Dashboard.
- Confirm the recipient user is online.
ConclusionYour React TypeScript app now integrates CometChat UI Kit, enabling users to log in, view conversations, and send messages.Next Steps- Enable image and file sharing.
- Store message history locally using IndexedDB.
- Add typing indicators and read receipts.
- Expand to voice/video calls using CometChat’s SDK
