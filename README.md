<p align="center">
  <img src="public/logo.svg" alt="Bambuu logo" width="160" />
</p> 

## Bambuu 🎍

Bambuu is a student-focused personal finance app built for users with irregular income, recurring subscriptions, and short-term savings goals.

Unlike traditional budgeting tools built around fixed monthly salaries, Bambuu is designed for part-time jobs, scholarships, allowances, and real student spending behaviour.

Check it out here: https://bambuu.me/

##  🍀 Key features 

- Transaction tracking for income and expenses
- Recurring transactions, including `biweekly` income
- Let users set specific savings goals and track progress (Our panda climbs each time you save!) with pinned priorities
- Budget category tracking
- Subscription management
- Advanced Data Visualisation and Spending Tips
- Student discount opportunity detection
- Investment insights: Tracking, Learning, and Tips
- Supports Different Currencies
- Bilingual Support (English/French)
- Transaction management and categorisation
- Dark Mode
- Clean and intuitive UI

## Why It Matters

Bambuu helps users answer the questions that matter most:

- How much money is actually coming in?
- What recurring payments are draining cash?
- Am I staying within budget?
- What am I saving toward?
- Where can I reduce costs?

This makes Bambuu more than an expense tracker. It is a practical money management product for a segment that is often underserved by traditional finance apps.

## 🛠️ Stack

- `React`
- `TypeScript`
- `Vite`
- `Supabase`
- `Tailwind CSS`
- `Recharts`

## Run Locally

```bash
npm install
cp .env.example .env
npm run dev
```

## GitHub Pages

This repo can be deployed to GitHub Pages as a static frontend. The included workflow is at [.github/workflows/deploy-pages.yml](/Users/zineb/Documents/GitHub/Bambu/.github/workflows/deploy-pages.yml).

Set these repository secrets before deploying:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`
- `VITE_API_BASE_URL` (optional, only if you host the Plaid backend elsewhere)

If `VITE_API_BASE_URL` is not set, the app still deploys, but Plaid bank-linking features are disabled on GitHub Pages.

## Supabase Setup

1. Create or open a Supabase project.
2. Run [supabase/schema.sql](/Users/zineb/Documents/GitHub/Bambu/supabase/schema.sql).
3. Set:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`

## Product Scope

Bambuu currently includes:

- authentication
- transactions
- recurring income and expenses
- savings goals and contributions
- budget categories
- subscriptions
- notifications
- analytics
- settings

## Future Developments? 
- Mobile app version using React Native for iOS and Android
- Banking API integration for automatic transaction import
- Enhanced discount detection with location-based offers near campuses
- Peer savings challenges to make financial goals social and motivating
- Financial literacy content tailored to student life stages
- Expense splitting features for group living situations and shared subscriptions

## Summary

Bambuu is a cleaner, more relevant finance experience for students and early-career users managing inconsistent income, recurring costs, and savings goals.
