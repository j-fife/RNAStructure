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
