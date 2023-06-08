# Lab Report 4: Doing it All from the Command Line
## 1. Log into ieng6
Log into your ieng6 account by typing ```ssh cs15lsp23[xx]@ieng6.ucsd.edu``` into the terminal in ```bash```. The ```xx``` should be your own letters, personalized for your account. Then ```Password:``` will show up where you put your own password.
<img width="760" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/24a34f80-0759-4477-8a07-1a76dd0527a9">

## 2. Clone your fork of the repository from your Github account
From your Github account find the link to the repository, then clone your fork by using the ``git clone <CTRL + C><CTRL + V>`` where the ``<CTRL + C><CTRL + V>`` is the link you got from your repository

<img width="760" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/f95d8d44-d480-435d-bde9-bd203d607714">

## 3. Run the tests, demonstrating that they fail
On the terminal do the following ``cd`` ``<space>`` ``lab7`` ``<tab>`` ``<enter>``. This auto fills "lab7" to the folder name downloaded then opens open the folder which has what we just cloned. Then do ``bash`` ``<space>`` ``<tab>`` ``test`` ``<tab>`` ``<enter>``. This will run the test and will show failure.
<img width="760" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/a616f54d-d7e8-4a4c-821b-2821c4619fa4">


## 4. Edit the code file to fix the failing test
Then do ``vim`` ``<space>`` ``<tab>`` ``ListExamples`` ``<tab>`` ``<enter>``. This will open vim open to the file which we need to edit to fix. Then we do
``</index1><enter>`` which will search for the word "index1" in the file, then``<n><n><n><n><n><n><n><n><n>``, which cycles through the "index1" words until you reach the correct one. After you do``<l><l><l><l><l>``, which will move you to the "1", next ``<r><2>``, which will replace "1" with "2"; last ``<esc><:wq><enter>``, this will save and exit, which will fix the error.
<img width="760" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/6eb609cc-0085-4ee4-b380-dc32d1b3da5d">
<img width="1389" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/4f9fb47b-6287-4a3c-8a68-ee1c949331b2">

## 5. Run the tests, demonstrating that they now succeed
Then re-run the test doing ``bash`` ``<space>`` ``<tab>`` ``test`` ``<tab>`` ``<enter>`` again.

<img width="760" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/c8f339dd-aa6f-4423-ab4b-8d1d914a5eee">

## 6. Commit and push the resulting change to your Github account (you can pick any commit message!)
We can commit by typing ```git comit -a``` then type in a message I put hello. Then do ``:wq`` to save and quit.
<img width="760" alt="image" src="https://github.com/drewlar/cse15l-lab-reports/assets/130115948/e83e4faa-5c7a-4525-ba0e-d0ab9ca15422">
Last but not least type in ```git push``` and <Enter> which will upload all the changes you have made and commited to the repository.
