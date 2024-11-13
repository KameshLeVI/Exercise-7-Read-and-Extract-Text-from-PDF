# Exercise-7-Read-and-Extract-Text-from-PDF

## Aim:

To automate the process of extracting text from a PDF file and saving the extracted content to a text file using UiPath.

## Equipment Required:

UiPath Studio – A tool for automating tasks and workflows.<br>
PDF File – The file from which the text will be extracted.<br>
Text File – The file where the extracted text will be saved.<br>
Computer with the following configuration:<br>
At least 4 GB RAM.<br>
A 2.0 GHz processor.<br>
Running Windows OS.

## Procedure:

### Create a New Project in UiPath Studio:

Open UiPath Studio.<br>
Under the New Project tab, select Process.<br>
Name the project (e.g., Extract PDF Text) and click Create.<br>
This will set up a new project for you to begin automating the task of reading from a PDF.

### Install the PDF Activities Package:

Click on Manage Packages from the top toolbar.<br>
Search for the UiPath.PDF.Activities package and install it.<br>
This package contains tools specifically designed to handle PDF files (like reading text, extracting tables, etc.).

### Define File Paths:

Go to the Variables pane in UiPath Studio to define paths for the PDF file and the output text file:<br>
Create a String variable called pdfFilePath for the PDF file path.

```
pdfFilePath = "C:\Users\admin\Documents\Sample.pdf"
```

Create a String variable called textFilePath for the output text file.

```
textFilePath = "C:\Users\admin\Documents\ExtractedText.txt"
```

### Use 'Read PDF Text' Activity:

In the Activities panel, search for Read PDF Text and drag it into your sequence.<br>
Set the FileName property of the activity to pdfFilePath (the variable containing the path to your PDF).<br>
Create a new String variable called pdfText to store the extracted text from the PDF file.<br>
Set the Output property of the Read PDF Text activity to pdfText.

### Write the Extracted Text to a File:

Search for the Write Text File activity in the Activities panel and drag it below the Read PDF Text activity.<br>
Set the FileName property of the Write Text File activity to textFilePath.<br>
Set the Text property to pdfText (the variable containing the extracted PDF text).<br>
This activity will write the extracted text from the PDF into the specified text file.

### Save and Run the Workflow:

Press CTRL+S to save your workflow.<br>
Click the Run button in UiPath Studio to execute the workflow.<br>
Once the process completes, the robot will extract the text from the PDF and save it into the designated text file.

## UiPath WorkFlow
![image](https://github.com/user-attachments/assets/3421a445-d81b-4829-8632-00fce90db183)
![image](https://github.com/user-attachments/assets/70d04b52-c398-49c3-ad82-78c73952c4ae)
![image](https://github.com/user-attachments/assets/eedff02f-14fb-4d58-8ca8-c1b1fad81d53)
![image](https://github.com/user-attachments/assets/ce5bbef6-e2b1-4028-9fd6-794ba63e75f6)
![image](https://github.com/user-attachments/assets/a3af9bcc-46ff-4dc0-ae8d-bbc38204bb88)
![image](https://github.com/user-attachments/assets/9dc7d0fd-b2e6-44f8-a49e-36de5266f6ec)

## Result:

The text from the PDF file is successfully extracted and saved to a text file using UiPath Studio. The process automates the extraction of text from a PDF, which can then be used in further automation tasks, such as data analysis or report generation.
