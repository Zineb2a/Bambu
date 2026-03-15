# Bambuu

Bambuu is a personal finance platform designed for students and early-career users who do not fit the assumptions of traditional budgeting apps.

Most finance products are built around fixed monthly salaries, stable expenses, and long financial histories. Bambuu is built for a different reality: part-time jobs, scholarships, allowances, recurring subscriptions, irregular spending, savings goals, and constant tradeoffs between short-term needs and long-term priorities.

## Business Case

### The Problem

Students and young adults are financially active, but financially underserved.

They often manage:

- multiple income sources instead of one salary
- non-monthly pay cycles such as `biweekly` wages
- recurring subscriptions that quietly drain cash
- short-term saving goals with high emotional importance
- inconsistent spending patterns month to month
- little visibility into what is actually safe to spend

Traditional budgeting tools usually feel too rigid, too corporate, or too complex for this segment. Bambuu addresses that gap with a product that is more visual, more guided, and more aligned with how younger users actually manage money.

### The Opportunity

Bambuu sits at the intersection of:

- personal finance
- student life
- subscription management
- financial habit building
- savings motivation

The product can position itself as a financial operating system for students:

- track what comes in
- understand what goes out
- stay ahead of recurring payments
- build savings discipline
- surface cost-saving opportunities

This creates room for a differentiated product that is practical on day one and expandable into a larger fintech or education-finance platform over time.

## Product Positioning

Bambuu is not just a budgeting app.

It is a student-first money management experience focused on clarity, action, and progress.

Its value proposition is:

> Help users understand their cash flow, manage recurring financial behavior, and make better day-to-day money decisions without needing a finance background.

## Core Product Features

### 1. Unified Financial Dashboard

The home dashboard gives users an immediate snapshot of:

- total balance
- income vs expenses
- recent transactions
- category-level spending patterns
- pinned savings goal progress

This makes Bambuu feel actionable from the first screen rather than forcing users to navigate multiple pages to understand their situation.

### 2. Transaction Tracking

Users can record and manage:

- income
- expenses
- recurring transactions
- multi-currency entries

The transaction system supports:

- search
- filters
- exports
- editing and deletion
- recurring visibility directly in the ledger

This is especially important for users with mixed cash flow sources like wages, scholarships, family support, and side income.

### 3. Recurring Transaction Management

Recurring behavior is a core financial driver, so Bambuu treats it as a first-class feature rather than a side option.

Supported recurring frequencies include:

- `daily`
- `weekly`
- `biweekly`
- `monthly`
- `yearly`

Users can:

- create recurring income and expenses
- edit them
- pause and resume them
- view them in a dedicated recurring screen

This makes Bambuu more realistic for students who are paid biweekly and billed monthly.

### 4. Savings Goals

Savings is not presented as an abstract number. It is tied to named goals with visual identity and progress tracking.

Users can:

- create multiple savings goals
- assign emojis for quick recognition
- pin the most important goal
- track progress through contributions
- see remaining amount at a glance

This shifts the product from expense tracking to forward-looking money behavior, which improves retention and emotional engagement.

### 5. Budget Categories

Bambuu allows users to define category budgets and compare them against real spending.

This helps users answer:

- where money is going
- which categories are getting out of control
- how spending compares against personal limits

The product is therefore useful not just for recordkeeping, but for spending control.

### 6. Subscription Oversight

Recurring digital services are a major leak in student budgets. Bambuu provides subscription tracking so users can see:

- what they are subscribed to
- how much those subscriptions cost monthly
- when renewals are coming up

This adds immediate practical value and supports a strong consumer-facing use case.

### 7. Analytics and Insight Layer

Bambuu includes a real analytics surface, not just static totals.

Users can explore:

- spending vs income trends
- savings rate
- category breakdowns
- budget comparisons
- time-based financial patterns

That gives the product a more premium feel and makes it easier to justify as a decision-support tool rather than a basic tracker.

### 8. Student Discount Discovery

One of Bambuu's strongest differentiation angles is cost reduction, not just cost tracking.

The app can surface student discount opportunities based on recurring services and known patterns. That turns Bambuu into a product that can actively help users save money, not only observe spending.

This is strategically important because it opens a path toward:

- affiliate partnerships
- student-focused offer ecosystems
- subscription optimization flows

## Why Bambuu Is Different

Most budgeting apps optimize for older users with stable income.

Bambuu is differentiated by focusing on:

- non-traditional income schedules like `biweekly` pay
- younger users with dynamic, uneven cash flow
- visual goal-based saving
- subscription awareness
- bilingual accessibility
- actionable, not overly technical, financial UX

It is more approachable than enterprise-style finance tools and more useful than a simple expense logger.

## Target Users

Primary audience:

- university students
- college students
- recent graduates
- part-time workers
- scholarship-supported users
- young adults building money habits for the first time

Secondary audience:

- parents helping students manage budgets
- early-career users with unstable income
- financially conscious subscription-heavy consumers

## Product Scope Today

Bambuu currently includes:

- authentication with Supabase Auth
- persistent user financial data
- recurring transaction support
- transactions, income, and expense views
- savings goals and contributions
- category budgets
- subscriptions
- analytics dashboards
- notifications
- settings and profile management
- English and French localization

## Technology Stack

- `React`
- `TypeScript`
- `Vite`
- `React Router`
- `Supabase Auth`
- `Supabase Postgres`
- `Supabase Edge Functions`
- `Tailwind CSS`
- `Recharts`
- `date-fns`

## Architecture Summary

```text
src/
  app/
    pages/           Product surfaces
    components/      UI and feature components
    lib/             Finance, currency, notifications, settings, transactions
    providers/       Auth and i18n providers
    types/           Shared domain types
  lib/
    supabase.ts      Supabase client configuration

supabase/
  schema.sql         Database schema, triggers, policies
  functions/server/  Serverless logic
```

## Local Setup

### Install dependencies

```bash
npm install
```

### Configure environment

```bash
cp .env.example .env
```

Required client-side variables:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`

### Set up Supabase

1. Create or open a Supabase project.
2. Run the SQL in [supabase/schema.sql](/Users/zineb/Documents/GitHub/Bambu/supabase/schema.sql).
3. Confirm Auth is enabled.
4. For easier local development, you can disable email confirmation in Supabase Auth.

### Start the app

```bash
npm run dev
```

### Build the app

```bash
npm run build
```

## Data Model

Bambuu persists:

- `profiles`
- `transactions`
- `savings_goals`
- `goal_contributions`
- `budget_categories`
- `subscriptions`
- `investments`
- `user_settings`
- `linked_cards`
- `notifications`

The schema includes:

- sign-up provisioning trigger
- row-level security policies
- recurring transaction support
- goal contribution history
- notification persistence

## Strategic Expansion Paths

Bambuu can evolve beyond budgeting into a larger financial product through:

- bank and card integrations
- smarter recurring cash flow forecasting
- savings automation
- student discount partnerships
- embedded financial education
- premium analytics
- subscription switching and optimization flows

## Summary

Bambuu is a credible consumer finance product aimed at a segment that is large, active, and poorly served by traditional budgeting software.

Its strength is not just that it tracks money. Its strength is that it understands how younger users earn, spend, save, and decide.

That makes it a stronger business proposition than a generic expense tracker and a better product foundation for long-term growth.
