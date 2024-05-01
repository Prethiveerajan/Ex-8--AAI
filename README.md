 <H3>ENTER YOUR NAME</H3>
<H3>ENTER YOUR REGISTER NO.</H3>
<H3>EX. NO.8</H3>
<H3>DATE:</H3>
<H1 ALIGN =CENTER>Implementation of Speech Recognition</H1>
<H3>Aim:</H3> 
 To implement the conversion of live speech to text.<BR>
<h3>Algorithm:</h3>
Step 1: Import the speech_recognition library<Br>
Step 2: Initialize the Recognizer<Br>
Step 3: Create an instance of the Recognizer class, which will be used for recognizing speech.<Br>
Step 4: Set the duration for audio capture<Br>
Step 5: Define a variable to specify the duration (in seconds) for which the program will capture audio from the microphone.<Br>
Step 6: Display a message in the console to prompt the user to speak.<Br>
Step 7: Capture audio from the default microphone<Br>
Step 9: Use the default microphone as the audio source.<Br>
Step 10: Record audio for the specified duration using the Recognizer instance.<Br>
Step 11: Perform speech recognition with exceptional handling:<Br>
•	Attempt to recognize speech from the captured audio using the Google Speech Recognition service.<Br>
•	If successful, print the recognized text.<Br>
•	Handle specific exceptions: If the recognition result is unknown or if there is an issue with the request to the Google Speech Recognition service, print corresponding error messages.<Br>
•	A generic exception block captures any other unexpected errors.<Br>
<H3>Program:</H3> :
import speech_recognition as sr
r = sr.Recognizer()
duration = 30
print("Say something")
with sr.Microphone() as source:
    audio_data = r.listen(source,timeout=duration)

try:
    text= r.recognize_google(audio_data)
except sr.UnknownValueError:
    print("Sorry, couldn't understand the audio")
except sr.RequestError as e:
    print(f'Error with request tp Google Speech Recognition service: {e}')
except Exception as e:
    print(f'Error : {e}')

<H3> Output:</H3>
https://private-user-images.githubusercontent.com/94154614/326515373-62ed02f8-0386-474b-a5d1-8ebc89d22cf9.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTQ1NDI3OTYsIm5iZiI6MTcxNDU0MjQ5NiwicGF0aCI6Ii85NDE1NDYxNC8zMjY1MTUzNzMtNjJlZDAyZjgtMDM4Ni00NzRiLWE1ZDEtOGViYzg5ZDIyY2Y5LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA1MDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwNTAxVDA1NDgxNlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTZmNjk4YmE3ODNjNTBjMDY3MmM0Nzg3NWFhYWIzZmZiZTBmZDhlNjRkMTIxZGM3NjczYWU0ZDA2ODQ3ZjQxMTYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.X3CRynUBk34w_c3rFuoSXe15afbiMDtYEkXmKlIxh0E

<H3> Result:</H3>
Thus, the python program for Speech Recognition is implemented successfully.
