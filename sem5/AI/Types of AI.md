 - [[# Simple Reflex]]
 - [[# Model-based reflex]]
 - [[# Goal based]]
 - [[# Utility based]]
 - [[# Learning based]]


# Simple Reflex


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.10 - 23.20pm.drawing",
	"width": 1186,
	"aspectRatio": 2.7905882352941176
}
```

## Psuedocode
function sra(percept) returns action
persistent rules
state <- interpret-input(percept)
action <- rule-match(state, rules)
return action

# Model-based reflex


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.10 - 23.26pm.drawing",
	"width": 1196,
	"aspectRatio": 2.787878787878788
}
```


## Psuedocode
function mra(percept) returns action
persistent rules, state, sensor_model, action, transition_model
state <- update-state(percept, state, transition_model, sensor_model)
action <- rule-match(state, rules)
return action

# Goal based


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.10 - 23.32pm.drawing",
	"width": 1136,
	"aspectRatio": 2.0394973070017954
}
```


# Utility based


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.10 - 23.35pm.drawing",
	"width": 1166,
	"aspectRatio": 1.3815165876777251
}
```


# Learning based



```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.11 - 0.55am.drawing",
	"width": 1172,
	"aspectRatio": 1.4415744157441575
}
```
