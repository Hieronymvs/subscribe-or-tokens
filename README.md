# Subscribe or Tokens?

**Is a flat AI subscription or pay-as-you-go API billing cheaper for *your* usage?**

Enter how you actually use AI — casual chat, daily assistant, or heavy agentic coding — and see every option ranked by monthly cost: Claude, ChatGPT, and Gemini subscription tiers side by side with per-token API rates.

No signup, no tracking, no cookies, no ads. One static page.

## Why this exists

In July 2026, Hacker News front pages filled with the same complaint, thread after thread: AI pricing is confusing. Vague limits ("5x more usage" of *what?*), flagship models quietly leaving subscriptions for usage credits, prices changing mid-year. People were making a real financial decision blind.

Plenty of calculators compare API rates against each other. Almost none answer the question people were actually asking: **should I keep my subscription, or switch to usage billing?** This page does that one comparison — with every price sourced, date-stamped, and an honesty box about what the math can and can't tell you.

It was scouted, chosen, and built autonomously by Claude (Fable 5) from those HN discussions, as an experiment in agent-built micro-projects. A human (Jerome) reviews and publishes.

## How the math works

Monthly API cost = requests/day × 30.4 × (input tokens × input rate + output tokens × output rate).

Subscriptions are flat-priced, so they appear at sticker price — with a caveat, because that's the honest part: API costs are exact math; subscription *value* is not. Providers publish vague, changeable limits. If your API-equivalent usage is many times a plan's price, you'd likely hit that plan's cap. Prompt caching (often ~90% off repeated input) isn't modeled, so real API bills for repetitive workloads can come in lower.

## How prices stay current

There is no live feed — all data sits in two plain arrays at the top of `index.html` (`SUBSCRIPTIONS` and `API_MODELS`), each entry with its source URL. House rules:

- **No unsourced prices.** If it can't be linked, it doesn't ship.
- Every re-verification bumps the visible "last verified" date.
- Provider pages beat secondary coverage where available.

Spotted a stale or wrong price? **Please open an issue or PR** — include a source link. That's the single most useful contribution to this project.

## What about images?

The same question exists for image generation, so the page compares that too: per-image API pricing (GPT Image, Imagen 4, Flux, Ideogram — from $0.005 to $0.06 per image) against Midjourney's flat tiers. One honest wrinkle: Midjourney doesn't sell images, it sells fast GPU hours, so its capacity figures (~200 images on Basic, ~3,600 on Mega) are estimates at roughly one GPU-minute per image — treat them as ballpark, not quota. Also worth knowing before you spend anything: ChatGPT and Google AI subscriptions already include image generation inside their general usage limits, so if you pay for one, try that first. All image prices currently come from secondary coverage rather than provider pages, and are date-stamped like everything else.
## Disclaimer

Prices were verified against public sources on the date shown on the page; some come from secondary coverage rather than provider pages. AI pricing changes frequently. Verify at the source before spending money. Not financial advice.



## License

MIT — see [LICENSE](LICENSE).
