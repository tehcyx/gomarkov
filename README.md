# Markov Chain
library for using Markov Chain in Go

# Usage
Create a dictionary:
```
dict := markov.TrainFromFolder("training", 10000000)


Adjust factors on the dictionary via builtin fitness function or roll your own:
```
dict = markov.BulkAdjustFactors(dict, 10000, []markov.FitnessFunc{markov.FitnessFunction})
```

Generate 20 words from dictionary (startword empty):
```
message := markov.Generate(dict, 20, "")
```