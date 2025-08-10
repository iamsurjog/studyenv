---
id: Environment Types
aliases: []
tags: []
---

1. [[#Fully Observable vs Partially observable]]
2. [[#Deterministic vs stochastic]]
3. [[#Competition vs Collaborative]]
4. [[#Single agent vs multi agent]]
5. [[#static vs dynamic]]
6. [[#Discrete vs Continuous]]
7. [[#Episodic vs Sequential]]
8. [[#Known vs Unknown]]


## Fully Observable vs Partially observable 

When an agent sensor is able to the complete state of the environment at all points of time - Fully Observable

 - Chess fully
 - Driving partially

## Deterministic vs stochastic

When the current state can determine the next states easily

- chess is deterministic
- driving is stochastic

## Competition vs Collaborative

when agents are competing and not collaborating

 - chess agents are competing
 - driving collaborating

## Single agent vs multi agent

Environment with only one agent 

## static vs dynamic

Idle environment with almost no changes is static while environment which is constantly changing is a dynamic

- Empty house
- Roller coaster

## Discrete vs Continuous

Environment having constant/finite number of actions vs continuous actions and not discrete

- chess is discrete
- driving continuous

## Episodic vs Sequential

previous action has no effect on current or future actions vs it does

- pick and place robot
- checkers/chess

## Known vs Unknown

consequence of action is known/unknown


|      agent       | observable | deterministic | competition | single | static | discrete | episodic | known |
| :--------------: | :--------: | :-----------: | :---------: | :----: | :----: | :------: | :------: | :---: |
|    crossword     |   fully    |      yes      |    nope     |  yes   |   no   |   yes    |    no    |  yes  |
| chess with clock |   fully    |      yes      |     yes     |   no   |   no   |   yes    |    no    |  yes  |
|      poker       | partially  |      no       |     yes     |   no   |   no   | discrete |    no    |  no   |
|                  |            |               |             |        |        |          |          |       |
