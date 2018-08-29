# digital scrap paper

A little in-browser note taking appliaction focused on simlicity and privacy.  
Your data never leaves your computer: no cloud storage, no browser extension.

**Link to publicly hosted copy:** http://averyn.scripts.mit.edu/monograph/

This project is basically just a glorified textbox. I'm sharing it here
not because it's particularly inventive in and of itself, but because I've
found it surprisingly useful, and I though that it might be of interest to others.

**How I use this little editor:**

I use this application
for taking notes as I work throughout the day. I've used
other note-taking tools in the past, but lately I've been trying to minimize
the amount of data I store in the cloud. I could always use sublime or another
text editor for taking notes, but I wanted something that I could use from my 
browser for jotting down ideas with minimal activitaion energy.

The application uses the following 5 lines of Javascript: this code keeps the title of the page
in sync with the title of the note, which means that a note titled `noteName` gets saved as `noteName.html`
```js
titleInput = document.getElementById('titleInput');
titleInput.addEventListener("input", function (e) {
    title = titleInput.value;
    document.title = title != "" ? title : "untitled";
});
```
When I want to save my note, I just save the whole page using `ctrl-s`,
to a "notes" directory on my desktop. Firefox also saves the contents of the textbox in the saved 
page-source. That way, when I want to view or edit my note, I can just open
up `~/Desktop/notes/myNote.html` in my browser, and overwrite the saved file
if I make any changes. 

I've found that, since I made this tool, I've gotten a lot better about writing 
notes and making lists as I work. This tool encourages me to dump my thoughts periodically,
in part because it feels even more "lightweight" than making a new 
Google Doc or firing up a text editor - it's like digital scratch-paper!
And best of all, my data never leaves my computer!

**Screenshot:**

![screenshot](screenshot.png)
