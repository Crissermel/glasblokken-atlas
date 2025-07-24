# Firebase Setup for Real-Time GlassBlock Atlas

## Overview
Firebase will enable real-time synchronization of glass block pins across all users worldwide. When someone adds, edits, or deletes a pin, it will instantly appear for everyone.

## Step 1: Create Firebase Project

1. Go to https://console.firebase.google.com/
2. Click "Create a project"
3. Name it: `glassblock-atlas`
4. Enable Google Analytics (optional)
5. Click "Create project"

## Step 2: Set Up Firestore Database

1. In Firebase Console, go to "Firestore Database"
2. Click "Create database"
3. Choose "Start in test mode" (for now)
4. Select a location close to your users
5. Click "Done"

## Step 3: Get Firebase Config

1. Go to Project Settings (gear icon)
2. Scroll down to "Your apps"
3. Click "Add app" → Web app
4. Name it: `glassblock-atlas-web`
5. Copy the config object

## Step 4: Update Security Rules

In Firestore Database → Rules, replace with:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Allow read/write access to glass block pins
    match /pins/{pinId} {
      allow read, write: if true; // Public access for community sharing
    }
  }
}
```

## Step 5: Install Firebase SDK

Add these scripts to your HTML before the closing </body> tag:

```html
<!-- Firebase SDK -->
<script src="https://www.gstatic.com/firebasejs/9.x.x/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.x.x/firebase-firestore.js"></script>
```

## Benefits of Firebase Solution

✅ **Real-time updates** - Changes appear instantly for all users
✅ **No server management** - Firebase handles everything
✅ **Free tier** - 50,000 reads/day, 20,000 writes/day
✅ **Automatic scaling** - Handles millions of users
✅ **Offline support** - Works without internet
✅ **Security rules** - Control who can read/write data

## Alternative Options

### Option 2: Supabase (PostgreSQL-based)
- More powerful database features
- Real-time subscriptions
- Free tier: 500MB database, 2GB bandwidth

### Option 3: MongoDB Atlas
- Document-based database
- Real-time with change streams
- Free tier: 512MB storage

### Option 4: Custom Backend
- Node.js + Express + MongoDB/PostgreSQL
- WebSocket for real-time updates
- More control but requires server management 