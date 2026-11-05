# VNS Parameter Explorer

An interactive teaching page showing how the four programmable parameters of vagus nerve stimulation (VNS) for epilepsy — output current, pulse width, frequency and duty cycle — change:

1. which nerve fibers a single pulse recruits (A, B, C fibers; acute vs chronic fibrosis),
2. the strength–duration relationship between current and pulse width,
3. the waveform the nerve actually receives (including the 2 s ramps counted in duty cycle),
4. battery longevity (LivaNova SenTiva table), and
5. hardware and safety limits (lead impedance, output-current limit ≈ 12 V ÷ impedance, ON > OFF warnings).

Open `index.html` in any browser. No build step and no external dependencies.

## Model and sources

- Fiber recruitment uses a Weiss strength–duration relation with a lognormal spread of thresholds. It is calibrated only to two anchors from Helmers et al. 2012 (about 99% of A/B fibers recruited at 1.5 mA / 500 µs acutely; about 53% with 110 µm fibrosis). It is an illustration, not a patient-specific model.
- Parameter ranges, impedance limits (high ≥ 5300 Ω, low ≤ 600 Ω), the output-current limit, ramp rules and duty-cycle definition follow the LivaNova VNS Therapy Physician's Manual — Epilepsy (US), August 2026.
- Battery values are from the LivaNova technical information sheet "Impact of SenTiva AutoStim Feature on Battery Longevity" (lead impedance 3000 Ω).
- Other sources: Krahl 2001 (C fibers not required), Hulsey 2017 (parameter effects on locus coeruleus firing), Agnew 1989 (stimulation safety), Entezami 2021 and Gigliotti 2018 (high impedance and revision).

## Disclaimer

For education only. Not a clinical programming tool. Always follow the manufacturer's manual and clinical judgment.

## License

Code: MIT. Cited data remain the property of their respective authors and publishers.
