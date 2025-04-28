# File Transfer between Two Virtual Machines

# Objective:
To create two text files on one virtual machine (source),
transfer them to another virtual machine (destination) using SCP,
and verify the files before and after transfer.

# Requirements:
1. Two Virtual Machines (VMs) installed on VirtualBox (e.g., Kali Linux, Ubuntu)

2. SSH service installed and running on the destination VM

3. Proper network setup (e.g., same internal network, host-only adapter)

# Steps:

# 1. Open Terminal on Both VMs
Source VM: where files are created

Destination VM: where files will be transferred

# 2. Check IP Address of Destination VM
On Destination VM terminal:

    ip a

Find and note the IP address (example: 192.168.56.101).

# 3. Start SSH Service on Destination VM
On Destination VM terminal:

    sudo systemctl start ssh
    sudo systemctl enable ssh
    sudo systemctl status ssh

Ensure the SSH service shows as active (running).

# 4. Create Two Text Files on Source VM
On Source VM terminal:

    touch file1.txt file2.txt

This creates two empty files.
Add text to files:

    echo "This is file1 before transfer." > file1.txt
    echo "This is file2 before transfer." > file2.txt

This writes text into the files.

# 5. Display Files on Source VM (Before Transfer)

    cat file1.txt
    cat file2.txt

Confirm the content.

# 6. Transfer Files Using SCP Command
Use the SCP (Secure Copy Protocol) to transfer the files from Source VM to Destination VM.

On Source VM terminal:

    scp file1.txt file2.txt username@destination_ip:~/

Where:

* username = the username of the logged-in user on the destination VM

* destination_ip = the IP address of the destination VM found earlier

Enter the password of the arnav-vaidya user on the destination VM when prompted.

Files are copied into the home directory /home/username/.

# 7. Verify Files on Destination VM (After Transfer)
On Destination VM terminal:

    cd ~
    ls
    cat file1.txt
    cat file2.txt

Confirm that the contents of the files match the original ones.

# 8. Modify Files on Destination VM (Optional)
Add more text into the files:

    echo "This is file1 after transfer." >> file1.txt
    echo "This is file2 after transfer." >> file2.txt

">>" appends new text to the end of the file.

Then check the updated contents:

    cat file1.txt
    cat file2.txt

Confirm that the files are updated successfully.
