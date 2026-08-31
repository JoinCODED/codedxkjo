# AI-Powered Data Analysis
### CODED × Al-Khafji Joint Operations (KJO)

Three days, six hours a day, at the Arabella Hotel. Fifteen participants from Finance,
Planning, HR and Operations.

This repository holds **the participant-facing site only**. It is a static site with no build
step and no backend.

## What is here

| Page | URL |
|---|---|
| Programme hub | `/` |
| Day 1 · Working With AI on Real Data | `/coded-ada-day-1` |
| Day 2 · From Data to Insight | `/coded-ada-day-2` |
| Day 3 · From Analysis to Recommendation | `/coded-ada-day-3` |
| Slide decks | `/coded-ada-day-{1,2,3}-deck` |
| Fillable workbooks | `/coded-ada-day-{1,2,3}-workbook` |
| Datasets | `/work-orders-40.xlsx`, `/work-orders-full.xlsx`, `/capstone-service-requests.xlsx` |

## What is deliberately NOT here

The facilitator scripts, the answer keys, the capstone answer key and the eight-claims answers
stay out of this repository. **This repo is public**, and those files give away every reveal the
three days are built on: Day 1's correct answer, Day 2's rank flip, Day 3's Industrial Branch trap
and the `SR-4885` collision. Publishing them would spoil the workshop for anyone who looks.

They live with the delivery team, in `FOR-INSTRUCTOR/`.

## Deploying

Static, no build step. Vercel serves `public/` as configured in `vercel.json`.

```
vercel --prod
```

Or connect the repository in the Vercel dashboard. Framework preset: **Other**. No build command.
Output directory: `public`.

`cleanUrls` is on, so `/coded-ada-day-1.html` redirects to `/coded-ada-day-1`. Internal links use
the `.html` form and are redirected, so both work.

## Workbook data

The workbooks save what participants type to `localStorage` in their own browser, per day, under
`ada_workbook_1|2|3`. Nothing is sent anywhere, there is no backend, and the facilitator cannot see
it. Participants take their work away with the **Print or save as PDF** and **Download my answers**
buttons in the workbook sidebar.

## Rebuilding

The site is generated. The generators, the day content and the deck slides live in the delivery
team's project folder (`11- Website 2.0/`), not here. This repository is the deploy target.
