# Unity-ML-Agents-Penguin-Tutorial
The unity project and code for Unity ML-Agents Penguin Tutorial, which are upgraded to the latest version of ML-Agents, release 3.0.

The tutorial pages are on [Unity learn (0.13)](https://learn.unity.com/project/ml-agents-penguins?uv=2019.3) and [immersivelimit (0.14)](https://www.immersivelimit.com/tutorials/reinforcement-learning-penguins-part-1-unity-ml-agents).


Repository structure
```
project
|  README.md
|
└──ML-agents_meshes // Tutorial materials
└──Penguins // Unity Project
```

The Library folder in Penguins is not included due to its big size.

### Changes in ML-Agents after 0.13

#### [release 1 to latest]
Trainer configuration, curriculum configuration, and parameter randomization configuration have all been moved to a single YAML file.

#### [0.15 -> release 1]
Using MLAgents -> Using Unity.MLAgents
Academy.instance.FloatProperties.GetPropertyWithDefault -> Academy.instance.EnvironmentParameters.GetWithDefault

(Agent's method)
- Heuristic() -> Heuristic(float[] actionsOut)
- maxStep -> MaxStep

#### [0.14 to 0.15]
(Agent's method)
- CollectObservations() -> CollectObservations(VectorSensor sensor)
- AddVectorObs() -> sensor.AddObservation()  // in CollectObservations()
- InitializeAgent() -> Initialize()
- AgentAction(float[]) -> OnActionReceived(float[])
- AgentReset() -> OnEpisodeBegin()
- Done() -> EndEpisode()
- GetStepCount() -> StepCount

#### [0.13 to 0.14]
curriculum file type: json -> yaml