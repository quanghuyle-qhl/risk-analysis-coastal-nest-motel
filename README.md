# Simulation-Based Pricing and Risk Analysis for Coastal Nest Motel
## Project Overview
**Tools:** Microsoft Excel (Monte Carlo Simulation), Scenario Analysis, Risk Profiling  

**Skills:** Simulation Modelling, Stochastic Modelling, Scenario Analysis, Risk Analysis, Decision Modelling

**Author:** Quang Huy Le
 
This project developed a simulation-driven decision support model for Coastal Nest Motel to help management make informed pricing and booking decisions during peak demand periods. The model ran **1,000 iterations per scenario** across four pricing and cancellation-fee combinations, quantifying profit distributions and risk profiles under uncertainty.
## Model Structure
 
The model integrates three input types to estimate daily profit:
 
**Stochastic Inputs (probability distributions):**
| Variable | Distribution | Parameters |
|---|---|---|
| Daily Online Bookings | Normal | μ=22, σ=3 ($150); μ=20 ($180) |
| Daily Cancellations | Binomial | 10–15% probability per booking |
| Daily Walk-ins | Discrete Uniform | 2–6 ($180); 3–7 ($150) |
| Miscellaneous Expenses | Triangular | Min=$100, Mode=$150, Max=$200 |
 
**Decision Variables:**
- Room Price: $150 or $180
- Late Cancellation Fee: $50 or $70
**Fixed Inputs:**
- Number of Rooms: 25
- Housekeeping Cost: $30 per occupied room
**Output:**
- Total Daily Profit = Total Revenue − Operation Cost
- Sold Out indicator (Yes/No)
## Scenario Analysis
 
### $180 Room Pricing
- Profit is highly sensitive to online bookings: ranges from **$2,700 (worst) to $3,600 (best)** — a $900 swing.
- Cancellations reduce profit by up to $400; cancellation fees partially offset the loss.
- Walk-ins provide moderate uplift ($2,850–$3,450) but are not a primary revenue driver.
- Miscellaneous expenses have minimal impact (±$50).
### $150 Room Pricing
- Profit range of $2,450–$2,900 shows lower revenue potential and tighter margins.
- Higher bookings risk overbooking compensation, which erodes profit.
- Same expense insensitivity holds; demand-side variables dominate.
**Key Takeaway:** The model is revenue-sensitive, not cost-sensitive. Booking volume and room price are the primary profit drivers.
## Simulated Output (1,000 Iterations)
 
| Scenario | Mean Profit | Min | Max | Std Dev |
|---|---|---|---|---|
| $180 Room + $50 Fee | $3,137.36 | $1,720 | $3,824 | $384.52 |
| $180 Room + $70 Fee | $3,157.55 | $1,758 | $3,880 | $376.13 |
| $150 Room + $50 Fee | $2,624.06 | $1,430 | $3,157 | $293.10 |
| $150 Room + $70 Fee | $2,685.79 | $1,567 | $3,385 | $297.25 |
## Risk Analysis
 
| Scenario | Below $2,500 | $2,500–$3,500 | Over $3,500 |
|---|---|---|---|
| $180 + $50 Fee | 7.6% | 73.3% | 19.1% |
| $180 + $70 Fee | 5.5% | 74.1% | **20.4%** |
| $150 + $50 Fee | 29.6% | 65.5% | 4.9% |
| $150 + $70 Fee | 24.1% | 63.2% | 12.7% |
 
**The $180 room with $70 cancellation fee is the optimal strategy**, delivering the highest average profit, lowest downside risk (0.4% < $2,000), and the highest probability of exceeding $3,500 (20.4%).
## Recommendations
 
| Recommendation | Rationale |
|---|---|
| **Adopt $180 room + $70 cancellation fee** | Best profit-risk balance for peak periods |
| **Limit overbooking to 2–3 rooms** | Compensation costs erode gains beyond this threshold |
| **Avoid $150 room + $50 fee** | Weakest performance and highest low-profit risk |
| **Use $150 + $70 fee for off-peak** | Better stability when profit maximisation is secondary |
| **Monitor and adjust policies regularly** | Model performance depends on alignment between forecasted and actual demand |
