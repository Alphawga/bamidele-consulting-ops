# alphawga.com launch blockers

Current status: site code exists at `~/bamidele-consulting` but is not production-ready. The site can run locally and likely builds, but forms will not send email and leads will not be saved without the missing environment variables and database.

## Blockers for minimum viable launch

These are the things that must be in place before the site can convert a warm referral into a booked call or a captured lead.

### 1. Environment variables

File: `~/bamidele-consulting/.env.local` (does not exist yet; copy from `.env.example`).

Required variables:

- `NEXT_PUBLIC_SITE_URL` → real domain, e.g. `https://alphawga.com`
- `NEXT_PUBLIC_CAL_LINK` → Cal.com booking link, e.g. `bamidele/intro-call`
- `NEXT_PUBLIC_BOOKING_URL` → same Cal.com link, used on the Aso-Oke pages
- `NEXT_PUBLIC_AUDIT_PRICE_NGN` → `10000` (the diagnostic price you mentioned)
- `CONTACT_TO_EMAIL` → your real email address
- `SCORECARD_NOTIFY_EMAIL` → your real email address (or the same as above)
- `RESEND_API_KEY` → get from resend.com
- `DATABASE_URL` → see below

### 2. Real email address

File: `~/bamidele-consulting/lib/site.ts` currently has `hello@example.com`. Replace with your real contact email.

### 3. Resend API key

- Sign up at resend.com.
- Verify your domain.
- Generate an API key.
- Add it to `.env.local` as `RESEND_API_KEY=`.
- Without this, the contact form falls back to `mailto`, which is not acceptable for a live site.

### 4. Database

- The site uses Prisma and expects a Postgres database.
- Options: Vercel Postgres, Supabase, or any Postgres provider.
- Create the database.
- Add the connection string to `.env.local` as `DATABASE_URL=`.
- Run `npx prisma db push` or `npx prisma migrate deploy` to create the schema.
- Without this, the scorecard and ERP waitlist forms will accept submissions but nothing will be saved.

### 5. Cal.com booking link

- Set up your Cal.com event type.
- Add the link to `.env.local` as both `NEXT_PUBLIC_CAL_LINK` and `NEXT_PUBLIC_BOOKING_URL`.
- Test the `/book` and `/audit` pages after deploying.

### 6. Build and deploy

- Run `npm install` in `~/bamidele-consulting`.
- Run `npm run build`.
- Fix any build errors.
- Deploy to Vercel.
- Add the environment variables to the Vercel project dashboard.
- Verify the live site.

## Blockers for full launch (not required for MVP)

These can be fixed after the site is live and converting.

- [ ] Real headshot on the About page.
- [ ] Real client logos and case study outcome numbers (Okoh).
- [ ] Final pricing for all offers.
- [ ] Blog content beyond the first post.
- [ ] Course page content.

## Launch sequence

1. Create `.env.local` with all required variables except the database.
2. Get Resend API key and add it.
3. Create database and add `DATABASE_URL`.
4. Run `npx prisma db push`.
5. Replace `hello@example.com` in `lib/site.ts`.
6. Run `npm run build` and fix errors.
7. Deploy to Vercel.
8. Test the contact form, scorecard, and booking links.
9. Go live.

## Notes

- The site README says nothing is blocked by missing values, but that is only true for local development. For a live site, missing email and database means leads disappear.
- Do not delay launch for the full-blocker list. The MVP only needs the items above.
- The database can be added after the site is live, but the scorecard and waitlist will lose leads until it is connected.
