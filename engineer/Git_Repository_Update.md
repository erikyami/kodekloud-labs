## Problem

The Nautilus development team started with new project development. They have created different Git repositories to manage respective project's source code. One of the repo /opt/apps.git was created recently. The team has given us a sample index.html file that is currently present on jump host under /tmp. The repository has been cloned at /usr/src/kodekloudrepos on storage server in Stratos DC.

Copy sample index.html file from jump host to storage server under cloned repository at /usr/src/kodekloudrepos, add/commit the file and push to master branch.

## Solution

```
scp index.html natasha@ststor01:/tmp/
```

```
ssh natasha@ststor01

sudo -s

cp /tmp/index.html /usr/src/kodekloudrepos/apps/

cd /usr/src/kodekloudrepos/apps/

git add index.html

git commit -m "Add index.html"

git push
```
