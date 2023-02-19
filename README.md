# The Git-Github lecture for MDG SoC'23

*This is a list of basic git commands you will be needing for **MDG SoC '23***
> Some pre-requisites:
> - Install [git](https://git-scm.com/downloads)
> - Sign up for [github](https://github.com/)

### 1. Configuring Git   

   - Setting your username
   ```sh
   git config --global user.name "FIRST_NAME LAST_NAME"
   ```   
   - Setting your email
   ```sh
   git config --global user.email "MY_NAME@example.com"
   ```   
   
### 2. Initializing / Cloning a Repository   
  
   - Initialize an empty git repository 
   ```sh
   git init
   ```   
   - Cloning a repository
   ```sh
   git clone https://github.com/user/this-is-just-an-example.git
   ```

### 3. Branches - Create, Switch, Delete and View

   - Create a new branch
   ```sh
   git branch new_branch
   ```   
   - Switching to a branch
   ```sh
   git checkout your_branch
   ```   
   > Or... you could use ```git checkout -b new_branch``` to create new_branch and switch to it.
   - Deleting a branch
   ```sh
   git branch --delete not_wanted_branch
   ```
   - View which branches exist
   ```sh
   git branch
   ```

### 4. Status, Add, Commit
   - Check the "status" of files
   ```sh
   git status
   ```
   - Add files to the staging area
   ```sh
   git add folder/file.txt
   ```
   > Or you can use ```git add .``` to add all the files in your working directory to the staging area
   - Commit your changes into the repo
   ```sh
   git commit -m "your commit message here"
   ```
   > If you have a really big commit message you think will need more than 1 line, just use ```git commit``` and you will be directed to your editor, where you can write your "big" commit message.
   >> Had to give this extra side note... a lot of you during the setup of git would have chosen vi/vim as your default editor(that's the default settings), and might find it a little hard to work with. **The memes are real**  
   ![A vim meme comes here](https://preview.redd.it/seriously-though-how-do-i-exit-vim-v0-mx7dxqljnnl81.png?auto=webp&s=03f895ee50952918687dfdfea03c0bc3af097754)
   Fret not if you don't see what you're typing on the screen... you're just in the esc mode. Type ```i``` and you should be in insert mode now - you can start typing now. Once you're done, go back to esc mode by pressing the esc key. To save your changes to the file and exit, ```:wq```, if you don't want to save your changes, ```:q!```. Learn [vim](https://github.com/iggredible/Learn-Vim) pliz.  

   *The convention we follow:*   
   ```
   feat: (addition of a new feature)   
   rfac: (refactoring the code: optimization/ different logic of existing code - output doesn't change, just the way of execution changes)   
   docs: (documenting the code, be it readme, or extra comments)   
   bfix: (bug fixing)   
   chor: (chore - beautifying code, indents, spaces, camelcasing, changing variable names to have an appropriate meaning)
   ptch: (patches - small changes in code, mainly UI, for example color of a button, incrasing size of tet, etc etc)
   conf: (configurational settings - changing directory structure, updating gitignore, add libraries, changing manifest etc) 
   ``` 
### 5. Logging your commit history
   ```sh
   git log
   ```
   > Alternatively, to visualize it better, use ```git log --oneline --graph --all```

### 5. Push to remote
   - Pushing your local changes to the remote 
   ```sh
   git push origin branch_name
   ```
### 6. Pulling from the origin
   - Pulling the changes from the remote
   > It is a good practice to fetch your changes first, with ```git fetch --prune --all``` - this will fetch all the branches and clear any outdated branches on the remote.
   ```sh
   git pull origin branch_name
   ```
### 7. Stash, pop
   *Sometimes, you might be working on a file, and your friend has pushed a newer version of the file on the same branch as yours on the remote repo. You want to pull his changes and continue working on the given file.*     
   You will encounter an error if you try to pull. So stash your changes, pull and then pop.
   ```sh
   git stash
   ```
   **&darr;**
   ```sh
   git pull origin branch_name
   ```
   **&darr;**
   ```sh
   git pop
   ```
   With this the files that both of you have made changes on should contain both versions of the code, enclosed in ```>>>>>>>``` and ```=======```... you can choose which changes to keep or keep a combination of them too.

### 8. Raising a PR
   *After you've made a number of commits on your branch, you can **raise a PR** to merge it with the parent branch*   


Here are some other useful links you might need:
- [Git-Github for Poets](https://www.youtube.com/playlist?list=PLozRqGzj97d02YjR5JVqDwN2K0cAiT7VK)
- [Official Git docs](https://git-scm.com/docs) - if reading is more your thing

*Welcome to MDG SoC'23...we'll be waiting for your first PR :heart:*
