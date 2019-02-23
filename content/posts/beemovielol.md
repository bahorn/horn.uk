---
title: "Bee Movie Markov chain..."
date: 2019-02-23T21:05:17Z
draft: false
---


`@jmsve` wanted a bee movie markov chain...

So I stole the markovify's [1] example code and a copy of the Bee Movie script [2]

Code:

```
import markovify
import sys

# Get raw text as string.
with open(sys.argv[1]) as f:
    text = f.read()

# Build the model.
text_model = markovify.Text(text)

# Print five randomly-generated sentences
for i in range(int(sys.argv[2])):
    line = None
    while True:
        line = text_model.make_sentence()
        if line != None: break
    print(line)

```

Output:
```
Let's see what this means?
Now we only have to be funny.
Where are you doing? - Wait a second.
And so here we have but everything we are!
Thank you. - No. - I can't.
It's a bee joke?
Anyway, if you know what it's like outside the hive, but I gotta say something.
We're in a lot of big life decisions to think bee, Barry. - Thinking bee.
Would a Miss Vanessa Bloome in 24B please report to the point where you can talk!
That's more pollen than you and I have another idea, and it's pretty much pure profit.
```

<script type="text/javascript" src="/js/speed-project.js"></script>
<script type="text/javascript">if (FATLab_SpeedProject) {FATLab_SpeedProject.Values.Format='normal'; FATLab_SpeedProject.Values.TimeSpent=5; FATLab_SpeedProject.Make();}</script>

```
* [1] https://github.com/jsvine/markovify
* [2] https://gist.githubusercontent.com/The5heepDev/a15539b297a7862af4f12ce07fee6bb7/raw/7164813a9b8d0a3b2dcffd5b80005f1967887475/entire_bee_movie_script
```
