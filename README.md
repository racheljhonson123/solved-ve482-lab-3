Download Link: https://assignmentchef.com/product/solved-ve482-lab-3
<br>
<h1>1         Project 1: presentations (part 2)</h1>

To ensure a more synthesized support during project 1, presentations are split into two parts. Topics are available on Canvas and their selection is on a first come first served basis.

Please well prepare your presentation and ask questions on others’ research. This should greatly help in the development of your mumsh. Be careful, mum might be listening!

<h1>2         Working with source code</h1>

When coding it is always important and useful to keep track of the changes, while also being able to export and import them in a simple fashion.

<strong>2.1    The </strong>rsync <strong>command</strong>

In Unix-like systems the rsync program allows to synchronise different folders on the same system or over the network. When applying some changes to the source code it is highly recommended to have a copy of the original version such as to be able to revert back to the previous version in case of problem.

Proceed with the following steps:

<ul>

 <li>In Minix 3 install the rsync software</li>

 <li>Install rsync on you Linux system</li>

 <li>Read rsync manpage</li>

 <li>Create an exact copy of the directory /usr/src into the directory /usr/src_orig</li>

 <li>If you have lready altered Minix 3 source code for homework 2 undo your changes from /usr/src_orig</li>

 <li>Create an exact copy of the Minix 3 directory /usr/src into your Linux system, using rsync and ssh (note that the ssh server must be activated under Linux)</li>

</ul>

<strong>2.2    The </strong>diff <strong>and </strong>patch <strong>commands</strong>

When dealing with source code two main situations are likely to arise: (i) you want to share your changes with others, or (ii) you want to apply changed performed by someone else.

Most of the time updates on source code concern few lines scattered over several files. Therefore instead of sharing all the files it is much more convenient to only specify which lines should be updated, and how. This is the role of the diff command. The patch command is used to apply the changes previously created with diff. Both diff and patch programs should already be installed in your OS.

Proceed with the following steps:

<ul>

 <li>Read the manpages of diff and patch</li>

 <li>Edit a file of your choice in /usr/src, e.g. add a comment to a file</li>

 <li>Using the diff command, create a patch corresponding to the above changes</li>

 <li>Retrieve your patch on your Linux system</li>

 <li>Apply your patch to the copy of /usr/src_orig on your Linux system</li>

 <li>Revert the patch

  <ul>

   <li><strong>Remarks</strong></li>

  </ul></li>

</ul>

The programs rsync, patch and diff are very useful however when big projects are managed by many people at the same time they are not convenient to handle. A more advanced, automatised approach is required such as to help solving collisions in a more simple way. For instance user <em>A </em>commits some changes on the initial version of the file foo.c. Then user <em>B </em>does the same. Notice that changes made by <em>B </em>may collide with updates from <em>A</em>. To prevent such issues <em>B </em>should have worked based on <em>A</em>’s version of the foo.c file.

To overcome such kind of issues and render things smoother and easier several systems were created; at the moment the most commonly used is called git, older ones such as svn or cvs are still used in some places.

In the remainder of this course you will be required to use the ve482 git server in order to keep track of your project work.

<ul>

 <li><strong>Basic git usage</strong></li>

</ul>

Go to <a href="https://learngitbranching.js.org/">http://learngitbranching.js.org/</a> and complete the following levels:

<ul>

 <li>Main → Introduction Sequence: all;</li>

 <li>Main → Ramping Up: all;</li>

 <li>Main → A mixed bag: 1, 4;</li>

 <li>Remote → Push &amp; Pull – Git Remotes!: 1-4, 6;</li>

</ul>

<h1>3         Scripting and regular expressions</h1>

Two programming languages often used in conjunction with Bash are sed and awk.

<ul>

 <li>Using curl or wget retrieve information on <a href="https://aqicn.org/?city=Shanghai&amp;widgetscript&amp;size=large&amp;id=52b39d71decf07.20261781">shanghai air quality</a> and pipe it to sed which should parse the output in order to display the information in the terminal following the format below AQ: value Temp: value ºC (e.g. AQ: 55 Temp: 24 ºC).</li>

 <li>Pipelining the output of ifconfig to awk return only the ip address of your current active network connection (the active network interface can be passed to ifconfig).</li>

</ul>