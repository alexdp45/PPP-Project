# Paid to Grow? Fund Scale and the GP–LP Principal–Agent Problem

*People, Power, and Pay: course project. Working draft; this README will change as the project develops.*

## Motivating fact

In private equity and real estate funds, investors (limited partners, or LPs) hand capital to managers (general partners, or GPs). The GPs decide what to buy. They are paid two ways:

- **management fees**, charged on fund size whether or not the fund performs
- a **promote** (carried interest), a share of profits above a hurdle rate

The fixed part is larger than many people assume. A study of 238 private equity funds found that "about two-thirds of expected revenue comes from fixed-revenue components that are not sensitive to performance." It also found that buyout managers grow their funds faster than venture managers, which raises revenue per partner ([Metrick & Yasuda, *Review of Financial Studies*, 2010](https://ideas.repec.org/a/oup/rfinst/v23y2010i6p2303-2341.html)).

From my work as a performance-paid operator in commercial real estate, small sponsors seem to live on promote: they need outsized returns to get paid. Large managers seem to live on fees: they get paid for gathering and deploying capital. The question is whether that shift changes how managers behave, and whether investors can do anything about it.

## Question

**How does fund scale change the principal–agent relationship between GPs and LPs?** As a GP grows, does its pay shift from performance-based (promote) to fixed (fees), weakening the alignment LPs rely on? And do LPs lose the power to correct it?

### Sub-questions

1. **The agent's incentive:** at what scale (assets under management) does a GP's income shift from mostly promote to mostly fees?
2. **The agent's behavior:** after crossing that point, do GPs act in ways that serve themselves over LPs? For example, growing the next fund faster than performance justifies, deploying faster near the end of the investment period, or shifting toward lower-return, fee-heavy strategies.
3. **The outcome for the principal:** do LPs' net returns fall as fund size grows? Is there an LP-optimal fund size that is smaller than the size the GP prefers?
4. **The principal's response:** do LPs' tools for disciplining GPs (refusing to re-up, negotiating fees, requiring GP co-investment, capping fund size) weaken as GPs get larger?

## Why it matters

- **LPs** include public pensions, endowments, and individual savers. If larger managers are paid mainly to grow, those investors may earn less than they would with smaller, performance-paid managers.
- **Pay structure:** this is a case where the form of pay, not just its amount, may change what a manager does.
- **Power:** if large GPs can raise capital no matter what LPs think, the ability to set the terms of the relationship moves from the principal to the agent.

## Economic connection

The anchor is **Chapter 10, "Information: Contracts, Norms, and Power."**

| Ch. 10 element | GP–LP version |
|---|---|
| Principal | The LP |
| Agent | The GP |
| Conflict of interest (§10.3) | LPs want the best net returns. GPs also earn from fund size and deployment, which pay fees regardless of returns. |
| Incomplete contract (§10.2) | Deal quality, effort, and price discipline can't be specified or verified when deals are made. Results arrive years later, so the chance that the LP detects a bad decision early (*t*, §10.13) is low. |
| Hidden actions | Which deals to do, how fast to deploy, how big to make the next fund |
| Principal's tools (Table 10.1, owner/manager row) | Profit sharing (promote), contingent renewal (re-upping in the next fund), and GP co-investment, which works like collateral in the credit model (Ch. 12) |

**The mechanism.** Scale may weaken each of the LP's tools:

1. **Profit sharing weakens.** Fees grow with fund size, while platform costs are largely fixed. Above some size, fee profit exceeds expected promote, and the GP's best response (the incentive compatibility constraint, §10.8) shifts toward deploying and growing.
2. **Contingent renewal weakens.** A large, oversubscribed GP is on the short side of the fundraising market (§10.10). LPs compete for allocations, so an LP's threat not to re-up stops being credible. Contingent renewal only works when the threat to cut off the agent is credible.
3. **Collateral weakens.** GP co-investment usually shrinks as a share of fund size, so the GP has less of its own money at risk.

**A model to build.** Both fees and promote grow with fund size. The crossover from promote-driven to fee-driven income therefore happens only if (a) fixed platform costs make fee profit grow faster than fee revenue, and/or (b) excess returns shrink as funds grow. The model will estimate:

- the **crossover fund size**
- the **wedge** between the fund size that maximizes LP net returns and the size that maximizes GP income

Ch. 8 (firms' costs) may supply the fixed-cost side [VERIFY coverage].

## Testable predictions

1. The fee share of GP income rises with assets under management.
2. GPs grow successor funds faster than their prior fund's performance justifies, especially above the crossover size.
3. Net LP returns decline with fund size, controlling for vintage and strategy. (Theory and prior evidence point both ways, so this is a test, not an assumption.)
4. Larger, oversubscribed GPs concede fewer LP-friendly terms, and LPs report less ability to walk away.
5. Higher GP co-investment and fee step-downs are associated with better price discipline.

## Evidence and next steps

- **Model:** GP and LP payoffs from a marginal deal and from fund-size decisions, with terms (fee rate and basis, step-downs, carry, hurdle, GP commitment, successor-fund clauses) taken from interviews and public documents. The crossover and the wedge will be tested under several assumptions about how returns change with size.
- **Public pension fund reports:** fund-level commitment, paid-in capital, distributions, IRR, and multiple, tracked across years. These give fund size growth, deployment pace, and net returns by size [VERIFY which pensions publish fund-level detail].
- **Fund terms:** pension board meeting materials and consultant memos, which often list fees, carry, hurdle, and GP commitment [VERIFY availability].
- **Large public managers:** publicly traded alternative asset managers report fee-related earnings separately from performance revenue, which shows the revenue mix at the top of the size range [VERIFY line items].
- **Interviews:** GPs and LPs, sampled on purpose across the size range, from deal-by-deal syndicators to multi-billion-dollar managers. Each gets a standard protocol covering revenue mix, when fees began covering overhead, what drove decisions to grow, how deal teams are paid, and how LPs monitor and discipline GPs. Interviewees are told about my role, participate with consent, and are anonymized. Only coded, aggregated findings go in this repo.
- **Literature:**
  - [Metrick & Yasuda (2010)](https://ideas.repec.org/a/oup/rfinst/v23y2010i6p2303-2341.html) on fixed vs. performance pay
  - [Kaplan & Schoar (2005)](https://econpapers.repec.org/RePEc:bla:jfinan:v:60:y:2005:i:4:p:1791-1823), who find that better-performing partnerships are more likely to raise follow-on and larger funds, but with a concave relationship. That is evidence on how contingent renewal works in practice.

## Competing explanations to address

- **Limited deal supply:** returns may fall with size because big funds run out of good deals, not because of incentives.
- **Cheaper capital:** larger GPs may have cheaper capital, which justifies lower returns without any agency problem.
- **LPs' own choices:** LPs may knowingly accept lower returns from large GPs in exchange for lower risk, operational ease, or the ability to invest more capital at once.
- **Data limits:** public pension data covers only funds with public LPs, and interim returns are GP estimates.

## Repository layout

- `README.md`: this overview
- `CLAUDE.md`: instructions for the AI agent
- `notes/`: original ideas, summarized and anonymized
- `iterations/`: condensed records of working sessions with the agent
- `CHANGELOG.md`: log of substantial edits
