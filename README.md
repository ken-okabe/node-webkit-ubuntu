node-webkit-ubuntu
==================

```

Fix the libudev.so.0 error on Ubuntu 13.04 / 13.10
If you are using Ubuntu 13.04 or 13.10, then you will get the following error when you first run nw.

error while loading shared libraries: libudev.so.0: cannot open shared object 
file: No such file or directory
The problem is that newer versions of Ubuntu use libudev.so.1 while node-webkit is built against libudev.so.0. However, fixing the error is easy.

sudo apt-get install ghex

cd ~/opt/node-webkit

ghex nw
The ghex GUI will open with nw loaded.

Expand the window as this makes editing easier.
Press Ctrl + F to open the Find dialog box.
Press Tab to move the cursor to the right textbox.
Type libudev.so.
Click Find Next.
You should now see libudev.so.0. Note: **libudev.so will be highlighted in red. Hint: Resize the window if you do not see every character in libudev.so.0.
Select 0 with your mouse and type 1.
Select File, click Save.
Select File, click Exit.
Run nw and you should see an empty node-webkit window.

```
