# Team workflow

## First-time setup

Clone this repository once, then work inside that clone:

```powershell
git clone https://github.com/bunnathtith-bjorn/epp1-maze-robot.git
cd epp1-maze-robot
git config user.name "Your Name"
git config user.email "YOUR-GITHUB-COMMIT-EMAIL"
```

Replace the author placeholders with your own details. Your name need not match your GitHub username. Use an email associated with your account or the private commit email displayed in GitHub Settings > Emails.

Open the sketches inside this repository in Arduino IDE and save before committing. Git does not upload unsaved editor changes.

## Begin a task

Run these commands with a clean working tree (check `git status` first):

```powershell
git switch main
git pull --ff-only
git switch -c firmware/motor-test
```

Choose a new descriptive branch name for each task, such as `firmware/motor-test`, `firmware/sensor-calibration`, or `electronics/wiring-diagram`. A branch contains both main folders. Two people should use different task branches.

## Save and upload firmware changes

```powershell
git status
git add firmware/
git diff --cached
git commit -m "Add motor test"
git push -u origin HEAD
```

`add` selects changes, `commit` saves a revision locally, and `push` uploads it. Inspect the staged diff before committing. Stop and resolve any error before running the next command; do not force-push to fix a rejected push.

On GitHub, create a pull request from your branch into `main`. Describe the changes and testing, ask a teammate to review, then merge when ready. A successful compile and an on-robot test are different checks: record both honestly.

## Upload electronics through GitHub

Open the appropriate folder on GitHub, then Add file > Upload files. Upload files or a folder, describe the change, and select a new branch for the commit. Open a pull request into `main`.

For KiCad, include the project, schematic, PCB, and any custom symbols/footprints needed to open the project. PDF exports help teammates review without KiCad.

After a pull request is merged, synchronise locally before the next task:

```powershell
git switch main
git pull --ff-only
```

Commit your current work before switching branches. Website uploads also change Git history; pull them after they reach main.

## Initial branches

`main` is the shared starting version. `setup/electronics` and `setup/firmware` are initial task branches for the first uploads. They begin at the same scaffold commit. After each is merged, use a new task branch for later work.

To use the initial firmware branch after it is available locally:

```powershell
git switch setup/firmware
```

For teammates who have just cloned and only have the remote branch:

```powershell
git switch --track origin/setup/firmware
```

## Documentation

Use relative links so they work for every teammate. Keep measured results separate from estimates and proposals. Record units, hardware configuration, and firmware revision with test data.
