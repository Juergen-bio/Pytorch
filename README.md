# Pytorch
In progress
Pytorch
In progress

Mount Drive The commands below will promote an action to give permission to mount you drive through any of your affiliated Google accounts. ACCEPT them.
After that, you will have mounted but still not in your actual cloud drive yet. You are still in colab storage vm.
if you ls in the colab terminal you will see that there are MyDrive (your actual drive) and other dir.

from google.colab import drive
drive.mount('/content/drive')
    
Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount("/content/drive", force_remount=True).


Get you to your actual drive cd MyDrive. write pwd it will show content/drive/MyDrive
From here you can create a different directory if you want to 3.git clone, cd into your clone dir.
Move your existing file into this directory that is now in your drive. You can use the following commands Example: !cp "/content/drive/MyDrive/Colab Notebooks/Untitled.ipynb" "/content/drive/MyDrive/Folder_name/Untitled.ipynb"
Note: You can use mv to move the file instead of copying it Untitled.ipynb can be renamed to anything
Now that your work is set up in your Drive, you can open a new Colab session directly from your Folder_name directory. There are two primary ways to do this, both of which avoid creating a temporary "Welcome" file.
Method 1: Using the Google Drive UI
This is the most common and straightforward method.
Open Google Drive in your web browser.
Navigate to your Folder_name folder.
Double-click on the .ipynb notebook file you want to open. It will automatically launch in Colab.
This method directly opens the existing notebook file, ensuring you're working on the correct, persistent version.

Method 2: Creating a New Notebook in the Correct Location
If you need to start a brand new notebook for a project within the folder_name directory, you can create it directly from your Google Drive.
Open Google Drive and navigate to the folder_name folder.
Right-click in an empty space within the folder.
Go to More > Google Colaboratory.
This creates a new, blank Colab notebook file directly inside your directory. You will then need to start your session by mounting your Drive and changing the working directory to your folder_name folder using cd /content/drive/MyDrive/folder_name.
This ensures any new files you create or clone are saved to the correct location.

    
We now set the device. Here we want to leverage colabs cuda gpu that is more capable. I mean why not
We then print the device to ensure it is what we want cuda
Import torch
device = torch.device("cuda" if torch.cuda.is_available() else 'cpu')
device




