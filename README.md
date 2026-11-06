# VNS Parameter Explorer

An interactive teaching page showing how the four programmable parameters of vagus nerve stimulation (VNS) for epilepsy — output current, pulse width, frequency and duty cycle — change:

1. which nerve fibers a single pulse recruits (A, B, C fibers; acute vs chronic fibrosis),
2. the strength–duration relationship between current and pulse width,
3. the waveform the nerve actually receives (including the 2 s ramps counted in duty cycle),
4. battery longevity (LivaNova SenTiva or AspireSR tables, selectable), and
5. hardware and safety limits (lead impedance, output-current limit ≈ 12 V ÷ impedance, ON > OFF warnings).

Open `index.html` in any browser. No build step and no external dependencies.

## Model and sources

Every control, readout and figure carries a source tag: **Manual** (LivaNova physician's manual or technical sheet), **Lit** (published study) or **Model** (an illustrative assumption made for this page). Parameter options, the four example presets (phase 1 targets by pulse width and the phase 2 44% duty-cycle step) and the duty-cycle rules (ON time longer than OFF time not recommended; OFF < 1.1 min unavailable with AutoStim) follow the manual. A duty-cycle picker lists the manual's phase 2 progression (Figure 39) and every ON/OFF combination in Table 32, flagging combinations that are not recommended or not available with AutoStim.

- Fiber recruitment is a qualitative sketch (a generic Weiss strength–duration relation with parameters chosen for this page). It shows only the direction of change, so the page displays no recruitment percentages. The numbers Helmers et al. 2012 actually reported from their computer model are listed separately on the page.
- Parameter ranges, impedance limits (high ≥ 5300 Ω, low ≤ 600 Ω), the output-current limit, ramp rules and duty-cycle definition follow the LivaNova VNS Therapy Physician's Manual — Epilepsy (US), August 2026.
- Battery values are from the physician's manual longevity tables at 3 kΩ lead impedance: SenTiva Model 1000/1000-D (§10.1) and AspireSR Model 106 (§10.2); years to end of service are the sum of BOL→IFI, IFI→NEOS and NEOS→EOS. The SenTiva values match the technical information sheet "Impact of SenTiva AutoStim Feature on Battery Longevity". For AspireSR with AutoStim off only the 10% duty column is used (its 33% and 50% columns give no ON/OFF times), and values whose BOL→IFI is listed as ">10 years" are shown as lower bounds. Both generators have the same programmable ranges; they differ in magnet stop time (SenTiva 10 s, AspireSR 5 s) and in day-night and scheduled programming (SenTiva only).
- Other sources: Krahl 2001 (C fibers not required), Hulsey 2017 (parameter effects on locus coeruleus firing), Agnew 1989 (stimulation safety), Entezami 2021 and Gigliotti 2018 (high impedance and revision).

## Disclaimer

For education only. Not a clinical programming tool. Always follow the manufacturer's manual and clinical judgment.

## License

Code: MIT. Cited data remain the property of their respective authors and publishers.
