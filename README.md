# Spend CSV

Mobile-first PWA for CSV-based spending tracking with Firebase sync.

## Firebase setup

1. Create a Firebase project.
2. Enable Authentication -> Google provider.
3. Enable Firestore Database.
4. Publish `firestore.rules` as your Firestore security rules.
5. Open the app and paste the Firebase web app config object.

The app stores data under:

```txt
users/{uid}/transactions
users/{uid}/categories
users/{uid}/rules
```

## Workflow

- Import a bank/Revolut CSV.
- Known merchants are categorized by rules.
- Unknown merchants go to Review.
- When you pick a category, the app can remember that merchant for next time.
- Export CSV for Sheets/Excel, or JSON for a full backup.
