# get-kindle-highlights
If you're anything like me, you probably like to keep your Kindle hihglights on a separate location. I use a Trello board to keep a record of the books I read and any highlights I made. This is a little bookmarklet that lets you copy your highlights from your Kindle books.

## How use it:

1. Drag the [bookmarklet link](javascript: (function(){const body=document.querySelector('body');const highlights=[...document.querySelectorAll('#highlight')];const newHighlights=highlights.map(highlight=> `${highlight.innerText}`).join('\n\n');const input=document.createElement('textarea');const close=document.createElement('button');input.value=newHighlights;input.style.position='absolute';input.style.left=0;input.style.top=0;input.style.width='100%';input.style.height='100%';input.style.backgroundColor='white';input.style.fontSize='14px';input.style.paddingTop='50px';input.classList.add('myClipboard');body.appendChild(input);const myClipboard=document.querySelector('.myClipboard');myClipboard.focus();myClipboard.select();close.innerText='Close';close.style.position='absolute';close.style.right='10px';close.style.top='10px';close.style.padding='5px';close.style.border='none';close.style.zIndex=10;close.style.backgroundColor='black';close.style.color='white';close.style.fontWeight='bold';close.style.fontSize='16px';close.classList.add('closeClipboard');body.appendChild(close);const closeBtn=document.querySelector('.closeClipboard');closeBtn.addEventListener("click", function(e){myClipboard.remove(); closeBtn.remove();});})();) to your browser's bookmarks toolbar.
2. Go to [https://read.amazon.com/kp/notebook](https://read.amazon.com/kp/notebook) and select a book from your list of books
3. Click the bookmarklet on your browser's bookmarks toolbar
4. Copy (cmd+c/ctrl+c) and paste your highlights on your location of choice.
