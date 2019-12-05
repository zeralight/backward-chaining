# Backward Chaining Implementation

This is an implementation of the AI backward chaining algorithm in logic theory.

## Usage
`python3 backchain.py knowledge_base_file question`
e.g
`cat animals.kb; ehco`
```
#facts
((mammal dog))
((mammal cat))
((bird penguin))
((marry cat dog))

((car ford))
    #rules
((mammal ?m) (animal ?m)) #forall m mammal(m) -> animal(m)
((bird ?m) (animal ?m))
```
Then, we ask the solver a question:
`python3 backchain.py animals.kb "((animal ?x))"`
Output:
`
((animal dog))
((animal cat))
((animal penguin))
`

Other models are available (including tic tac toe game).