### Sherwood Lab guide for using RNAStructure on the Virtual Machine

The program is set up on Sam's Google Cloud platform account, contact him at sammy.barkal@gmail.com for access. 

#### Step 1) Upload a .fasta or .fa file to the VM



1) Change directories from the home directory to where we're keeping the required scripts and the .fasta files. to do this type `cd ASOproj`

2) If you've used an ssh client to access this, you'll need to file transfer using your method's protocol, something like `scp`, however, you're most likely using this through Sam's Google terminal through a browser. Once you have the terminal window open, click the gear icon in the top right corner -> Upload file -> Select your file in .fasta format.

3) Make sure your file is there, type `ls` in the terminal and see if your file is listed in the directory


#### Step 2) Run the program 

RNAStructure is a perl (.PL) file that takes the input file (the one you just uploaded) as its first argument and the output file as its second argument. Assuming you did everything in step 1 correctly you should have no problem running this. One thing we've noticed is that the sequence(s) in your file need to be all uppercase, pattern matching issues arise with lowercase characters. 

You'll need to also specify the output file. You can call this whatever you want, as long as it has a .csv extension. If you type a file that already exists on the machine, it will be overwritten, otherwise the filename you typed will be created.

To run the program type `perl ASOproj.PL <your-uploaded-file-name>.fasta <your-output-file>.csv`

#### Step 3) Download the output

Again if you're using an ssh client this will be different, but if you're using Sam's CGP account follow the steps below:

Click the Gear icon in the top right -> Download File
it will ask you for the fully qualified file path, in this location that path is `/home/sbarkal/ASOproj/<your-output-file>.csv`
The download should proceed as it does when you download other files with your browser. 

#### Step 4) Shut down the instance

If you're doing multiple .fasta files you don't need to follow this step after each run, only after you're done with the program. This is really inportant becuase the machine is billed by the minute of use. 

To do this, exit the terminal window, and go back to the google cloud dashboard. You should see a bar titled 'instance-1' with a green mark next to it. On the far right, next to `ssh` clich the three vertical dots and select stop. The green icon will turn gray and start spinning indicating it's shutting down, but don't leave until it's stopped to ensure it shut down correctly. 

Contact me with any issues or concerns at jamesdavidfife@gmail.com 
