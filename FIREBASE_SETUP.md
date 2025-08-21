# Firebase Setup Guide for Daily Averages

## Step 1: Create Firebase Project

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Add project" 
3. Enter project name (e.g., "the-cost-is-correct")
4. Disable Google Analytics for now (optional)
5. Click "Create project"

## Step 2: Set up Firestore Database

1. In your Firebase project, click "Firestore Database" in the left menu
2. Click "Create database"
3. Choose "Start in test mode" for now
4. Select a location (choose closest to your users)

## Step 3: Get Firebase Configuration

1. Click the gear icon (Project Settings) in the left menu
2. Scroll down to "Your apps" section
3. Click "Web" icon (</>) 
4. Enter app nickname: "the-cost-is-correct-web"
5. Copy the `firebaseConfig` object

## Step 4: Add Config to Your HTML ✅ COMPLETE

✅ **Your Firebase config has been added to the HTML file!**

The following configuration is now active in your `index.html`:
- Project: "the-cost-is-correct"
- Ready for daily average tracking

## Step 5: Configure Security Rules (Important!)

In Firestore Database > Rules, **replace the existing rules** with this exact text:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Allow read/write to daily_scores collection
    match /daily_scores/{document} {
      allow read, write: if true;
    }
  }
}
```

**⚠️ Important:** 
- Don't include "```javascript" or any markdown formatting
- Copy only the rules text above
- Click "Publish" after pasting

## Step 6: Test

1. Deploy your game to a web server (GitHub Pages, Netlify, etc.)
2. Complete a game - you should see daily average appear
3. Check Firebase Console > Firestore to see stored scores

## Features Added

✅ **Daily Average Display**: Shows average score for current day
✅ **Player Count**: Shows how many people played today  
✅ **Automatic Storage**: Scores saved with date/timestamp
✅ **Global Stats**: Works across all players worldwide

## Security Notes

- The current rules allow anyone to read/write scores
- For production, consider adding rate limiting
- You can restrict to specific domains in Firebase Console

## Troubleshooting

- **No daily average showing**: Check browser console for errors
- **Firebase errors**: Verify config values are correct
- **Database not updating**: Check Firestore rules allow writes

## Next Steps

Consider adding:
- Weekly/monthly averages
- Leaderboards 
- Score history graphs
- Share results feature
