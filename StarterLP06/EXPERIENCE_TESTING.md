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
