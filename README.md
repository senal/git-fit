# how to set up SSH
1. Generate SSH Key
   bash
    ```
    ssh-keygen -t ed25519 -C "your_email@example.com"

    ```
    - Save Location: When prompted to "Enter a file in which to save the key," press Enter to accept the default location.
    - Passphrase: Type a secure passphrase when prompted, or press Enter twice to skip this for a no-password login (though a passphrase is recommended for security). 

2. Copy the public key
   You need to copy the contents of the .pub file created in the previous step.
   Mac: Run `pbcopy < ~/.ssh/id_ed25519.pub`
   Windows(Git Bash/Command Prompt): Run `cat ~/.ssh/id_ed25519.pub | clip`

3. Add key to GitHub Account
    - Log in to your GitHub Account.
    - Select your profile photo in the upper-right corner and select **Settings**.
    - In the left sidebar, click **SSH and GPG keys**.
    - Click the **New SSH** key (or **Add SSH** key) button.
    - In the "Title" field, give the key a descriptive name (e.g., "Work Laptop").
    - Paste your key into the Key field and click Add SSH key.

4. Test the connection
   To verify everything is working, run this command in your terminal:
   `ssh -T git@github.com`
   If successful, you will see a message like: *Hi username! You've successfully authenticated...*.
          
# git-fit

repo to experience:
git worktree
    creating a feature branch
git automation
