# html-goto
Want to change the URL of a WebView tab that won't let you edit the address bar? This is for you.

## Step 1
Right click on the current WebView page you're on and select **`Inspect`**, or hit `F12` on your keyboard.

## Step 2
Paste the following code in the console line:
```javascript
fetch('https://raw.githubusercontent.com/diamondSierra/html-goto/main/index.html')
  .then(response => response.text())
  .then(html => {
    let newWindow = window.open();
    newWindow.document.write(html);
    newWindow.document.close();
  });
```

If prompted, enter `allow pasting` and hit enter, if your browser blocks direct code pasting.
