## Applying Changes from Another User Without Committing as Them
1. Second User: Create Patch Without Committing
Stage the Changes
```
git add .
```
Create the Patch File
```
git diff --cached > changes.patch
```
2. Second User: Send Patch File to the first user.
3. First User: Apply Patch
Switch to the dev Branch
```
git checkout dev
```
Apply the Patch
```
git apply /path/to/changes.patch
```
Stage the Changes
```
git add .
```
First User: Commit Changes
```
git commit -m "Commit message"
```
This method ensures that the first user is the author of the commit in the git log, and the second user's involvement is not visible in the history of the dev branch.

