# Setup

1) npm install

# Reproduction

1) npm run start
2) Open the application on your browser (problably at http://localhost:3000/)
3) Open the developer console on your browser
4) Run the following code:
```
fetch('', {
  method: 'POST',
  headers: {
    ['content-type']: 'multipart/form-data; boundary=----WebKitFormBoundaryoo6vortfDzBsDiro',
    ['content-length']: '145',
    host: '127.0.0.1:3000',
    connection: 'keep-alive',
  },
  body: '------WebKitFormBoundaryoo6vortfDzBsDiro\r\n Content-Disposition: form-data; name="bildbeschreibung"\r\n\r\n\r\n------WebKitFormBoundaryoo6vortfDzBsDiro--'
});
```

The error is problably going to be something like this:
```
this.header[h][this.header[h].length - 1] += lines[i];
                                    ^
TypeError: Cannot read properties of undefined (reading 'length')
```

This is from dicer HeaderParser.