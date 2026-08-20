# CTO Candidate Case Study Response - AlliedOne Limited (AOL)

Hi there! Thanks for the opportunity to review the case study for the CTO position at AOL. I've spent some time thinking through our constraints—especially the goal to see initial revenue within 6 months, combined with our small, part-time, and relatively inexperienced team. 

Here is how I would approach our very first product launch to maximize our chances of success.

## 1. Which product should we build first?

I strongly recommend we start with **Product B: The basic e-commerce storefront for a partner business, paired with digital marketing services.**

**Here's my thought process:** 
When we only have 6 months to prove traction and a team of part-time junior developers, speed and risk-reduction are everything. Building a mobile app (Product A) from scratch with quizzes and video streaming is highly technical. It takes a long time just to get an app stable across different devices, not to mention the massive effort required to create all the educational content. 

With Product B, we can move incredibly fast. Even though we are building a custom website, an e-commerce storefront is a very well-understood technical challenge. We can leverage modern, developer-friendly frameworks (like Next.js or React) that our junior devs from BUET/RUET are likely already familiar with or can pick up rapidly. This plays perfectly to our team's current strengths: our devs can focus on building a clean, high-performing custom UI and a straightforward database, while our business student can immediately start running digital marketing campaigns to drive traffic to the partner's products. Since we are partnering with an existing business, we also don't have to worry about sourcing our own inventory or figuring out logistics from zero. It’s the fastest, lowest-friction path to getting real cash flowing.

## 2. What do we need before we launch?

Before we start building, we need to lock down a few critical dependencies:

1. **The Partner Agreement:** We need absolute clarity on how the revenue split works, who handles the physical shipping/customer service, and how we sync their inventory with our custom database.
2. **Tech Stack & Domain Setup:** Finalizing our custom tech stack (e.g., Next.js, Node.js, PostgreSQL), setting up our cloud hosting environment (like AWS or Vercel), and buying the domain name.
3. **Payment Processing:** Getting a local payment gateway (like SSLCommerz or bKash) approved and integrating their API into our custom backend so we can actually collect money securely.
4. **Product Content:** We need high-quality photos, descriptions, and pricing from our partner business. (If the photos are bad, the site won't convert, no matter how good the code is).
5. **Marketing Infrastructure:** Establishing our initial ad budget and getting our tracking pixels (like Meta Pixel and Google Analytics) installed in our custom code so we can measure our marketing ROI.

## 3. Budget & Team Plan

**Estimated Budget for the First 3 Months:**
We can run this very lean to start, taking advantage of modern cloud free tiers where possible.
*   **Infrastructure (Domain, Cloud Hosting/Database like Vercel/Supabase):** ~$50 - $100
*   **Payment Gateway & Legal Setup:** ~$100
*   **Initial Marketing Budget (for pilot testing):** $300 - $500 per month (so around $900 - $1,500 total)
*   **Misc Tools (Canva, analytics tools, etc.):** ~$50
*   **Total Estimate:** Roughly $1,100 to $1,750 to get off the ground, excluding team stipends.

**How I'd Divide the Work:**
Since everyone is working 15 hours a week, we have to be ruthlessly efficient.
*   **Me (CTO):** I'll handle the big architectural decisions—designing the system architecture, picking the frameworks, negotiating with the payment gateway, and overseeing the marketing strategy. Most importantly, I'll spend time pair-programming with the devs, setting up the CI/CD pipeline, and doing code reviews to ensure our custom codebase stays clean and scalable.
*   **The Dev Team (BUET/RUET students):** I'll have one dev focus purely on the custom front-end (building out the UI components in React, ensuring it looks premium and works perfectly on mobile devices). The other will handle the custom back-end architecture—designing the product database schema, building the API, securely connecting the payment gateway, and setting up shipping logic.
*   **The Business Student (IBA):** They will be our marketing engine. They'll research the target audience, write ad copy, design social media posts, and run the actual Meta/Google ad campaigns. They'll also act as the project manager for getting product assets from our partner.

## 4. The Pilot Launch Strategy

Instead of a massive, risky launch day, we'll do a "soft opening" for a few weeks. We'll only list the partner's top 10 best-selling products and spend a very small amount on highly targeted ads.

**What we are testing:**
We want to make sure our custom website loads fast under traffic, the payment API integration processes cards/mobile money without errors, and that when an order is placed, the partner actually receives the notification and ships it on time.

**How we know it's working:**
We'll watch the checkout completion rate closely (are people abandoning their carts due to UI bugs?), and we'll calculate our Customer Acquisition Cost (CAC) to see how expensive it is to get a single sale.

**When to go fully commercial:**
Once we process 20+ real orders without any major operational bugs, and we can prove that it costs us less to acquire a customer through ads than the profit we make on an order, we’ll open the floodgates, add the rest of the products to the database, and scale the ad budget.

## 5. What if revenue is 60% below target?

If we hit month 3 and we're drastically missing our goals, we don't panic; we look at the data funnel to find the "leak." 

I'd immediately dive into our analytics to see where people are dropping off:
*   Are we not getting enough clicks on our ads? (Top of funnel problem: our ads aren't engaging or targeting the right people).
*   Are people clicking but leaving the site immediately? (Middle of funnel problem: our pricing is too high, or the website design doesn't build trust).
*   Are people adding to cart but not buying? (Bottom of funnel problem: shipping is surprisingly expensive, or our custom checkout process has friction/bugs).

**My first two actions would be:**
1. **Stop the bleeding:** I'd immediately pause our main ad spend so we aren't burning cash on campaigns that aren't working. We'll leave a small retargeting budget running while we investigate.
2. **Fix the biggest bottleneck based on the data:** If the data shows people are abandoning carts at the very end, I'll run test transactions myself to see if our backend gateway integration is failing. If the bounce rate on the homepage is huge, I'll do some quick, scrappy user testing (even just having friends navigate the site on their phones while I watch) to see if they are hitting UI bugs or confusing flows, and push an immediate code fix.
