# Final SUEWS Community Hackathon Submission

Author: Farrah Jasmine Dingal

This repository publishes the final SUEWS Community Hackathon submission for the UDA-city heat hazard-to-risk workflow. The page uses the official UDA-city dataset, runs the present hot-humid and +2.5 C humidity-preserving future stress-test scenarios, and reports dangerous-heat hours plus a UNDRR-style socio-economic heat-risk indicator.

- Pages URL: https://farrahdingal.github.io/suews-hackathon-submission/
- Official UDA-city dataset: https://github.com/UMEP-dev/uda-city-hackathon
- Dataset entry point: https://github.com/UMEP-dev/uda-city-hackathon/blob/main/agent_manifest.yml
- SUEWS project: https://suews.io/

The published page is in `docs/index.html`. It includes an interactive risk explorer so readers can switch scenarios, compare dry-bulb heat with a WBGT screening proxy, and adjust the relative weight placed on hazard, exposure, and vulnerability. These controls are interpretation levers based on the completed SUEWS outputs; they do not rerun SUEWS.

CSV outputs are in `analysis/` and mirrored in `docs/data/` for page downloads. The main files are:

- `hazard_risk_summary.csv`: combined present/future dangerous-heat hours and socio-economic heat-risk ranks.
- `risk_present.csv`: present scenario risk bridge.
- `risk_future.csv`: future +2.5 C scenario risk bridge.
- `heat_stress_screen_summary.csv`: dry-bulb hazard, WBGT screening proxy, hot-sunny-low-wind hours, and maximum heat-stress values by neighbourhood.
- `heat_stress_time_of_day.csv`: detailed time-of-day heat-stress summary by neighbourhood.
- `heat_stress_time_of_day_by_type.csv`: compact time-of-day summary by neighbourhood type.

The SUEWS-agent tool-call log is in `transcripts/suews_agent_tool_log.md`.

## SUEWS citation note

Please cite SUEWS following the official guidance at <https://docs.suews.io/stable/#how-to-cite-suews>, including Jarvi, Grimmond & Christen (2011) and Ward, Kotthaus, Jarvi & Grimmond (2016). This workflow used `supy 2026.6.5`.
