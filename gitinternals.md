Git Internals
Q. How git store data 
Ans: it stores data in snapshots, after changing any one file of projet if we do another commit it store another snapshot
it stores another snapshot that references unchanged content efficiently through its object database.

Git Object Database:
everything inside git store as objects.
there are 4 types of object:
1.Blob 2. Tree 3. Commit 4. Tag

(1) Blob: file content
example: 
hello.txt      -->   git stores   -->   blob

Hello World                            Hello World

(2) Tree: Tree represent folders 
example:
Project             tree

README.md            blob
             ---->
src                 tree

(3) commit: commit stores
(4) Tag: used for relases
v1.0

v2.0

v3.0
example: git tag v1.0

SHA-1 Hash:Git identifies every object by a hash.
example: commit

↓

6c8a42d83d...
Every object gets a unique ID. if one bytes change entire hash as been changed

HEAD: point  to the current branch
Working tree:  files on your laptop
Staging Area(index) :
git add // move changes to staging area.

Three Areas:

Working directory -> git add --> Staging Area --> git commit -->Repository

(Q). Does Git copy the whole repository when creating a branch?

Answer

No.

