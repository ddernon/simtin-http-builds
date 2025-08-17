# simtin-http-builds

Automatic builds on every push to `master`. Bugs may occur 👀

Archives contain a compressed build + a non-compressed one.
This is because I know many people get scared when they see AV false positives,
and the compressed version triggers many, while the non-compressed version seems
globally well accepted.
And this way you can also easily make fun of antiviruses that are
[nothing more than UPX compression detectors](https://www.virustotal.com/gui/file/99c3ec93eeef5f471cc1379b1f98b0132b782874077e6f2e04f387abc7d4a226/community).

Windows builds should work on Windows 7 (which is outdated, blah blah blah) and up.
Linux buids use musl and should work on most Linux distros without particular additional setup. At some point I ran it on Ubuntu 18.

## Quick start

1. Create a file named config.json with this minimal content:

```json
{
  "serverBindings": [
    {
      "basePath": "folder to serve"
    }
  ],
  "enableDirectoryListing": true,
  "showServerSignature": 2
}
```
(obviously, put a real folder name there)

2. Place config.json in the same folder as simtin-http.exe

3. Run simtin-http.exe

4. Open your browser and go to http://127.0.0.1:8080/.  
You’ll find a more detailed manual in the server signature there.
It’s also [here](http://simtin.daviddernoncourt.com/4d61726961.html) (but this one might not be up all the time)
