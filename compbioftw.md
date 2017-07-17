Computational Biology Resources FTW
---------------

### A bunch of papers

If you need a good reference or just to persuade your colleague or supervisor that she really needs to get to [where the puck is going to be](http://www.canadianbusiness.com/blogs-and-comment/stop-using-gretzky-where-the-puck-is-quote/). Actually scrape that, this train has been puffing along for quite a while now and all we can do now is not get left behind.

Also, [bioinformatics != computational biology](https://rbaltman.wordpress.com/2009/02/18/bioinformatics-computational-biology-same-no/).

- Loman, N. & Watson, M. [So you want to be a computational biologist?](http://www.nature.com/nbt/journal/v31/n11/full/nbt.2740.html) Nat Biotechnol 31, 996–998 (2013).
- Wilson, G. et al. [Best Practices for Scientific Computing.](http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745) PLoS Biol 12, e1001745 (2014).
- Wilson, G. et al. [Good Enough Practices in Scientific Computing.](https://doi.org/%2010.1371/journal.pgen.1006328) PLoS Genet 13(6): e1006328 (2017)
- Tippmann, S. [Programming tools: Adventures with R.](http://www.nature.com/news/programming-tools-adventures-with-r-1.16609) Nature 517, 109–110 (2015).

### Do not use Excel for handling dates and gene identifiers

In particular, do not export gene IDs and dates to Excel and then import
it back to R or other programming tools. You have been warned.

- Zeeberg, B. R. et al. [Mistaken identifiers: gene name errors can be introduced inadvertently when using Excel in bioinformatics.](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-5-80) BMC Bioinformatics 5, 80 (2004). Also check this blog post (with comments), from 2012 (_sic_): [Gene name errors and Excel: lessons not learned](https://nsaunders.wordpress.com/2012/10/22/gene-name-errors-and-excel-lessons-not-learned/).
- Mallona, I. & Peinado, M. A. [Truke, a web tool to check for and handle excel misidentified gene symbols.](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-3631-8) 1–3 (2017). doi:10.1186/s12864-017-3631-8

### Recommended general tutorials and tools on command line

- <http://ryanstutorials.net/linuxtutorial/navigation.php>
- <http://korflab.ucdavis.edu/Unix_and_Perl/>
- [Software Carpentry Unix Shell lesson](http://swcarpentry.github.io/shell-novice/)
- [explainshell.com](http://explainshell.com) will try to give you explanation for every element of a command line expression that you type in the search box (try it, it's really cool)

### How to install Bash shell on Windows 10

- [Bash shell on Windows 10! Pigs fly!](http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)

### Two very useful and inexpensive books on command line

- [Take Control: Command Line by Joe Kissell](https://www.takecontrolbooks.com/command-line) (aimed at
Mac users, but good for everyone - as usual ;-)
- [The UNIX workbench by Sean Kross](http://seankross.com/the-unix-workbench/introduction.html) (donationware); now with [a Coursera course](https://www.coursera.org/learn/unix)!

### Four books on computational biology I highly recommend - they will give you excellent background in various aspects of data analysis

- [Practical Computing for Biologists](http://amzn.eu/bjL85Es) by Steven H.D. Haddock and Casey W. Dunn. It covers command line, Python, installing software and manipulation of graphics.
- [Bioinformatics Data Skills](http://amzn.eu/83378iQ) by Vince Buffalo. Shell, R, Git with empasis on life science data analysis, including next-generation sequencing file handling.
- [R for Data Science](http://amzn.eu/3UPfxlL) by Garett Golemund and Hadley Wickham. Solid introduction to `tidyverse` ways of handling data and analysis by the creators and evangelists :-)
- [R Graphics Cookbook](http://amzn.eu/bi8RnNQ) by Winston Chang. ggplot2 explained using clear examples akin to recipes ("if you want to plot this, do this and that").

GitHub files from Vince’s book (there are some useful comments about
setting up the Terminal etc.): [Vince Buffalo’s GitHub account](https://github.com/vsbuffalo) and his [book-related files on GitHub](https://github.com/vsbuffalo/bds-files).

How to move around shell
------------------------

- `control-a` : move cursor to beginning of line
- `control-e` : move cursor to end of line
- `control-c` : cancel input or stop a running command
- `control-k` : delete all text from cursor to end of line
- `control-d` deletes a character in place
- `option-delete` : delete an entire word (may not work depending on whether your option key is reassigned; this is a preference in your Terminal settings)
- `option-b` : move cursor backwards an entire word (as above)
- `option-f` : move cursor forwards an entire word (as above)
- `up arrow` : access last entered command
- `control-r` : start searching shell history (start typing to search; enter will enter the current command; `command-.` will cancel)
- `control-v + [some key]` will literally print `[some key]` - useful if you want to enter a tab and `\t` doesn’t work
- `history | ![some number]` where `[some number]` is a number of a history command you want to execute (no need to copy and paste)
- You can also narrow down the last command selection by including the first letter of the last command you want to use, e.g.: `!d</code>` (if your favourite last command starts with `d`)
- `!$` retrieves the last word of the last command

### Shell prompt

Take time to make your terminal window and the font big enough!

- Default (at least on my machine): `\h:\W \u\$`
- How to check what's your current prompt: `echo $PS1`
- Hot to change your prompt: `PS1="yournewprompt"`. A very nice trick is to use PS1="\n\W\u-$ " so that you have a new line before your prompt - it's visually separated from the output of a previous command.

Useful link with options to modify your prompt: [https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)

#### Difference between .bash_profile and .bashrc

This is relevant for modifying the `$PATH`:

- [http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html)
- [http://stackoverflow.com/questions/9832770/where-is-the-default-terminal-path-located-on-mac](http://stackoverflow.com/questions/9832770/where-is-the-default-terminal-path-located-on-mac)

### Clear your screen

[How to really clear the
terminal](http://askubuntu.com/questions/25077/how-to-really-clear-the-terminal#25079)

- `clear` : clears the screen
- `control-l` : works just like `clear`
- `command-k` : clears the screen and prevents from scrolling back
- `exit` : exit shell (it closes the terminal window)

### Listing stuff (`ls`)

- `ls [a-z]*.txt` list every .txt file with lowercase letters in their name
- `ls {pear,peach}.txt` lists pear.txt and peach.txt
- `ls -1` show output in a single column
- `ls -alh` show output including hidden files (`-a`), in a long format (`-l`) and human-readable file sizes (`-h`)
- `history` displays history of the commands (can be piped into a file). If you don't want the terminal to remember the history between sessions, [start with this thread here](http://stackoverflow.com/questions/6709349/delete-terminal-history-in-linux#6709403) (it sometimes doesn't work in all systems).

### How to move around your folders

- `cd -` : go to last directory
- `.` : current folder
- `..` : parent folder

### Four ways to go home:

- `cd`
- `cd ~`
- `cd /Users/Jarek`
- `cd -` (if you were in your home folder in a previous command)

### If your folder or file names include spaces

- `\` : will escape the space character (e.g. “My\ folder”)
- If you drag your folder from Finder to a Terminal window, it will automatically recognise the path to this folder and escape spaces

### To repeat last command

- `!!`: works just like the `up arrow`, but you can modify it by adding stuff in front or behind it, e. g.: `!! -h` or `sudo !!`
- You can also narrow down the last command selection by including the first letter of the last command you want to use, e.g.: `!d` (if your favourite last command starts with “d”)

### Reading/displaying text files

- `cat`
- `less` : space to move forward, B to move back, Q to quit
- `more` : `more` on a Mac is the same as `less`
- `head` : show first few lines of the file; parameter -n specifies number of lines to show
- `tail` : as above, but for the end of the file
- `(head -n5; tail -n5) < inputfile` : display the first and last 5 lines of the input file
- `touch newfilename` : will create an empty file with a name *newfilename*
- `touch existingfilename` : will update modification date of the *exsitingfilename*
- `head -n[line number]` to display \[line number\] number of lines (if you want a range use pipes and `tail` after head -n)
- `wc` word count (displays line, word and character count); `-l -w -c` limits display to line, word or character only\

### Wildcards in shell (to do stuff on more than one file at a time)

- `*` : a wildcard for “zero or more” instances (\*og would catch anything that ends with “og”)
- `?` : a wildcard for “any single” instance (?og would catch: dog, fog, log etc.)
- `{}` : brackets will select a range of stuff ({A..Z}, {1..3}, {apple, pear, watermelon}) (this is called “brace expansion”)

Regular expressions and grep
----------------------------

### Everything you wanted to know about regular expressions

- [www.regular-expressions.info](http://www.regular-expressions.info/quickstart.html)

### Two useful regular expression testers

...but rememeber that `grep` in Notepadd++, Ruby, JavaScript or Mac
terminal can have slightly different implementations (i.e. not all
functions will work or not all functions will work the same way). When
stuff doesn't work, try `egrep` (*extended grep*) and always RTFM.

- <https://regex101.com>
- <https://regexpr.com>

A very cool regular expression recognition web app - you put in your
input and it tries to automatically find a regexp pattern to match it.
When it works, it's like magic.

- [rexpy: Automatic Discovery of Regular
  Expressions](http://rexpy.herokuapp.com)

### Wildcards for regular expression pattern matching

- `\w` Letters, numbers and \_
- `.` Any character except \\n \\r
- `\d` Numerical digits
- `\t` Tab
- `\r` Return character. Also used as the generic end-of-line character in TextWrangler
- `\n` Line-feed character. Also used as the generic end-of-line character in Notepad++
- `\s` Space, tab, or end of line
- `[A-Z]` A single character of the ranges indicated in square brackets
- `[^A-Z]` A single character including all characters not in the brackets. Note that this will include \\n unless otherwise specified, and may cause you to match across lines
- `\` Used to escape punctuation characters so they are searched for as them- selves, not interpreted as wildcards or special symbols
- `\\` The \ symbol itself, escaped

### Boundaries

- `^` Match the start of the line, i.e., the position before the first
 character
- `$` Match the last position before the end-of-line character

### Quantifiers, used in combination with characters and wildcards

- `+` Look for the longest possible match of one or more occurrences of the character, wildcard, or bracketed character range immediately preced- ing. The match will extend as far as it can while still allowing the entire expression to match.
- `*` As above, matches as many of the previous character to occur, but allows for the character not to occur at all if the match still succeeds
- `?` Modifies greediness of + or \* to match the shortest possible match instead of longest
- `{}` Specify a range of numbers to repeat the match of the previous character. For example:
- `\d{2,4}` matches between 2 and 4 digits in a row
- `[AC]{4,}` matches 4 or more of the letter A or C in a row

### Capturing and replacing

- `()` Capture the search results between the parentheses for use in the re- placement term
- `\1` or `$1` Substitute the contents of the matched into the replacement term, in numerical order. Syntax depends on the text editor or language that you are using.

### Basic grep commands

- `grep "@" [file name]` search for lines that contain "@"
- `grep -c "@" [file name]` count matching lines
- `grep -v "@" [file name]` find non-matching lines
- `grep -v -c "@"`
- `grep -c "^CGATA" [file name]` count lines beginning with CGATA
- `grep "0\.98"` greps literal dot

Other bits that didn't fit anywhere else
----------------------------------------

- `mkdir -p` : make multiple directories at once
- `tr` to substitute one thing with another or delete a query from a string

### Extracting columns and sorting

- `cut` will cut out characters or columns from a delimited file
- `cut -d":" -f2` will first split each line into columns delimited with the ":" and then extract -f2 (second) column from each line
- `sort` can use column numbers `sort -k[number of the column]n` (n is for numerical, r is for reverse). You can combine sorting by column, i.e. first by column 3 then by 2 `sort -k 3 -k 2nr`
- `uniq` will collapse multiple matches, but they have to be next to each other, so the file has to be first sorted by `sort`

### Prevent accidental deletion or overwriting files or folders

- `rm -i` flag `-i` will prompt you to confirm before proceeding to remove. It can be used with other commands, such as `mv`.

------------------------------------------------------------------------

Some less basic stuff
---------------------

### Another book on bioinformatics

-   [Computational Biology - A Practical Introduction to BioData
    Processing and Analysis with Linux, MySQL, and
    R](http://www.amazon.co.uk/Computational-Biology-Practical-Introduction-Processing/dp/3642347487/ref=sr_1_fkmr0_1?ie=UTF8&qid=1455484205&sr=8-1-fkmr0&keywords=oComputational+Biology+-+BioData+Processing+and+Analysis)
    by Röbbe Wünschiers (Amazon.co.uk), which includes good coverage of
    *awk* and *sed*. The book’s website is at
    <http://www.staff.hs-mittweida.de/~wuenschi/doku.php?id=rwbook2>.

### The extensive “missing manuals” for *awk* and *sed*

-   [AWK](http://www.grymoire.com/Unix/Awk.html#TOC)
-   [SED](http://www.grymoire.com/Unix/Sed.html#TOC)

**screen**

`Ctrl-a` d to disconnect from the screen\
`screen -ls` list of screens\
`screen -r [id of the screen]` to reconnect to the screen

apparently there is a copy mode where I can use cursor to select and
copy the contents of the terminal

`source` will execute the commands inside text files as if they were put
in directly\
`source [filename]`

dates should be in an ISO format to be sorted correctly e.g. 2010–04–19

data frame is a column-based data type, not row-based

#### Enable NTFS read/write in MacOS

-   <http://www.makeuseof.com/tag/write-ntfs-drives-el-capitan-free/>
-   [http://osxdaily.com/2013/10/02/enable-ntfs-write-support-mac-os-x/](http://www.makeuseof.com/tag/write-ntfs-drives-el-capitan-free/)

`open /Volumes`\
`sudo echo "LABEL=DRIVE_NAME none ntfs rw,auto,nobrowse" >> /etc/fstab`

### Extract sequences from the fastq file

-   <https://www.biostars.org/p/72433/>
-   <http://linuxcommando.blogspot.co.uk/2008/04/using-awk-to-extract-lines-in-text-file.html>
-   <http://bioinformatics.cvr.ac.uk/blog/essential-awk-commands-for-next-generation-sequence-analysis/>

`reads.fastq | awk '{if(NR%4==2) print length($1)}' | sort -n | uniq -c > read_length.txt`\
`awk '0 == (NR + 1) % 2' inputfile.txt`

`cat barcount.txt | sed -E -e 's/^ +([0-9]+) [ACGTN]+/\1/' | awk 'BEGIN{total=0} {if ($1>10000) total+=$1} END{print total}'`\
228852

-   <http://stackoverflow.com/questions/19748184/unix-awk-deleting-every-two-lines>

#### How to add Dropbox to remote machines at the command line {#howtoadddropboxtoremotemachinesatthecommandline}

-   <http://cymeandcystidium.com/2012/08/tiny-tutorial-adding-dropbox-to-remote-machines-at-the-command-line/>

### Automator script to convert multiple *docx files into* .pdf (Mac only) {#automatorscripttoconvertmultipledocxfilesinto.pdfmaconly}

-   <http://igikorn.com/batch-convert-word-documents-pdf/>

### Utitlities to handle fastq files etc. {#utitlitiestohandlefastqfilesetc.}

-   [seqtk](https://github.com/lh3/seqtk)
-   [fastx-toolkit](http://hannonlab.cshl.edu/fastx_toolkit/download.html)
-   [emboss](http://emboss.sourceforge.net/what/)
-   [biopieces](http://maasha.github.io/biopieces/)

#### Setting up ftp proxy via command line {#settingupftpproxyviacommandline}

This assumes you cannot modify or don’t trust the system–wide settings
in Ubuntu or Mac

-   [HowTo: Use a Proxy on the Linux Command
    Line](http://www.shellhacks.com/en/HowTo-Use-a-Proxy-on-the-Linux-Command-Line)
-   [How to change proxy setting using Command line in Mac
    OS?](http://superuser.com/questions/316502/how-to-change-proxy-setting-using-command-line-in-mac-os)
-   [ftp MAN page](http://linux.about.com/od/commands/l/blcmdl1_ftp.htm)

#### Tutorial on scp {#tutorialonscp}

- [https://www.garron.me/en/articles/scp.html](https://www.garron.me/en/articles/scp.html)

#### Git basics {#gitbasics}

`git init` to initialise repository (a tracked directory)\
`git add` to explicitly add files to tracking (files can also be
explicitly ignored)\
`git commit` to “upload” the tracked version to a repository\
`git status` to check\
`git diff` to check differences between committed version and current
version (must be done before add?)\
`git log` to list all commits in reverse chronological order

To push local repository to github:

`git remote add origin https://github.com/jarekbryk/example_repository.git`
(all in one line)

To check if it was pushed all right:

`git remote -v`

**origin** is the remote\
**master** is the local one

To synchronise the local with the remote:

`git -u push origin master` (it pushes TO origin FROM master)