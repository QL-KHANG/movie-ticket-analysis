# Movie Ticket Business Analysis

**Type:** Personal / capstone project (learning)
**Tools:** Python (pandas, numpy, matplotlib, seaborn)

## Business Context
The company operates a movie-ticketing platform (mobile app + website) where customers browse showtimes, pay via card/bank/e-wallet, and redeem promotional campaigns. Management wants to understand who its customers are, when and how they buy, whether promotions are paying off, and where payment failures are costing the business revenue.

## Objective
Turn 4 years of raw transactional data (2019–2022) into insight the business can act on — customer profile, purchase timing, payment behavior, promotion effectiveness, retention, and payment-failure patterns.

## Data Source
Five relational tables (customer, ticket_history, device_detail, status_detail, campaign), simulated for this learning project to resemble a real ticketing platform's schema.

## Key Questions
1. **Customer profile** — Who are the customers (age, gender, generation), and how reliable is that data?
2. **Purchase timing** — When do customers buy tickets (month, weekday, hour), and how did COVID-19 disrupt the trend?
3. **Purchase behavior** — Which platform, OS, and payment method do customers prefer, and how has that shifted over time?
4. **Customer value** — How do frequency, monetary value, and promotion usage vary across the customer base, and are any usage patterns anomalous (e.g., bulk buyers, promotion abuse)?
5. **Retention** — Do customers acquired through promotions come back, and how does that compare to organically acquired customers?
6. **Payment reliability** — What is the platform's payment success rate over time, and what's driving failures?

## Approach
- Cleaned and validated 5 raw tables (data types, nulls, duplicates) and joined them into a single analytical table.
- Built a full-year time dimension to correctly show the COVID-19 gap instead of misleadingly interpolating it.
- Engineered customer-level metrics (success rate, promotion rate, discount rate) to flag anomalous behavior.
- Ran cohort retention analysis (2019 vs. 2022) and isolated the retention rate of promotion-acquired vs. organic customers.
- Investigated the payment success-rate trend and root-caused failure types (bank-side errors vs. account-verification blocks).

## Key Findings
- **~11% of customers** have unverified gender/DOB data, defaulting to an inaccurate age bucket — a data-quality issue worth flagging to the product team.
- **Promotions drive acquisition, not loyalty:** 97% of 2022 promotion users were first-time customers, but only 13% returned for a second purchase — statistically no better than the 12% return rate of organic customers.
- **Payment failures are concentrated**, not random: a distinct customer segment with 0% success rate is driven primarily by bank-side declines and account-verification blocks rather than platform issues.
