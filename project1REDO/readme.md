homework #1

<font size="5">**CIS211—Computer Science II**</font>

<font size="5">**Homework #1**</font>

<font size="5">**due: Thursday, 4/7/2011, 9 pm**</font>

<font face="Times New Roman, serif"><font size="3">For this assignment you are to implement an inheritance hierarchy to represent items at a library. At the root of the hierarchy is the abstract base class LibraryItem. Each LibraryItem can be checked in or out, and the toString() method provides a detailed description. Some basic information -- title, publication year, and checkout status -- can be obtained as well. LibraryItem has three subclasses: Book, Magazine, and Video. Video itself has two subclasses: DVD and VideoTape. The different types of objects store different information (e.g., books have authors and magazines have issues).</font></font>

<font face="Times New Roman, serif"><font size="3">The end goal of this assignment is create the objects that the given library catalog will use to do all the things that you would normally do at a library. We will provide a stub of the LibraryItem class to get you started, as well as a simple test file. You will find more details below.</font></font>

<font face="Times New Roman, serif"><font size="3">You must have the following classes:</font></font>

<center>

<table border="1" cellpadding="2" cellspacing="0" width="722"><colgroup><col width="206"> <col width="506"></colgroup>

<tbody>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">Class</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">Description</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">LibraryItem (stub)</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">This abstract class should hold a title (String), a year (int), and checkedOut (boolean) status. It already has methods to check-out and check-in itself. You will need to finish implementing toString, for generating a detailed description for each LibraryItem, and compareTo, for ordering items alphabetically based on their titles. You will also need to add getters getTitle() and getYear(), for the item's title and publication year, respectively.</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">Book</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">Book should have a new constructor that accepts five arguments: title, publication year, author first name, author last name, and number of pages. Its implementation of getType() should return "Book". You should add methods getAuthorFirst(), getAuthorLast(), and getNumPages() that return the author first name, last name, and number of pages, respectively.</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">Magazine</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">Magazine should have a new constructor that accepts three arguments: title, publication year, and issue number. Its implementation of getType() should return "Magazine". You should also add a method getIssue() to get the issue number.</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">Video</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">Video should have a new constructor that accepts three arguments: title, publication year, and running time, in minutes. It should be an abstract class and not implement getType(). You should also add a method getRunTime(), which returns the number of minutes.</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">VideoTape</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">The VideoTape constructor should take the same parameters as the Video constructor. Its implementation of getType() should return "VideoTape".</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">DVD</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">The DVD constructor should take four parameters: title, year, running time (in minutes), and the number of chapters. Its implementation of getType() should return "DVD". You should also add a method getNumChapters(), which returns the number of chapters.</font></font>

</td>

</tr>

</tbody>

</table>

</center>

<font face="Times New Roman, serif"><font size="3">Each concrete class that extends the LibraryItem class must have the following public methods.</font></font>

<center>

<table border="1" cellpadding="2" cellspacing="0" width="722"><colgroup><col width="206"> <col width="506"></colgroup>

<tbody>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">Method</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">Description</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">constructor</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">Each item should have a constructor that creates a new instance of the class by creating an instance of the super class (LibraryItem) and filling in all of its own fields by using the inputs of the constructor. Parameters for each item are described above.</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">String getType()</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">This should return the object's type (a field inherited from the LibraryItem). Specific strings are described above.</font></font>

</td>

</tr>

<tr valign="TOP">

<td width="206">

<font face="Times New Roman, serif"><font size="3">String toString()</font></font>

</td>

<td width="506">

<font face="Times New Roman, serif"><font size="3">This should return a string that gives detailed information on the object in question by using **and** overriding the toString() method inherited from LibraryItem and adding specific fields unique to its sub-classes.</font></font>

</td>

</tr>

</tbody>

</table>

</center>

<font face="Times New Roman, serif"><font size="3">An example of how these classes are used is shown in the provided [LibraryTest.java](http://www.cs.uoregon.edu/classes/11S/cis211/a1/LibraryTest.java) file. The expected output is here: [LibraryTest-output.txt](http://www.cs.uoregon.edu/classes/11S/cis211/a1/LibraryTest-output.txt).</font></font>

As shown by the example output file, the output for toString() should follow the format: [Type] -- [Title] ([Year]) -- [type specific information (separated by '. ' (periods)).] Here are a few examples for different types:

<pre>Book -- Frankenstein (1818) -- Author: Shelley, Mary. 100 pages.
Magazine -- Newsweek (2010) -- Issue: 6.
DVD -- Blade Runner (1982) -- 112 minutes. 12 chapters.
VideoTape -- Tron (1982) -- 96 minutes.
</pre>

The beginning of this string should be generated by the toString() method of LibraryItem. The child classes should each override the toString() method, but their implementations should call the toString() method of the superclass to generate the beginning of the description string. **If your solution duplicates code unnecessarily, you will lose points.**

Also note that the style of the each constructor is illustrated in the above example (LibraryItem info followed by object specific): please stick with each one exactly.

In order to sort items by title, we want to be able to compare items easily. We do this by implementing the Comparable interface in the LibraryItem class. This means that you must fill in a method called compareTo(LibraryItem other) in the LibraryItem class. The compareTo method should return a negative value if this item has a title that comes earlier in the alphabet than the other, a 0 if the same titles are being compared, and a positive value if this item would come later in an alphabetic ordering of the titles (if the object with the title: Newsweek had an other object with the title:Tron as its input in its compareTo class, it should return a negative number (e.g., -1) because Tron would come later in the alphabet (in code form):

<font face="Courier New, monospace"><font size="2"><font color="#7f0055">**int**</font> <font color="#000000">result;</font></font></font>

<font face="Courier New, monospace"><font size="2"><font color="#000000">VideoTape aVideo =</font> <font color="#7f0055">**new**</font> <font color="#000000">VideoTape(</font><font color="#2a00ff">"Tron"</font><font color="#000000">, 1982, 92);</font></font></font>

<font face="Courier New, monospace"><font size="2"><font color="#000000">Magazine aMagazine =</font> <font color="#7f0055">**new**</font> <font color="#000000">Magazine(</font><font color="#2a00ff">"Newsweek"</font><font color="#000000">, 2010, 6);</font></font></font>

<font face="Courier New, monospace"><font size="2">result = aVideo.compareTo(aMagazine);</font></font>

<font color="#3f7f5f"><font face="Courier New, monospace"><font size="2">//result should now be a positive number (e.g., 1)</font></font></font>

Hint: there is a trick using a built-in method to do this method in one step (but you do not have to use it)...

Based on a question in _Building Java Programs_ by Stuart Reges and Marty Stepp.

For UoO CIS 211
