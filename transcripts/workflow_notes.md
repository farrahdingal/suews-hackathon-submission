# Workflow Notes

This note summarises the AI-assisted workflow for the final SUEWS Community Hackathon submission by Farrah Jasmine Dingal. It complements the ordered SUEWS-agent tool-call log in `transcripts/suews_agent_tool_log.md` and the public session transcript in `transcripts/codex_session_transcript.md`.

## Submission Brief

The workflow was required to use the official UDA-city hackathon dataset, starting from `agent_manifest.yml`, rather than the London practice case. The modelling task was to run all ten UDA-city neighbourhoods for the present hot-humid scenario and the official humidity-preserving +2.5°C future stress test, then translate dangerous-heat hours into a socio-economic heat-risk indicator.

The core question was: across the ten UDA-city neighbourhoods, where is heat most dangerous to people now and under the +2.5°C stress test, and is that the same as where it is simply hottest?

## Agent-Assisted Modelling Rule

SUEWS was not run directly from the command line as the primary workflow. The required SUEWS-agent checks happened first:

1. `assess_readiness`
2. `validate_config`
3. `run_suews_present`
4. `run_suews_future`
5. `apply_risk_bridge_present`
6. `apply_risk_bridge_future`
7. `combine_hazard_risk_results`

The readiness and validation diagnostics are saved in `transcripts/diagnostics/`. The post-processing for WBGT screening and time of day used already completed SUEWS outputs and did not rerun SUEWS.

## Interpretation Choices

The final page defends four choices: the dangerous-heat threshold, the hazard-exposure-vulnerability risk framing, the visual comparison of hazard and people-risk, and the caveats that explain where the bridge from modelled heat to people holds or breaks.

The main finding is that Jade Gardens is the hottest neighbourhood by dry-bulb dangerous-heat hours, while Kampong Lama is the highest people-risk priority because hazard, exposure, and vulnerability overlap there.

## Limits Of The Workflow

The socio-economic layer is synthetic, the risk values are relative to the ten UDA-city neighbourhoods, and neighbourhood averages do not represent individual health outcomes. The WBGT result is a screening proxy based on SUEWS outputs, not a field-measured WBGT assessment.
