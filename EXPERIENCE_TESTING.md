# Experience-Based Testing: Airbnb Clone

## Step 1: Error Guessing

**Selected Feature:** Creating a booking (`/bookings/add`)

1. **Missing or invalid date/guest input:** Submitting the form without a date or with `0` or negative guests could submit bad data, fail silently, or show unclear validation.
2. **Backend/API failure (`json-server` not running):** If `http://localhost:3001/rentals` is unreachable, rental options may fail to load or leave the form in a broken state.
3. **Booking list not updating or persisting:** Submitting a new booking might not immediately show up on `/bookings` or could disappear after a page reload.

## Step 2: Exploratory Testing

**Charter:** Investigate how creating a booking (`/bookings/add`) handles valid inputs, missing or edge-case fields, API unavailability, and navigation to `/bookings`.

### Exploratory Testing Notes

| What I Tried | What Happened | What I Decided to Try Next |
| ------------ | --------------- | -------------------------- |
| Loaded `/bookings/add` with `json-server` running on port 3001 | | |
| Submitted valid rental, date, and guest count | | |
| Submitted with blank date or `0`/negative guests | | |
| Checked `/bookings` after submitting | | |

### Future Session Ideas
- Test search/filtering on `/` and standalone `BookingForm.tsx` behavior.

## Step 3: Checklist-Based Testing

| # | Checklist Item | Status | Notes |
| - | -------------- | ------ | ----- |
| 1 | `/bookings/add` renders form fields and loads rentals from `http://localhost:3001/rentals` | Unable to Test | Pending browser verification with `json-server` on port 3001 and Vite running |
| 2 | Submitting a valid rental, date, and positive guest count creates a booking | Unable to Test | Needs live form submission check in browser |
| 3 | Newly created booking appears on `/bookings` and remains after a page reload | Unable to Test | Verify list update and persistence across refresh |
| 4 | Submitting with a missing/blank date is prevented or displays clear validation | Unable to Test | Check required/date validation behavior |
| 5 | Submitting with `0` or negative guests is blocked or shows a clear error | Unable to Test | Check boundary/negative guest input handling |
| 6 | Stopping `json-server` on port 3001 surfaces a clear error or fallback rather than failing silently | Unable to Test | Test API failure handling when port 3001 is down |
