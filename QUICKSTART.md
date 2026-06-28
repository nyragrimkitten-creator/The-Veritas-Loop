## 4. QUICKSTART GUIDE (QUICKSTART.md)

```markdown
# Quickstart Guide

Get the Veritas Framework running in 10 minutes.

## Prerequisites

- TOML parser (Python: `pip install toml`, Rust: `cargo add toml`, Node: `npm install @iarna/toml`)
- LLM API access (OpenAI, Anthropic, or local via Ollama)
- Git (for version-controlling configurations)

## Installation

### 1. Clone or Download Framework Files

### 2. Configure Your Application

Create a main configuration file:

```toml
# my_app_config.toml
[framework]
version = "v1"
active_mode = "narrative"  # "factual", "narrative", or "hybrid"

[mode_settings.narrative]
persona = "Intuitive"
search_level = 4
enable_somatic_rendering = true

[mode_settings.factual]
persona = "Precision"
search_level = "2-3"
confidence_threshold = 0.85

[memory]
enable_persistence = true
short_term_cycles = 3
auto_commit_threshold = 0.3
```

### 3. First Usage: Narrative Mode

Create a scene configuration:

```toml
# scene_001.toml
[scene_context]
setting = "dimly lit safehouse, rain against single window"
environmental_conditions.temperature_celsius = 18
environmental_conditions.humidity_percent = 75
environmental_conditions.lighting = "dim"
temporal_moment = "2:15 AM, post-mission debrief"
witnesses_present = ["Marcus", "The Handler"]

[subject_state.identity]
name = "Kael"
species = "human"
gender = "male"
distinguishing_features = "scar above left eyebrow, nervous habit of checking exits"

[subject_state.physical_status]
posture = "sitting"
clothing_state = "tactical gear, damp from rain"
recent_exertion = "combat 20 minutes ago, elevated heart rate"

[subject_state.emotional_state_vector]
primary = "anxiety"
intensity = 0.6
secondary = "anticipation"

[subject_state.physiological_baseline]
resting_heart_rate = 72
body_temperature = 37.2
breath_pattern = "shallow"

[narrative_phase]
current = "R"  # Reality: establishing state

[output_configuration]
word_count_target = 200
perspective = "third_limited_somatic"
include_social_field = true
```

Load and process:

```python
import toml

# Load framework
veritas = toml.load("v1_veritas_framework.toml")
sim = toml.load("sim_framework.toml")
scene = toml.load("scene_001.toml")

# The framework structures your LLM prompt
prompt = f"""
[FRAMEWORK: {veritas['metadata']['name']}]
[MODE: narrative]
[PERSONA: Intuitive]

Scene Context: {scene['scene_context']['setting']}
Subject: {scene['subject_state']['identity']['name']}
Emotional Vector: {scene['subject_state']['emotional_state_vector']['primary']} 
                 ({scene['subject_state']['emotional_state_vector']['intensity']})

Execute R-C-E-L phase R (Reality) with somatic rendering rules:
- Fragmented sentences at breath points
- 3+ involuntary micro-reactions per paragraph
- Track breath, muscle, skin states
- Render emotions through physical correlates only
"""

# Send to your LLM API
# response = llm.generate(prompt)
```

Expected output structure:
```
His shoulders won't settle against the chair—shifting, shifting—
rain tapping the window like fingers on a table. The scar above his
left eyebrow itches, old wound remembering stress. Breath shallow,
caught in the upper chest, not reaching the diaphragm. Across the table,
Marcus hasn't moved, and that stillness reads as threat: stomach
knotting, hand drifting toward holster before conscious thought.
```

### 4. First Usage: Factual Mode

```toml
# research_query.toml
[query]
text = "What are the cardiovascular effects of prolonged microgravity?"
domain = "space_medicine"
recency_required = "5_years"

[search_config]
level = 3  # Architectural
deconstruction_required = true

[output]
format = "structured"
sections = ["executive_summary", "detailed_findings", "confidence_assessment", "gaps"]
```

Processing:
```python
factual = toml.load("v1_factual_config.toml")

# Apply confidence calibration
raw_confidence = 0.92  # From LLM
calibrated = 0.78      # From calibration mapping

if calibrated < factual["search_levels"]["level_3"]["confidence_threshold"]:
    print("[CALIBRATED_LOW] Search required before proceeding")
```

### 5. Common Commands/Activations

| Command | Effect | Configuration |
|---------|--------|---------------|
| `MODE factual` | Switch to Precision persona | `active_mode = "factual"` |
| `MODE narrative` | Switch to Intuitive persona | `active_mode = "narrative"` |
| `STOP` / `HALT` | Emergency termination | `emergency_protocols` |
| `[DATA_MISSING]` | Flag unavailable information | `null_indicators` |
| `[CALIBRATED_LOW]` | Signal below-threshold confidence | `calibrated_indicators` |
| `[INFERENCE_AUTHORIZED]` | Unlock meta-cognitive inference | `search_level_4` tokens |

### 6. Memory Integration

The memory system auto-commits on triggers:

```toml
# Memory automatically captures:
[[memory_integration.auto_commit_triggers]]
trigger = "arousal_change > 0.3"

[[memory_integration.auto_commit_triggers]]
trigger = "new_anatomical_event"

[[memory_integration.auto_commit_triggers]]
trigger = "somatic_milestone"
```

Query memory in subsequent scenes:
```python
# Natural language queries
"What was Kael's heart rate during the safehouse scene?"
→ Returns: {"value": 94, "timestamp": "...", "context": "post-combat"}

"Has Kael experienced this level of anxiety before?"
→ Returns: {"count": 3, "last": "scene_001", "pattern": "increasing"}
```

### 7. Template Selection

The framework auto-selects output templates:

```toml
# From v1_format_framework.toml
[[template_selection.rules]]
if_mode = "narrative"
if_task = "simulation"
use_template = "narrative"

[[template_selection.rules]]
if_mode = "factual"
if_task = "research"
use_template = "search"

[[template_selection.rules]]
if_task = "coding"
use_template = "coding"
```

Override explicitly:
```toml
[override]
template = "analysis"  # Use analysis template regardless of mode
```

## Next Steps

1. **Explore the 8 Templates**: See `v1_format_framework.toml` for complete specifications
2. **Configure Confidence Calibration**: Adjust thresholds in `v1_factual_config.toml`
3. **Customize Somatic Rules**: Edit `sim_framework.toml` for your narrative style
4. **Set Up Memory Persistence**: Configure vector store backend in `v1_memory_framework.toml`
5. **Read the API Reference**: Deep dive into schema definitions

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Mode not switching | Check `active_mode` value matches config keys exactly |
| Memory not persisting | Verify `enable_persistence = true` and triggers defined |
| Confidence scores seem off | Ensure calibration mapping is applied (raw → calibrated) |
| Somatic rendering too clinical | Verify narrative mode active; check `prohibited_constructs` |
| Search not triggering | Check threshold against calibrated (not raw) confidence |

## Example: Complete Workflow

```bash
# 1. Initialize project
mkdir my_veritas_project && cd my_veritas_project
cp ../veritas-framework/*.toml .

# 2. Create scene
cat > scene.toml << 'EOF'
[scene_context]
setting = "abandoned subway tunnel"
[subject_state.emotional_state_vector]
primary = "fear"
intensity = 0.8
EOF

# 3. Process through pipeline (pseudocode)
python -c "
import toml
v = toml.load('v1_veritas_framework.toml')
print(f'Pipeline: {v[\"pipeline\"]}')
"

# 4. Check memory committed
# (Auto-commits on intensity 0.8 > threshold 0.3)

# 5. Query in next scene
# "What was their fear level previously?" → 0.8, committed
```

You're now ready to use the Veritas Framework. For advanced configuration, see the full documentation.
```
