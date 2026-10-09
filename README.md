# En.Gredient — Single-Unit Economics Model

Unit economics for a 24/7 unmanned micro-retail pilot: a smart-fridge unit selling prepped meals, with production outsourced to a wholesale prep partner (platform model — the operator owns brand, locations, and data; kitchens are interchangeable suppliers).

## Model structure

- **Capacity:** 120 meals/day at full capacity, $16 average ticket, 30-day months
- **Ramp:** 50% → 65% → 80% → 95% → 100% → 100% over six months (no day-one full capacity assumption)
- **Shrink:** 7% of produced meals go unsold (fresh product, 2–3 day shelf life); revenue recognized on sold meals only, COGS incurred on everything prepped
- **COGS:** 32% of produced revenue (ingredients, packaging, prep labor via wholesale partner)
- **OpEx:** $8,000/month fixed (location, software, base route labor, utilities) + ~19.1% of produced revenue variable (fuel, card fees, consumables) — calibrated to $19,008 total at full capacity

## Monthly model

| Month | Capacity | Produced revenue | Sold revenue | COGS | Gross profit | OpEx | EBITDA |
|---|---|---|---|---|---|---|---|
| 1 | 50% | $28,800 | $26,784 | $9,216 | $17,568 | $13,504 | $4,064 |
| 2 | 65% | $37,440 | $34,819 | $11,981 | $22,838 | $15,155 | $7,683 |
| 3 | 80% | $46,080 | $42,854 | $14,746 | $28,108 | $16,806 | $11,302 |
| 4 | 95% | $54,720 | $50,890 | $17,510 | $33,380 | $18,458 | $14,922 |
| 5 | 100% | $57,600 | $53,568 | $18,432 | $35,136 | $19,008 | $16,128 |
| 6 | 100% | $57,600 | $53,568 | $18,432 | $35,136 | $19,008 | $16,128 |
| **Total** | — | **$282,240** | **$262,483** | **$90,317** | **$172,166** | **$101,939** | **$70,227** |

Full machine-readable version: [`monthly_model.csv`](monthly_model.csv)

## Key findings

- **Payback:** ~$8,000–$12,000 hardware setup pays back in roughly 2 months of operating cash flow (vs. ~3 weeks in the naive no-ramp version — the ramp is the honest version).
- **Steady-state margin:** ~30% EBITDA at full capacity ($16,128 / $53,568), vs. 35% before shrink and ramp.
- **Supplier ceiling:** at full capacity the COGS budget is $18,432/month over 3,600 meals = **$5.12/meal all-in** wholesale target for the prep partner.
- **Self-funding scale:** the 6-month reinvestment reserve (~17% of EBITDA, ~$11,939) funds a second unit outright at the low end of the hardware range — unit 1 finances unit 2 with no outside capital.
- **Distribution of 6-month EBITDA ($70,227):** operator 58% ($40,732) · team pool 18% ($12,641) · reinvestment reserve 17% ($11,939) · partner return 7% ($4,916).

## Limitations

Illustrative model, not a forecast. Demand, ticket price, and shrink are assumptions to be replaced with pilot data. The single highest-sensitivity input is the capacity ramp — a slower ramp roughly halves 6-month EBITDA; the model stays cash-positive throughout.
