First, we'll add another line to the Sundanese file, this time about word order:
$ nano sundanese.txt
$ cat sundanese.txt
belongs to the Austronesian language family
spoken in western Indonesia
diff --git a/sundanese.txt b/sundanese.txt
--- a/sundanese.txt
+++ b/sundanese.txt
 belongs to the Austronesian language family
 spoken in western Indonesia
$ git add sundanese.txt
diff --git a/sundanese.txt b/sundanese.txt
--- a/sundanese.txt
+++ b/sundanese.txt
 belongs to the Austronesian language family
 spoken in western Indonesia
    start notes on Sundanese
We've been adding one line at a time to `sundanese.txt`, so it's easy to track our
let's make a change to `sundanese.txt`, adding yet another line which unfortunately contains misinformation:
$ nano sundanese.txt
$ cat sundanese.txt
belongs to the Austronesian language family
spoken in western Indonesia
$ git diff HEAD sundanese.txt
diff --git a/sundanese.txt b/sundanese.txt
--- a/sundanese.txt
+++ b/sundanese.txt
 belongs to the Austronesian language family
 spoken in western Indonesia
$ git diff HEAD~1 sundanese.txt
$ git diff HEAD~2 sundanese.txt
diff --git a/sundanese.txt b/sundanese.txt
--- a/sundanese.txt
+++ b/sundanese.txt
 belongs to the Austronesian language family
+spoken in western Indonesia
$ git show HEAD~2 sundanese.txt
    start notes on Sundanese
diff --git a/sundanese.txt b/sundanese.txt
+++ b/sundanese.txt
+belongs to the Austronesian language family
Alright! So
as we realize Sundanese is in fact not related to Spanish and decide to scrap that line. 
	modified:   sundanese.txt
$ git checkout HEAD sundanese.txt
$ cat sundanese.txt
belongs to the Austronesian language family
spoken in western Indonesia
$ git checkout f22b25e sundanese.txt
$ cat sundanese.txt
belongs to the Austronesian language family
#	modified:   sundanese.txt
$ git checkout HEAD sundanese.txt