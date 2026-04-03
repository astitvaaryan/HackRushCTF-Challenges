# Challenge: Buried

## What the Challenge Was
We were given a PDF file named `confidential.pdf`. When you open it, it looks like a normal document with some text, but certain parts are covered with black boxes, like a top-secret file. The challenge gave us a clue: "Not Everything is as it appears!"

## What Did Not Work
At first, I thought the secret flag was just hidden under the black boxes. 
- **My First Try:** I tried to select the text under the black boxes, copy it, and paste it into a blank notepad. 
- **Why it failed:** I did find words hidden under the black boxes, but it was just random, nonsense text. The creator of the challenge put it there on purpose to trick us!

## How I Solved It
Since the flag wasn't written on the actual pages of the PDF, I realized it must be hidden in the file's background details. Every file has hidden information attached to it called "metadata," which tells you things like who created the file and when.

### My Steps:
1. **Checking the Background Details:** I decided to look at the hidden metadata of the PDF to see if the author left a secret message there.
2. **Using a Tool:** I used a free online PDF metadata viewer. This is a tool that reads the hidden background information of a file for you.
3. **Uploading the File:** I uploaded `confidential.pdf` into the tool.
4. **Finding the Answer:** The tool gave me a list of all the hidden details. I read through the list and looked at sections like the "Author" and "Title". Finally, I found the secret flag hiding in the "keywords" section!

*Here is what the hidden background details looked like:*
> file_name: confidential.pdf
> author: The Almighty Kalp Shah
> title: Hackrush CTF
> keywords: HRCTF{h4ck3r_bh41_h4ck3r}

## What I Learned
I learned that files contain a lot more information than what you can just see on the screen. Background details (like the author's name or keywords) are often ignored, but they can be used to hide secret data. In real life, it is important to clear out these background details before sharing a document, so you don't accidentally leak private information.

## The Flag
`HRCTF{h4ck3r_bh41_h4ck3r}`
