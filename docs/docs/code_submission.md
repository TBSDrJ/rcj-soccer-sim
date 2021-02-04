# Code submission

To play the competition, the code that's powering the team's robots needs to
get to the organizers.

Let's talk a bit about how to do this.

## From controllers to a submission

Suppose you have the folder structure which looks like this

```
controllers/
├── robot1/
│   └── robot1.py
│   └── utils.py
├── robot2/
│   └── robot2.py
└── robot3/
    └── robot3.py
```

To submit it for the competition, there are two things we need to do:
1. Add a team name
2. Create a ZIP archive

### Add a team name

The folder structure above does contain some code but it is not immediately
obvious which team does it belong to.

To make it obvious, please create a file called `team_name.txt` on the same
level as `robot1/`, `robot2/` and `robot3/`. This file should contain a single
line of text: the name of the team (up to 32 characters).

The resulting folder structure would then look as follows:

```
controllers/
├── robot1/
│   └── robot1.py
│   └── utils.py
├── robot2/
│   └── robot2.py
├── robot3/
│   └── robot3.py
└── team_name.txt
```

### Create a ZIP archive

This step is very simple: you just pick the **three directories** that contain
the code for your three robots and the `team_name.txt` file and put them all
together into a single `.ZIP` file. There are many utilities that will do the
job -- we can recommend [7-Zip](https://www.7-zip.org/).

When you look into the resulting `.ZIP` file, the folder structure should look
as follows:

```
.
├── robot1/
│   └── robot1.py
│   └── utils.py
├── robot2/
│   └── robot2.py
├── robot3/
│   └── robot3.py
└── team_name.txt
```

Note that there is no `controllers/` folder anymore -- the `.ZIP` file only
contains three folders and a single text file called `team_name.txt`.

## Uploading your submission

Once you have your `.ZIP` file ready, the only thing left is to submit it to
the organizers. In practice, this generally means uploading it to a specific
location that will be shared with all the participating teams well before the
submission deadline.

## Things to keep in mind

- The resulting `.ZIP` file can be at most 10MB in size.

- The `.ZIP` file you submit needs to have **exactly three** first-level
  folders. That is, the folder structure after unzipping cannot look as
  follows:

```
.
├── robot1
│   └── robot1.py
├── robot2
│   └── robot2.py
├── robot3
│   └── robot3.py
└── robot4
    └── robot4.py
```

  The tournament organization software would not know which three robots to
  pick up and would most likely end up picking them up randomly.

- The organizers will run a code similarity detector on the submitted code.
    Yes, wheels really do not need to be reinvented but it would really not be
    fair to win a competition with something that's not primarily the team's
    own work. Submissions with significant overlap of duplicated code will not
    be permitted to compete in the competition.

- The code you submit will be open sourced at the end of the competition.

- If you managed to find a bug, have any question or ran into some problem,
    please do not hesitate to ask [on the forum](https://junior.forum.robocup.org/c/robocupjunior-soccer/5).
