# Listed_Wav2Lip_Lipsync

To achieve the output we have used the pretrained model from Wav2Lip, more specificallt the Wav2Lip + GAN model, the github page for which can be found [here](https://github.com/Rudrabha/Wav2Lip).

##Steps that were followed:
1. The makers of the Wav2Lip model have provided a great resource in the form a quick start guide which is in the form of the Google Notebook. We can make our own modifications to this notebook.
2. Next I created two folders on my drive to store the model which has to be downloaded and another one to store the testing audio and video files.
3. Another notebook in the Wav2Lip repo also has a fantastic piece of code that allowed mw to download chunks of the YouTube video provided and it automatically muted the audio. (Note: The testing is doen using the first 7 seconds of the YouTube video provided)
4. After mounting our drive and cloning the repositiory I had to deal with some dependency issues and other errors, the details of which are mentioned below.
5. Finally the output was stored in the results folder from which it can be downloaded.

##Errors and Issues that were encountered:
1. The first error that I encountered was that the required version for librosa for the model to work was 0.8.0, however running the requirements.txt file of the Wav2Lip repo installs the 0.7.0 version of librosa which throws an error while running the last piece of code. This was solved using simple uninstall and reinstallation of librosa using the pip command.
2. The next error which occured was due to the fact that the mel() function in the audio.py file only took two positional arguments, however when we ran the code mentioned in the guide, 3 arguments were being passed to the mel() function which threw an error. This was fixed using the solution mentioned in this discussion [thread](https://github.com/Rudrabha/Wav2Lip/issues/471).
3. The third and last problem faced was that the model is limited to a video and audio of 7seconds only. As such to dub an entire video we have to chop it down and string it up together again to get our desired output. Due to this limitation I have only tried using the first 7 seconds of the video clip pertaining to the time constraints of the assignment.

