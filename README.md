# Final SUEWS Community Hackathon Submission

Author: Farrah Jasmine Dingal

This repository publishes the final SUEWS Community Hackathon submission for the UDA-city heat hazard-to-risk workflow. The page uses the official UDA-city dataset, runs the present hot-humid and +2.5°C humidity-preserving future stress-test scenarios, and reports dangerous-heat hours plus a UNDRR-style socio-economic heat-risk indicator.

- Pages URL: https://farrahdingal.github.io/suews-hackathon-submission/
- Official UDA-city dataset: https://github.com/UMEP-dev/uda-city-hackathon
- Dataset entry point: https://github.com/UMEP-dev/uda-city-hackathon/blob/main/agent_manifest.yml
- Pinned UDA-city commit checked for this final package: `0df6835c5832fb0ec78094d6acd09a45a953826b`
- Pinned manifest URL: https://github.com/UMEP-dev/uda-city-hackathon/blob/0df6835c5832fb0ec78094d6acd09a45a953826b/agent_manifest.yml
- SUEWS project: https://suews.io/

The published page is in `docs/index.html`. It includes an interactive risk explorer so readers can switch scenarios, compare dry-bulb heat with a WBGT screening proxy, and adjust the relative weight placed on hazard, exposure, and vulnerability. These controls are interpretation levers based on the completed SUEWS outputs; they do not rerun SUEWS.

CSV outputs are in `analysis/` and mirrored in `docs/data/` for page downloads. The main files are:

- `hazard_risk_summary.csv`: combined present/future dangerous-heat hours and socio-economic heat-risk ranks.
- `risk_present.csv`: present scenario risk bridge.
- `risk_future.csv`: future +2.5°C scenario risk bridge.
- `heat_stress_screen_summary.csv`: dry-bulb hazard, WBGT screening proxy, hot-sunny-low-wind hours, and maximum heat-stress values by neighbourhood.
- `heat_stress_time_of_day.csv`: detailed time-of-day heat-stress summary by neighbourhood.
- `heat_stress_time_of_day_by_type.csv`: compact time-of-day summary by neighbourhood type.

The public Codex session transcript is in `transcripts/codex_session_transcript.md`. The SUEWS-agent tool-call log is in `transcripts/suews_agent_tool_log.md`, with a CSV copy in `transcripts/suews_agent_tool_log.csv`. Readiness and validation diagnostics are saved in `transcripts/diagnostics/`, and `transcripts/workflow_notes.md` summarises the AI-assisted workflow.

Important caveat: the socio-economic layer is synthetic, risk scores are relative to these ten neighbourhoods, and the WBGT result is a screening proxy derived from completed SUEWS outputs rather than field-measured WBGT.

## SUEWS citation note

Please cite SUEWS following the official guidance at <https://docs.suews.io/stable/#how-to-cite-suews>. This workflow used `supy 2026.6.5`.

- Järvi, L., Grimmond, C. S. B., and Christen, A. (2011). The Surface Urban Energy and Water Balance Scheme (SUEWS): evaluation in Los Angeles and Vancouver. *Journal of Hydrology*, 411(3-4), 219-237. https://doi.org/10.1016/j.jhydrol.2011.10.001
- Ward, H. C., Kotthaus, S., Järvi, L., and Grimmond, C. S. B. (2016). Surface Urban Energy and Water Balance Scheme (SUEWS): development and evaluation at two UK sites. *Urban Climate*, 18, 1-32. https://doi.org/10.1016/j.uclim.2016.05.001
