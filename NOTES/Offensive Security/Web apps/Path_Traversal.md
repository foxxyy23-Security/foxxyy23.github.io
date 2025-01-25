# Path Traversal or File path Traversal

## info
- This happens when a web server tries to pull a file from thier interal database to display or use it on the web app.
- The server pulls the file from a specified directoy based on that specific web app.
- If there are no protections in place, we can try to have it pull and disaplay a file of our choice vs the file that they want

## examples
- File path looks something like this
    - /loadImage?filename=File.txt
- We can try to exploit this. 
    - /loadImage?filename=../../../etc/hosts

The amount of ../ (moving backword in said direcotry path) is dictated by the server/application (whereever files are stored)

## Random notes
- if you are trying to get a file from a filepath that has spaces - (C:\Program Files (x86)) - Use a + for the spaces in the file path
    - This is if you are using Burp