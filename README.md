# ISSUE-Automate-Sort-Files-
When running code it gets 0 errors, but it does not complete its task
import os
from pathlib import Path
import shutil



os.chdir('C:/Users/NCS TRAINING/Downloads')
our_files = 'C:/Users/NCS TRAINING/Downloads'



documents=['.pdf','.docx','.doc','.txt']
pictures=['.jpeg','.png','.PNG','.gif']
videos=['.mp4','.mkv','.vlc','.flv']
audio=['.mp3','.OGG','.flac']
software=['.exe','.msi']
compressedFiles=['.zip','.rar']

DocsLocation='C:/Users/NCS TRAINING/Documents/Documents'
PhotoLocation='C:/Users/NCS TRAINING/Pictures'
VideoLocation='C:/Users/NCS TRAINING/Videos'
AudioLocation='C:/Users/NCS TRAINING/Music'
SoftwareLocation='C:/Users/NCS TRAINING/Documents/Software'
CompressedFilesLocation='C:/Users/NCS TRAINING/Documents/Video'


for f in os.listdir():
    file_name, file_ext = (os.path.splitext(f))
    if file_ext == documents:
        shutil.move(f,DocsLocation)

    if file_ext == pictures:
        shutil.move(f,PhotoLocation)

    if file_ext == videos:
        shutil.move(f,VideoLocation)

    if file_ext == audio:
        shutil.move(f,AudioLocation)

    if file_ext == software:
        shutil.move(f,SoftwareLocation)

    if file_ext == compressedFiles:
        shutil.move(f,CompressedFilesLocation)
