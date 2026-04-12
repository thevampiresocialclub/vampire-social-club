# How to Add a New Event to The Vampire Social Club Website

No coding experience needed! Follow these steps to add a new event.

---

## What You'll Need

- A GitHub account (free)
- Access to the repository (ask the admin to add you as a collaborator)
- Your event flyer image (JPG or PNG)

---

## Step 1: Upload the Flyer Image

1. Go to the repository on GitHub: `https://github.com/YOUR-USERNAME/vampire-social-club`
2. Click the **`images`** folder
3. Click **"Add file"** > **"Upload files"** (top right)
4. Drag your flyer image in, or click "choose your files"
5. **Name your file something simple** like `my-event-name.jpg` (no spaces — use dashes)
6. Click the green **"Commit changes"** button at the bottom

---

## Step 2: Add the Event to events.json

1. Go back to the main repository page
2. Click on **`events.json`**
3. Click the **pencil icon** (top right of the file) to edit
4. Find the very first event in the list (right after `"events": [`)
5. **Copy this template** and paste it ABOVE the first event:

```json
    {
      "id": 999,
      "title": "Your Event Title Here",
      "date": "2025-04-15",
      "time": "7:00 PM",
      "venue": "Venue Name",
      "address": "123 Main St, Santa Ana, CA",
      "description": "A short description of the event. Keep it to 1-2 sentences.",
      "attendees": 0,
      "image": "images/my-event-name.jpg",
      "status": "upcoming",
      "cancelled": false
    },
```

6. **Edit each field** with your event's info:
   - **id**: Just pick a number higher than the last event (doesn't matter much)
   - **title**: The event name
   - **date**: Format MUST be `YYYY-MM-DD` (e.g., `2025-04-15` for April 15, 2025)
   - **time**: The start time (e.g., `7:00 PM`)
   - **venue**: The venue name
   - **address**: Full address
   - **description**: Short blurb about the event
   - **attendees**: Set to 0 for new events, update later if you want
   - **image**: Must match the filename you uploaded in Step 1 (include `images/`)
   - **status**: Use `"upcoming"` for future events
   - **cancelled**: Set to `true` if the event is cancelled, otherwise `false`

7. Click the green **"Commit changes"** button

---

## Step 3: Wait ~1 Minute

GitHub Pages takes about 30-60 seconds to update. Refresh the website and your new event should appear in the "Upcoming Events" section!

---

## After the Event Happens

Once an event has passed, you can optionally:

1. Edit `events.json` again
2. Find your event
3. Change `"status": "upcoming"` to `"status": "past"`
4. Update the `"attendees"` count if you want

(The website will also automatically move events to "Past" if their date has passed, even if you forget to update the status.)

---

## Common Mistakes to Avoid

- **Missing comma**: Make sure there's a comma after the `}` of your event (before the next event). The LAST event in the file should NOT have a trailing comma.
- **Wrong date format**: Use `YYYY-MM-DD`, not `MM/DD/YYYY`
- **Wrong image path**: Make sure it starts with `images/` and matches your filename exactly (case-sensitive)
- **Forgetting quotes**: Every value needs to be in double quotes except numbers and true/false

---

## Need Help?

If something breaks, don't panic! GitHub keeps a history of every change. Click the "History" button on events.json to see past versions and revert if needed.

Questions? Ask in the Discord!
