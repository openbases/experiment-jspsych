# Experiment Factory Experiment

 - [JsPsych base](https://jspsych.org) base
 - [Experiment Factory](https://expfactory.github.io) ready
 - [Open Bases](https://openbases.github.io) deploy and publish option

Hi Friend! This is a [jspsych base](https://jspsych.org) for an Experiment that is friendly for use in the [Experiment Factory](https://expfactory.github.io/expfactory), and optionally reproducibly deploy and publish with [Open Bases](https://openbases.github.io). You can run it locally by putting these files in a web server, or use the Experiment Factory to generate a reproducible container. Check out the documentation above for more information, or [post an issue](https://www.github.com/expfactory/expfactory/issues) if you have any questions.

![https://expfactory.github.io/expfactory/img/expfactoryticketyellow.png](https://expfactory.github.io/expfactory/img/expfactoryticketyellow.png)

## How was it changed?

There were very minimal changes to the [tutorial provided]() and we will discuss
them here so you know you you can prepare any experiment for this template!

### 1. The organization of css and js files is different.

We place all assets under an "assets" folder, and create subfolders "js" and "css."
We do this so there is consistency with regard to the level of the files, and so
that they are easy to find based on the folder names. 

### 2. The experiment is in experiment.js

Instead of writing the javascript to control the experiment all in the [index.html](index.html), We've moved it to [experiment.js](experiment.js). This component is for the creation of the timeline, which we call `timeline`. We move it to its own file
so that it's "movable" in the case that we want to use the code in a different
deployment context (e.g., the index.html assumes a particular URL to post to, and way
to start the experiment.


### 3. We've added a LICENSE and README.md

Adding the [LICENSE](LICENSE) and this README are standard (and good!) practice for
open source experiments. You should 
[choose a permissive license](https://choosealicense.com/) so that
others can easily use (and give you credit for) your work.

### 4. We are using Jquery

We use jquery to control the timeline. This isn't totally necessary, but rather
a preference of this author.

### 5. We've added a config.json

The [config.json](config.json) is a metadata file that belongs at the top
of the folder. You can change the values for your experiment. See te Experiment
Factory [documentation](https://expfactory.github.io/contribute) for how to define these fields.

```bash
{
    "cognitive_atlas_task_id": "tsk_4a57abb949dc8",
    "instructions":"Respond to the stimuli on the screen.",
    "description":"The reaction time task in Jspsych, as an example",
    "url":"https://www.github.com/openbases/experiment_jspsych",
    "contributors": [
        "Vanessa Sochat",
        "Josh de Leeuw",
        "Felix Henninger",
        "Arfon Smith",
        "Tyler Burleigh"
    ],
    "exp_id": "experiment_jspsych",
    "name": "Simple Reaction Time Example with JSpsych",
    "reference": ["http://www.sciencedirect.com/science/article/pii/0001691869900651"],
    "template": "jspsych",
    "time": 8
}
```
